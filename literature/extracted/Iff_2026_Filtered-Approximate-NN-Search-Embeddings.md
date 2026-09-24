---
id: "Iff_2026_Filtered-Approximate-NN-Search-Embeddings"
source_pdf: "../pdf/Iff_2026_Filtered-Approximate-NN-Search-Embeddings.pdf"
source_filename: "Iff_2026_Filtered-Approximate-NN-Search-Embeddings.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Iff_2026_Filtered-Approximate-NN-Search-Embeddings.references.md"
---

<!-- p:1 -->

## Benchmarking Filtered Approximate Nearest Neighbor Search Algorithms on Transformer-based Embedding Vectors

Patrick Iff ETH Zurich Switzerland iffp@inf.ethz.ch

## Abstract

Advances in embedding models for text, image, audio, and video drive progress across multiple domains, including retrieval-augmented generation, recommendation systems, and others. Many of these applications require an efficient method to retrieve items that are close to a given query in the embedding space while satisfying a filter condition based on the item's attributes, a problem known as filtered approximate nearest neighbor search (FANNS). By performing an in-depth literature analysis on FANNS, we identify a key gap in the research landscape: publicly available datasets with embedding vectors from state-of-the-art transformer-based text embedding models that contain abundant real-world attributes covering a broad spectrum of attribute types and value distributions. To fill this gap, we introduce the arxiv-for-fanns dataset of transformer-based embedding vectors for the abstracts of over 2.7 million arXiv papers, enriched with 11 real-world attributes such as authors and categories. We benchmark eleven different FANNS methods on our new dataset to evaluate their performance across different filter types, numbers of retrieved neighbors, dataset scales, and query selectivities. We distill our findings into eight key observations that guide users in selecting the most suitable FANNS method for their specific use cases.

Code: https://github.com/spcl/fanns-benchmark Dataset: https://hf.co/datasets/SPCL/arxiv-for-fanns-large

## 1 Introduction

Advances in embedding models for text [82, 84, 157], image [94, 133], video [129], audio [17, 32], and other modalities [85] have significantly enhanced semantic search, where items are mapped to a high-dimensional vector space and similarity is measured by the distance between embedding vectors. Efficient similarity search algorithms are essential to navigate this space. Given the scale of modern datasets, exact nearest neighbor search (ENNS) algorithms are too slow, necessitating the use of approximate nearest neighbor search (ANNS) methods [18, 54, 57, 61, 71, 74, 75, 99, 100, 130]. Additionally, many applications, including large language models (LLMs) with retrieval-augmented generation [53, 124, 149], recommendation systems [79, 131, 153], vehicle and person re-identification [93, 163], and others [58, 86, 122, 147, 153], require retrieving only items that satisfy filtering conditions on item attributes, such as access rights for a document, a video's timestamp, or a product's price. These requirements have driven the development of filtered approximate nearest neighbor search (FANNS). Both academia and industry have recognized its growing importance, leading to numerous research publications [44, 56, 63, 76, 89, 97, 107, 115, 116, 141, 146, 152, 163, 164] and adoption in database solutions [118, 136, 137].

Paul Brügger ETH Zurich Switzerland Marcin Chrapek ETH Zurich Switzerland David Kochergin ETH Zurich Switzerland Maciej Besta ETH Zurich Switzerland Torsten Hoefler ETH Zurich Switzerland htor@inf.ethz.ch These efforts require suitable benchmarks to guide the development of FANNS methods, and while transformer-based text embeddings are widely used in practice, no existing FANNS benchmarks with transformer-based embedding vectors exist. Motivated by these developments, we make three main contributions:

First, to clarify the requirements for FANNS benchmarks, we present a comprehensive taxonomyandsurvey of existing FANNS methods. We identify three key dimensions for the classification of FANNS methods: fi ltering approach , indexing technique , and supported fi lter types . To cover all fi lter types , a FANNS benchmark must contain categorical, numerical, and set-valued attributes, and to reflect the strengths and weaknesses of various fi ltering approaches , these attributes should exhibit diverse value distributions. The indexing technique is largely orthogonal to the benchmark.

Second, we present the novel arxiv-for-fanns dataset with transformer-based embeddings of paper abstracts from the arXiv dataset [31] using the model stella\_en\_400M\_v5 [110, 157]. Our dataset has eleven real-world attributes, including categorical (e.g., venue), numerical (e.g., publication year), and set-valued (e.g., authors) ones, and exhibits diverse value distributions.

Third, we perform a comprehensive benchmarking study of eleven FANNS methods on our novel dataset, evaluating their performance across different filter types, varying numbers of retrieved neighbors, different dataset scales, and a wide range of query selectivities. We distill the results of this benchmarking effort into eight key observations that offer practical guidance for selecting the most appropriate FANNS method for specific application scenarios.

## 2 Background

### 2.1 Filtered Approx. Nearest Neighbor Search

To introduce the FANNS concepts that we leverage throughout the paper, we walk the reader through the process of building and using a semantic search engine for research papers with filtering capabilities, which is a practical use case of FANNS that can be built using our arxiv-for-fanns dataset. Figure 1 provides an overview of this example application, with components and actions referenced using letters A to E and numbers 1 to 11 , respectively.

Index Construction: To build such a system, we transform each of the n papers in our database A into an item . Formally, an item I i = ( v i , a i, 1 , . . . , a i,m ) for i ∈ { 1 , . . . , n } consists of a d -dimensional embedding vector v i and a value for each of the m attributes ( a i, 1 to a i,m ). In our example, the paper's venue, publication year, and authors define 1 the item's attributes . The paper's abstract is processed 2 by a text embedding model B , such as NV-Embed [82, 111], LENS [83, 84], Stella [110, 157], GTE [4, 88], or BGE [27, 112], to generate the item's embedding vector v i . To efficiently answer FANNS queries for these items , we insert 3 all items into a FANNS index C .


<!-- p:2 -->


Figure 1: (§2.1) An Example Application of FANNS.

Queryexecution: During runtime, users interact with the search engine by entering 4 search terms and filter conditions. We use p to denote the number of user requests submitted during a session. We transform each user request into a FANNS query , formally defined as Q j = ( q j , k j , f j ) for j ∈ { 1 , . . . , p } and consisting of a d -dimensional query vector q j , the number of items to return k j , and a filter function f j . The filter f j and the number of requested results k j are set 5 based on the user's filter conditions. The search term is processed 6 by the same text embedding model B used during index construction to generate the query vector q j . The query is submitted 7 to a FANNS algorithm E , which utilizes 8 the FANNS index C to retrieve the IDs of the most relevant papers. These IDs are forwarded 9 to a retriever D , which fetches 10 the corresponding papers from the database A and returns 11 them to the user.

### 2.2 Approximate Nearest Neighbor Search

Since many FANNS algorithms build on ANNS methods without filtering, we first review the most relevant ANNS approaches. They fall into four categories: tree-based, hash-based, graph-based, and quantization-based. For detailed surveys, see Han et al. [65] and Echihabi et al. [42]. Benchmarks [15, 16] show that no algorithm dominates across datasets; performance is dataset-dependent.

2.2.1 Tree-based methods. Tree-based methods partition the vector space into regions using search trees, where nodes denote regions or their boundaries. Deeper levels represent finer partitions. Examples include k-d trees [22], R-trees [64], ball trees [113], cover trees [24], RP trees [33], M-trees [29], K-means trees [134], and best bin first [21], as well as many variants [68, 96, 109, 126]. These methods are effective for low-dimensional vectors but degrade under the curse of dimensionality [101].

2.2.2 Hash-based methods. Hash-based methods use a set of hash functions to map vectors from a continuous d -dimensional space into discrete hash buckets. These functions are designed so that similar vectors are mapped into the same bucket with high probability. When querying a hash-based index, the query vector is hashed, and the vectors in the corresponding bucket are compared to the query vector. Hash-based methods include locality-sensitive hashing (LSH) [34, 71], spectral hashing [148], iDEC [57], deep hashing [91], mmLSH [73], PM-LSH [162], R2LSH [95], EI-LSH [92], and others [6, 7, 51, 55, 69, 87, 98, 114, 132].

2.2.3 Graph-based methods. Graph-based methods represent vectors as vertices, connecting those close in the embedding space to form a neighborhood graph [9, 138]. Nearest neighbors are found by traversing the graph from one or more entry points, following the shortest distance to the query. Navigable small world (NSW) graphs [99] add long edges between distant vertices to accelerate traversal. Hierarchical navigable small world (HNSW) graphs [100] extend NSW with a hierarchy: upper layers hold long edges, lower layers short ones, and traversal proceeds top-down. Other graph-based methods include DiskANN [74], FreshDiskANN [128], NSG [49], GRNG [46], and others [47, 48, 66, 72, 160].

2.2.4 Quantization-based methods. Quantization-based methods map the n vectors to a set of c ≪ n clusters, each represented by a cluster centroid. Each vector is assigned to the cluster whose centroid is closest to the vector. One can either store all vectors assigned to a given cluster, as in inverted file (IVF) [130], or approximate all vectors of a cluster by the respective cluster centroid, which is less accurate but requires less storage space and allows for faster query times. To find the nearest neighbors of a query vector, we only compare it to the database vectors in the w ≤ c clusters whose centroids are closest to the query vector. Product quantization (PQ) [75] and inverted file with product quantization (IVF-PQ) [75] are more advanced quantization-based methods that split the vector space into s orthogonal subspaces and quantize each subspace separately. Other quantization-based ANNS methods include additive quantization [18], BAPQ [61], LOPQ [77], OPQ [54], RaBitQ [52], SPANN [28], and others [8, 19, 104, 142, 145].

## 3 Taxonomy and Survey of FANNS Methods

By analyzing the vast landscape of existing FANNS methods, we identify three key dimensions for classifying these methods. First, they differ in the approach they take to combine ANNS with attribute filtering, which we discuss in Section 3.1. Second, we observe that all FANNS methods are based on the same four fundamental indexing techniques as ANNS methods, namely, hashing, trees, graphs, and quantization, or combinations thereof (see Section 2.2). Third, we distinguish between different fi lter types that FANNS methods support, which we discuss in Section 3.2. A fourth, less important dimension is the precise problem definition of FANNS that is addressed. Most works guarantee that all returned items pass the filter and only the distance in embedding space is approximated; however, a small number of methods also approximate the filtering step, sometimes returning items that do not match the filter. We refer to this relaxed problem as approximately filtered approximate nearest neighbor search (AFANNS).


<!-- p:3 -->


Table 1: (§3.3) Overview of FANNS methods. † Does not mention a filtering step during query execution. *We have not been able to find the source code of this work. 1 The index is constructed for a single ordered attribute, in-filtering is proposed to handle secondary attributes. 2 Any EMIS filter can be used as an EM filter by using a set attribute with only a single value.

| Method             |   Year | Problem   | Approach            | Technique(s)         | Filters - EM   | Filters - R   | Filters - EMIS   | Filters - MEM   | Filters - MR   | Filters - MEMIS   | Filters - C   | Open - source   |
|--------------------|--------|-----------|---------------------|----------------------|----------------|---------------|------------------|-----------------|----------------|-------------------|---------------|-----------------|
| Rii [103]          |   2018 | FANNS     | pre-/in-filtering   | quantization         | ✔              | ✔             | ✔                | ✔               | ✔              | ✔                 | ✔             | ✔ [102]         |
| MA-NSW [150]       |   2019 | FANNS     | hybrid index        | graph                | ✔              | ✘             | ✘                | ✔               | ✘              | ✘                 | ✘             | ✘ *             |
| PASE [153]         |   2020 | FANNS     | post-filtering      | quantization / graph | ✔              | ✔             | ✔                | ✔               | ✔              | ✔                 | ✔             | ✔ [5]           |
| AnalyticDB-V [147] |   2020 | FANNS     | pre-/post-filtering | quantization         | ✔              | ✔             | ✔                | ✔               | ✔              | ✔                 | ✔             | ✘ *             |
| Milvus [139]       |   2021 | FANNS     | pre-/post-filtering | quantization / graph | ✘              | ✔             | ✘                | ✘               | ✔              | ✘                 | ✘             | ✔ [119]         |
| NHQ [140, 141]     |   2022 | AFANNS    | hybrid index        | graph                | ✔              | ✘             | ✘                | ✔               | ✘              | ✘                 | ✘             | ✔ [50]          |
| HQANN [154]        |   2022 | AFANNS †  | hybrid index        | graph                | ✔              | ✘             | ✘                | ✔               | ✘              | ✘                 | ✘             | ✘ *             |
| AIRSHIP [161]      |   2022 | FANNS     | in-filtering        | graph                | ✔              | ✔             | ✔                | ✔               | ✔              | ✔                 | ✔             | ✘ *             |
| HQI [107]          |   2023 | FANNS     | hybrid index        | tree + quantization  | ✔              | ✔             | ✘                | ✔               | ✔              | ✘                 | ✔             | ✘ *             |
| VBASE [159]        |   2023 | FANNS     | post-filtering      | any                  | ✔              | ✔             | ✔                | ✔               | ✔              | ✔                 | ✔             | ✔ [106]         |
| FDANN [56]         |   2023 | FANNS     | hybrid index        | graph                | 2              | ✘             | ✔                | ✘               | ✘              | ✘                 | ✘             | ✔ [105]         |
| CAPS [63]          |   2023 | FANNS     | hybrid index        | quantization + tree  | ✔              | ✘             | ✘                | ✔               | ✘              | ✘                 | ✘             | ✔ [62]          |
| ARKGraph [163]     |   2023 | FANNS     | hybrid index        | graph                | ✘              | ✔             | ✘                | ✘               | ✘              | ✘                 | ✘             | ✔ [10]          |
| ACORN [115]        |   2024 | FANNS     | in-filtering        | graph                | ✔              | ✔             | ✔                | ✔               | ✔              | ✔                 | ✔             | ✔ [60]          |
| β -WST [44]        |   2024 | FANNS     | hybrid index        | tree + graph         | ✘              | ✔             | ✘                | ✘               | ✘              | ✘                 | ✘             | ✔ [43]          |
| SeRF [164]         |   2024 | FANNS     | hybrid index        | graph                | ✘              | ✔             | ✘                | ✘               | 1              | ✘                 | ✘             | ✔ [12]          |
| iRangeGraph [152]  |   2024 | FANNS     | hybrid index        | tree + graph         | ✘              | ✔             | ✘                | ✘               | 1              | ✘                 | 1             | ✔ [151]         |
| UNIFY [89]         |   2024 | FANNS     | hybrid index        | graph                | ✘              | ✔             | ✘                | ✘               | ✘              | ✘                 | ✘             | ✔ [36]          |
| UNG [26]           |   2024 | FANNS     | hybrid index        | graph                | 2              | ✘             | ✔                | 2               | ✘              | ✔                 | ✘             | ✔ [25]          |
| RangePQ [158]      |   2025 | FANNS     | hybrid index        | tree + quantization  | ✘              | ✔             | ✘                | ✘               | ✘              | ✘                 | ✘             | ✔ [14]          |
| DIGRA [76]         |   2025 | AFANNS    | hybrid index        | tree + graph         | ✘              | ✔             | ✘                | ✘               | ✘              | ✘                 | ✘             | ✔ [13]          |
| DSG [116]          |   2025 | FANNS     | hybrid index        | graph                | ✘              | ✔             | ✘                | ✘               | ✘              | ✘                 | ✘             | ✔ [11]          |
| TFANNS [97]        |   2025 | FANNS     | hybrid index        | graph                | 2              | ✘             | ✔                | ✘               | ✘              | ✘                 | ✘             | ✔ [1]           |

### 3.1 Filtering Approaches

Two common approaches to solving the FANNS problem are prefiltering and post-filtering . In pre-filtering , an attribute-only index such as a B-tree [20], B+-tree [2], or qd-tree [155] identifies all items matching the filter. The k nearest neighbors (KNN) of these items are then determined by computing the distance to the query vector or approximating this distance using quantized embedding vectors precomputed during index construction. In post-filtering , a nearest neighbor search is performed on an unfiltered ANNS index, followed by filtering out non-matching items. This can be done by retrieving k ′ &gt; k items in the hope that enough pass the filter or by iteratively retrieving more items until k matches are found. Many graph-based ANNS indices support a third approach, in-filtering , where attributes are ignored during index construction, and only vertices satisfying the filter are considered during query execution. A fourth approach involves a hybrid index that integrates embedding vectors and attributes in a single index.

Figure 2: (§3.1) The best approach for solving FANNS depends on the filter's selectivity within a given dataset.

The efficiency of different approaches to solving the FANNS problem depends on the dataset and filtering condition (see Figure 2). We define the selectivity of a filter f on a dataset D as the fraction of items in D that satisfy the filter f , following previous work 1 [89, 107, 115, 159]. Pre-filtering is most efficient when selectivity is low, meaning only a few items remain for the ENNS. Post-filtering and in-filtering are most efficient when selectivity is high, i.e., most items pass the filter. If selectivity is too low, ANNS may not return enough valid candidates for post-filtering , and graph traversal with in-filtering may fail due to a sparsely connected or disconnected graph. A hybrid index is most efficient when selectivity is moderate, making none of the three previous approaches optimal.

### 3.2 Filter Types

Weidentify three fundamental fi lter types based on a single attribute. In Exact match (EM) filtering , the item's attribute value must equal a specified query value. While EM filtering is usually applied to a categorical attribute, it can also be used on numerical attributes. Range (R) filtering applies to numerical attributes and considers only items where the attribute value is within a specified query range. Finally, Exact match in set (EMIS) filtering applies to set-valued attributes and considers only items whose attribute set contains a queried value. FANNS algorithms that apply the same filter type to multiple attributes implement multiple exact match (MEM) , multiple range (MR) , and multiple exact match in set (MEMIS) fi lters. We define a combined (C) filter as a filter that can combine the three fundamental single-attribute filters using arbitrary logical operators and may also support arbitrary SQL-style filter predicates.

1 Note that some works [139, 147, 152] use the inverse definition of selectivity.


<!-- p:4 -->


### 3.3 Overview of FANNS Methods

In Table 1, we organize existing FANNS methods according to our taxonomy. We observe that most FANNS methods are based on graphs or quantization, with trees often used in combination with quantization- or graph-based techniques. Figure 3 groups FANNS methods according to their internal working principles, and in the following, we describe these methods in more detail.

Figure 3: (§3.3) Grouping of FANNS method based on their internal working principles.

- 3.3.1 Rii. The Rii [103] index is based on IVF-PQ. It takes a bitmap of matching items as input. If the selectivity is low, it compares the query vector directly with the efficiently accessible, contiguously stored PQ codes (pre-filtering). If the selectivity is high, it first performs the IVF step of IVF-PQ to identify the closest clusters. Within those clusters, a PQ code is compared to the query vector only if the corresponding item matches the filter (in-filtering).
- 3.3.2 MA-NSW. MA-NSW [150] is a graph-based FANNS index that supports both EM and MEM filters. It constructs multiple NSWlike, graph-based ANNS indices, one for each possible combination of attribute values. During query execution, MA-NSW queries the ANNS index that matches the query's filter expression to approximately retrieve the KNN that satisfy the filter conditions.
- 3.3.3 PASE. PASE [153] integrates ANNS into the PostgreSQL [59] database by implementing the IVF and HNSW ANNS indices. It employs an iterative post-filtering approach, in which it repeatedly retrieves items from the ANNS index and filters them until k matching items are found.
- 3.3.4 AnalyticDB-V. Alibaba's AnalyticDB-V [147] extends the AnalyticDB [156] SQL database with FANNS capabilities. It introduces its own ANNS index, called Voronoi graph product quantization (VGPQ), which is similar to IVF-PQ. For FANNS implementation, it supports both pre-filtering and post-filtering.
- 3.3.5 Milvus. Milvus [139] extends the FAISS ANNS library [41, 121] by incorporating range filtering for one or multiple attributes. It supports both pre- and post-filtering, as well as a filtering scheme that partitions the data based on the most frequently filtered attribute and builds a separate ANNS index for each partition.
- 3.3.6 NHQ. NHQ [141] proposes a method to extend any proximity graph-based ANNS index into a hybrid FANNS index. Instead of

constructing the ANNS index solely based on embedding distance, it introduces a fusion distance that combines embedding distance with attribute dissimilarity. While this approach is applicable to any proximity graph-based ANNS index, NHQ also presents construction schemes for two novel proximity graphs. Since its query execution scheme operates using the fusion distance without an explicit filtering step, NHQ may return items that do not match the filter, thus addressing the AFANNS rather than the FANNS problem.

- 3.3.7 HQANN. Like NHQ [141], HQANN [154] employs a fusion distance to transform any proximity graph-based ANNS index into a hybrid FANNS index. The key difference to NHQ is that HQANN prioritizes attribute dissimilarity in the fusion distance, whereas NHQ emphasizes embedding distance.
- 3.3.8 AIRSHIP. AIRSHIP [161] (see Figure 4) is a graph-based FANNS index capable of handling arbitrary filter functions. It relies on a graph-based ANNS index constructed without considering attributes but adapts query execution to FANNS through in-filtering and a series of optimizations. During query execution, AIRSHIP traverses the entire graph but includes only vertices that satisfy the filter in the results. It selects a starting point within a cluster of items that match the filter and traverses the graph in multiple directions concurrently.
- 3.3.9 HQI. Apple's HQI [107] (see Figure 5) is a hybrid FANNS index. To integrate attribute filtering with nearest neighbor search, HQI transforms embedding vectors into attributes by applying kmeans clustering and storing each item's cluster ID as an attribute. It then employs a balanced qd-tree [155], an attribute-only index, to partition the items. Each non-leaf node in the qd-tree contains a predicate over the item attributes (including the cluster ID), with its two child nodes holding items that do or do not satisfy the predicate. During query execution, HQI identifies the query vector's w closest cluster IDs and prunes all branches of the tree that do not contain any of these w cluster IDs or whose attributes do not match the filter. An IVF index is used within each leaf.

Figure 4: (§3.3.8) Visualization of the AIRSHIP index.

Figure 5: (§3.3.9) Visualization of the HQI index.

<!-- p:5 -->


3.3.10 VBASE. VBASE [159] extends PostgreSQL [59] by integrating ANNS into the database system. Its key insight is that most ANNS query execution methods follow a two-stage process: an initial stage where traversal moves from a starting point in the direction of the query vector, and a second stage where the search gradually moves away from the query vector to identify its KNN. Rather than employing a naïve pre-filtering approach, where the ANNS index is queried with a fixed k ′ ≥ k and non-matching items are filtered out, VBASE runs the ANNS query only until the traversal starts moving away from the query vector. From that point onward, it iteratively retrieves and filters additional items until the required k matches are found.

3.3.11 FDANN. Microsoft's Filtered-DiskANN (FDANN) [56] (see Figure 6) implements a graph-based index with EMIS filtering. In addition to supporting an EMIS filter with a single query-label, it also allows filtering with multiple query-labels, where at least one of them must be present in the item's set attribute. FilteredDiskANN introduces two methods for constructing FANNS indices based on Vamana graphs [74]: FilteredVamana and StitchedVamana . During query execution, it traverses the graph starting from a set of entry points that contain the query-label. Throughout its NSW-like graph traversal, it considers only those vertices that satisfy the filter criteria.

Figure 6: (§3.3.11) The Filtered-DiskANN index visualized.

3.3.12 CAPS. In contrast to most FANNS methods, CAPS [63] (see Figure 7) introduces a quantization- and tree-based index that is easier to parallelize than the more common graph-based indices. The CAPS index consists of two levels. The first level organizes items into clusters based on their embedding distance only or a combination of embedding distance and attribute dissimilarity. At the second level, CAPS constructs an attribute frequency tree (AFT), which is an attribute-only index. Each level of the AFT splits items into two buckets: one containing items with the most common attribute value (a leaf node) and another with the remaining items (a non-leaf node), unless the maximum depth is reached. During query execution, CAPS selects the w clusters closest to the query vector and uses the corresponding AFTs to identify matching items.

Figure 7: (§3.3.12) Visualization of the CAPS index.

3.3.13 ARKGraph. Given a set of items, each with a single ordered attribute , ARKGraph [163] (see Figure 8) addresses the more general problem of constructing the K-nearest-neighbor graph (KGraph) [40] for the subset of items that satisfy a range filter. The resulting KGraph can be utilized for solving the FANNS problem or for other data analysis tasks. A naïve approach would store O ( n 2 ) KGraphs, one for each possible query range. For any given item I with attribute value x , this would require maintaining O ( n 2 ) different lists of KNN, one for each possible query range [ l, r ] such that l ≤ x ≤ r . ARKGraph's first key insight is that the KNN of I for any query range [ l, r ] can be efficiently computed by merging the KNN of I from the partial query ranges [ l, x ) and ( x, r ] . Thus, instead of storing KNN lists for all O ( n 2 ) query ranges, it suffices to maintain KNN lists for only O ( n ) partial query ranges and reconstruct the KNN dynamically for any given range. The second key insight is that an item often shares the same KNN across multiple similar partial query ranges. By grouping query ranges and storing only one KNN set per group, ARKGraph further reduces index size and storage overhead.

Figure 8: (§3.3.13) Visualization of the adjacency lists of item 3 in ARKGraph using the three different approaches.

3.3.14 ACORN. ACORN [115] (see Figure 9) supports arbitrary filter types and filtering across multiple attributes. The ACORN index is a denser variant of the HNSW ANNS index [100], constructed without considering attributes. During query execution, ACORN traverses only the subgraph induced by vertices that match the filter. This approach differs from AIRSHIP [161], which traverses the entire graph but includes only matching vertices in the result set. The ACORN index's subgraphs approximate an HNSW [100].

Figure 9: (§3.3.14) Visualization of the ACORN index.

3.3.15 β -WST. β -WST [44] (see Figure 10) is a FANNS index designed for range filtering on a single attribute. A β -WST index is structured as a segment tree [37] with a uniform branching factor of β . At layer l , the attribute value range is divided into β l segments, with a graph-based ANNS index constructed for each segment. The default query strategy selects a minimal set of tree nodes that fully cover the query range, queries the corresponding ANNS indices, and merges the results. Additional strategies include OptimizedPostfiltering , TreeSplit , and SuperPostfiltering .


<!-- p:6 -->


Figure 10: (§3.3.15) Visualization of the β -WST for β = 3 .

3.3.16 SeRF. SeRF [164] introduces the segment graph , a data structure for range-filtered FANNS queries with half-bounded query ranges (i.e., where the query range has an upper limit but no lower limit). It losslessly compresses n HNSW indices [100], corresponding to the n possible half-bounded query ranges, into a single index. This is achieved by incrementally inserting items into an HNSW index in attribute-value order. Each edge in the resulting graph stores the attribute value at which it was added and, if pruned during construction, the attribute value at which it was removed. As a result, the HNSW graph contains edges that are valid only within specific attribute value intervals. During query execution, only edges whose validity interval contains the upper limit of the query range are considered. For query ranges with an upper and a lower limit, SeRF introduces the 2D segment graph (see Figure 11). This structure compresses n segment graphs, one for each possible lower limit, into a single graph with n vertices, where edges store validity intervals for the upper and lower limit of the query range.

Figure 11: (§3.3.16) SeRF's 2D segment graph visualized.

3.3.17 TFANNS. TFANNS [97] proposes three graph-based FANNS indices for EMIS filtering: The local-, global, and packing method .

3.3.18 iRangeGraph. iRangeGraph [152] (see Figure 12) is a graphbased FANNS index designed for range filtering. It is primarily built around a single ordered attribute but also supports in-filtering or post-filtering for secondary attributes of arbitrary types. iRangeGraph constructs a set of graph-based ANNS indices, referred to as elemental graphs . These elemental graphs are organized in a segment tree [37] with O ( log n ) layers. At layer l , the entire attributevalue range is divided into 2 l segments, and a graph-based ANNS index is built for each segment, ensuring that each item appears once in each of the log n layers. Query execution employs an efficient on-the-fly method to dynamically merge a subset of elemental graphs into a single ANNS index containing only items within the query range. While its index construction is similar to β -WST [44], iRangeGraph differs in query execution: instead of querying multiple graph-based indices for different subsets of items and merging the results, it constructs a single graph-based ANNS index dynamically at query time.

Figure 12: (§3.3.18) Visualization of the iRangeGraph index.

3.3.19 RangePQ. RangePQ[158] answers R-filtered FANNS queries by combining a PQ index for embedding vectors with a binary search tree (BST) for attribute values.

3.3.20 UNIFY. UNIFY [89] is a graph-based method that supports range filtering for a single attribute. It introduces two new types of proximity graph, the segmented inclusive graph (SIG) and its HNSWlike variant the hierarchical segmented inclusive graph (HSIG) (see Figure 13). It divides the range of possible attribute values into s segments, s.t., each segment contains approximately the same number of items. The high-level idea of a SIG is to build a proximity graph [143] for each of the 2 s - 1 possible combinations of segments, and then merge these graphs into a single graph that contains the 2 s - 1 smaller graphs as subgraph. Due to a clever construction algorithm, the SIG can be built without explicitly constructing all 2 s - 1 smaller graphs. The SIG is stored as a segmented adjacency list, where outgoing edges are grouped by their destination segment. When querying the SIG, we only traverse the subgraph that correspond to those segments that intersect with the query range. The HSIG is a multi-layered variant of the SIG which is traversed from top to bottom in order to speed-up the query execution. To handle queries with low selectivity, UNIFY supports a pre-filtering variant and for queries with high selectivity, it supports unfiltered ANNS with post-filtering.

Figure 13: (§3.3.20) UNIFY's HSIG index visualized.

3.3.21 UNG. UNG [26] (see Figure 14) is a graph-based FANNS index that supports both EMIS and MEMIS filters. It first identifies all distinct label sets in the database and constructs a label navigating graph (LNG), which is a directed acyclic graph (DAC) with one vertex for each distinct label set and a directed edge from label set a to label set b if a is a subset of b . The unified navigating graph (UNG) index is built by constructing a proximity graph for each vertex in the LNG, where the vertices of each proximity graph represent the items with the corresponding label set. To unify these proximity graphs, cross-edges are added between vertices in the proximity graphs of label sets a and b if there is a corresponding edge from a to b in the LNG. When querying the UNG, the standard graph traversal is initiated, starting in all proximity graphs whose label sets are minimal supersets of the query label set.


<!-- p:7 -->


Figure 14: (§3.3.21) Visualization of the UNG index.

3.3.22 DIGRA. DIGRA [76] uses a multi-way tree structure to organize items based on the value of their single ordered attribute. At each node of this tree, a NSW [99] graph is used to perform ANNS on its subtree. Each R filtered query can be answered by querying only two of these NSW graphs.

3.3.23 DSG. The Dynamic Segment Graph (DSG) [116] is an extension of SeRF [164] that is optimized for cases, where the vectors are dynamically inserted into the index in random order, and first sorting them by attribute value is not possible.

## 4 A New Dataset to Benchmark FANNS

Benchmarking FANNS methods requires suitable datasets. Ideally, such datasets should contain real-world attributes (criterion 1), queries with ground truth (criterion 2), and be publicly available (criterion 3). The most common approach to evaluate FANNS methods that we observed in scientific literature is to use an ANNS dataset such as SIFT [80], GIST [80], GloVe [117], UQ-V [50], Msong [50], Audio [50], Crawl [50], Enron [50], BIGANN [127], Deep1B [39], MSTuring [127], or YandexT2I [127] and extend it with synthetic, randomly generated attributes [26, 44, 56, 63, 76, 89, 107, 139, 141, 150, 154, 158, 161, 164] (failing to meet criterion 1). Another common, though more labor-intensive, approach is to repurpose a dataset not originally intended for FANNS such as TripClick [120], MNIST [81], LAION [123], RedCaps [38], YouTube-Rgb [3], Youtube-Audio [3], Words [45], MTG [135], or WIT-Image [35] by manually creating embedding vectors and queries, or by crawling the web to obtain suitable real-world attributes [26, 44, 76, 89, 115, 152, 164] (failing to meet criterion 2). Finally, some papers originating from industry rely on proprietary in-house datasets that are not publicly available [107, 147, 154] (violating criterion 3). The only dataset we are aware of that meets all three criteria is the Paper dataset [50], containing 200-dimensional embeddings of research paper abstracts.

In addition to the scarcity of suitable datasets that fulfill all three criteria, we observe that text embeddings from state-of-theart transformer-based models such as NV-Embed [82, 111], LENS [83, 84], GTE [4, 88], Stella [110, 157], and BGE [27, 112] with thousands of dimensions are not represented in existing FANNS datasets. To clarify whether such a dataset is desperately needed or if the performance of FANNS methods is agnostic to the embedding model used, we need to answer the following two questions:

- (1) Do the characteristics of embedding vectors vary significantly across different embedding models?
- (2) Does the performance of FANNS methods depend on the characteristics of the embedding vectors?

To answer the first question, we compare embeddings from the SIFT [80] (images), Audio [50] (audio), UQ-V [50] (video), and Paper

[50] (text) datasets to transformer-based text embeddings. In Table 2 we report the dimensionality of embedding vectors, the mean absolute correlation between dimensions of the embedding space, as well as the mean, standard deviation, and best-fitting distribution (among ten candidates) for vector norms and pairwise distances between vectors in each dataset . Figures 15 to 17 show histograms for the vector norms and pairwise distances, as well as the correlation matrix for inter-dimension correlations of all five datasets. These results reveal our first key observation:

Observation 1 : The characteristics of embedding vectors vary significantly across different embedding models.

Table 2: (§4) Summary statistics of embedding vectors.

| Dataset                     | Quantity                                             | Mean ( ± Std)                                                      | Best Fit                                                    |
|-----------------------------|------------------------------------------------------|--------------------------------------------------------------------|-------------------------------------------------------------|
| SIFT                        | Dimensions Correlation Vector Norms Pairw. Distances | 128 0.182 509 ± 0.66 536 ± 115                                     | - - Beta ( a = 5 . 5 ,b = 8 . 7) Beta ( a = 168 ,b = 2 . 1) |
| Audio                       | Dimensions Correlation Vector Norms Pairw. Distances | 192 0.155 7 . 9 × 10 5 ± 2 . 0 × 10 4 1 . 46 × 10 5 ± 3 . 8 × 10 4 | - - Beta ( a = 12 . 2 ,b = 10 . 1) Normal                   |
| UQ-V                        | Dimensions Correlation Vector Norms Pairw. Distances | 256 0.738 0.225 ± 0.267 0.201 ± 0.201                              | - - Lognormal ( s = 0 . 81) Lognormal ( s = 0 . 71)         |
| Paper                       | Dimensions Correlation Vector Norms Pairw. Distances | 200 0.192 2.13 ± 0.14 1.10 ± 0.24                                  | - - Lognormal ( s = 0 . 31) Beta ( a = 472 ,b = 19 . 6)     |
| Ours (trans- former- based) | Dimensions Correlation Vector Norms Pairw. Distances | 4096 0.099 1.00 ± 1 . 3 × 10 - 7 1.08 ± 0.14                       | - - Normal Weibull ( k = 4 . 6 × 10 4 )                     |

To answer the second question, we evaluate seven representative FANNS methods on the SIFT [80], Audio [50], UQ-V [50], and Paper [50] datasets. For these experiments, we follow the same methodology as described in Section 5. Figure 18 shows the recall vs. QPS trade-off for each method on each dataset and Figure 19 shows the corresponding index construction time, peak memory usage, and index size. We observe that while some methods such as UNG or FDANN (both stitched and filtered) perform consistently across datasets, many methods exhibit significant performance variations depending on the dataset used. ACORN is significantly slower on Paper compared to other datasets, NHQ (nsw) fails to achieve a recall of over 0.4 on the Audio dataset, NHQ (kgraph) achieves significantly higher recall on SIFT and Paper than on Audio and UQ-V , and CAPS is way more competitive on Paper and Audio than on SIFT and UQ-V , which leads us to our second observation:

Observation 2 : The performance of most FANNS methods depends on the characteristics of the embedding vectors.

Our first two observations motivate the need for a new FANNS dataset that includes embeddings from state-of-the-art transformerbased models. To this end, we introduce the arxiv-for-fanns dataset, where each item corresponds to a research paper. Our dataset is available in three scales: small (1k items, 197 MB), medium (100k items, 1.86 GB), and large (over 2.7M items, 46.1 GB). Each item includes a 4096-dimensional, normalized text embedding of the paper abstract, computed using the stella\_en\_400M\_v5 model [110, 157], based on abstracts from the arXiv dataset [31]. We select stella because it is the most lightweight among the top 10 models 2 on the English MTEB leaderboard [108]. Critically, each item contains 11 real-world attributes (see Table 3) covering categorical, numerical and set-valued attributes with diverse value distributions (shown in Figure 20), fulfilling criterion 1. To satisfy criterion 2, each dataset variant includes three sets of 10k queries for EM, R, and EMIS filters (see Section 3.2), along with their corresponding precomputed ground truth. Our queries filter for the number of sub categories (EM), update date (R), and for the main categories (EMIS), but a user can easily construct his own queries using any combination of the 11 attributes.


<!-- p:8 -->


Figure 17: (§4) Correlation between different dimensions among sampled embedding vectors.

Figure 18: (§4) Recall@10 vs. QPS plots for EM filtering on four widely used datasets of different modalities.

2 As of March 11, 2025

Table 3: (§4) Attributes in the novel arXiv dataset.

| Name                                                                                                                                                                     | Attribute Type                                                                                                                                                                                  | Data type                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| submitter has_comment number_of_main_categories main_categories number_of_sub_categories sub_categories license number_of_versions update_date number_of_authors authors | unordered attribute unordered attribute ordered attribute set attribute ordered attribute set attribute unordered attribute ordered attribute ordered attribute ordered attribute set attribute | string boolean integer list of strings integer list of strings string integer integer integer list of strings |


<!-- p:9 -->


Figure 19: (§4) Index construction time, peak memory usage, and index size for EM filtering on four widely used datasets.

Figure 20: (§4) Distribution of the unordered attributes (blue), ordered attributes (green), and set attributes (yellow) in the arxiv-for-fanns-large dataset. We show inverse histograms for authors and submitter since they have many possible values and only few items with a given value. Outliers are omitted for clarity. The has\_comment attribute is true for 74.216% of items.

Query vectors are generated by embedding search terms synthesized by GPT-4o [70], while filter values are sampled from the dataset attributes. Figure 21 illustrates the selectivity distribution (as defined in Section 3.1) across queries in arxiv-for-fanns-large . To support unfiltered ANNS evaluation, we also provide ground truth results without any filtering. All three versions of the dataset are publicly available on Hugging Face 345 , fulfilling criterion 3.

3 https://hf.co/datasets/SPCL/arxiv-for-fanns-small

4 https://hf.co/datasets/SPCL/arxiv-for-fanns-medium

5 https://hf.co/datasets/SPCL/arxiv-for-fanns-large

Figure 21: (§4) Selectivity of the three query sets.

<!-- p:10 -->


## 5 Benchmarking FANNS

We benchmark ACORN [115], CAPS [63], two versions of FDANN [56] (filtered and stitched), two versions of NHQ [141] (nsw and kgraph), SeRF [164], iRangeGraph [152], DIGRA [76], DSG [116], and UNG [26] on our arxiv-for-fanns dataset. This selection of methods covers a wide range of filtering approaches, indexing techniques, and filter types.

### 5.1 Collected Metrics

To illustrate the trade-off between accuracy and query throughput, we focus on recall vs. queries per second (QPS) plots as our primary evaluation metric. We define recall@k as:

$$\ r e c a l { \varpi } { k } = \frac { | k n n _ { a l g } \cap k n n _ { g t } | } { k } \\$$

where knnalg denotes the set of k nearest neighbors returned by the algorithm, and knngt is the ground truth. In addition, we report the index construction time, peak memory usage during both index construction and query execution, and the index size.

### 5.2 Parameter Search

Since all FANNS methods considered involve tunable parameters that influence index construction, we perform a dedicated parameter search for each combination of method, dataset, and filter type prior to benchmarking. Given that some methods expose up to eight parameters, a full grid search is computationally infeasible and we therefore rely on a greedy search strategy. For some combinations of method and dataset, even the greedy search takes multiple weeks to complete. Algorithm 1 presents the pseudocode of our parameter search algorithm.

```
to complete. Algorithm 1 presents the pseudocode of our parameter
            search algorithm.
            =============================
            Algorithm 1 ($5.2) Greedy Parameter Search
            =============================
            Require: params, value_lists, default_indices
                1: indices = default_indices
                2: P = {p : value_lists[p][indices[p]] for p in params}
                3: best_reward = get_reward(P)
                4: do_repeat = true
                5: while do_repeat do
                    do_repeat = false
                    for all par = params do
                        for all change = [ -1, 1] do
                            P = {p : value_lists[p][indices[p]] for p in params}
                            P[par] = value_lists[par][indices[par] + change]
                            reward = get_reward(P)
                            if reward > best_reward then
                                if reward > (best_reward * 1.01) then
                                    do_repeat = true
                                end if
                                best_reward = reward
                                indices[par] = indices[par] + change
                            end if
                        end for
                end while
            return {p : value_lists[p][indices[p]] for p in params}
            This algorithm takes as input a list of tunable parameters, their
            corresponding candidate values, and the index of each parame-
            ter's default value inside the list of candidate values. Candidate
```

Algorithm 1 (§5.2) Greedy Parameter Search

This algorithm takes as input a list of tunable parameters, their corresponding candidate values, and the index of each parameter's default value inside the list of candidate values. Candidate and default values are selected based on the literature and publicly available implementations of each method. The get\_reward() function performs two iterations of building the index with a given parameter configuration and querying it using 50 randomly sampled queries from the dataset. It computes the recall vs. QPS curve averaged over both iterations and returns the highest QPS achieved at a recall of at least 0.95. If a method does not reach a recall of 0.95, it returns the highest achieved recall instead.

To validate our parameter search strategy, we perform a full grid search for the ACORN algorithm (only 3 parameters) on the Audio dataset, which is much smaller than arxiv-for-fanns . Both search strategies found parameters M = 24 and β = 32. The greedy search settled for γ = 15 while the grid search found γ = 12. Figure 22 confirms that both parameter configurations yield nearly identical recall vs. QPS curves, and the different parameters are likely caused by randomness in index construction and query execution stages.

Queries per Second (QPS)

Figure 22: (§3.1) Performance of ACORN on the Audio dataset with parameters from grid and greedy search.

The parameters identified by our search strategy for the SIFT , Audio , UQ-V , and Paper datasets used in Section 4 and for the arxiv-for-fanns-medium and arxiv-for-fanns-large datasets (see Sections 5.6 and 5.7) are reported in Table 4. For the study varying the parameter k (see Section 5.8), we use the parameters obtained for k = 10, as the choice of k does not affect index construction. For the study on varying query selectivity (see Section 5.9), we perform a separate parameter search for each selectivity value. The resulting parameters are available in our repository 6 .

### 5.3 Benchmarking Methodology

Once the parameter search is complete, we benchmark each method five times and report the mean and standard deviation for all measured metrics following scientific benchmarking practice [67]. Index construction is performed using all available hardware threads on the respective system (see Section 5.4), while query execution is restricted to a single thread, following common practice [26, 63, 141]. Unless stated otherwise, we search for k = 10 nearest neighbors and report recall@10, which is a standard choice in the literature [26, 56, 115, 141, 154]. All benchmarks use Euclidean distance, as it is supported by all methods under evaluation. Since our transformer-based embeddings are normalized, KNN under Euclidean distance is equivalent to KNN under cosine distance. We exclude any preprocessing, such as sorting items by attribute value or transforming vectors into alternate formats when reporting index construction time to avoid making any assumptions on the format of the input data.

6 https://github.com/spcl/fanns-benchmark


<!-- p:11 -->


Table 4: (§5.2) Parameters used for benchmarking (found through parameter search, see Section 5.2).

| Method                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Parameters                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Experiment ACORN [115] all SIFT , EM filter Audio , EM filter UQ-V , EM filter Paper , EM filter arxiv-medium , EM filter arxiv-medium , R filter arxiv-medium , EMIS filter                                                                                                                                                                                                                                                                                                                           | ef s ∈ { 10 , 15 , 20 , 25 , 30 , 50 , 100 , 250 , 500 , 750 } M = 32 ,M β = 16 ,γ = 12                                                                                                                                                                                                                                                                                                                                                                                                                         |
| arxiv-large , EM filter arxiv-large , R filter arxiv-large , EMIS filter CAPS (kmeans) [63] all m ∈ { 200 , 400 , 1 k, 5 k, 10 k, 20 k, 40 SIFT , EM filter B = 256 Audio , EM filter B = 256 UQ-V , EM filter B = 128 Paper , EM filter B = 1024 arxiv-medium , EM filter B = 128 arxiv-large , EM filter B = 512 all SIFT , EM filter Audio , EM filter UQ-V , EM filter Paper , EM filter arxiv-medium , EM filter arxiv-medium , EMIS filter arxiv-large , EM filter arxiv-large , EMIS filter all | M = 24 ,M β = 32 ,γ = 12 M = 24 ,M β = 32 ,γ = 12 M = 32 ,M β = 24 ,γ = 12 M = 16 ,M β = 24 ,γ = 10 M = 32 ,M β = 24 ,γ = 12 M = 16 ,M β = 24 ,γ = 15 M = 32 ,M β = 32 ,γ = 10 M = 32 ,M β = 16 ,γ = 12 M = 48 ,M β = 48 ,γ = 15 k, 60 k }                                                                                                                                                                                                                                                                      |
| FDANN (stitched) [56] L ∈ { 10 , 20 , 30 , 50 , 100 , 150 , 200 , R small = 32 ,L small = 80 ,R stitched = R ,L ,R                                                                                                                                                                                                                                                                                                                                                                                     | 300 , 500 , 1 k } 48 ,α = 1 . 3 small = 16 small = 80 stitched = 96 ,α = 1 . 2 R small = 32 ,L small = 80 ,R stitched = 64 ,α = 1 . 1 R small = 32 ,L small = 100 ,R stitched = 128 ,α = 1 . 3 R small = 32 ,L small = 80 ,R stitched = 48 ,α = 1 . 1 R small = 32 ,L small = 100 ,R stitched = 48 ,α = 1 . 2 R small = 96 ,L small = 100 ,R stitched = 64 ,α = 1 . 4 R small = 64 ,L small = 80 ,R stitched = 64 ,α = 1 . 2                                                                                    |
| FDANN (filtered) [56] L ∈ { , , , , , , SIFT , EM filter Audio , EM filter UQ-V , EM filter Paper , EM filter arxiv-medium , EM filter arxiv-medium , EMIS filter arxiv-large , EM filter                                                                                                                                                                                                                                                                                                              | search 10 20 30 50 100 150 200 , 300 , 500 , 1 k } R = 48 ,L = 100 ,α = 1 . 0 R = 32 ,L = 100 ,α = 1 . 2 R = 96 ,L = 60 ,α = 1 . 0 R = 48 ,L = 100 ,α = 1 . 3 R = 48 ,L = 100 ,α = 1 . 0 R = 48 ,L = 80 ,α = 1 . 2 R = 48 ,L = 200 ,α = 1 . 2                                                                                                                                                                                                                                                                   |
| arxiv-large , EMIS filter R = 48 ,L = 150 ,α = 1 . 2 NHQ (kgraph) [141] all SIFT , EM filter Audio , EM filter UQ-V , EM filter Paper , EM filter arxiv-medium , EM filter                                                                                                                                                                                                                                                                                                                             | L search ∈ { 10 , 25 , 50 , 75 , 100 , 150 , 200 , 300 , 400 } , iter = 12 ,M = 1 . 0 K = 100 ,L = 100 ,S = 15 ,R = 300 , RANGE = 50 ,PL = 400 ,B = 0 . 4 , weight = 1 M K = 40 ,L = 40 ,S = 4 ,R = 300 , RANGE = 70 ,PL = 400 ,B = 0 . 6 , weight = 10 B K = 80 ,L = 80 ,S = 10 ,R = 200 , RANGE = 60 ,PL = 300 ,B = 0 . 5 , weight = 1 M K = 60 ,L = 40 ,S = 15 ,R = 400 , RANGE = 20 ,PL = 200 ,B = 0 . 3 , weight = 100 M K = 100 ,L = 80 ,S = 15 ,R = 200 , RANGE = 70 ,PL = 200 ,B = 0 . 5 , weight = 1 M |
| arxiv-large , EM filter all SIFT , EM filter                                                                                                                                                                                                                                                                                                                                                                                                                                                           | K = 80 ,L = 60 ,S = 10 ,R = 200 , RANGE = 60 ,PL = 300 ,B = 0 . 6 , weight = 1 M                                                                                                                                                                                                                                                                                                                                                                                                                                |
| NHQ (nsw) [141] Audio , EM filter UQ-V , EM filter Paper , EM filter arxiv-medium , EM arxiv-large , EM filter                                                                                                                                                                                                                                                                                                                                                                                         | ef_search ∈ { 50 , 100 , 150 , 200 , 300 , 500 , 1 k, 2 k, 4 k } M = 50 , MaxM0 = 50 , efConstruction = 200 , weight_search = 1 M M = 40 , MaxM0 = 50 , efConstruction = 300 , weight_search = 1 M M = 20 , MaxM0 = 40 , efConstruction = 300 , weight_search = 1 M M = 40 , MaxM0 = 50 , efConstruction = 300 , weight_search = 1 M M = 40 , MaxM0 = 40 , efConstruction = 300 , weight_search = 1 M M , , , M                                                                                                 |
| filter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | = = = =                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| all SIFT , EM filter Audio , EM filter UQ-V , EM filter Paper , EM filter arxiv-medium , EM filter                                                                                                                                                                                                                                                                                                                                                                                                     | 40 MaxM0 60 efConstruction 150 weight_search 1 L search ∈ { 10 , 20 , 30 , 40 , 50 , 100 , 150 , 200 , 300 , 500 , 1 k } δ = 6 ,R = 32 ,L = 100 ,α = 1 . 4 ,σ = 12 δ = 6 ,R = 48 ,L = 100 ,α = 1 . 4 ,σ = 16 δ = 6 ,R = 48 ,L = 100 ,α = 1 . 2 ,σ = 16 δ = 6 ,R = 32 ,L = 100 ,α = 1 . 4 ,σ = 16                                                                                                                                                                                                                |
| UNG [26] arxiv-medium , EMIS filter arxiv-large , EM filter arxiv-large , EMIS filter                                                                                                                                                                                                                                                                                                                                                                                                                  | δ = 2 ,R = 24 ,L = 80 ,α = 1 . 4 ,σ = 16 δ = 8 ,R = 32 ,L = 100 ,α = 1 . 4 ,σ = 16 δ = 6 ,R = 48 ,L = 150 ,α = 1 . 6 ,σ = 24                                                                                                                                                                                                                                                                                                                                                                                    |
| SeRF [164] all arxiv-medium , R filter arxiv-large , R filter all                                                                                                                                                                                                                                                                                                                                                                                                                                      | δ = 6 ,R = 48 ,L = 150 ,α = 1 . 4 ,σ = 24 ef_search ∈ { 4 , 8 , 16 , 32 , 64 , 128 , 256 , 512 , 1024 } index_k = 100 , ef_construction = 100 , ef_max = 500 index_k = 100 , ef_construction = 100 , ef_max = 600 ef_search ∈ { 1 , 2 , 3 , 4 , 5 , 6 , 8 , 10 , 15 , 20 , 30 , 50 , 100 , 200 }                                                                                                                                                                                                                |
|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | M = 32 , ef_construction = 200 M = 24 , ef_construction = 100                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| arxiv-medium , R filter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | ef_search ∈ { 4 , 8 , 16 , 32 , 64 , 128 , 256 , 512 , 1024 } ,M = 24 , ef_construction = 200 , ef_max = 500 ,α = 1 .                                                                                                                                                                                                                                                                                                                                                                                           |
|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DSG [116]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| , , , , , , , , , , , , , ,M ,                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| filter ef_search 1 2 3 4 5 6 8 10 15 20 30 50 100 200                                                                                                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| , R                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| = 24                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | = 24                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ∈ { }                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | ef_construction 200                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | =                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| arxiv-medium                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| arxiv-large , R DIGRA [76]                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| filter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | filter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| iRangeGraph [152]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| arxiv-medium , R filter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

### 5.4 Software and Hardware Configuration

We encapsulate our benchmarking infrastructure in a Docker container based on Ubuntu 20.04.6. We use Python 3.8.10, gcc 9.4.0, and g++ 9.4.0. Benchmarks on the medium-scale dataset are run on an Intel Core i7-1165G7 CPU with 4 physical cores, 8 hardware threads, and 16 GB RAM, running Arch Linux with kernel version 6.15.5-arch1-1 and those on the large dataset run on a machine with 384 GB of RAM and two Intel Xeon Gold 6154 CPUs, each with 18 physical cores and 36 hardware threads, running CentOS Linux 8.


<!-- p:12 -->


Figure 23: (§5.6) Recall@10 vs. QPS plots for the three filter types (EM, R, EMIS) on the arxiv-for-fanns-medium dataset.

Figure 24: (§5.6) Index construction time, peak memory usage, and index size on the arxiv-for-fanns-medium dataset.

### 5.5 Remarks on Algorithms

NHQ-kgraph. We exclude the call to optimize\_graph() from query execution timing, as it is independent of the number of queries and its cost is amortized when processing large batches.

ACORN. Algorithmically, ACORN only needs to check the filter condition for visited vertices during graph traversal. However, the implementation we benchmark performs this check for all items prior to traversal. Since prior work is inconsistent on whether this cost is included [26] or not [115], we report two recall vs. QPS curves for ACORN: one including the filtering overhead (labeled 'upper bound') and one excluding it (labeled 'lower bound').

SeRF, DIGRA. Unlike most other methods, SeRF and DIGRA perform index construction and query execution within a single process, without persisting the index to disk. Therefore, we report only the overall peak memory usage, and we omit the index size from our results.

FDANN. The code provided in the FDANN repository [105] stores two versions of the index, each approximately the size of the original dataset. We optimize the code to store only one index at a time, reducing the overall index size to half.

DSG, DIGRA. Unlike most of the other methods, DSG and DIGRA do not parallelize index construction. Therefore, we report index construction time for a single thread in our benchmarking on arxiv-for-fanns-medium and we omit DSG and DIGRA from our benchmarking on arxiv-for-fanns-large .

### 5.6 Results on arxiv-for-fanns-medium

Figure 23 shows the recall vs. QPS curves for the three filter types on the arxiv-for-fanns-medium dataset. We observe that ACORN, the only evaluated method applicable to all three filter types, is generally outperformed by more specialized methods. FDANN, which lagged slightly behind UNG on the established datasets (see Figure 18), matches UNG's performance on our transformer-based embeddings with EM filters and even outperforms UNG with EMIS filters. NHQ (kgraph), a top performer on only two of the four established datasets, is among the best methods on our dataset.

Observation 3 : Specialized FANNS methods that only support specific filters outperform more versatile methods by up to 10 × .

Figure 24 summarizes index construction time, peak memory usage, and index size on the arxiv-for-fanns-medium dataset. Index construction time varies by more than an order of magnitude across methods, with DIGRA and DSG being the slowest since they are the only methods that do not parallelize index construction. Except for NHQ (kgraph) and SeRF, which show noticeably higher peak memory usage, differences in memory consumption during index construction and query execution are moderate across methods. The index built by most methods is approximately 1.6 GB, corresponding to the size of the dataset. Some methods produce very small indexes but require access to the original database vectors during query execution, resulting in the same effective index size.

Observation 4 : Index construction times vary by up to 16 × across methods but do not correlate with query performance.


<!-- p:13 -->


Figure 25: (§5.7) Recall@10 vs. QPS plots for the three filter types (EM, R, EMIS) on the arxiv-for-fanns-large dataset.

Figure 26: (§5.7) Index construction time, peak memory usage, and index size on the arxiv-for-fanns-large dataset.

### 5.7 Results on arxiv-for-fanns-large

5.7.1 Challenges In Scaling Up the Dataset Size. While 2 . 7 million vectors may not sound particularly large, note that our transformerbased embeddings have 4 , 096 dimensions, making our dataset over 85 × larger than the well-known SIFT1M dataset [80] which uses 128-dimensional embedding vectors. We had to modify the source code of four out of the eleven methods we benchmarked to fix int32 overflows during memory allocation (UNG [26], CAPS [63], and NHQ (KGraph) [141]) or to reduce the index size (FDANN (stitched) [56]) to fit in the local persistent storage. Because index construction for DSG and DIGRA is non-parallelized, takes over a day per run, and requires dozens of runs for parameter tuning, we could not benchmark these two methods on the large dataset.

5.7.2 Results. Figure 25 shows the recall vs. QPS curves for the three filter types on the arxiv-for-fanns-large dataset. Comparing these results to those on the medium-scale dataset in Figure 23 provides insights into scalability. ACORN, both NHQ variants, FDANN (filtered), SeRF, and iRangeGraph maintain their relative performance, with throughput dropping by only a factor of about 4 despite the dataset being 27 × larger. This indicates good scalability, especially considering that both experiments used a single thread, albeit on different machines. FDANN (stitched), CAPS, and UNG perform poorly on the large dataset and fail to exceed 25% recall. We cannot rule out that suboptimal parameter choices contribute to this performance drop as our greedy parameter search may have converged to local optima. This highlights the difficulty of parameter tuning for FANNS methods on large datasets.

Observation 5 : Scaling to large datasets can cause recall to drop below 0 . 2, rendering some methods useless. Adjustments of the implementation or parameter tuning strategies may be required.

Figure 26 reports index construction time, peak memory usage, and index size for all methods. On the 27 × larger dataset, construction time increased by roughly an order of magnitude. Since 9 × more threads were used, this suggests super-linear growth with dataset size or sublinear thread speedup. CAPS remains the fastest to build, with NHQ and FDANN also being relatively fast. UNG has by far the longest construction time, likely because it failed to reach the 0 . 95 recall target and the search shifted toward more expensive configurations. Memory usage scales roughly linearly with dataset size, and relative differences remain similar to the medium-scale case. UNG is notable for compressing the index to about 25% of the dataset with CAPS, iRangeGraph, and NHQ (kgraph) producing compact indexes but requiring access to the original vectors.

Observation 6 : Parameter tuning is difficult on large datasets, with indexes construction taking up to 6 hours for 2.7M items.

### 5.8 Analysis for Different Values of k

In Figure 27, we show recall vs. QPS plots for EM filters on the arxiv-for-fanns-medium dataset with k ∈ { 20 , 40 , 60 , 80 , 100 } . Figures 28 and 29 present the same study for R and EMIS filters, respectively. Index construction time, memory usage, and index size show almost no variation with k and are therefore omitted.

Observation 7 : The relative performance of different FANNS methods remains consistent across different values of k .


<!-- p:14 -->


Figure 27: (§5.8) Recall@k vs. QPS plots for varying values of k on the arxiv-for-fanns-medium dataset with EM filtering.

Figure 28: (§5.8) Recall@k vs. QPS plots for varying values of k on the arxiv-for-fanns-medium dataset with R filtering.

Figure 29: (§5.8) Recall@k vs. QPS plots for varying values of k on the arxiv-for-fanns-medium dataset with EMIS filtering.

Figure 30: (§5.9) Index construction time, peak memory usage, and index size for EM filtering with varying selectivity.

<!-- p:15 -->


多

Figure 31: (§5.9) Recall@10 vs. QPS plots for EM filtering on arxiv-for-fanns-medium with different query selectivities.

Query Execution Query Execution

SeRF

ACORN

iRangGraph DIGRA

DSG

WMH

SeRF

ACORN

iRangGraph DIGRA

DSG

Index size

2.00

1.75

1.50

1.25

1.00

0.75

0.50

Index Size [GB]

0.25

0.00

ACORN

iRangGraph

DIGRA

DSG

Figure 32: (§5.9) Index construction time, peak memory usage, and index size for R filtering with varying selectivity.

Figure 33: (§5.9) Recall@10 vs. QPS plots for R filtering on arxiv-for-fanns-medium with different query selectivities.


<!-- p:16 -->


Figure 34: (§5.9) Index construction time, peak memory usage, and index size for EMIS filtering with varying selectivity.

Figure 35: (§5.9) Recall@10 vs. QPS plots for EMIS filtering on arxiv-for-fanns-medium with different query selectivities.

### 5.9 Analysis for Different Query Selectivities

To explore the impact of query selectivity on FANNS performance, we benchmark a version of our arxiv-for-fanns-medium dataset where we generate synthetic attributes in order to control the query selectivity. Figures 31, 33 and 35 show recall vs. QPS plots for EM, R, and EMIS filters with selectivities of 0 . 2, 0 . 4, 0 . 6, and 0 . 8. Figures 30, 32 and 34 report index construction time, peak memory usage, and index size for the same experiments. We observe that NHQ (nsw) with EM filters exhibits substantial difficulty with low selectivity scenarios, while UNG with EMIS filters handles low selectivity scenarios slightly better than high selectivity ones. There are also some variations in index construction time, with ACORN being slower to build for selectivity close to 0 . 5 than for more extreme selectivities, and DIGRA being faster to build for lower selectivities. Memory usage and index size are unaffected by selectivity.

Observation 8 : The performance and resource usage of most FANNS methods is largely consistent across query selectivities; however, some methods exhibit significant performance degradation in low-selectivity scenarios.

## 6 Related Work

Interest in FANNS is growing, with new methods introduced each year, an ACM SIGMOD programming contest [30] dedicated to FANNS, and survey and benchmark preprints appearing around the same time as ours. Lin et al. [90] classify methods in a pruningoriented framework, analyzing the combination of vector pruning (i.e., ANNS) and scalar pruning (i.e., attribute filtering), while Shi et al. [125] benchmark selected methods on existing datasets, though, to the best of our knowledge, not on transformer-based embeddings. Our work complements these efforts by introducing a taxonomy along three dimensions: filtering approach, indexing technique, and filter types, and by contributing a transformer-based dataset together with benchmarks on both established and new datasets.

Such transformer-based datasets that reflect emerging retrievalaugmented generation (RAG) workloads are currently missing in the ANNS and FANNS literature. We generate our embedding vectors with the stella\_en\_400M\_v5 model [110, 157], widely adopted in LLM research [23, 78]. Unlike our arxiv-for-fanns dataset, end-to-end RAG benchmarks such as the Massive Text Embedding Benchmark [108] contain text passages rather than vectors, making them unsuitable for direct evaluation of FANNS methods.


<!-- p:17 -->


In the broader ANNS field, surveys by Echihabi et al. [42] and Han et al. [65] provide comprehensive overviews, and large-scale benchmarks [15, 16, 144] compare methods across datasets. To the best of our knowledge, these do not cover transformer-based embeddings; since our dataset also contains the ground truth for unfiltered ANNS, it could be used to extend these prior works.

## 7 Conclusion

The rapid progress of embedding models for text, image, audio, and video has created strong demand for fast and accurate FANNS methods. Recent work has proposed diverse approaches supporting EM, R, and EMIS filtering. To structure this evolving field, we present a taxonomy classifying methods by filtering approach, indexing technique, and filter type, and we survey FANNS methods accordingly. By analyzing how FANNS methods are evaluated in literature, we identify a key limitation: the lack of open datasets with transformer-based embeddings and real-world attributes. Analyzing embeddings from images, audio, video, and text, we find that the embedding model strongly shapes vector characteristics and hence FANNS performance, which motivates the need for transformerbased datasets.

To address this gap, we release the arxiv-for-fanns dataset, which contains over 2.7 million 4096-dimensional vectors with 11 attributes and reflects realistic transformer-based workloads. Using this dataset, we perform an in-depth benchmarking study of FANNS methods, analyzing their performance across different filter types, dataset scales, numbers of retrieved neighbors, and query selectivities. By distilling our results into eight key observations, we provide practical guidance for selecting and configuring FANNS methods, and by publishing our dataset, we establish a benchmark that helps steer future research towards more efficient FANNS methods for state-of-the-art, transformer-based embedding vectors.

## 8 Acknowledgements

We thank the Swiss National Supercomputing Centre (CSCS) for access to their Ault system, which we used to execute our benchmarks. Furthermore, we thank the PLGrid Consortium for access to their Athena system, which we used to create the arxiv-for-fanns dataset. This work was supported by the ETH Future Computing Laboratory (EFCL), financed by a donation from Huawei Technologies. It also received funding from the European Research Council (Project PSAP, No. 101002047) and from the European Union's HE research and innovation programme under the grant agreement

- No. 101070141 (Project GLACIATION).
