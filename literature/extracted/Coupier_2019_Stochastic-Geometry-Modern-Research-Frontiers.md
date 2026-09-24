---
id: "Coupier_2019_Stochastic-Geometry-Modern-Research-Frontiers"
source_pdf: "../pdf/Coupier_2019_Stochastic-Geometry-Modern-Research-Frontiers.pdf"
source_filename: "Coupier_2019_Stochastic-Geometry-Modern-Research-Frontiers.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Coupier_2019_Stochastic-Geometry-Modern-Research-Frontiers.references.md"
---

<!-- p:1 -->

Lecture Notes in Mathematics  2237

David Coupier Editor

## Stochastic Geometry

Modern Research Frontiers Springer

<!-- p:2 -->


##### Lecture Notes in Mathematics 2237

####### Editors-in-Chief:

Jean-Michel Morel, Cachan Bernard Teissier, Paris

####### Advisory Editors:

Michel Brion, Grenoble Camillo De Lellis, Princeton Alessio Figalli, Zurich Davar Khoshnevisan, Salt Lake City Ioannis Kontoyiannis, Cambridge Gábor Lugosi, Barcelona Mark Podolskij, Aarhus Sylvia Serfaty, New York Anna Wienhard, Heidelberg CEMPI is a joint project for research, training and technology transfer of the Laboratoire de Mathématiques Paul Painlevé and the Laboratoire de Physique des Lasers, Atomes et Molécules (PhLAM) of the Université Lille 1 and the CNRS. It was created as a "Laboratoire d'Excellence" in the framework of the "Programme d'Investissements d'Avenir" of the French government in February 2012.


<!-- p:3 -->

Research at CEMPI covers a wide spectrum of knowledge from pure and applied mathematics to experimental and applied physics. CEMPI organizes every year the Painlevé-CEMPI-PhLAM Thematic Semester that brings together leading scholars from around the world for a series of conferences, workshops and post-graduate courses on CEMPI's main research topics.

For more information, see CEMPI's homepage http://math.univ-lille1.fr/~cempi/.

CEMPI Scientific Coordinator and CEMPI Series Editor Stephan DE BIÈVRE (Université Lille 1)

CEMPI Series Editorial Board Prof. Fedor A. BOGOMOLOV (New York University) Dr. Jean-Claude GARREAU (Université Lille 1 and CNRS) Prof. Alex LUBOTZKY (Hebrew University) Prof. Matthias NEUFANG (Carleton University and Université Lille 1) Prof. Benoît PERTHAME (Université Pierre et Marie Curie) Prof. Herbert SPOHN (Technische Universität München)

More information about this series at

http://www.springer.com/series/13851


<!-- p:4 -->


David Coupier Editor

### Stochastic Geometry

Modern Research Frontiers

123


<!-- p:5 -->


Editor David Coupier LAMAV Université Polytechnique des Hauts de France (UPHF) Valenciennes, France

####### ISSN 0075-8434 ISSN 1617-9692 (electronic) Lecture Notes in Mathematics ISBN 978-3-030-13546-1 ISBN 978-3-030-13547-8 (eBook) https://doi.org/10.1007/978-3-030-13547-8

Mathematics Subject Classification (2010): Primary: 60

©Springer Nature Switzerland AG 2019 This work is subject to copyright. All rights are reserved by the Publisher, whether the whole or part of the material is concerned, specifically the rights of translation, reprinting, reuse of illustrations, recitation, broadcasting, reproduction on microfilms or in any other physical way, and transmission or information storage and retrieval, electronic adaptation, computer software, or by similar or dissimilar methodology now known or hereafter developed. The use of general descriptive names, registered names, trademarks, service marks, etc. in this publication does not imply, even in the absence of a specific statement, that such names are exempt from the relevant protective laws and regulations and therefore free for general use. The publisher, the authors and the editors are safe to assume that the advice and information in this book are believed to be true and accurate at the date of publication. Neither the publisher nor the authors or the editors give a warranty, express or implied, with respect to the material contained herein or for any errors or omissions that may have been made. The publisher remains neutral with regard to jurisdictional claims in published maps and institutional affiliations.

This Springer imprint is published by the registered company Springer Nature Switzerland AG. The registered company address is: Gewerbestrasse 11, 6330 Cham, Switzerland


<!-- p:6 -->


## Preface

This manuscript is the third volume of the 'CEMPI subseries' common to Lecture Notes in Mathematics and Lecture Notes in Physics.

Stochastic geometry can be succinctly described as the study of random spatial patterns. It is traditionally considered to have been born in the eighteenth century with the well-known Buffon's needle problem, and it has received growing attention from the mathematical community during the second part of the twentieth century. Nowadays, stochastic geometry draws on a large variety of subdomains of mathematics such as point processes, geometric random graphs, percolation, convex geometry, random fields and spatial statistics and admits a wide range of applications. Let us cite for example astronomy, computational geometry, telecommunication networks, image analysis and stereology, and material science.

The GDR GeoSto (http://gdr-geostoch.math.cnrs.fr/) is a national research structure funded by the CNRS and created in 2012, which aims to federate the French community working on stochastic geometry. Since 2014, its yearly meeting has been preceded by two introductory courses. This volume contains five of these introductory lectures.

The first chapter is a historically motivated introduction to stochastic geometry, whereas each of the other four gives an introduction to one important branch of contemporary stochastic geometry, which we have called 'Highlights in Stochastic Geometry'. The chapters also have in common their proximity to applications. Let us describe them briefly.

The first chapter, entitled 'Some classical problems in random geometry', is based on lectures by Pierre Calka (Université de Rouen, France) given in Lille in 2014. It presents four historical questions on geometric probabilities, namely the Buffon's needle problem, the Bertrand paradox, the Sylvester four-point problem and the bicycle wheel problem. Through each of these classical problems, the author highlights the topics currently most active in stochastic geometry.

The second chapter entitled 'Understanding spatial point patterns through intensity and conditional intensities', written by Jean-François Coeurjolly (Université du Québec, Canada) and Frédéric Lavancier (Université de Nantes, France), is based on lectures by Jean-François Coeurjolly given in Lille in 2014. This chapter presents point process statistics from an original point of view, namely through intensities and conditional intensities, in order to capture interactions between points of the process. With several references to implemented packages, the authors are concerned with remaining close to applications: their exposition should be very useful for the working spatial statistician.


<!-- p:7 -->


The third chapter, entitled 'Stochastic methods for image analysis', is based on lectures by Agnès Desolneux (CMLA and ENS Paris-Saclay, France) given in Poitiers in 2015. It is about stochastic methods for computer vision and image analysis. It starts with a very nice introduction to the Gestalt theory that is a psychophysiological theory of human visual perception, which can be translated into a mathematical framework thanks to the non-accidentalness principle, and is illustrated by many convincing pictures.

While fractal analysis of one-dimensional signals is mainly based on the use of fractional Brownian motion, its generalization to higher dimensions, motivated in particular by medical imaging questions, requires a deep understanding of random fields. The fourth chapter, entitled 'Introduction to random fields and scale invariance', based on lectures by Hermine Biermé (Université de Poitiers, France) given in Nantes in 2016, appears as a useful survey and an overview of recent achievements for the worker in this field.

The fifth chapter, entitled 'Introduction to the theory of Gibbs point processes', is based on lectures by David Dereudre (Université de Lille, France) given in Nantes in 2016. This last chapter is a very clear and stimulating review of Gibbs point processes, an area of research with a long tradition in statistical physics and novel impulses from stochastic geometry and spatial statistics. After a careful introduction, the author summarizes recent results on the main challenging question in the topic: the uniqueness of Gibbs point processes in infinite volume.

In conclusion, this volume offers a unique and accessible overview (up to the frontiers of recent research) of the most active fields in stochastic geometry. We hope that it will make the reader want to go further.

Valenciennes, France November 2018

David Coupier


<!-- p:8 -->


## Acknowledgements

On behalf of GDR GeoSto, we sincerely acknowledge the authors of the five chapters contained in this book for their precious work and all the participants of the annual meetings of the GDR without whom this book would not exist.

Since its creation in 2012, the GDR GeoSto is totally funded by the French National Center for Scientific Research (CNRS).

The edition of this manuscrit was made possible by the Labex CEMPI (ANR-11LABX-0007-01).


<!-- p:9 -->


## Contents

|   1 Some Classical Problems in Random Geometry . . . . . . . . . . . . . . . . . . . . . . . . | 1 Some Classical Problems in Random Geometry . . . . . . . . . . . . . . . . . . . . . . . .                                                                                                             | 1 Some Classical Problems in Random Geometry . . . . . . . . . . . . . . . . . . . . . . . .                                                                              | . 1          |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
|                                                                                                | Pierre Calka                                                                                                                                                                                             |                                                                                                                                                                           |              |
|                                                                                            1.1 |                                                                                                                                                                                                          | Introduction: Geometric Probability, Integral Geometry, Stochastic Geometry . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | . . . . . 1  |
|                                                                                            1.2 | From                                                                                                                                                                                                     | Buffon's Needle to Integral Geometry . . . . . . . . . . . . . . . . . . . . .                                                                                            | . . . . . 3  |
|                                                                                                | 1.2.1                                                                                                                                                                                                    | Starting from Buffon's Needle . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                     | . . . . . 4  |
|                                                                                                | 1.2.2                                                                                                                                                                                                    | Cauchy-Crofton formula . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                | . . . . . 6  |
|                                                                                                | 1.2.3                                                                                                                                                                                                    | Extension to Higher Dimension................................                                                                                                             | 6            |
|                                                                                            1.3 | From Bertrand's Paradox to Random                                                                                                                                                                        | Tessellations . . . . . . . . . . . . . .                                                                                                                                 | . . . . . 10 |
|                                                                                                | 1.3.1                                                                                                                                                                                                    | Starting from Bertrand's Paradox . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                        | . . . . . 10 |
|                                                                                                | 1.3.2                                                                                                                                                                                                    | Random Sets of Points, Random Sets of Lines and Extensions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                      | . . . . . 12 |
|                                                                                                | 1.3.3                                                                                                                                                                                                    | On Two Examples of Random Convex Tessellations . . . .                                                                                                                    | . . . . . 13 |
|                                                                                                | 1.3.4                                                                                                                                                                                                    | Mean Values and Distributional Properties of the Zero-Cell and of the Typical Cell . . . . . . . . . . . . . . . . . .                                                    | . . . . . 17 |
|                                                                                            1.4 | From                                                                                                                                                                                                     | Sylvester's Four-Point Problem to Random Polytopes . . . .                                                                                                                | . . . . . 20 |
|                                                                                                | 1.4.1                                                                                                                                                                                                    | Starting from Sylvester's Four-Point Problem . . . . . . . . . . .                                                                                                        | . . . . . 20 |
|                                                                                                | 1.4.2                                                                                                                                                                                                    | Random Polytopes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . 28 |
|                                                                                            1.5 | From and                                                                                                                                                                                                 | the Bicycle Wheel Problem to Random Coverings Continuum Percolation.............................................                                                          | 32           |
|                                                                                                | 1.5.1                                                                                                                                                                                                    | Starting from the Bicycle Wheel Problem and Random Covering of the Circle . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                       | . . . . . 32 |
|                                                                                                | 1.5.2                                                                                                                                                                                                    | A Few Basics on the Boolean Model . . . . . . . . . . . . . . . . . . . . .                                                                                               | . . . . . 35 |
|                                                                                                | References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                     | . . .                                                                                                                                                                     | . . . . . 38 |
|                                                                                              2 | Understanding Spatial Point Patterns Through Intensity and Conditional Intensities . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . Jean-François Coeurjolly and Frédéric Lavancier | . . . . . . . . .                                                                                                                                                         | . . . . . 45 |
|                                                                                            2.1 | Introduction . . . . . . . . . . . . . . .                                                                                                                                                               | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                         | . . . . . 45 |
|                                                                                                | 2.2                                                                                                                                                                                                      | Intensity and Conditional Intensity Functions . . . . . . . . . . . . . . . . . . . .                                                                                     | . . . . . 47 |


<!-- p:10 -->


x

|           | 2.2.1                                                                                                                                            | Definition and Theoretical Characterization of a Spatial Point Process . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .   | . . . . . . . 47                    |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
|           | 2.2.2                                                                                                                                            | Moment Measures Factorial Moment Measures and Intensity Functions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                              | . . . . . . . 48                    |
|           | 2.2.3                                                                                                                                            | Palm Distributions and Palm Intensities . . . . . . . . . . . . . . . .                                                                                            | . . . . . . . 49                    |
|           | 2.2.4                                                                                                                                            | Papangelou Conditional Intensities . . . . . . . . . . . . . . . . . . . . .                                                                                       | . . . . . . . 52                    |
| 2.3       | Examples on Standard Models of Spatial Point Processes . . .                                                                                     | . .                                                                                                                                                                | . . . . . . . 54                    |
|           | 2.3.1                                                                                                                                            | Poisson Point Process . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . . 54                    |
|           | 2.3.2                                                                                                                                            | Gibbs Point Processes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . . 56                    |
|           | 2.3.3                                                                                                                                            | Cox Processes...................................................                                                                                                   | 59                                  |
|           | 2.3.4                                                                                                                                            | Determinantal Point Processes . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                  | . . . . . . . 62                    |
| 2.4       | Estimating the Intensity Function .                                                                                                              | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                                        | . . . . . . . 63                    |
|           | 2.4.1                                                                                                                                            | Constant Intensity...............................................                                                                                                  | 64                                  |
|           | 2.4.2                                                                                                                                            | Non Parametric Estimation of the Intensity Function.........                                                                                                       | 66                                  |
|           | 2.4.3                                                                                                                                            | Parametric Estimation of the Intensity Function . . . . . . .                                                                                                      | . . . . . . . 67                    |
| 2.5       |                                                                                                                                                  | Higher-Order Interaction Estimation via Conditional Intensity                                                                                                      | . . . . . . 72                      |
|           | 2.5.1                                                                                                                                            | Parametric Estimation with the Papangelou Conditional Intensity . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                            | . . . . . . . 73                    |
|           | 2.5.2                                                                                                                                            | Palm Likelihood Estimation....................................                                                                                                     | 80                                  |
| 2.6       | Conclusion . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                 | . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                                            | . . . . . . . 81                    |
|           | References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .         | References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                           | . . . . . . 82                      |
| 3         | Stochastic Methods for Image Analysis . .                                                                                                        | . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                                                | . . . . . . . 87                    |
| Agnès 3.1 | Desolneux Visual Perception and the Non-accidentalness Principle..............                                                                   | Desolneux Visual Perception and the Non-accidentalness Principle..............                                                                                     | 87                                  |
|           | 3.1.1                                                                                                                                            | Gestalt Theory of Visual Perception . . . . . . . . . . . . . . . . . . . .                                                                                        | . . . . . . . 89                    |
|           | 3.1.2                                                                                                                                            | The Non-accidentalness Principle . . . . . . . . . . . . . . . . . . . . . .                                                                                       | . . . . . . . 93                    |
| 3.2       | A Contrario Method for the Detection of Geometric Structures in Images                                                                           | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                  | . . . . . . . 95                    |
|           | 3.2.1                                                                                                                                            | General Formulation of a Contrario Methods . . . . . . . . . .                                                                                                     | . . . . . . . 95                    |
|           | 3.2.2                                                                                                                                            | Detection of Alignments in an Image..........................                                                                                                      | 96                                  |
|           | 3.2.3                                                                                                                                            | Detection of Contrasted or Smooth Curves....................                                                                                                       | 102                                 |
|           | 3.2.4                                                                                                                                            | Detection of Vanishing Points..................................                                                                                                    | 108                                 |
|           | 3.2.5                                                                                                                                            | Detection of the Similarity of a Scalar Attribute . . . . . . .                                                                                                    | . . . . . . . 111                   |
|           | 3.2.6                                                                                                                                            | Discussion.......................................................                                                                                                  | 113                                 |
| 3.3       | Stochastic Models of Images: The Problem of Modeling and Synthesizing Texture Images . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | .                                                                                                                                                                  | . . . . . . . 114                   |
|           | . . .                                                                                                                                            | . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                                                            | . . . . . . . 115                   |
|           | 3.3.1                                                                                                                                            | What is a Texture Image?                                                                                                                                           |                                     |
|           | 3.3.2                                                                                                                                            | Texture Synthesis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                  | . . . . . . . 115                   |
|           | 3.3.3 3.3.4                                                                                                                                      | Discrete Fourier Transform and the RPN Algorithm . . Gaussian Models for Texture Images . . . . . . . . . . . . . . . . . .                                        | . . . . . . . 118 . . . . . . . 121 |
|           | 3.3.5                                                                                                                                            | Shot Noise Model and Dead Leaves Model . . . . . . . . . . .                                                                                                       | . . . . . . . 124                   |
|           | References                                                                                                                                       | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                      | . . . . . . . 126                   |


<!-- p:11 -->


| 4 Introduction to Random Fields and Scale Invariance . . . . . . .   | 4 Introduction to Random Fields and Scale Invariance . . . . . . .   | .                                                                                                                           | . . . . . . . . . . . 129   |
|----------------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| Hermine                                                              | Biermé                                                               |                                                                                                                             |                             |
| 4.1                                                                  | Random                                                               | Fields and Scale Invariance...................................                                                              | 129                         |
|                                                                      | 4.1.1                                                                | Introduction to Random Fields . . . . . . . . . . . . . . . . . . . . . .                                                   | . . . . . . . . . . . 130   |
|                                                                      | 4.1.2                                                                | Stationarity and Invariances . . . . . . . . . . . . . . . . . . . . . . . . .                                              | . . . . . . . . . . . 135   |
| 4.2                                                                  | Sample                                                               | Paths Properties . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                  | . . . . . . . . . . . 149   |
|                                                                      | 4.2.1                                                                | Sample Paths Regularity........................................                                                             | 149                         |
|                                                                      | 4.2.2                                                                | Hausdorff Dimension of Graphs . . . . . . . . . . . . . . . . . . . .                                                       | . . . . . . . . . . . 154   |
| 4.3                                                                  | Simulation                                                           | and Estimation..............................................                                                                | 157                         |
|                                                                      | 4.3.1                                                                | Simulation.......................................................                                                           | 157                         |
|                                                                      | 4.3.2 . . .                                                          | Estimation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                | . . . . . . . . . . . 163   |
|                                                                      | 4.3.3                                                                | Application in Medical Imaging Analysis . . . . . . . . . .                                                                 | . . . . . . . . . . . 168   |
| 4.4                                                                  | Geometric                                                            | Construction . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                      | . . . . . . . . . . . 171   |
|                                                                      | 4.4.1                                                                | Random Measures . . . . . . . . . . . .                                                                                     | . . . . . . . . . . . 171   |
|                                                                      | 4.4.2                                                                | . . . . . . . . . . . . . . . . . . . . . . . Chentsov's Representation: Lévy and Takenaka                                  |                             |
|                                                                      |                                                                      | Constructions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                               | . . . . . . . . . . . 173   |
|                                                                      | 4.4.3                                                                | Fractional Poisson Fields . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                           | . . . . . . . . . . . 175   |
| References                                                           | to the Theory of Gibbs Point Processes . . . .                       | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | . . . . . . . 178           |
| 5                                                                    | Introduction                                                         | . . . . .                                                                                                                   | . . . . . . . . . . . 181   |
| David                                                                | Dereudre                                                             |                                                                                                                             |                             |
|                                                                      | 5.1                                                                  | Introduction . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .            | . . . . . . . . . . . 181   |
| 5.2                                                                  | Finite                                                               | Volume Gibbs Point Processes . . . . . . . . . . . . . . . . . . . . . . .                                                  | . . . . . . . . . . . 183   |
|                                                                      | 5.2.1                                                                | Poisson Point Process . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                         | . . . . . . . . . . . 184   |
|                                                                      | 5.2.2                                                                | Energy Functions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                    | . . . . . . . . . . . 185   |
|                                                                      | 5.2.3                                                                | Finite Volume GPP . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                       | . . . . . . . . . . . 188   |
|                                                                      | 5.2.4                                                                | DLR Equations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                   | . . . . . . . . . . . 190   |
|                                                                      | 5.2.5                                                                | GNZ Equations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                   | . . . . . . . . . . . 191   |
|                                                                      | 5.2.6                                                                | Ruelle Estimates . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                  | . . . . . . . . . . . 193   |
| 5.3                                                                  | Infinite                                                             | Volume Gibbs Point Processes.................................                                                               | 194                         |
|                                                                      | 5.3.1                                                                | The Local Convergence Setting . . . . . . . . . . . . . . . . . . . . .                                                     | . . . . . . . . . . . 195   |
|                                                                      | 5.3.2                                                                | An Accumulation Point P z,β . . . . . . . . . . . . . . . . . . . . . . . .                                                 | . . . . . . . . . . . 196   |
|                                                                      | 5.3.3                                                                | The Finite Range Property . . . . . . . . . . . . . . . . . . . . . . . . . .                                               | . . . . . . . . . . . 198   |
|                                                                      | 5.3.4                                                                | DLR Equations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                   | . . . . . . . . . . . 199   |
|                                                                      | 5.3.5                                                                | GNZ Equations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                   | . . . . . . . . . . . 201   |
|                                                                      | 5.3.6                                                                | Variational Principle . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                     | . . . . . . . . . . . 203   |
|                                                                      | 5.3.7                                                                | A Uniqueness Result . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                         | . . . . . . . . . . . 206   |
|                                                                      | 5.3.8                                                                | A Non-uniqueness Result . . . . . . . . . . . . . . . . . . . . . . . . . . .                                               | . . . . . . . . . . . 209   |
| 5.4                                                                  |                                                                      | Parameters . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                            | . . . . . . . . . . . 214   |
|                                                                      | Estimation of 5.4.1                                                  | . . . . . . . . . Maximum Likelihood Estimator . . . . . . . . . . . . . . . . . . . .                                      | . . . . . . . . . . . 215   |
|                                                                      | 5.4.2                                                                | Takacs-Fiksel Estimator . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                           | . . . . . . . . . . . 217   |
|                                                                      | 5.4.3                                                                | Maximum Pseudo-Likelihood Estimator . . . . . . . . . . .                                                                   | . . . . . . . . . . . 220   |
|                                                                      | 5.4.4                                                                | Solving an Unobservable Issue . . . . . . . . . . . . . . . . . . . . .                                                     | . . . . . . . . . . . 222   |
|                                                                      | 5.4.5                                                                | A Variational Estimator.........................................                                                            | 223                         |
|                                                                      | References                                                           | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .         | . . . . . . . . . . . 227   |


<!-- p:12 -->


## Contributors

| Hermine Biermé LMA, UMR CNRS 7348, Université de Poitiers, Chasseneuil, France                               |
|--------------------------------------------------------------------------------------------------------------|
| Pierre Calka University of Rouen, LMRS, Saint-Étienne-du-Rouvray, France                                     |
| Jean-François Coeurjolly Université du Québec à Montréal, Département de Mathématiques, Montréal, QC, Canada |
| David Dereudre University Lille, Villeneuve-d'Ascq, France                                                   |
| Agnès Desolneux CNRS, CMLA and ENS Paris-Saclay, Paris, France                                               |
| Frédéric Lavancier Université de Nantes, Laboratoire de Mathématiques Jean Leray, Nantes, France             |


<!-- p:13 -->


## Chapter 1 Some Classical Problems in Random Geometry

####### Pierre Calka

Abstract This chapter is intended as a first introduction to selected topics in random geometry. It aims at showing how classical questions from recreational mathematics can lead to the modern theory of a mathematical domain at the interface of probability and geometry. Indeed, in each of the four sections, the starting point is a historical practical problem from geometric probability. We show that the solution of the problem, if any, and the underlying discussion are the gateway to the very rich and active domain of integral and stochastic geometry, which we describe at a basic level. In particular, we explain how to connect Buffon's needle problem to integral geometry, Bertrand's paradox to random tessellations, Sylvester's fourpoint problem to random polytopes and Jeffrey's bicycle wheel problem to random coverings. The results and proofs selected here have been especially chosen for nonspecialist readers. They do not require much prerequisite knowledge on stochastic geometry but nevertheless comprise many of the main results on these models.

### 1.1 Introduction: Geometric Probability, Integral Geometry, Stochastic Geometry

Geometric probability is the study of geometric figures, usually from the Euclidean space, which have been randomly generated. The variables coming from these random spatial models can be classical objects from Euclidean geometry, such as a point, a line, a subspace, a ball, a convex polytope and so on.

It is commonly accepted that geometric probability was born in 1733 with Buffon's original investigation of the falling needle. Subsequently, several open questions appeared including Sylvester's four-point problem in 1864, Bertrand's paradox related to a random chord in the circle in 1888 and Jeffreys's bicycle wheel problem in 1946. Until the beginning of the twentieth century, these questions were

<!-- p:14 -->


all considered as recreational mathematics and there was a very thin theoretical background involved which may explain why the several answers to Bertrand's question were regarded as a paradox.

After a course by G. Herglotz in 1933, W. Blaschke developed a new domain called integral geometry in his papers Integralgeometrie in 1935-1937, see e.g. [17]. It relies on the key idea that the mathematically natural probability models are those that are invariant under certain transformation groups and it provides mainly formulas for calculating expected values, i.e. integrals with respect to rotations or translations of random objects. Simultaneously, the modern theory of probability based on measure theory and Lebesgue's integral was introduced by S.N. Kolmogorov in [72].

During and after the Second World War, people with an interest in applications in experimental science-material physics, geology, telecommunications, etc.- realized the significance of random spatial models. For instance, in the famous foreword to the first edition of the reference book [31], D.G. Kendall narrates his own experience during the War and how his Superintendent asked him about the strength of a sheet of paper. This question was in fact equivalent to the study of a random set of lines in the plane. Similarly, J.L. Meijering published a first work on the study of crystal aggregates with random tessellations while he was working for the Philips company in 1953 [82]. In the same way, C. Palm who was working on telecommunications at Ericsson Technics proved a fundamental result in the onedimensional case about what is nowadays called the Palm measure associated with a stationary point process [96]. All of these examples illustrate the general need to rigorously define and study random spatial models.

We traditionally consider that the expression stochastic geometry dates back to 1969 and was due to D.G. Kendall and K. Krickeberg at the occasion of the first conference devoted to that topic in Oberwolfach. In fact, I. Molchanov and W.S. Kendall note in the preface of [95] that H.L. Frisch and J.M. Hammersley had already written the following lines in 1963 in a paper on percolation: Nearly all extant percolation theory deals with regular interconnecting structures, for lack of knowledge of how to define randomly irregular structures. Adventurous readers may care to rectify this deficiency by pioneering branches of mathematics that might be called stochastic geometry or statistical topology .

For more than 50 years, a theory of stochastic geometry has been built in conjunction with several domains, including

- the theory of point processes and queuing theory, see notably the work of Mecke [79], Stoyan [122], Neveu [93], Daley [34] and [41],
- convex and integral geometry, see e.g. the work of Schneider [111] and Weil [127] as well as their common reference book [113],
- the theory of random sets, mathematical morphology and image analysis, see the work of Kendall [67], Matheron [78] and Serra [115],
- combinatorial geometry, see the work of Ambartzumian [3].

It is worth noting that this development has been simultaneous with the research on spatial statistics and analysis of real spatial data coming from experimental science,


<!-- p:15 -->


1

for instance the work of B. Matérn in forestry [77] or the numerous papers in geostatistics, see e.g. [94].

In this introductory lecture, our aim is to describe some of the best-known historical problems in geometric probability and explain how solving these problems and their numerous extensions has induced a whole branch of the modern theory of stochastic geometry. We have chosen to embrace the collection of questions and results presented in this lecture under the general denomination of random geometry . In Sect. 1.2, Buffon's needle problem is used to introduce a few basic formulas from integral geometry. Section 1.3 contains a discussion around Bertrand's paradox which leads us to the construction of random lines and the first results on selected models of random tessellations. In Sect. 1.4, we present some partial answers to Sylvester's four-point problem and then derive from it the classical models of random polytopes. Finally, in Sect. 1.5, Jeffrey's bicycle wheel problem is solved and is the front door to more general random covering and continuum percolation.

We have made the choice to keep the discussion as non-technical as possible and to concentrate on the basic results and detailed proofs which do not require much prerequisite knowledge on the classical tools used in stochastic geometry. Each topic is illustrated by simulations which are done using Scilab 5.5 . This chapter is intended as a foretaste of some of the topics currently most active in stochastic geometry and naturally encourages the reader to go beyond it and carry on learning with reference to books such as [31, 95, 113].

Notation and Convention The Euclidean space R d of dimension d ≥ 1 and with origin denoted by o is endowed with the standard scalar product 〈· , ·〉 , the Euclidean norm ‖·‖ and the Lebesgue measure Vd . The set Br(x) is the Euclidean ball centered at x ∈ R d and of radius r &gt; 0. We denote by B d (resp. S d - 1 , S d - 1 + ) the unit ball (resp. the unit sphere, the unit upper half-sphere). The Lebesgue measure on S d - 1 will be denoted by σd . We will use the constant κd = Vd( B d ) = 1 d σd( S d - 1 ) = π d 2 Γ( d 2 + 1 ) . Finally, a convex compact set of R d (resp. a compact intersection of a finite number of closed half-spaces of R d ) will be called a d -dimensional convex body (resp. convex polytope ).

### 1.2 From Buffon's Needle to Integral Geometry

In this section, we describe and solve the four century-old needle problem due to Buffon and which is commonly considered as the very first problem in geometric probability. We then show how the solution to Buffon's original problem and to one of its extensions constitutes a premise to the modern theory of integral geometry. In particular, the notion of intrinsic volumes is introduced and two classical integral formulas involving them are discussed.


<!-- p:16 -->


Fig. 1.1 Simulation of Buffon's needle problem with the particular choice l/D = 1 / 2: over 1000 samples, 316 were successful (red), 684 were not (blue)

#### 1.2.1 Starting from Buffon's Needle

In 1733, Georges-Louis Leclerc, comte de Buffon, raised a question which is nowadays better known as Buffon's needle problem. The solution, published in 1777 [20], is certainly a good candidate for the first-ever use of an integral calculation in probability theory. First and foremost, its popularity since then comes from being the first random experiment which provides an approximation of π .

Buffon's needle problem can be described in modern words in the following way: a needle is dropped at random onto a parquet floor which is made of parallel strips of wood, each of same width. What is the probability that it falls across a vertical line between two strips (Fig. 1.1)?

Let us denote by D the width of each strip and by l the length of the needle. We assume for the time being that l ≤ D , i.e. that only one crossing is possible. The randomness of the experiment is described by a couple of real random variables, namely the distance R from the needle's mid-point to the closest vertical line and the angle Θ between a horizontal line and the needle.

The chosen probabilistic model corresponds to our intuition of a random drop: the variables R and Θ are assumed to be independent and both uniformly distributed on ( 0 , D/ 2 ) and ( - π/ 2 , π/ 2 ) respectively.

Now there is intersection if and only if 2 R ≤ l cos (Θ) . Consequently, we get

$$p = \frac { 2 } { \pi \, D } \int _ { - \frac { \pi } { 2 } } ^ { \frac { \pi } { 2 } } \int _ { 0 } ^ { \frac { 1 } { 2 } \ell \cos ( \theta ) } d r d \theta = \frac { 2 \ell } { \pi \, D } .$$


<!-- p:17 -->


1

This remarkable identity leads to a numerical method for calculating an approximate value of π . Indeed, repeating the experiment n times and denoting by Sn the number of hits, we can apply Kolmogorov's law of large numbers to show that 2 ln DSn converges almost surely to π with an error estimate provided by the classical central limit theorem.

In 1860, Joseph-Émile Barbier provided an alternative solution for Buffon's needle problem, see [6] and [71, Chapter 1]. We describe it below as it solves at the same time the so-called Buffon's noodle problem , i.e. the extension of Buffon's needle problem when the needle is replaced by any planar curve of class C 1 .

Let us denote by pk , k ≥ 0, the probability of exactly k crossings between the vertical lines and the needle. Henceforth, the condition l ≤ D is not assumed to be fulfilled any longer as it would imply trivially that p = p 1 and pk = 0 for every k ≥ 2. We denote by f(l) = ∑ k ≥ 1 kpk the mean number of crossings. The function f has the interesting property of being additive, i.e. if two needles of respective lengths l 1 and l 2 are pasted together at one of their endpoints and in the same direction, then the total number of crossing is obviously the sum of the numbers of crossings of the first needle and of the second one. This means that f(l 1 + l 2 ) = f(l 1 ) + f(l 2 ) . Since the function f is increasing, we deduce from its additivity that there exists a positive constant α such that f(l) = αl .

More remarkably, the additivity property still holds when the two needles are not in the same direction. This implies that for any finite polygonal line C , the mean number of crossings with the vertical lines of a rigid noodle with same shape as C , denoted by f( C ) with a slight abuse of notation, satisfies

$$f ( \mathcal { C } ) = \alpha \mathcal { L } ( \mathcal { C } )$$

where L ( · ) denotes the arc length. Using both the density of polygonal lines in the space of piecewise C 1 planar curves endowed with the topology of uniform convergence and the continuity of the functions f and L on this space, we deduce that the formula (1.1) holds for any piecewise C 1 planar curve.

It remains to make the constant α explicit, which we do when replacing C by the circle of diameter D . Indeed, almost surely, the number of crossings of this noodle with the vertical lines is 2, which shows that α = 2 πD . In particular, when K is a convex body of R 2 with diameter less than D and p(K) denotes the probability that K intersects one of the vertical lines, we get that

$$p ( K ) = \frac { 1 } { 2 } f ( \partial K ) = \frac { \mathcal { L } ( \partial K ) } { \pi \, D } .$$

Further extensions of Buffon's needle problem with more general needles and lattices can be found in [18]. In the next subsection, we are going to show how to derive the classical Cauchy-Crofton's formula from similar ideas.


<!-- p:18 -->


#### 1.2.2 Cauchy-Crofton formula

We do now the opposite of Buffon's experiment, that is we fix a noodle which has the shape of a convex body K of R 2 and let a random line fall onto the plane. We then count how many times in mean the line intersects K .

This new experiment requires to define what a random line is, which means introducing a measure on the set of all lines of R 2 . We do so by using the polar equation of such a line, i.e. for any ρ ∈ R and θ ∈ [ 0 , π) , we denote by Lρ,θ the line

$$L _ { \rho , \theta } = \rho ( \cos ( \theta ) , \sin ( \theta ) ) + \mathbb { R } ( - \sin ( \theta ) , \cos ( \theta ) ) .$$

Noticing that there is no natural way of constructing a probability measure on the set of random lines which would satisfy translation and rotation invariance, we endow the set R ×[ 0 , π) with its Lebesgue measure. The integrated number of crossings of a line with a C 1 planar curve C is then represented by the function

$$g ( \mathcal { C } ) = \int _ { - \infty } ^ { \infty } \int _ { 0 } ^ { \pi } \# ( L _ { \rho , \theta } \cap \mathcal { C } ) d \theta d \rho .$$

The function g is again additive under any concatenation of two curves so it is proportional to the arc length. A direct calculation when C is the unit circle then shows that

$$g ( \mathcal { C } ) = 2 \mathcal { L } ( \mathcal { C } ) .$$

This result is classically known in the literature as the Cauchy-Crofton formula [28, 33]. Going back to the initial question related to a convex body K , we apply (1.2) to C = ∂K and notice that # (Lρ,θ ∩ C ) is equal to 2 1 { Lρ,θ ∩ K ̸=∅} . We deduce that

$$\mathcal { L } ( \partial K ) = \int _ { - \infty } ^ { \infty } \int _ { 0 } ^ { \pi } 1 _ { \{ L _ { \rho , \theta } \cap K \neq \emptyset \} } \mathrm d \theta \rho .$$

#### 1.2.3 Extension to Higher Dimension

We aim now at extending (1.3) to higher dimension, that is we consider the set K d of convex bodies of R d , d ≥ 2, and for any element K of K d , we plan to calculate integrals over all possible k -dimensional affine subspaces Lk of the content of Lk ∩ K . This requires to introduce a set of fundamental functionals called intrinsic volumes on the space of convex bodies of R d . This is done through the rewriting of the volume of the parallel set (K + Bρ(o)) as a polynomial in ρ &gt; 0. Indeed, we are


<!-- p:19 -->


1

going to prove that there exists a unique set of d functions V 0 , · · · , Vd - 1 such that

$$V _ { d } ( K + B _ { \rho } ( o ) ) = \sum _ { k = 0 } ^ { d } \kappa _ { d - k } \rho ^ { d - k } V _ { k } ( K ) .$$

The identity (1.4) is known under the name of Steiner formula and was proved by Steiner for d = 2 and 3 in 1840 [120]. In particular, the renormalization with the multiplicative constant κd - k guarantees that the quantity Vk(K) is really intrinsic to K , i.e. that it does not depend on the dimension of the underlying space. We explain below how to prove (1.4), following closely [112, Section 1].

In the first step, we start by treating the case when K is a convex polytope P . We denote by F the set of all faces of P and by F k , 0 ≤ k ≤ d , the subset of F consisting of the k -dimensional faces of P . For any face F ∈ F \ { P } , the open outer normal cone of F denoted by NP(F) is the set of x ∈ R d \ { o } such that there exists an affine hyperplane H with normal vector x satisfying H ∩ P = F and 〈 x, y - h 〉 ≤ 0 for every y ∈ P and h ∈ H . In particular, when F ∈ F k , 0 ≤ k ≤ (d - 1 ) , NP(F) is a (d - k) -dimensional cone. Moreover, (F + NP(F)) is the set of points outside P whose nearest point in P lies in F and no other lowerdimensional face. The set of all sets (F + NP(F)) , often called the normal fan of P , is a partition of R d \ P , see Fig. 1.2. Consequently, from the decomposition of

Fig. 1.2 A two-dimensional convex polygon P (gray), the region (P + Br (o)) \ P (pink), the sets (F + NP(F)) with two examples for the edge F 1 and the vertex F 2 (striped regions)

<!-- p:20 -->


(P + Bρ(o)) \ P combined with Fubini's theorem, we get

$$V _ { d } ( P + B _ { \rho } ( o ) ) & = V _ { d } ( P ) + \sum _ { F \in \mathcal { V } ( P ) } V _ { d } ( F + ( N _ { P } ( F ) \cap B _ { \rho } ( o ) ) ) \\ & = V _ { d } ( P ) + \sum _ { k = 0 } ^ { d - 1 } \sum _ { F \in \mathcal { F } _ { k } } V _ { k } ( F ) \gamma ( F , P ) \rho ^ { d - k } \kappa _ { d - k } \\$$

where γ(F,P) is the normalized area measure on the unit sphere S d - k - 1 of NP(F) ∩ S d - k - 1 . In particular, we deduce from (1.5) that (1.4) holds for K = P as soon as

$$V _ { k } ( P ) = \sum _ { F \in \mathcal { F } _ { k } } V _ { k } ( F ) \gamma ( F , P ) .$$

In the second step, we derive the Steiner formula for any convex body K . In order to define Vk(K) , we use the trick to rewrite (1.4) for a polytope P and for several values of ρ , namely ρ = 1 , · · · , (d + 1 ) . The (d + 1 ) equalities constitute a Vandermonde system of (d + 1 ) equations in (κd V 0 (P), · · · , κ 0 Vd(P)) . These equations are linearly independent because the Vandermonde determinant of n pairwise distinct real numbers is different from zero. When solving the system by inverting the Vandermonde matrix, we construct a sequence αk,l , 0 ≤ k ≤ d , 1 ≤ l ≤ (d + 1 ) such that for every polytope P and 0 ≤ k ≤ d ,

$$V _ { k } ( P ) = \sum _ { l = 1 } ^ { d + 1 } \alpha _ { k , l } V _ { d } ( P + B _ { l } ( o ) ) .$$

It remains to check that the set of functions Vk( · ) = ∑ d + 1 l = 1 αk,l Vd ( · + Bl(o)) , 0 ≤ k ≤ d , defined on K d satisfies (1.4). This follows from the continuity of Vd , and hence of all Vk on the space K d endowed with the Hausdorff metric and from the fact that (1.4) holds on the set of convex polytopes which is dense in K d .

For practical reasons, we extend the definition of intrinsic volumes to K = ∅ by taking Vk( ∅ ) = 0 for every k ≥ 0. Of particular interest are:

- the functional V 0 equal to 1 { K ̸=∅} ,
- the functional Vd - 1 equal to half of the Hausdorff measure of ∂K .
- the functional V 1 equal to the so-called mean width up to the multiplicative constant dκd/( 2 κd - 1 ) ,

Furthermore, Hadwiger's theorem, which asserts that any additive, continuous and motion-invariant function on K d is a linear combination of the Vk 's, provides an alternative way of characterizing intrinsic volumes [49].


<!-- p:21 -->


1

Wenowgobackto our initial purpose, i.e. extending the Cauchy-Crofton formula to higher dimension. We do so in two different ways:

First, when K ∈ K 2 , an integration over ρ in (1.3) shows that

$$\mathcal { L } ( \partial K ) = 2 V _ { 1 } ( K ) = \int _ { 0 } ^ { \pi } V _ { 1 } ( K | L _ { 0 , \theta } ) d \theta$$

where (K | L 0 ,θ ) is the one-dimensional orthogonal projection of K onto L 0 ,θ . When K ∈ K d , d ≥ 2, Kubota's formula asserts that any intrinsic volume Vk can be recovered up to a multiplicative constant as the mean of the Lebesgue measure of the projection of K onto a uniformly distributed random k -dimensional linear subspace. In other words, there exists an explicit positive constant c depending on d and k but not on K such that for every K ∈ K d ,

$$V _ { k } ( K ) = c \int _ { \text {SO} _ { d } } V _ { k } ( K | \mathcal { R } ( L ) ) \text {d} \nu _ { d } ( \mathcal { R } ) \quad$$

where L is a fixed k -dimensional linear subspace of R d , SO d is the usual special orthogonal group of R d and νd is its associated normalized Haar measure.

Secondly, with a slight rewriting of (1.3), we get for any K ∈ K 2

$$\mathcal { L } ( \partial K ) = \iint _ { \mathbb { R } \times ( 0 , \pi ) } V _ { o } ( K \cap ( \text {rot} _ { \theta } ( L _ { 0 , 0 } ) + \rho ( \cos ( \theta ) , \sin ( \theta ) ) ) ) d \rho d \theta ,$$

where rot θ is the rotation around o and of angle θ . When K ∈ K d , d ≥ 2, for any 0 ≤ l ≤ k ≤ d and any fixed (d - k + l) -dimensional linear subspace Ld - k + l , the Crofton formula states that the k -th intrinsic volume of K is proportional to the mean of the l -th intrinsic volume of the intersection of K with a uniformly distributed random (d - k + l) -dimensional affine subspace, i.e. there exists an explicit positive constant c ′ depending on d , k and l but not on K such that

$$V _ { k } ( K ) = c ^ { \prime } \int _ { \text {SO} _ { d } } \int _ { L _ { d - k + l } ^ { \perp } } V _ { l } ( K \cap ( \mathcal { R } L _ { d - k + l } + t ) ) d t d v _ { d } ( \mathcal { R } ) ,$$

where Ld - k + l is a fixed (d - k + l) -dimensional affine subspace of R d .

For the proofs of (1.6) and (1.7) with the proper explicit constants and for a more extensive account on integral geometry and its links to stochastic geometry, we refer the reader to the reference books [110, Chapters 13-14], [109, Chapters 4-5] and [113, Chapters 5-6]. We will show in the next section how some of the formulas from integral geometry are essential to derive explicit probabilities related to the Poisson hyperplane tessellation.


<!-- p:22 -->


### 1.3 From Bertrand's Paradox to Random Tessellations

In this section, we recall Bertrand's problem which leads to three different and perfectly correct answers. This famous paradox questions the several potential models for constructing random lines in the Euclidean plane. The fundamental choice of the translation-invariance leads us to the definition of the stationary Poisson line process. After that, by extension, we survey a few basic facts on two examples of stationary random tessellations of R d , namely the Poisson hyperplane tessellation and the Poisson-Voronoi tessellation.

#### 1.3.1 Starting from Bertrand's Paradox

In the book entitled Calcul des Probabilités and published in 1889 [12], J. Bertrand asks for the following question: a chord of the unit circle is chosen at random. What is the probability that it is longer than √ 3, i.e. the edge of an equilateral triangle inscribed in the circle?

The paradox comes from the fact that there are several ways of choosing a chord at random . Depending on the model that is selected, the question has several possible answers. In particular, there are three correct calculations which show that the required probability is equal to either 1 / 2, or 1 / 3 or 1 / 4. Still a celebrated and well-known mathematical brain-teaser, Bertrand's problem questions the foundations of the modern probability theory when the considered variables are not discrete. We describe below the three different models and solutions (Fig. 1.3).

Solution 1 (Random Radius) We define a random chord through the polar coordinates (R, Θ) of the orthogonal projection of the origin onto it. The variable Θ is assumed to be uniformly distributed on ( 0 , 2 π) because of the rotation-invariance of the problem while R is taken independent of Θ and uniformly distributed in ( 0 , 1 ) . The length of the associated chord is 2 √ 1 - R 2 . Consequently, the required

Fig. 1.3 Simulation of Bertrand's problem with 100 chords: ( a ) Solution 1 (left): 54 successful (plain line, red), 46 unsuccessful (dotted line, blue). ( b ) Solution 2 (middle): 30 successful. ( c ) Solution 3 (right): 21 successful

<!-- p:23 -->


1

probability is

$$p _ { 1 } = P ( 2 \sqrt { 1 - R ^ { 2 } } \geq \sqrt { 3 } ) = P ( R \leq 1 / 2 ) = 1 / 2 .$$

Solution 2 (Random Endpoints) We define a random chord through the position Θ of its starting point in the anticlockwise direction and the circular length Θ ′ to its endpoint. Again, Θ is uniformly distributed on ( 0 , 2 π) while Θ ′ is chosen independent of Θ and also uniformly distributed in ( 0 , 2 π) . The length of the associated chord is 2 sin (Θ ′ / 2 ) . Consequently, the required probability is

$$p _ { 2 } = P ( 2 \sin ( \Theta ^ { \prime } / 2 ) \geq \sqrt { 3 } ) = P ( \Theta ^ { \prime } / 2 \in ( \pi / 3 , 2 \pi / 3 ) ) = \frac { \frac { 4 \pi } { 3 } - \frac { 2 \pi } { 3 } } { 2 \pi } = \frac { 1 } { 3 } .$$

Solution 3 (Random Midpoint) We define a random chord through its midpoint X . The random point X is assumed to be uniformly distributed in the unit disk. The length of the associated chord is 2 √ 1 -‖ X ‖ 2 . Consequently, the required probability is

$$p _ { 3 } = P ( \| X \| \leq 1 / 2 ) = \frac { V _ { 2 } ( B _ { o } ( 1 / 2 ) ) } { V _ { 2 } ( B _ { o } ( 1 ) ) } = \frac { 1 } { 4 } .$$

In conclusion, as soon as the model, i.e. the meaning that is given to the word random , is fixed, all three solutions look perfectly correct. J. Bertrand considers the problem as ill-posed, that is he does not decide in favor of any of the three. Neither does H. Poincaré in his treatment of Bertrand's paradox in his own Calcul des probabilités in 1912 [100]. Actually, they build on it a tentative formalized probability theory in a continuous space. Many years later, in his 1973 paper The well-posed problem [66], E.T. Jaynes explains that a natural way for discriminating between the three solutions consists in favoring the one which has the most invariance properties with respect to transformation groups. All three are rotation invariant but only one is translation invariant and that is Solution 1. And in fact, in a paper from 1868 [33], long before Bertrand's book, M.W. Crofton had already proposed a way to construct random lines which guarantees that the mean number of lines intersecting a fixed closed convex set is proportional to the arc length of its boundary.

Identifying the set of lines Lρ,θ with R × [ 0 , π) , we observe that the previous discussion means that the Lebesgue measure d ρ d θ on R × [ 0 , π) plays a special role when generating random lines. Actually, it is the only rotation and translation invariant measure up to a multiplicative constant. The construction of a natural random set of lines in R 2 will rely heavily on it.


<!-- p:24 -->


#### 1.3.2 Random Sets of Points, Random Sets of Lines and Extensions

Generating random geometric shapes in the plane requires to generate random sets of points and random sets of lines. Under the restriction to a fixed convex body K , the most natural way to generate random points consists in constructing a sequence of independent points which are uniformly distributed in K . Similarly, in view of the conclusion on Bertrand's paradox, random lines can be naturally taken as independent and identically distributed lines with common distribution

$$\frac { 1 } { \mu _ { 2 } ( K ) } 1 _ { \{ L _ { \rho , \theta } \cap K \neq \emptyset \} } \text {d} \rho d \theta$$

$$\mu _ { 2 } ( \cdot ) = \iint _ { \mathbb { R } \times ( 0 , \pi ) } 1 _ { \{ L _ { \rho , \theta } \cap \cdot \neq \emptyset \} } d \rho d \theta .$$

These constructions present two drawbacks: first, they are only defined inside K and not in the whole space and secondly, they lead to undesired dependencies. Indeed, when fixing the total number of points or lines thrown in K , the joint distribution of the numbers of points or lines falling into several disjoint Borel subsets of K is multinomial. Actually, there is a way of defining a more satisfying distribution on the space of locally finite sets of points (resp. lines) in the plane endowed with the σ -algebra generated by the set of functions which to any set of points (resp. lines) associates the number of points falling into a fixed Borel set of R 2 (resp. the number of lines intersecting a fixed Borel set of R 2 ). Indeed, for any fixed λ &gt; 0, there exists a random set of points (resp. lines) in the plane such that:

- for every Borel set B with finite Lebesgue measure, the number of points falling into B (resp. the number of lines intersecting B ) is Poisson distributed with mean λV 2 (B) (resp. λμ 2 (B) )
- for every finite collection of disjoint Borel sets B 1 , · · · , Bk , k ≥ 1, the numbers of points falling into Bi (resp. lines intersecting Bi ) are mutually independent.

This random set is unique in distribution and both translation and rotation invariant. It is called a homogeneous Poisson point process (resp. isotropic and stationary Poisson line process ) of intensity λ . For a detailed construction of both processes, we refer the reader to e.g. [113, Section 3.2].

The Poisson point process can be naturally extended to R d , d ≥ 3, by replacing V 2 with Vd . Similarly, we define the isotropic and stationary Poisson hyperplane process in R d by replacing μ 2 by a measure μd which is defined in the following way. For any ρ ∈ R and u ∈ S d - 1 + , we denote by Hρ, u the hyperplane containing the point ρ u and orthogonal to u . Let μd be the measure on R d such that for any

where


<!-- p:25 -->


1

Borel set B of R d ,

$$\mu _ { d } ( B ) = \iint _ { \mathbb { R } \times \mathbb { S } _ { + } ^ { d - 1 } } 1 _ { \{ H _ { \rho , u } \cap B \neq \emptyset \} } d \rho d \sigma _ { d } ( u ) .$$

Another possible extension of these models consists in replacing the Lebesgue measure Vd (resp. the measure μd ) by any locally finite measure which is not a multiple of Vd (resp. of μd ). This automatically removes the translation invariance in the case of the Poisson point process while the translation invariance is preserved in the case of the Poisson hyperplane process only if the new measure is of the form d ρ d νd( u ) where νd is a measure on S d - 1 + . For more information on this and also on non-Poisson point processes, we refer the reader to the reference books [31, 35, 70, 93]. In what follows, we only consider homogeneous Poisson point processes and isotropic and stationary Poisson hyperplane processes, denoted respectively by P λ and ̂ P λ . These processes will constitute the basis for constructing stationary random tessellations of the Euclidean space.

#### 1.3.3 On Two Examples of Random Convex Tessellations

The Poisson hyperplane process ̂ P λ induces naturally a tessellation of R d into convex polytopes called cells which are the closures of the connected components of the set R d \ ⋃ H ∈ ̂ P λ H . This tessellation is called the (isotropic and stationary) Poisson hyperplane tessellation of intensity λ . In dimension two, with probability one, any crossing between two lines is an X-crossing, i.e. any vertex of a cell belongs to exactly four different cells while in dimension d , any k -dimensional face of a cell, 0 ≤ k ≤ d , is included in the intersection of (d - k) different hyperplanes and belongs to exactly 2 d - k different cells almost surely.

Similarly, the Poisson point process P λ also generates a tessellation in the following way: any point x of P λ , called a nucleus , gives birth to its associated cell C(x | P λ) defined as the set of points of R d which are closer to x than to any other point of P λ for the Euclidean distance, i.e.

$$C ( x | \mathcal { P } _ { \lambda } ) = \{ y \in \mathbb { R } ^ { d } \colon \| y - x \| \leq \| y - x ^ { \prime } \| | \forall \, x ^ { \prime } \in \mathcal { P } _ { \lambda } \} .$$

This tessellation is called the Voronoi tessellation generated by P λ or the PoissonVoronoi tessellation in short. In particular, the cell C(x | P λ) with nucleus x is bounded by portions of bisecting hyperplanes of segments [ x, x ′ ] , x ′ ∈ P λ \ { x } . The set of vertices and edges of these cells constitute a graph which is random and embedded in R d , sometimes referred to as the Poisson-Voronoi skeleton . In dimension two, with probability one, any vertex of this graph belongs to exactly three different edges and three different cells while in dimension d , any k -dimensional face of a cell, 0 ≤ k ≤ d , is included in the intersection of


<!-- p:26 -->


Fig. 1.4 Simulation of the Poisson line tessellation (left) and the Poisson-Voronoi tessellation (right) in the square

(d + 1 - k)(d - k)/ 2 different bisecting hyperplanes and belongs to exactly (d + 1 - k) different cells almost surely (Fig. 1.4).

The Poisson hyperplane tessellation has been used as a natural model for the trajectories of particles inside bubble chambers [45], the fibrous structure of paper [83] and the road map of a city [54]. The Voronoi construction was introduced in the first place by R. Descartes as a possible model for the shape of the galaxies in the Universe [36]. The Poisson-Voronoi tessellation has appeared since then in numerous applied domains, including telecommunication networks [5] and materials science [74, 102].

In both cases, stationarity of the underlying Poisson process makes it possible to do a statistical study of the tessellation. Indeed, let f be a translation-invariant, measurable and non-negative real-valued function defined on the set P d of convex polytopes of R d endowed with the topology of the Hausdorff distance. For r &gt; 0, let C r and Nr be respectively the set of cells included in Br(o) and its cardinality. Then, following for instance [32], we can apply Wiener's ergodic theorem to get that, when r →∞ ,

$$\frac { 1 } { N _ { r } } \sum _ { C \in \mathbf C _ { r } } f ( C ) \rightarrow \frac { 1 } { E ( V _ { d } ( C _ { o } ) ^ { - 1 } ) } E \left ( \frac { f ( C _ { o } ) } { V _ { d } ( C _ { o } ) } \right ) \quad \text {almost surely}$$

where Co is the almost-sure unique cell containing the origin o in its interior.

This implies that two different cells are of particular interest: the cell Co , often called the zero-cell , and the cell C defined in distribution by the identity

$$E ( f ( \mathcal { C } ) ) = \frac { 1 } { E ( V _ { d } ( C _ { o } ) ^ { - 1 } ) } E \left ( \frac { f ( C _ { o } ) } { V _ { d } ( C _ { o } ) } \right ) .$$


<!-- p:27 -->


The convergence at (1.9) suggests that C has the law of a cell chosen uniformly at random in the whole tessellation, though such a procedure would not have any clear mathematical meaning. That is why C is called the typical cell of the tessellation even if it is not defined almost surely and it does not belong to the tessellation either. In particular, the typical cell is not equal in distribution to the zero-cell and is actually stochastically smaller since it has a density proportional to Vd(Co) - 1 with respect to the distribution of Co . Actually, it is possible in the case of the Poisson hyperplane tessellation to construct a realization of C which is almost surely strictly included in Co [80]. This fact can be reinterpreted as a multidimensional version of the classical bus waiting time paradox , which says the following: if an individual arrives at time t at a bus stop, the time between the last bus he/she missed and the bus he/she will take is larger than the typical interarrival time between two consecutive busses.

Relying on either (1.9) or (1.10) may not be easy when calculating explicit mean values or distributions of geometric characteristics of C . Another equivalent way of defining the distribution of C is provided by the use of a so-called Palm distribution, see e.g. [96], [90, Section 3.2], [113, Sections 3.3,3.4] and [73, Section 9]. For sake of simplicity, we explain the procedure in the case of the Poisson-Voronoi tessellation only. Let f be a measurable and non-negative real-valued function defined on P d . Then, for any Borel set B such that 0 &lt; Vd(B) &lt; ∞ , we get

$$E ( f ( \mathcal { C } ) ) = \frac { 1 } { \lambda V _ { d } ( B ) } E \left ( \sum _ { x \in \mathcal { P } _ { \lambda } \cap B } f ( C ( x | \mathcal { P } _ { \lambda } ) - x ) \right ) .$$

where C(x | P λ) - x is the set C(x | P λ) translated by - x . The fact that the quantity on the right-hand side of the identity (1.11) does not depend on the Borel set B comes from the translation invariance of the Poisson point process P λ . It is also remarkable that the right-hand side of (1.11) is again a mean over the cells with nucleus in B but contrary to (1.9) there is no limit involved, which means in particular that B can be as small as one likes, provided that Vd(B) &gt; 0.

Following for instance [90, Proposition 3.3.2], we describe below the proof of (1.11), i.e. that for any translation-invariant, measurable and non-negative function f , the Palm distribution defined at (1.11) is the same as the limit of the means in the law of large numbers at (1.9). Indeed, let us assume that C be defined in law by the identity (1.11) and let us prove that (1.10) is satisfied, i.e. that C has a density proportional to Vd( · ) - 1 with respect to Co . By classical arguments from measure theory, (1.11) implies that for any non-negative measurable function F defined on the product space P d × R d ,

$$\lambda \int E ( F ( \mathcal { C } , x ) ) d x = E \left ( \sum _ { x \in \mathcal { P } _ { \lambda } } F ( C ( x | \mathcal { P } _ { \lambda } ) - x , x ) \right ) .$$


<!-- p:28 -->


Applying this to F(C,x) = f (C) Vd(C) 1 {- x ∈ C } and using the translation invariance of f , we get

$$\lambda E ( f ( \mathcal { C } ) ) = E \left ( \sum _ { x \in \mathcal { P } _ { \lambda } } \frac { f ( C ( x | \mathcal { P } _ { \lambda } ) ) } { V _ { d } ( C ( x | \mathcal { P } _ { \lambda } ) ) } 1 _ { o \in \mathcal { C } ( x | \mathcal { P } _ { \lambda } ) } \right ) = E \left ( \frac { f ( C _ { o } ) } { V _ { d } ( C _ { o } ) } \right ) .$$

Applying (1.12) to f = 1 and f = Vd successively, we get

$$E ( V _ { d } ( \mathcal { C } ) ) = \frac { 1 } { E ( V _ { d } ( C _ { o } ) ^ { - 1 } ) } = \frac { 1 } { \lambda } .$$

Combining (1.12) and (1.13), we obtain that the typical cell C defined at (1.11) satisfies (1.10) so it is equal in distribution to the typical cell defined earlier through the law of large numbers at (1.9).

In addition to these two characterizations of the typical cell, the Palm definition (1.11) of C in the case of the Poisson-Voronoi tessellation provides a very simple realization of the typical cell C : it is equal in distribution to the cell C(o | P λ ∪ { o } ) , i.e. the V oronoi cell associated with the nucleus o when the origin is added to the set of nuclei of the tessellation. This result is often called Slivnyak's theorem, see e.g. [113, Theorem 3.3.5].

The classical problems related to stationary tessellations are mainly the following:

- (a) making a global study of the tessellation, for instance on the set of vertices or edges: calculation of mean global topological characteristics per unit volume, proof of limit theorems, etc;
- (b) calculating mean values and whenever possible, moments and distributions of geometric characteristics of the zero-cell or the typical cell or a typical face;
- (c) studying rare events, i.e. estimating distribution tails of the characteristics of the zero-cell or the typical cell and proving the existence of limit shapes in some asymptotic context.

Problem (a) As mentioned earlier, Cowan [32] showed several laws of large numbers by ergodic methods which were followed by second-order results from the seminal work due to F. Avram and Bertsimas on central limit theorems [4] to the more recent additions [53] and [55]. Topological relationships have been recently established in [128] for a general class of stationary tessellations.

Problem (b) The question of determining mean values of the volume or any combinatorial quantity of a particular cell was tackled early. The main contributions are due notably to Matheron [78, Chapter 6] and Miles [85, 86] in the case of the Poisson hyperplane tessellation and to Møller [88] in the case of the PoissonVoronoi tessellation. Still, to the best of our knowledge, some mean values are unknown like for instance the mean number of k -dimensional faces of the PoissonVoronoi typical cell for 1 ≤ k ≤ (d - 1 ) and d ≥ 3. Regarding explicit distributions,


<!-- p:29 -->


1

several works are noticeable [11, 22, 23] but in the end, it seems that very few have been computable up to now.

Problem (c) The most significant works related to this topic have been rather recent: distribution tails and large-deviations type results [43, 56], extreme values [29], high dimension [57] . . . Nevertheless, many questions, for instance regarding precise estimates of distribution tails, remain open to this day. One of the most celebrated questions concerns the shape of large cells. A famous conjecture stated by D.G. Kendall in the forties asserts that large cells from a stationary and isotropic Poisson line tessellation are close to the circular shape, see e.g. the foreword to [31]. This remarkable feature is in fact common to the Crofton cell and the typical cell of both the Poisson hyperplane tessellation and the Poisson-Voronoi tessellation in any dimension. It was formalized for different meanings of large cells and proved, with an explicit probability estimate of the deviation to the limit shape, by D. Hug, M. Reitzner and R. Schneider in a series of breakthrough papers, see e.g. [58, 61, 62].

Intentionally, we have chosen to skip numerous other models of tessellations. Noteworthy among these are those generated by non-Poisson point processes [44], Johnson-Mehl tessellations [89] and especially STIT tessellations [92].

In the next subsection, we collect a few explicit first results related to Problem (b), i.e. the mean value and distribution of several geometric characteristics of either the zero-cell Co or the typical cell C .

#### 1.3.4 Mean Values and Distributional Properties of the Zero-Cell and of the Typical Cell

This subsection is not designed as an exhaustive account on the many existing results related to zero and typical cells from random tessellations. Instead, we focus here on the basic first calculations which do not require much knowledge on Poisson point processes. For more information and details, we refer the reader to the reference books [90], [113, Section 10.4] and to the survey [23].

##### 1.3.4.1 The Zero-Cell of a Poisson Hyperplane Tessellation

We start with the calculation of the probability for a certain convex body K to be included in Co the zero-cell or the typical cell. In the case of the planar Poisson line tessellation, let K be a convex body containing the origin-if not, K can be replaced by the convex hull of K ∪ { o } . Since the number of lines from the Poisson line process intersecting K is a Poisson variable with mean λμ 2 (K) , we get

$$P ( K \subset C _ { o } ) & = P ( \{ L _ { \rho , \theta } \cap K = \emptyset \ \forall \ L _ { \rho , \theta } \in \mathcal { P } _ { \lambda } ) \\ & = \exp ( - \mu _ { 2 } ( K ) ) \\ & = \exp ( - \mathcal { L } ( \partial K ) ) ,$$


<!-- p:30 -->


where the last equality comes from the Cauchy-Crofton formula (1.3) and is obviously reminiscent of Buffon's needle problem. For d ≥ 3, we get similarly, thanks to (1.7) applied to k = 1 and l = 0,

$$P ( K \subset C _ { o } ) = \exp ( - \mu _ { d } ( K ) ) = \exp ( - \kappa _ { d - 1 } V _ { 1 } ( K ) ) .$$

The use of Crofton formula for deriving the probability P(K ⊂ Co) may explain why the zero-cell of the isotropic and stationary Poisson hyperplane tessellation is often referred to as the Crofton cell .

Applying (1.14) to K = Br(o) , r &gt; 0, and using the equality V 1 ( B d ) = dκd κd - 1 , we obtain that the radius of the largest ball centered at o and included in Co is exponentially distributed with mean (dκd) - 1 .

##### 1.3.4.2 The Typical Cell of a Poisson Hyperplane Tessellation

Let us denote by f 0 ( · ) the number of vertices of a convex polytope. In the planar case, some general considerations show without much calculation that E(f 0 ( C )) is equal to 4. Indeed, we have already noted that with probability one, any vertex of a cell belongs to exactly 4 cells and is the highest point of a unique cell. Consequently, there are as many cells as vertices. In particular, the mean 1 Nr ∑ C ∈ C r f 0 (C) is equal, up to boundary effects going to zero when r → ∞ , to 4 times the ratio of the total number of vertices in Br(o) over the total number of cells included in Br(o) , i.e. converges to 4. Other calculations of means and further moments of geometric characteristics can be found notably in [78, Chapter 6] and in [83-85].

One of the very few explicit distributions is the law of the inradius of C , i.e. the radius of the largest ball included in C . Remarkably, this radius is equal in distribution to the radius of the largest ball centered at o and included in Co , i.e. is exponentially distributed with mean (dκd) - 1 . This result is due to R.E. Miles in dimension two and is part of an explicit construction of the typical cell C based on its inball [86], which has been extended to higher dimension since then, see e.g. [24].

##### 1.3.4.3 The Typical Cell of a Poisson-Voronoi Tessellation

In this subsection, we use the realization of the typical cell C of a Poisson-Voronoi tessellation as the cell C(o | P λ ∪ { o } ) , as explained at the end of Sect. 1.3.3. We follow the same strategy as for the zero-cell of a Poisson hyperplane tessellation, i.e. calculating the probability for a convex body K to be contained in C and deducing from it the distribution of the inradius of C .


<!-- p:31 -->


1

Fig. 1.5 Voronoi Flower (red) of the convex body K (black) with respect to o

Let K be a convex body containing the origin. The set K is contained in C(o | P λ ∪ { o } ) if and only if o is the nearest nucleus to any point in K , which means that for every x ∈ K , the ball B ‖ x ‖ (x) does not intersect P λ . Let us consider the set

$$\mathcal { F } _ { o } ( K ) = \bigcup _ { x \in K } B _ { \| x \| } ( x )$$

that we call the Voronoi flower of K with respect to o , see Fig. 1.5.

Using the fact that the number of points of P λ in F o(K) is Poisson distributed with mean λVd( F o(K)) , we get

$$P ( K \subset C ( o | \mathcal { P } _ { \lambda } \cup \{ o \} ) ) = \exp ( - \lambda V _ { d } ( \mathcal { F } _ { o } ( K ) ) ) .$$

Applying this to K = Bo(r) , r &gt; 0, we deduce that the radius of the largest ball centered at o and included in C(o | P λ ∪ { o } ) is Weibull distributed with tail probability equal to exp ( - λ 2 d κdr d ) , r &gt; 0.

In the next section, we describe a different way of generating random polytopes: they are indeed constructed as convex hulls of random sets of points.

Similarly to the case of the typical cell of a Poisson line tessellation, some direct arguments lead us to the calculation of E(f 0 ( C )) in dimension two: any vertex of a cell belongs to exactly 3 cells and with probability one, is the either highest or lowest point of a unique cell. Consequently, there are as twice as many vertices as cells. In particular, the mean 1 Nr ∑ C ∈ C r f 0 (C) is equal, up to boundary effects going to zero when r →∞ , to 3 times the ratio of the total number of vertices in Br(o) over the total number of cells included in Br(o) , i.e. equal to 6. This means that E(f 0 ( C )) = 6.


<!-- p:32 -->


### 1.4 From Sylvester's Four-Point Problem to Random Polytopes

This section is centered around Sylvester's four-point problem, another historical problem of geometric probability which seemingly falls under the denomination of recreational mathematics but in fact lays the foundations of an active domain of today's stochastic geometry, namely the theory of random polytopes. We aim at describing first Sylvester's original question and some partial answers to it. We then survey the topic of random polytopes which has been largely investigated since the sixties, partly due to the simultaneous development of computational geometry.

#### 1.4.1 Starting from Sylvester's Four-Point Problem

In 1864, J.J. Sylvester published in The Educational Times [123] a problem which is nowadays known under the name of Sylvester's four-point problem and can be rephrased in the following way: given a convex body K in the plane, what is the probability that 4 random points inside K are the vertices of a convex quadrilateral (Fig. 1.6)?

Let us denote by p 4 (K) the probability that 4 random points which are independent and uniformly distributed in K are the vertices of a convex quadrilateral. If not, one of the 4 points is included in the triangle whose vertices are the 3 other points. Denoting by A(K) the mean area of a random triangle whose vertices are 3 i.i.d. uniform points in K , we get the identity

$$p _ { 4 } ( K ) = 1 - 4 \frac { \overline { A } ( K ) } { V _ { 2 } ( K ) } .$$

Fig. 1.6 Simulation of Sylvester's four-point problem in the triangle: the convex hull of the 4 uniform points (red) is either a convex quadrilateral (left) or a triangle (right)

<!-- p:33 -->


1

Solving Sylvester's problem is then equivalent to calculating the mean value A(K) . In particular, the quantity A(K) V 2 (K) is scaling invariant and also invariant under any area-preserving affine transformation.

##### 1.4.1.1 Calculation of Sylvester's Probability in the Case of the Disk

In this subsection, we provide an explicit calculation of p 4 ( D ) where D is the unit disk. As in the next subsection, we follow closely the method contained in [68, pages 42-46].

Step 1 We can assume that one of the points is on the boundary of the disk. Indeed, isolating the farthest point from the origin, we get

$$V _ { 2 } ( \mathbb { D } ) ^ { 3 } \overline { A } ( \mathbb { D } ) = 3 \int _ { \mathbb { D } } \left [ \iint _ { \mathbb { D } ^ { 2 } } 1 _ { \{ | x _ { 1 } | , | x _ { 2 } | \in ( 0 , | x _ { 3 } | ) \} } V _ { 2 } ( \text {Conv} ( \{ x _ { 1 } , x _ { 2 } , x _ { 3 } \} ) ) d z _ { 1 } d z _ { 2 } \right ] d z _ { 3 } .$$

Now for a fixed z 3 ∈ D \ { o } , we apply the change of variables z ′ i = zi ‖ z 3 ‖ , i = 1 , 2, in the double integral and we deduce that

$$\overline { A } ( \mathbb { D } ) = \frac { 3 } { \pi ^ { 3 } } \int _ { \mathbb { D } } \| z _ { 3 } \| ^ { 6 } \left [ \iint _ { \mathbb { D } ^ { 2 } } V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } ^ { \prime } , z _ { 2 } ^ { \prime } , \frac { z _ { 3 } } { \| z _ { 3 } \| } \} ) ) d z _ { 1 } d z _ { 2 } ^ { \prime } \right ] d z _ { 3 } .$$

Since the double integral above does not depend on z 3, we get

$$\overline { A } ( \mathbb { D } ) = \frac { 3 } { 4 \pi ^ { 2 } } I$$

$$I = \iint _ { \mathbb { D } ^ { 2 } } V _ { 2 } ( C o n v ( \{ z _ { 0 } , z _ { 1 } , z _ { 2 } \} ) ) d z _ { 1 } d z _ { 2 } ,$$

z 0 being a fixed point on the boundary of D .

Step 2 Let us now calculate I , i.e. π 2 times the mean area of a random triangle with one deterministic vertex on the unit circle and two random vertices independent and uniformly distributed in D .

For sake of simplicity, we replace the unit disk D by its translate D + ( 0 , 1 ) and the fixed point on the boundary of D + ( 0 , 1 ) is chosen to be equal to o . This does not modify the integral I . The polar coordinates (ρi , θi ) of zi , i = 1 , 2, satisfy ρi ∈ ( 0 , 2 sin (θi )) and

$$V _ { 2 } ( \text {Conv} ( \{ o , z _ { 1 } , z _ { 2 } \} ) ) = \frac { 1 } { 2 } \rho _ { 1 } \rho _ { 2 } | \sin ( \theta _ { 2 } - \theta _ { 1 } ) | .$$

where Consequently, we obtain


<!-- p:34 -->


$$C o n s e q u d e n t y , w e o b a n l \\ I = \iint _ { 0 < \theta _ { 1 } < \theta _ { 2 } < \pi } \left [ \int _ { 0 } ^ { 2 \sin ( \theta _ { 1 } ) } \rho _ { 1 } ^ { 2 } d \rho _ { 1 } \int _ { 0 } ^ { 2 \sin ( \theta _ { 2 } ) } \rho _ { 2 } ^ { 2 } d \rho _ { 2 } \right ] \sin ( \theta _ { 2 } - \theta _ { 1 } ) d \theta _ { 1 } d \theta _ { 2 } \\ = \frac { 6 4 } { 9 } \iint _ { 0 < \theta _ { 1 } < \theta _ { 2 } < \pi } \sin ^ { 3 } ( \theta _ { 1 } ) \sin ^ { 3 } ( \theta _ { 2 } ) \sin ( \theta _ { 2 } - \theta _ { 1 } ) d \theta _ { 1 } d \theta _ { 2 } \\ = \frac { 3 5 \pi } { 3 6 } . \\$$

Conclusion Combining this result with (1.17) and (1.15), we get

$$p _ { 4 } ( \mathbb { D } ) = 1 - \frac { 3 5 } { 1 2 \pi ^ { 2 } } \approx 0 . 7 0 4 4 8 \dots$$

##### 1.4.1.2 Calculation of Sylvester's Probability in the Case of the Triangle

In this subsection, we calculate the probability p 4 ( T ) where the triangle T is the convex hull of the three points o , ( 1 , 1 ) and ( 1 , - 1 ) . We recall that the calculation of p 4 (K) is invariant under any area-preserving affine transformation.

Step 1 We can assume that one of the points is on the edge facing o . Indeed, denoting by (xi , yi ) the Cartesian coordinates of zi , i = 1 , 2 , 3, we get

$$V _ { 2 } ( \mathbb { T } ) ^ { 3 } \overline { A } ( \mathbb { T } ) = 3 \int _ { \mathbb { T } } \left [ \iint _ { \mathbb { T } ^ { 2 } } \mathbf 1 _ { \{ x _ { 1 } , x _ { 2 } \in ( 0 , x _ { 3 } ) \} } V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } , z _ { 2 } , z _ { 3 } \} ) ) d z _ { 1 } d z _ { 2 } \right ] d z _ { 3 } .$$

Now for a fixed z 3 ∈ T \ { o } , we apply the change of variables z ′ i = zi x 3 , i = 1 , 2, in the double integral. We get

$$\overline { A } ( \mathbb { T } ) & = 3 \int _ { x _ { 3 } = 0 } ^ { 1 } \int _ { y _ { 3 } = - x _ { 3 } } ^ { x _ { 3 } } \left [ \iint _ { \mathbb { T } ^ { 2 } } x _ { 3 } ^ { 6 } V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } ^ { \prime } , z _ { 2 } ^ { \prime } , \frac { z _ { 3 } } { x _ { 3 } } \} ) ) d z _ { 1 } ^ { \prime } d z _ { 2 } ^ { \prime } \right ] d z _ { 3 } \\ & = 6 \int _ { x _ { 3 } = 0 } ^ { 1 } \int _ { y _ { 3 } = 0 } ^ { x _ { 3 } } x _ { 3 } ^ { 6 } \left [ \iint _ { \mathbb { T } ^ { 2 } } V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } ^ { \prime } , z _ { 2 } ^ { \prime } , \frac { x _ { 3 } } { x _ { 3 } } \} ) ) d z _ { 1 } ^ { \prime } d z _ { 2 } ^ { \prime } \right ] d z _ { 3 } . \\ \text {Finally, for fixed } x _ { 3 } , \, we \, \text {apply the change of variables } h \, = \, \frac { y _ { 3 } } { 2 } , \, \text {Since the double}$$

Finally, for fixed x 3, we apply the change of variables h = y 3 x 3 . Since the double integral in square brackets above does not depend on x 3, we get

$$\overline { A } ( \mathbb { T } ) & = 6 \int _ { 0 } ^ { 1 } x _ { 3 } ^ { 7 } d x _ { 3 } \int _ { h = 0 } ^ { 1 } \left [ \iint _ { \mathbb { T } ^ { 2 } } v _ { 2 } ( C o n v ( \{ z _ { 1 } , z _ { 2 } , ( 1 , h ) \} ) ) d z _ { 1 } d z _ { 2 } \right ] d h \\ & = \frac { 3 } { 4 } \int _ { h = 0 } ^ { 1 } I ^ { \prime } ( h ) d h \\ \intertext { w h e r e } \text {where } I ^ { \prime } ( h ) & = \int _ { \{ \mathbb { T } _ { 2 } V _ { 2 } ( C o n v ( \{ z _ { 1 } , z _ { 2 } , ( 1 , h ) \} ) ) d z _ { 1 } d z _ { 2 } } .$$

where I ′ (h) = ∫∫ T 2 V 2 ( Conv ( { z 1 , z 2 , ( 1 , h) } )) d z 1d z 2.


<!-- p:35 -->


1

Step 2 Let us now calculate I ′ (h) , 0 &lt; h &lt; 1, i.e. the mean area of a random triangle with one deterministic vertex at ( 1 , h) on the vertical edge and two random vertices independent and uniformly distributed in T . The point ( 1 , h) divides T into two subtriangles, the upper triangle T + (h) = Conv ( { o, ( 1 , h), ( 1 , 1 ) } ) and the lower triangle T - (h) = Conv ( { o, ( 1 , h), ( 1 , - 1 ) } ) . Let us rewrite I ′ (h) as

$$I ^ { \prime } ( h ) = 2 I _ { + , - } ^ { \prime } ( h ) + V _ { 2 } ( T _ { + } ( h ) ) ^ { 2 } \widehat { A } ( T _ { + } ( h ) ) + V _ { 2 } ( T _ { - } ( h ) ) ^ { 2 } \widehat { A } ( T _ { - } ( h ) ) \\ \text {where}$$

where

$$I _ { + , - } ^ { \prime } ( h ) = \int _ { z _ { 1 } \in T _ { + } ( h ) , z _ { 2 } \in T _ { - } ( h ) } V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } , z _ { 2 } , ( 1 , h ) \} ) ) ) d z _ { 1 } d z _ { 2 } \quad$$

and ̂ A(T ) , for a triangle T , is the mean area of a random triangle which shares a common vertex with T and has two independent vertices uniformly distributed in T .

We start by making explicit the quantity ̂ A(T ) for any triangle T . It is invariant under any area-preserving affine transformation and is multiplied by λ 2 when T is rescaled by λ - 1 . Consequently, it is proportional to V 2 (T ) , i.e.

$$\widehat { A } ( T ) = \widehat { A } ( \mathbb { T } ) V _ { 2 } ( T ) .$$

̂


$$\widehat { A } ( \mathbb { T } ) = \int _ { \mathbb { T } ^ { 2 } } V _ { 2 } ( \text {Conv} ( \{ o , z _ { 1 } , z _ { 2 } \} ) ) d z _ { 1 } d z _ { 2 } . \\$$

The polar coordinates (ρi , θi ) of xi , i = 1 , 2, satisfy ρi ∈ ( 0 , cos - 1 (θi )) and equality (1.18). Consequently, we obtain

$$\text {equality} \left ( 1 . 1 8 \colon \text {Comedy uniformly, we obtain} \right ) \\ \widehat { A } ( \mathbb { T } ) & = \int _ { - \frac { \pi } { 4 } } ^ { \frac { \pi } { 4 } } \int _ { 0 } ^ { \frac { \pi } { 4 } } \left [ \int _ { 0 } ^ { \cos ^ { - 1 } ( \theta _ { 1 } ) } \rho _ { 1 } ^ { 2 } d \rho _ { 1 } \int _ { 0 } ^ { \cos ^ { - 1 } ( \theta _ { 2 } ) } \rho _ { 2 } ^ { 2 } d \rho _ { 2 } \right ] \sin ( \theta _ { 2 } - \theta _ { 1 } ) d \theta _ { 1 } d \theta _ { 2 } \\ & = \frac { 1 } { 9 } \iint _ { - \frac { \pi } { 4 } < \theta _ { 1 } < \theta _ { 2 } < \frac { \pi } { 4 } } \frac { \sin ( \theta _ { 2 } - \theta _ { 1 } ) } { \cos ^ { 3 } ( \theta _ { 1 } ) \cos ^ { 3 } ( \theta _ { 2 } ) } d \theta _ { 1 } d \theta _ { 2 } \\ & = \frac { 4 } { 2 7 } \cdot \\ \text {Combining} \left ( 1 . 2 2 \right ) \text { and } \left ( 1 . 2 3 \right ) \text {, we obtain in particular that}$$

Combining (1.22) and (1.23), we obtain in particular that

$$\widehat { A } ( T _ { + } ( h ) ) = \frac { 2 ( 1 - h ) } { 2 7 } , \text { and } \widehat { A } ( T _ { - } ( h ) ) = \frac { 2 ( 1 + h ) } { 2 7 } .$$

We now calculate We turn now our attention to the quantity I ′ + , - (h) defined at (1.21). Using the rewriting of the area of a triangle as half of the non-negative determinant of two vectors and introducing g + (h) (resp. g - (h) ) as the center of mass of T + (h) (resp. T - (h) ), we obtain


<!-- p:36 -->


$$( \text {resp. } T _ { - } ( h ) , \text { we obtain} \\ I _ { + , - } ^ { \prime } ( h ) & = \frac { 1 } { 2 } \int _ { z _ { 1 } \in T _ { + } ( h ) , z _ { 2 } \in T _ { - } ( h ) } \det ( z _ { 1 } - ( 1 , h ) , z _ { 2 } - ( 1 , h ) ) d z _ { 1 } d z _ { 2 } \\ & = \frac { 1 } { 2 } \int _ { z _ { 1 } \in T _ { + } ( h ) } \det \left ( ( z _ { 1 } - ( 1 , h ) ) , \int _ { z _ { 2 } \in T _ { - } ( h ) } ( z _ { 2 } - ( 1 , h ) ) \right ) d z _ { 1 } \\ & = \frac { V _ { 2 } ( T _ { - } ( h ) ) } { 2 } \det \left ( \int _ { z _ { 1 } \in T _ { + } ( h ) } ( z _ { 1 } - ( 1 , h ) ) d z _ { 1 } , ( g _ { - } ( h ) - ( 1 , h ) ) \right ) \\ & = V _ { 2 } ( T _ { - } ( h ) ) V _ { 2 } ( T _ { + } ( h ) ) V _ { 2 } ( \text {Conv} ( \{ g _ { + } ( h ) , g _ { - } ( h ) , ( 1 , h ) \} ) ) \\ & = \frac { ( 1 - h ) ( 1 + h ) } { 4 } \frac { V _ { 2 } ( \mathbb { T } ) } { 9 } = \frac { 1 - h ^ { 2 } } { 3 6 } . \\ \text {Inserting } ( 1 . 2 ) \text { and } ( 1 . 2 ) \text { ), we get}$$

Inserting (1.24) and (1.25) into (1.20), we get

$$I ^ { \prime } ( h ) = \frac { 1 - h ^ { 2 } } { 1 8 } + \frac { ( 1 - h ) ^ { 3 } } { 5 4 } + \frac { ( 1 + h ) ^ { 3 } } { 5 4 } = \frac { 5 + 3 h ^ { 2 } } { 5 4 } .$$

Conclusion Combining (1.26) with (1.19) and (1.15), we get A( T ) = 1 12 and

$$p _ { 4 } ( T ) = \frac { 2 } { 3 } = 0 . 6 6 6 6 6 \dots$$

##### 1.4.1.3 Extremes of p 4 (K)

In 1917, W. Blaschke proved a monotonicity result for Sylvester's four-point problem, namely that the probability p 4 (K) is maximal when K is a disk and minimal when K is a triangle, see [15] and [16, §24, §25]. Because of (1.15), this amounts to saying that the mean area of a random triangle in a unit area convex body K is minimal when K is a disk and maximal when K is a triangle.

This assertion is due to the use of symmetrization techniques which have become classical since then in convex and integral geometry. We describe below the main arguments developed by W. Blaschke and also rephrased in a nice way in the historical note [99].

Let K be a unit area convex body of R 2 and let us denote by x min and x max the minimal and maximal projection on the x -axis of a point of K . The boundary of K is parametrized by two functions f + , f - : [ x min , x max ] -→ R such that f + ≥ f - with equality at x min and x max . We use the term Steiner symmetrization of K with


<!-- p:37 -->


1

Fig. 1.7 Two

symmetrizations (red) of a convex body delimited by translates of the curves

f + (x) = √ x and f - (x) = x(x - 2 + √ 2 2 ) on the interval [ 0 , 2 ] (black) and the image of a triangle by symmetrization (blue): the Steiner symmetrization (left) and the shaking (right)

respect to the x -axis for the transformation

$$\mathcal { S } \colon \left \{ \begin{matrix} K & \longrightarrow \mathbb { R } ^ { 2 } \\ ( x , y ) \longmapsto \left ( x , y - \frac { f _ { + } ( x ) + f _ { - } ( x ) } { 2 } \right ) \end{matrix}$$

In other words, S sends any segment which is the intersection of K with a vertical line to its unique vertical translate which is symmetric with respect to the x -axis; see Fig. 1.7. In particular, S is area-preserving and the image of K is a convex body which is symmetric with respect to the x -axis, see e.g. [109, Section 10.3]. Let us show that

$$\overline { A } ( K ) \geq \overline { A } ( \mathcal { S } ( K ) )$$

Let zi = (xi , yi ) , i = 1 , 2 , 3, be three points of K . In particular, we start by noticing that the area of the parallelogram spanned by the two vectors (z 2 - z 1 ) and (z 3 - z 1 ) is twice the area of the triangle Conv ( { z 1 , z 2 , z 3 } ) . Consequently, we get

$$V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } , z _ { 2 } , z _ { 3 } \} ) = \frac { 1 } { 2 } | \begin{array} { c } x _ { 2 } - x _ { 1 } \ x _ { 3 } - x _ { 1 } \\ y _ { 2 } - y _ { 1 } \ y _ { 3 } - y _ { 1 } \end{array} | = \frac { 1 } { 2 } | \begin{array} { c } 1 & 1 & 1 \\ x _ { 1 } \ x _ { 2 } \ x _ { 3 } \\ y _ { 1 } \ y _ { 2 } \ y _ { 3 } \end{array} | . \quad ( 1 . 2 8 ) \\ \\ \text {We will also use the points } z _ { i } ^ { * } = \mathcal { I } ( z _ { i } ) = ( x _ { i } , y _ { i } ^ { * } ) , \overline { z _ { i } } ^ { * } = ( x _ { i } , - y _ { i } ^ { * } ) \text { and } w _ { i } =$$

We will also use the points z ∗ i = S (zi ) = (xi , y ∗ i ) , zi ∗ = (xi , - y ∗ i ) and wi = (xi , yi - 2 y ∗ i ) , i = 1 , 2 , 3. In particular, the identity S (wi) = zi ∗ is satisfied and the two triangles Conv ( { z 1 , z 2 , z 3 } ) and Conv ( { w 1 , w 2 , w 3 } ) have same area. Consequently,

$$V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } , z _ { 2 } , z _ { 3 } \} ) + V _ { 2 } ( \text {Conv} ( \{ w _ { 1 } , w _ { 2 } , w _ { 3 } \} ) \\$$

$$\geq \frac { 1 } { 2 } | \begin{matrix} 1 & 1 & 1 \\ x _ { 1 } & x _ { 2 } & x _ { 3 } \\ y _ { 1 } & y _ { 2 } & y _ { 3 } \end{matrix} | & | \begin{matrix} 1 & 1 & 1 \\ x _ { 1 } & x _ { 2 } & x _ { 3 } \\ y _ { 1 } & y _ { 2 } & - 2 y _ { 1 } ^ { * } & y _ { 2 } - 2 y _ { 2 } ^ { * } & y _ { 3 } - 2 y _ { 3 } ^ { * } \end{matrix} |$$

<!-- p:38 -->


$$& \geq \frac { 1 } { 2 } | \begin{array} { c c c } 1 & 1 & 1 & 1 \\ x _ { 1 } & x _ { 2 } & x _ { 3 } & | | \\ 2 y _ { 1 } ^ { * } & 2 y _ { 2 } ^ { * } & 2 y _ { 3 } ^ { * } & \end{array} | \\ & = 2 V _ { 2 } ( \text {Conv} ( \{ z _ { 1 } ^ { * } , z _ { 2 } ^ { * } , z _ { 3 } ^ { * } \} ) ) .$$

Integrating (1.29) with respect to z 1 , z 2 , z 3 ∈ K and using the fact that both the transformation S and the reflection with respect to the x -axis preserve the Lebesgue measure, we obtain (1.27). It remains to use the fact that the equality in (1.27) is satisfied only when K is an ellipse. In fact, for any convex body K , there exists a sequence of lines such that the image of K under consecutive applications of Steiner symmetrizations with respect to the lines of that sequence converges to a disk [26]. The function A( · ) being continuous on the set of convex bodies, we obtain A(K) ≥ A( 1 √ π D ) and therefore p 4 (K) ≤ p 4 ( D ) .

We turn now our attention to the proof of p 4 (K) ≤ p 4 ( T ) . The method relies on a transformation T in the same spirit as the Steiner symmetrization, called Schüttelung or shaking and defined as follows:

$$\mathcal { T } \colon \left \{ \begin{matrix} K & \longrightarrow \mathbb { R } ^ { 2 } \\ ( x , y ) \longmapsto ( x , y - f _ { - } ( x ) ) \end{matrix}$$

In other words, T sends any segment which is the intersection of K with a vertical line to its unique vertical translate with a lower-end on the x -axis, see Fig. 1.7. In particular, T is area-preserving and preserves the convexity.

Using both (1.28) and the fact that K is a unit-area convex body which satisfies the equality

$$K = \{ ( x , y ) \colon x \in [ x _ { \min } , x _ { \max } ] , f _ { - } ( x ) \leq y \leq f _ { + } ( x ) \} ,$$

we get that

$$\overline { A } ( K ) = \iint _ { [ x _ { \min } , x _ { \max } ] } I \left ( x _ { 1 } , x _ { 2 } , x _ { 3 } \right ) d x _ { 1 } d x _ { 2 } d x _ { 3 } \quad \ \ ( 1 . 3 0 )$$

where

$$I ( x _ { 1 } , x _ { 2 } , x _ { 3 } ) \\ = \int _ { f _ { - } ( x _ { 1 } ) } ^ { f _ { + } ( x _ { 1 } ) } \int _ { f _ { - } ( x _ { 2 } ) } ^ { f _ { + } ( x _ { 2 } ) } \int _ { f _ { - } ( x _ { 3 } ) } ^ { f _ { + } ( x _ { 3 } ) } \frac { 1 } { 2 } | \begin{array} { c | c c } 1 & 1 & 1 & 1 \\ | d y _ { 3 } d y _ { 2 } d y _ { 1 } \\ | y _ { 1 } & y _ { 2 } & y _ { 3 } \\ \end{array} | \\ = \int _ { f _ { - } ( x _ { 1 } ) } ^ { f _ { + } ( x _ { 1 } ) } \int _ { f _ { - } ( x _ { 2 } ) } ^ { f _ { + } ( x _ { 2 } ) } \int _ { f _ { - } ( x _ { 3 } ) } ^ { f _ { + } ( x _ { 3 } ) } \frac { 1 } { 2 } | a _ { 1 } y _ { 1 } + a _ { 2 } y _ { 2 } + a _ { 3 } y _ { 3 } | d y _ { 3 } d y _ { 2 } d y _ { 1 } .$$

$$\int f _ { - } ( x _ { 1 } ) \ \int f _ { - } ( x _ { 2 } ) \ \int f _ { - } ( x _ { 3 } )$$


<!-- p:39 -->


1

and with a 1 = a 1 (x 1 , x 2 , x 3 ) = (x 3 - x 2 ) , a 2 = a 2 (x 1 , x 2 , x 3 ) = (x 1 - x 3 ) and a 3 = a 3 (x 1 , x 2 , x 3 ) = (x 2 - x 1 ) . For sake of simplicity, the dependency of the coefficients ai on the coordinates xi is omitted. When x 1 , x 2 , x 3 are fixed, the function I calculates the 4-dimensional volume of the parallelepiped region delimited by the rectangular basis [ f - (x 1 ), f + (x 1 ) ] × [ f - (x 2 ), f + (x 2 ) ] × [ f - (x 3 ), f + (x 3 ) ] × { 0 } and the surface of equation y 4 = 1 2 | a 1 y 1 + a 2 y 2 + a 3 y 3 | . In particular, if we allow the rectangular basis to be translated, the integral I only depends on the distance D in R 3 from the midpoint ( f - (x 1 ) + f + (x 1 ) 2 , f - (x 2 ) + f + (x 2 ) 2 , f - (x 3 ) + f + (x 3 ) 2 ) of the rectangular basis to the set { (y 1 , y 2 , y 3 ) : a 1 y 1 + a 2 y 2 + a 3 y 3 = 0 } and is even an increasing function of D . We notice that D satisfies

$$\mathcal { D } & = \frac { | a _ { 1 } ( f _ { - } ( x _ { 1 } ) + f _ { + } ( x _ { 1 } ) ) + a _ { 2 } ( f _ { - } ( x _ { 2 } ) + f _ { + } ( x _ { 2 } ) ) + a _ { 3 } ( f _ { - } ( x _ { 3 } ) + f _ { + } ( x _ { 3 } ) ) | } { 2 \sqrt { a _ { 1 } ^ { 2 } + a _ { 2 } ^ { 2 } + a _ { 3 } ^ { 2 } } } \\ & = \frac { 1 } { 2 \sqrt { a _ { 1 } ^ { 2 } + a _ { 2 } ^ { 2 } + a _ { 3 } ^ { 2 } } } | \Big | _ { f _ { - } ( x _ { 1 } ) } \Big | _ { f _ { - } ( x _ { 2 } ) } \Big | _ { f _ { - } ( x _ { 3 } ) } \Big | + \Big | _ { x _ { 1 } } \Big | _ { x _ { 2 } } \Big | _ { x _ { 3 } } \Big | _ { x _ { 3 } } \Big | | .$$

Now, the two determinants in the last equality above are two times the algebraic areas of two triangles whose vertices are on ∂K and have respective x -coordinates x 1, x 2 and x 3. Because of the convexity of K , they must have opposite signs. Consequently, we get from the triangular inequality || a | - | b || ≤ | a - b | that

$$= \frac { 1 } { 2 \sqrt { a _ { 1 } ^ { 2 } + a _ { 2 } ^ { 2 } + a _ { 3 } ^ { 2 } } } | \left | \begin{array} { c c c } x _ { 1 } & x _ { 2 } & x _ { 3 } \\ f _ { - } ( x _ { 1 } ) & f _ { - } ( x _ { 2 } ) & f _ { - } ( x _ { 3 } ) \end{array} \right | & \left | \begin{array} { c c c } x _ { 1 } & x _ { 2 } & x _ { 3 } \\ f _ { + } ( x _ { 1 } ) & f _ { + } ( x _ { 2 } ) & f _ { + } ( x _ { 3 } ) \end{array} \right | \\$$

$$\mathcal { D } & \leq \frac { 1 } { 2 \sqrt { a _ { 1 } ^ { 2 } + a _ { 2 } ^ { 2 } + a _ { 3 } ^ { 2 } } } | \begin{array} { c c c } 1 & 1 & 1 \\ x _ { 1 } & x _ { 2 } & x _ { 3 } \\ f _ { + } ( x _ { 1 } ) - f _ { - } ( x _ { 1 } ) & f _ { + } ( x _ { 2 } ) - f _ { - } ( x _ { 2 } ) & f _ { + } ( x _ { 3 } ) - f _ { - } ( x _ { 3 } ) \end{array} | . \\ \intertext { In particular, after application of the transformation }$$

In particular, after application of the transformation T , the distance is equal to the right-hand side of the inequality above. The integral I (x 1 , x 2 , x 3 ) being an increasing function of D , it is greater, which implies thanks to (1.30) that

$$\overline { A } ( K ) \leq \overline { A } ( \mathcal { T } ( K ) ) .$$

It remains to use the fact that there exists a sequence of lines such that the image of K under consecutive applications of the Schüttelung operations with respect to these lines converges to a triangle [13]. Therefore, we get the inequality A(K) ≤ A( T ) and thanks to (1.15), the required inequality p 4 (K) ≥ p 4 ( T ) .


<!-- p:40 -->


#### 1.4.2 Random Polytopes

There are several ways of extending Sylvester's initial question:

- (a) increasing the number of random points inside K and ask for the probability that n i.i.d. points uniformly distributed in a two-dimensional convex body K are in convex position , i.e. are extreme points of their convex hull;
- (b) increasing the dimension and ask for the probability that (d + 2 ) or more i.i.d. points uniformly distributed in a d -dimensional convex body K are the vertices of a convex polytope;
- (c) increasing the number of random points in any dimension and ask more general questions, such as the distribution and mean value of the number of extreme points and of other characteristics of the convex hull;
- (d) replacing the uniform distribution in K by another probability distribution in R d .

The topic of random polytopes has become more popular in the last 50 years and this is undoubtedly due in part to the birth of computational geometry and the need to get quantitative information on the efficiency of algorithms in discrete geometry, in particular algorithms designed for the construction of the convex hull of multivariate data. We describe below the state of the art on each of the problems above.

Problem (a) Let us denote by pn(K) the probability that n i.i.d. points uniformly distributed in K are in convex position. Using combinatorial arguments, P. Valtr obtained explicit calculations for pn( [ 0 , 1 ] 2 ) [124] and pn( T ) [125]. More recently, J.-F. Marckert provided a recursive formula for pn( D ) , which he implements to derive explicit values up to p 8 ( D ) [75]. Though there is no general formula for every K , the sequences pn(K) for all convex bodies K share a common asymptotic behavior when n →∞ . In a breakthrough paper [8] in 1999, I. Bárány showed that for every K with area 1, when n →∞ ,

$$\log p _ { n } ( K ) = - 2 n \log ( n ) + n \log ( \frac { 1 } { 4 } e ^ { 2 } p a ( K ) ) + o ( n )$$

where f(n) = o(g(n)) means that lim n →∞ f(n)/g(n) = 0 and pa (K) is the supremum of the so-called affine perimeter of all convex bodies included in K , see Sect. 1.4.2.2.

Problem (b) Let us denote by p (d) n (K) the probability that n i.i.d. points uniformly distributed in a convex body K of R d are in convex position. J.F.C. Kingman calculated p (d) d + 2 ( B d ) in 1969 [69] and it was shown by H. Groemer in 1973 that p (d) d + 2 (K) is minimal when K is the unit ball (or an ellipsoid) [48]. It is still undecided whether the d -dimensional simplex should maximize p (d) d + 2 (K) though W. Blaschke had claimed that his proof in the case d = 2 could be directly extended [15]. Regarding the asymptotic behavior of p (d) n (K) when n → ∞ , I. Bárány conjectured a two-term expansion in the spirit of the two-dimensional case and


<!-- p:41 -->


1

showed the following one-term expansion [9]:

$$\log p _ { n } ( K ) = - \frac { 2 } { d - 1 } n \log ( n ) + O ( n ) \\$$

where f(n) = O(g(n)) means that f/g is bounded.

Problem (c) Let K be a convex body of R d and let Kn be the convex hull of n i.i.d. points uniformly distributed in K . The natural questions on this model have to do with the shape of Kn and the distributions of the geometric characteristics of Kn such as the number of vertices, number of faces or the volume. They can be treated in the two different contexts of fixed n and n large. This will be the focus of the end of the section.

Problem (d) There have been several works related to Problem (d). Wendel's result described below is one of them in the case of a symmetric distribution with respect to o . Other papers have focused on isotropic distributions [27] and especially the Gaussian distribution, see e.g. [10, 107].

For a more detailed account on the topic of random polytopes, we refer the reader to [113, Chapter 8], the lecture [58] and the very exhaustive survey [106]. In the rest of the section, we will present a few results related to Problem (c) in both the nonasymptotic and asymptotic regimes.

##### 1.4.2.1 Non-asymptotic Results

In this subsection, we describe two of the non-asymptotic results on the convex hull Kn of n i.i.d. points uniformly distributed in a convex body K of R d (Fig. 1.8): the Efron identity relating first moments of functionals of Kn and Wendel's calculation of the probability that the origin o belongs to Kn . In the sequel, fk( · ) is the number of k -dimensional faces of a convex polytope. In particular, f 0 ( · ) denotes the number of vertices.

In 1965, B. Efron proved an extension of (1.15), i.e. he provided an identity which connects in a very simple way the mean number of vertices of the convex hull of n points to the mean volume of the convex hull of (n - 1 ) points [39]. The calculation, which has been extended since then by several identities for higher moments due to Buchta [19], goes as follows. Let X 1 , · · · , Xn be the n i.i.d. uniform points in K . Then almost surely,

$$f _ { 0 } ( K _ { n } ) = \sum _ { k = 1 } ^ { n } 1 _ { \{ X _ { k } \notin C o n v ( X _ { 1 } , \cdots , X _ { k - 1 } , X _ { k + 1 } , \cdots , X _ { n } ) \} } .$$


<!-- p:42 -->


Fig. 1.8 Simulations of the random polytope K 100 (black) when K is a disk (left) and K is a square (right)

Taking the expectation of this equality, we obtain

$$E ( f _ { 0 } ( K _ { n } ) ) & = n P ( X _ { n } \not \in \text {Conv} ( X _ { 1 } , \cdots , X _ { n - 1 } ) ) \\ & = n E ( E ( \mathbf 1 _ { \{ X _ { n } \not \in \text {Conv} ( X _ { 1 } , \cdots , X _ { n - 1 } ) \} | X _ { 1 } , \cdots , X _ { n - 1 } ) } \\ & = n \left ( 1 - \frac { E ( V _ { d } ( K _ { n - 1 } ) ) } { V _ { d } ( K ) } \right ) .$$

In 1962, J.G. Wendel showed an explicit formula for the probability that the origin o lies inside the convex hull of n i.i.d. points with a symmetric distribution with respect to o [129]. Let X 1 , · · · , Xn , n ≥ 1, be the random points and we assume additionally that their common distribution is such that with probability one, all subsets of size d are linearly independent. We first notice that o is not in the convex hull if and only if there exists a half-space containing all the points, i.e. there exists y ∈ R d such that 〈 y, Xk 〉 &gt; 0 for every 1 ≤ k ≤ n . This implies in particular that the probability P(o ̸∈ Conv ( { X 1 , · · · , Xn } )) equals 1 as soon as n ≤ d and 2 - (n - 1 ) when d = 1. Now the calculation for n ≥ (d + 1 ) ≥ 3 is done by purely combinatorial arguments.

Indeed, each Xk defines a set of authorized y which is a half-space bounded by the linear hyperplane Hk with normal vector Xk . Consequently, each connected component of the complement of ⋃ n k = 1 Hk can be coded by a sequence in {- 1 , 1 } n where + 1 at the k -th position means that the connected component lies in the authorized half-space bounded by Hk . There are 2 n possible codes and we denote by Nd,n the total number of connected components. The variable Nd,n is almost surely constant, as we shall see later on. Recalling from the earlier discussion that a necessary and sufficient condition to have the origin outside of the convex hull is that the intersection of all authorized half-spaces bounded by the hyperplanes Hk is not empty, we obtain the following equivalence: o is not in the convex hull of { X 1 , · · · , Xn } if and only if one of the connected components is coded by


<!-- p:43 -->


1

( 1 , · · · , 1 ) . This happens with probability

$$P ( o \notin \text {Conv} ( \{ X _ { 1 } , \cdots , X _ { n } \} ) = \frac { N _ { d , n } } { 2 ^ { n } } .$$

As announced earlier, the variable Nd,n is constant on the event of probability one that any subset of size d of the n points is linearly independent. We calculate Nd,n on this event by proving a recurrence relation. For fixed n ≥ 2, the n -th hyperplane Hn separates into two subparts each connected component of R d \ ⋃ n - 1 k = 1 Hk that it meets and leaves unchanged the remaining connected components of R d \ ⋃ n - 1 k = 1 Hk . The number of connected components of R d \ ⋃ n - 1 k = 1 Hk that Hn meets is equal to the number of connected components of Hn \ ⋃ n - 1 k = 1 Hk , i.e. Nd - 1 ,n - 1 while the number of untouched connected components of R d \ ⋃ n - 1 k = 1 Hk is Nd,n - 1 - Nd - 1 ,n - 1. Consequently, we get the relation

$$N _ { d , n } = N _ { d - 1 , n - 1 } + N _ { d , n - 1 } .$$

Using that Nd, 1 = 2 for every d ≥ 1, we deduce that Nd,n = 2 ∑ d - 1 k = 0 ( n - 1 k ) thanks to Pascal's triangle. This last equality combined with (1.31) leads to

$$P ( o \notin C o n v ( \{ X _ { 1 } , \cdots , X _ { n } \} ) = 2 ^ { - ( n - 1 ) } \sum _ { k = 0 } ^ { d - 1 } \binom { n - 1 } { k } .$$

In particular, when n →∞ , this probability goes to zero exponentially fast. In the next section, we investigate the general asymptotic behavior of Kn .

##### 1.4.2.2 Asymptotic Results

When n → ∞ , Kn converges to K itself and studying the asymptotic behavior of Kn means being able to quantify the quality of the approximation of K by Kn . The first breakthrough is due to A. Rényi and R. Sulanke in 1963 and 1964 [107, 108]. They showed in particular that in the planar case, the mean number of vertices of Kn has a behavior which is highly dependent on the regularity of the boundary of K . Indeed, when ∂K is of class C 2 ,

$$E ( f _ { 0 } ( K _ { n } ) ) _ { n \to \infty } \sim 2 ^ { \frac { 1 } { 3 } } 3 ^ { - \frac { 1 } { 3 } } \Gamma \left ( \frac { 5 } { 3 } \right ) V _ { d } ( K ) ^ { - \frac { 1 } { 3 } } \int _ { \partial K } r _ { s } ^ { - \frac { 1 } { 3 } } d s \, n ^ { \frac { 1 } { 3 } } .$$

where rs is the radius of curvature of ∂K at s and f(n) ∼ n →∞ g(n) means that f/g

When K is a convex polygon itself, the number of vertices of Kn is expected to be smaller in mean as, roughly speaking, it does not require many edges to

has limit 1. The quantity ∫ ∂K r - 1 3 s d s is called the affine perimeter of K .


<!-- p:44 -->


approximate the flat parts of the boundary of K . While the extreme points of Kn are more or less homogeneously spread along the curve ∂K when it is smooth, they are concentrated in the corners , i.e. around the vertices of K when K is a convex polygon. Consequently, the growth rate of E(f 0 (Kn)) becomes logarithmic, as opposed to the polynomial rate from (1.32). Denoting by r the number of vertices of the convex polygon K , we get

$$E ( f _ { 0 } ( K _ { n } ) ) \underset { n \to \infty } { \sim } \frac { 2 r } { 3 } \log n .$$

The two estimates (1.32) and (1.33) have been extended in many directions: asymptotic means of fk(Kn) , 1 ≤ k ≤ d and of Vd(Kn) in any dimension and convergences [7, 105], same for the intrinsic volumes in the smooth case [103, 114], concentration estimates [126], second-order results [25, 104] and so on. Many basic questions remain unanswered, like for instance the asymptotic behavior of the mean intrinsic volumes of Kn when K is a polytope.

In the next section, we generate for the first time non-convex random sets as unions of translates of a so-called grain .

### 1.5 From the Bicycle Wheel Problem to Random Coverings and Continuum Percolation

In this section, we start with a practical problem which can be reinterpreted as a random covering problem on the circle by random arcs with fixed length. We solve it and discuss possible extensions. This leads us to a classical model of random covering of the Euclidean space called the Boolean model and we present briefly some of the questions related to it: covering of a particular set, continuum percolation and shapes of the connected components of the two phases.

#### 1.5.1 Starting from the Bicycle Wheel Problem and Random Covering of the Circle

In 1989, C. Domb tells how his work during the second World War in radar research for the Admiralty led him to ask H. Jeffreys in 1946 about a covering problem [37]. H. Jeffreys related his question to his own bicycle wheel problem which he had formulated several years before in the following way: a man is cycling along a road and passes through a region threwn with tacks. He wishes to know whether one has entered his tire. Because of the traffic, he can only snatch glances at random times. At each glance he has covered a fraction x of the wheel. What is the probability that after n glances, he has covered the whole wheel? It turns out that the problem had


<!-- p:45 -->


1

Fig. 1.9 Simulations of the bicycle wheel problem for x = 0 . 01: the random intervals in the cases n = 20 (left), n = 50 (middle) and n = 100 (right)

been solved by W.L. Stevens in 1939 [121], see also [119, Chapter 4]. Surprisingly, his method that we describe below relies exclusively on combinatorial arguments (Fig. 1.9).

We start by rephrasing the problem in mathematical terms in the following way: a set of n intervals of length x are placed randomly on a circle of length one and we aim at calculating the probability qn(x) that the circle is fully covered. The endpoints in the anticlockwise direction of the n random intervals of length x are denoted by U 1 , · · · , Un and are assumed to be n i.i.d. random variables uniformly distributed in ( 0 , 1 ) . For every 1 ≤ i ≤ n , we consider the event denoted by Ai that the endpoint of the i -th arc is not covered by the other (n - 1 ) random intervals. The key idea consists in noticing that the circle is fully covered by the n random intervals if and only if all endpoints are covered. Consequently, using the inclusion-exclusion principle, we obtain that the probability p cov (n, x) satisfies

$$\text { principle, we obtain that the probability } & \ p _ { c o w } ( n , x ) \ s t a s h e s \\ & 1 - p _ { c o w } ( n , x ) = P \left ( \cup _ { i = 1 } ^ { n } A _ { i } \right ) \\ & = \sum _ { k = 1 } ^ { n } ( - 1 ) ^ { k + 1 } \sum _ { 1 \leq i < 2 < \cdots < k - n } P \left ( A _ { i _ { 1 } } \cap A _ { i _ { 2 } } \cap \cdots \cap A _ { i _ { k } } \right ) \\ & = \sum _ { k = 1 } ^ { n } ( - 1 ) ^ { k + 1 } \binom { n } { k } P ( A _ { 1 } \cap A _ { 2 } \cap \cdots A _ { k } ) , \quad ( 1 . 3 4 ) \\ \text {where the last equality comes from the fact that the variables } U _ { 1 } , \cdots , U _ { n } \text { are}$$

where the last equality comes from the fact that the variables U 1 , · · · , Un are exchangeable. It remains to calculate P(A 1 ∩ A 2 ∩ · · · Ak) , 1 ≤ k ≤ n , i.e. the probability that the endpoint of each of the first k random intervals is not covered, not only by the (k - 1 ) other intervals from the first bunch but also by the (n - k) remaining intervals. This means that the event A 1 ∩ A 2 ∩··· Ak can be rewritten as

$$A _ { 1 } \cap A _ { 2 } \cap \cdots A _ { k } = B _ { k } \bigcap \left ( \bigcap _ { i = k + 1 } ^ { n } C _ { i , k } \right ) \\ \vdots \, d o w h t h e t h e \colon \, \intertext { a $ A _ { 1 } \cap A _ { 2 } \cap \cdots A _ { k } = B _ { k } \bigcap \left ( \bigcap _ { i = k + 1 } ^ { n } C _ { i , k } \right ) } \colon$$

where Bk is the event that the endpoint of each of the first k random intervals is not covered by the (k - 1 ) other intervals from the first bunch and Ci,k , k + 1 ≤ i ≤ n , is the event that the i -th random arc does not cover any of the endpoints from the first k random intervals.


<!-- p:46 -->


On the event Bk , the k endpoints are at distance at least x from each other. Consequently, P(Bk) is the probability that a random division of the circle into k parts produces parts of lengths larger than x . This is in particular the exact problem 666 that W.A. Whitworth solves in his book Choice and Chance published in 1870 [130]. By a direct integral calculation, we get

$$P ( B _ { k } ) = ( 1 - k x ) _ { + } ^ { k - 1 } .$$

Conditional on the positions of the first k random intervals which satisfy the condition of the event Bk , the events Ci,k are independent. The set of allowed positions on the circle for the endpoint of the i -th random arc is then the complement of a union of k disjoint intervals of length x . Consequently,

$$P ( \bigcap _ { i = k + 1 } ^ { n } C _ { i , k } | B _ { k } ) = ( 1 - k x ) _ { + } ^ { n - k } .$$

Combining (1.36), (1.37) with (1.35) and (1.34) shows that

$$p _ { c o v } ( n , x ) ( x ) = \sum _ { k = 0 } ^ { n } ( - 1 ) ^ { k } { n \choose k } ( 1 - k x ) _ { + } ^ { n - 1 } .$$

In 1982, the formula was extended by A.F. Siegel and L. Holst to the explicit calculation of p cov (n, μ) , i.e. the probabiity to cover the circle with i.i.d. intervals which have random lengths such that these lengths are i.i.d. μ -distributed variables which are independent of the positions of the intervals on the circle [118]. They even provided the distribution of the number of uncovered gaps on the circle in this context. Following their work, T. Huillet obtained the joint distribution of the lengths of the connected components [63]. In [117], A.F. Siegel conjectured that p cov (n, μ) satisfies a monotonicity result which is proved in [22] and is the following: if two probability distributions μ,ν on ( 0 , 1 ) are such that μ ≤ ν for the convex order, see e.g. [91, Chapter 1], then p cov (n, μ) ≤ p cov (n, μ) . In particular, thanks to Jensen's inequality, this implies that p cov (n, x) ≤ p cov (n, μ) where x is the mean of μ .

To the best of our knowledge, the most recent contribution in higher dimension is due to Bürgisser et al. [21] and contains on one hand an exact formula for the probability to cover the sphere with n spherical caps of fixed angular radius when this radius is larger than π/ 2 and on the other hand an upper bound for this probability when the angular radius is less than π/ 2.

Finally, a related question introduced by A. Dvoretzky in 1956 concerns the covering of the circle by an infinite number of intervals (In)n with deterministic lengths (ln)n such that the sequence (ln)n is non-increasing [38]. In 1972, L.A. Shepp showed that the circle is covered infinitely often with probability 1 if and only if the series ∑ ∞ n = 1 n - 2 exp (l 1 +··· + ln) is divergent [116].


<!-- p:47 -->


1

#### 1.5.2 A Few Basics on the Boolean Model

A natural extension of the bicycle wheel problem consists in considering random coverings of the Euclidean space by so-called grains with random positions and possibly random shapes or sizes. Considering the discussion on the translation invariance in Sect. 1.3, we construct directly such a model in R d . Let P λ be a homogeneous Poisson point process of intensity λ and let K be a fixed non-empty compact set of R d , called the grain . Then the associated Boolean model is defined as the random set ⋃ x ∈ P λ (x + K) , sometimes also called the occupied phase of the Boolean model. In the case when K = Br(o) , r &gt; 0, it was introduced by E.N. Gilbert in 1961 as a simplified approximation of the coverage of a radio transmission network where each individual can send a signal up to distance r [42]. When K is a random grain, for instance K = BR(o) with R a non-negative random variable, the model can be extended in the following way: the occupied phase is ⋃ x ∈ P λ (x + Kx) where (Kx)x is a collection of i.i.d. copies of K and independentof the Poisson point process P λ (Fig. 1.10).

The Boolean model is well-adapted in a series of applied situations including flow in porous media [64], conduction in dispersions [76] and the elastic behavior of composites [131]. In practice, there are of course lots of fundamental statistical issues related in particular to the estimation of the intensity or of the grain distribution from the observation of the intersection of the Boolean model with a window or from sections or projections of this intersection on lower-dimensional subspaces. We shall omit this aspect and describe only the following probabilistic questions related to the model:

- (a) estimating the covering probability of a particular set;
- (b) concentrating on percolation, i.e. looking for the existence of an unbounded connected component of either the occupied or vacant phase;
- (c) studying the geometry of the occupied or vacant phase or of their connected components.

Fig. 1.10 Simulation of the Boolean model in the unit square in the case λ = 100 and K = BR(o) where R is uniform on ( 0 , 0 . 1 )

<!-- p:48 -->


Problem (a) In the eighties, L. Flatto and D.J. Newman followed by S. Janson investigated the distribution of the number of random balls with fixed radius necessary to cover a bounded subset of R d or a Riemannian manifold in two seminal works [40, 65]. Though this distribution is not explicit, S. Janson showed in particular a convergence in distribution, when the radius goes to 0, of the renormalized number to a Gumbel law. Regarding the covering of the whole space R d , it is shown in [51, Theorem 3.1] and [81, Proposition 7.3] that R d = ⋃ x ∈ P λ BR(x) occurs almost surely when R d is a non-integrable random variable and if not, the vacant set has infinite Lebesgue measure almost surely. P. Hall obtained upper and lower bounds for the probability of not covering R d when R is deterministic, see [51, Theorem 3.11]. These results have been recently extended by a study of the covering of R d by unions of balls Br(x) when the couples (x, r) belong to a Poisson point process in R d × ( 0 , ∞ ) [14].

Problem (b) This question has been treated mostly in the case of i.i.d. grains of type BR(o) where R is a non-negative random variable. In [50], P. Hall shows notably that if E(R 2 d - 1 ) is finite, then there exists a critical intensity λc ∈ ( 0 , ∞ ) such that if λ &lt; λc , all the connected components of the occupied phase are bounded almost surely. A breakthrough due to Gouéré [46] extends P. Hall's result in the following way: there exists a positive critical intensity λc under which all connected components of the occupied phase are bounded if and only if E(R d ) is finite. We also refer to [47] for the extension of that result for unions of balls Br(x) when the couples (x, r) belong to a Poisson point process in R d × ( 0 , ∞ ) .

In the reference book [81] by R. Meester and R. Roy, it is shown that for any such Poisson Boolean model, the number of unbounded connected components of the occupied (resp. vacant) phase is either 0 or 1 almost surely, see Theorems 3.6 and 4.6 therein. Moreover, in the particular case of a two-dimensional Boolean model with almost surely bounded radii, criticality of the occupied and vacant phases coincide, i.e. there exists λc ∈ ( 0 , ∞ ) such that for λ &lt; λc , there is possible percolation of the vacant phase and no unbounded component of the occupied phase almost surely, for λ = λc , neither the occupied phase nor the vacant phase percolates and for λ &gt; λc , there is possible percolation of the occupied phase and no unbounded component of the vacant phase, see [81, Theorems 4.4, 4.5]. The equality of the two critical intensities of the vacant and occupied phases has been proved without the condition of almost surely bounded radii in two very recent works due to Penrose [98] and to Ahlberg et al. [1].

Problem (c) The first formulas which connect the mean values of the characteristics of the grain to the mean values of the characteristics of the Boolean model intersected with a window are available in seminal papers due to Miles [87] and Davy [30]. A few decades later, [52] investigates large deviation probabilities for the occupied volume in a window. More recently, in [59], asymptotic covariance formulas and central limit theorems are derived for a large set of geometric functionals, including intrinsic volumes and so-called Minkowski tensors. We describe below two very simple examples of questions related to (c).


<!-- p:49 -->


1

##### 1.5.2.1 The Spherical Contact Distribution of the Vacant Phase

We aim at determining the so-called spherical contact distribution of the vacant phase , i.e. the distribution of the radius Rc of the largest ball centered at o and included in the vacant phase, conditional on the event { o ̸∈ ⋃ x ∈ P λ (x + K) } . We observe that Rc ≥ r means that there is no point of P λ at distance less than r from - K . Consequently, we get

$$P ( R \geq r ) & = P ( \mathcal { P } _ { \lambda } \cap ( - K + B _ { r } ( o ) ) = \emptyset ) \\ & = \exp ( - \lambda V _ { d } ( K + B _ { r } ( o ) ) ) .$$

When K is a convex body, we can use the Steiner formula (1.4) and get that

$$P ( R \geq r ) = \exp \left ( - \lambda \sum _ { k = 0 } ^ { d } \kappa _ { d - k } V _ { k } ( K ) r ^ { d - k } \right ) .$$

This calculation shows that when the grain K is convex, the quantity log (P(R ≥ r)) is a polynomial in r . In [60], it is shown that the converse is not true in general, unless the spherical contact distribution is replaced by another contact distribution.

##### 1.5.2.2 The Number of Grains in a Typical Connected Component of the Occupied Phase

Similarly to the construction in Sect. 1.3 of the typical cell of a stationary tessellation, there is a way to define a typical connected component of the occupied phase: we add a deterministic point at the origin to the homogeneous Poisson point process and consider the connected component containing the origin of ⋃ x ∈ P λ ∪{ o } (x + K) . The aim of the calculation below is to derive a general formula for the distribution of the number N o of grains contained in that connected component. The method below follows the work by Penrose [97], see also [101]. For any n ≥ 0, we get

$$P ( \mathcal { N } _ { o } = n + 1 ) = E \left ( \sum _ { \{ x _ { 1 } , \cdots , x _ { n } \} \in \mathcal { P } _ { \lambda } ^ { ( n ) } } F ( \{ x _ { 1 } , \cdots , x _ { n } \} , \mathcal { P } _ { \lambda } ) \right )$$

where P (n) λ is the set of finite subsets of P λ with exactly n elements and the functional F( { x 1 , · · · , xn } , P λ) is the indicator function of the event that the union (o + K) ∪ (x 1 + K) ∪· · ·∪ (xn + K) is connected and all the remaining grains (x + K) , x ∈ P λ \ { x 1 , · · · , xn } are disconnected from that union. The expectation in (1.38) can be made explicit thanks to Mecke's formula for Poisson point processes, see e.g.


<!-- p:50 -->


[113, Corollary 3.2.3]. We get indeed, for n ≥ 1,

$$[ 1 5 , \text {Conditional } 5 . 2 . 5 ] \colon & \text { we get } \text {gcd} ( x _ { 1 } , \cdots , x _ { n } ) \, \text {, } \mathcal { P } _ { \lambda } \cup \{ x _ { 1 } , \cdots , x _ { n } \} \text {d} x _ { 1 } \cdots \text {d} x _ { n } \\ P ( \mathcal { N } _ { o } = n + 1 ) & = \frac { \lambda ^ { n } } { n ! } \int E ( F ( \{ x _ { 1 } , \cdots , x _ { n } \} , \mathcal { P } _ { \lambda } \cup \{ x _ { 1 } , \cdots , x _ { n } \} ) d x _ { 1 } \cdots d x _ { n } \\ & = \frac { \lambda ^ { n } } { n ! } \int \int ^ { 1 } _ { 0 \leq k \leq n } ( x _ { 1 } + K ) \, \text {connected} \int \\ & \quad P ( \forall x \in \mathcal { P } _ { \lambda } , ( x + K ) \cap \bigcup _ { 0 \leq k \leq n } ( x _ { i } + K ) = \emptyset ) d x _ { 1 } \cdots d x _ { n } \\ \intertext { where for sake of simplicity, the origin o h as been denoted by x _ { 0 } . U sing again the }$$

where for sake of simplicity, the origin o has been denoted by x 0. Using again the fact that P λ is a Poisson point process, we deduce that

$$P ( \mathcal { N } _ { 0 } & = n + 1 ) \\ & = \frac { \lambda ^ { n } } { n ! } \int _ { \{ \cup _ { 0 \leq k \leq n } ( x _ { i } + K ) \text { connected} \} } e ^ { - \lambda V _ { d } ( ( \cup _ { 0 \leq k \leq n } ( x _ { i } + K ) ) + ( - K ) ) d x _ { 1 } \cdots d x _ { n } } . \\$$

When K = Br(o) for fixed r &gt; 0, the previous formula becomes

$$P ( \mathcal { N } _ { 0 } = n + 1 ) & = \frac { \lambda ^ { n } } { n ! } \int \mathbf 1 _ { \{ \cup _ { 0 \leq k \leq n } B _ { r } ( x _ { i } ) \text { connected} \} } e ^ { - \lambda V _ { d } ( \cup _ { 0 \leq k \leq n } B _ { 2 ^ { r } } ( x _ { i } ) ) _ { d x _ { 1 } \cdots d x _ { n } } } . \\$$

Alexander [2] showed that when λ →∞ , this probability satisfies

$$\log P ( \mathcal { N } _ { o } = n + 1 ) = - \lambda \kappa _ { d } r ^ { d } + ( d - 1 ) n \log ( \frac { \lambda } { n } ) + O ( 1 )$$

where f(λ) = O(g(λ)) means that the function f/g is bounded for large λ . A side result is the so-called phenomenon of compression which says roughly that in a high-density Boolean model, the density inside a bounded connected component is larger than the ambient density.

Acknowledgements The author warmly thanks two anonymous referees for their careful reading of the original manuscript, resulting in an improved and more accurate exposition.

### References

1. D. Ahlberg, V. Tassion, A. Teixeira, Existence of an unbounded vacant set for subcritical continuum percolation (2017). https://arxiv.org/abs/1706.03053
2. K.S. Alexander, Finite clusters in high-density continuous percolation: compression and sphericality. Probab. Theory Relat. Fields 97 , 35-63 (1993)
3. R.V. Ambartzumian, A synopsis of combinatorial integral geometry. Adv. Math. 37 , 1-15 (1980)
4. F. Avram, D. Bertsimas, On central limit theorems in geometrical probability. Ann. Appl. Probab. 3 (4), 1033-1046 (1993)


<!-- p:51 -->


1

5. F. Baccelli, S. Zuyev, Poisson-Voronoi spanning trees with applications to the optimization of communication networks. Oper. Res. 47 , 619-631 (1999)
6. J.-E. Barbier, Note sur Ie probleme de l'aiguille et Ie jeu du joint couvert. J. Math. Pures Appl. 5 , 273-286 (1860)
7. I. Bárány, Random polytopes in smooth convex bodies. Mathematika 39 , 81-92 (1992)
8. I. Bárány, Sylvester's question: the probability that n points are in convex position. Ann. Probab. 27 , 2020-2034 (1999)
9. I. Bárány, A note on Sylvester's four-point problem. Studia Sci. Math. Hungar. 38 , 733-77 (2001)
10. Y.M. Baryshnikov, R.A. Vitale, Regular simplices and Gaussian samples. Discret. Comput. Geom. 11 , 141-147 (1994)
11. V. Baumstark, G. Last, Gamma distributions for stationary Poisson flat processes. Adv. Appl. Probab. 41 , 911-939 (2009)
12. J. Bertrand, Calcul des probabilités (Gauthier-Villars, Paris, 1889)
13. T. Biehl, Über Affine Geometrie XXXVIII, Über die Schüttlung von Eikörpern. Abh. Math. Semin. Hamburg Univ. 2 , 69-70 (1923)
14. H. Biermé, A. Estrade, Covering the whole space with Poisson random balls. ALEA Lat. Am. J. Probab. Math. Stat. 9 , 213-229 (2012)
15. W. Blaschke, Lösung des 'Vierpunktproblems' von Sylvester aus der Theorie der geometrischen Wahrscheinlichkeiten. Leipziger Berichte 69 , 436-453 (1917)
16. W. Blaschke, Vorlesungen über Differentialgeometrie II: Affine Differentialgeometrie (Springer, Berlin, 1923)
17. W. Blaschke, Integralgeometrie 2: Zu Ergebnissen von M.W. Crofton. Bull. Math. Soc. Roum. Sci. 37 , 3-11 (1935)
18. D. Bosq, G. Caristi, P. Deheuvels, A. Duma P. Gruber, D. Lo Bosco, V. Pipitone, Marius Stoka: Ricerca Scientifica dal 1951 al 2013 , vol. III (Edizioni SGB, Messina, 2014)
19. C. Buchta, An identity relating moments of functionals of convex hulls. Discret. Comput. Geom. 33 , 125-142 (2005)
20. G.-L.L. Comte de Buffon, Histoire naturelle, générale et particulière, avec la description du cabinet du Roy . Tome Quatrième (Imprimerie Royale, Paris, 1777)
21. P. Bürgisser, F. Cucker, M. Lotz, Coverage processes on spheres and condition numbers for linear programming. Ann. Probab. 38 , 570-604 (2010)
22. P. Calka, The distributions of the smallest disks conta ining the Poisson-Voronoi typical cell and the Crofton cell in the plane. Adv. Appl. Probab. 34 , 702-717 (2002)
23. P. Calka, Tessellations, in New Perspectives in Stochastic Geometry , ed. by W.S. Kendall, I. Molchanov (Oxford University Press, Oxford, 2010), pp. 145-169
24. P. Calka, Asymptotic methods for random tessellations, in Stochastic Geometry, Spatial Statistics and Random Fields , ed. by E. Spodarev. Lecture Notes in Mathematics, vol. 2068 (Springer, Heidelberg, 2013), pp. 183-204
25. P. Calka, T. Schreiber, J.E. Yukich, Brownian limits, local limits and variance asymptotics for convex hulls in the ball. Ann. Probab. 41 , 50-108 (2013)
26. C. Carathéodory, E. Study, Zwei Beweise des Satzes daß der Kreis unter allen Figuren gleichen Umfanges den größten Inhalt hat. Math. Ann. 68 , 133-140 (1910)
27. H. Carnal, Die konvexe Hülle von n rotationssymmetrisch verteilten Punkten. Z. Wahrscheinlichkeit. und verw. Gebiete 15 , 168-176 (1970)
28. A. Cauchy, Notes sur divers théorèmes relatifs à la rectification des courbes, et à la quadrature des surfaces. C. R. Acad. Sci. Paris 13 , 1060-1063 (1841)
29. N. Chenavier, A general study of extremes of stationary tessellations with examples. Stochastic Process. Appl. 124 , 2917-2953 (2014)
30. P. Davy, Projected thick sections through multi-dimensional particle aggregates. J. Appl. Probab. 13 , 714-722 (1976)
31. S.N. Chiu, D. Stoyan, W.S. Kendall, J. Mecke, Stochastic Geometry and its Applications , 3rd edn. Wiley Series in Probability and Statistics (Wiley, Chichester, 2013)


<!-- p:52 -->


32. R. Cowan, The use of ergodic theorems in random geometry. Adv. Appl. Probab. 10 , 47-57 (1978)
33. M.W. Crofton, On the theory of local probability, applied to straight lines drawn at random in a plane; the methods used being also extended to the proof of certain new theorems in the integral calculus. Philos. Trans. R. Soc. Lond. 156 , 181-199 (1868)
34. D.J. Daley, Asymptotic properties of stationary point processes with generalized clusters. Z. Wahrscheinlichkeitstheorie und Verw. Gebiete 21 , 65-76 (1972)
35. D.J. Daley, D. Vere-Jones, An Introduction to the Theory of Point Processes . Springer Series in Statistics (Springer, New York, 1988)
36. R. Descartes, Principia Philosophiae (Louis Elzevir, Amsterdam, 1644)
37. C. Domb, Covering by random intervals and one-dimensional continuum percolation. J. Stat. Phys. 55 , 441-460 (1989)
38. A. Dvoretzky, On covering a circle by randomly placed arcs. Proc. Natl. Acad. Sci. U S A 42 , 199-203 (1956)
39. B. Efron, The convex hull of a random set of points. Biometrika 52 , 331-343 (1965)
40. L. Flatto, D.J. Newman Random coverings. Acta Math. 138 , 241-264 (1977)
41. P. Franken, D. König, U. Arndt, V. Schmidt, Queues and Point Processes (Akademie-Verlag, Berlin, 1981)
42. E.N. Gilbert, Random plane networks. J. Soc. Ind. Appl. Math. 9 , 533-543 (1961)
43. A. Goldman, Sur une conjecture de D.G. Kendall concernant la cellule de Crofton du plan et sur sa contrepartie brownienne. Ann. Probab. 26 , 1727-1750 (1998)
44. A. Goldman, The Palm measure and the Voronoi tessellation for the Ginibre process. Ann. Appl. Probab. 20 , 90-128 (2010)
45. S. Goudsmit, Random distribution of lines in a plane. Rev. Mod. Phys. 17 , 321-322 (1945)
46. J.-B. Gouéré, Subcritical regimes in the Poisson Boolean model of continuum percolation. Ann. Probab. 36 , 1209-1220 (2008)
47. J.-B. Gouéré, Subcritical regimes in some models of continuum percolation. Ann. Appl. Probab. 19 , 1292-1318 (2009)
48. H. Groemer, On some mean values associated with a randomly selected simplex in a convex set. Pac. J. Math. 45 , 525-533 (1973)
49. H. Hadwiger, Vorlesungen Über Inhalt, Oberfläche und Isoperimetrie (Springer, Berlin, 1957)
50. P. Hall, On continuum percolation. Ann. Probab. 13 , 1250-1266 (1985)
51. P. Hall, Introduction to the Theory of Coverage Processes (Wiley, New York, 1988)
52. L. Heinrich, Large deviations of the empirical volume fraction for stationary Poisson grain models. Ann. Appl. Probab. 15 , 392-420 (2005)
53. L. Heinrich, L. Muche, Second-order properties of the point process of nodes in a stationary Voronoi tessellation. Math. Nachr. 281 , 350-375 (2008). Erratum Math. Nachr. 283 , 16741676 (2010)
54. L. Heinrich, H. Schmidt, V. Schmidt, Limit theorems for stationary tessellations with random inner cell structures. Adv. Appl. Probab. 37 , 25-47 (2005)
55. L. Heinrich, H. Schmidt, V. Schmidt, Central limit theorems for Poisson hyperplane tessellations. Ann. Appl. Probab. 16 , 919-950 (2006)
56. H.J. Hilhorst, Asymptotic statistics of the n -sided planar Poisson-Voronoi cell. I. Exact results. J. Stat. Mech. Theory Exp. 9 , P09005 (2005)
57. J. Hörrmann, D. Hug, M. Reitzner, C. Thäle, Poisson polyhedra in high dimensions. Adv. Math. 281 , 1-39 (2015)
58. D. Hug, Random polytopes, in Stochastic Geometry, Spatial Statistics and Random Fields , ed. by E. Spodarev. Lecture Notes in Mathematics, vol. 2068 (Springer, Heidelberg, 2013), pp. 205-238
59. D. Hug, G. Last, M. Schulte, Second order properties and central limit theorems for geometric functionals of Boolean models. Ann. Appl. Probab. 26 , 73-135 (2016)
60. D. Hug, G. Last, W. Weil, Polynomial parallel volume, convexity and contact distributions of random sets. Probab. Theory Relat. Fields 135 , 169-200 (2006)


<!-- p:53 -->


1

61. D. Hug, M. Reitzner, R. Schneider, The limit shape of the zero cell in a stationary Poisson hyperplane tessellation. Ann. Probab. 32 , 1140-1167 (2004)
62. D. Hug, R. Schneider, Asymptotic shapes of large cells in random tessellations. Geom. Funct. Anal. 17 , 156-191 (2007)
63. T. Huiller, Random covering of the circle: the size of the connected components. Adv. Appl. Probab. 35 , 563-582 (2003)
64. A. Hunt, R. Ewing, B. Ghanbarian, Percolation theory for flow in porous media , 3rd edn. Lecture Notes in Physics, vol. 880 (Springer, Cham, 2014)
65. S. Janson, Random coverings in several dimensions. Acta Math. 156 , 83-118 (1986)
66. E.T. Jaynes, The well-posed problem. Found. Phys. 3 , 477-492 (1973)
67. D.G. Kendall, Foundations of a Theory of Random Sets. Stochastic Geometry (A Tribute to the Memory of Rollo Davidson) (Wiley, London, 1974), pp. 322-376
68. M.G. Kendall, P.A.P. Moran, Geometrical Probability (Charles Griffin, London, 1963)
69. J.F.C. Kingman, Random secants of a convex body. J. Appl. Probab. 6 , 660-672 (1969)
70. J.F.C. Kingman, Poisson Processes (Clarendon Press, Oxford, 1993)
71. D.A. Klain, G.-C. Rota, Introduction to Geometric Probability (Cambridge University Press, Cambridge, 1997)
72. A.N. Kolmogorov, Grundbegriffe der Wahrscheinlichkeitsrechnung (Springer, Berlin, 1933)
73. G. Last, M. Penrose, Lectures of the Poisson Process (Cambridge University Press, Cambridge, 2017)
74. W. Lefebvre, T. Philippe, F. Vurpillot, Application of Delaunay tessellation for the characterization of solute-rich clusters in atom probe tomography. Ultramicroscopy 111 , 200-206 (2011)
75. J.-F. Marckert, The probability that n random points in a disk are in convex position. Braz. J. Probab. Stat. 31 (2), 320-337 (2017)
76. K.Z. Markov, C.I. Christov, On the problem of heat conduction for random dispersions of spheres allowed to overlap. Math. Models Methods Appl. Sci. 2 , 249-269 (1992)
77. B. Matérn, Spatial variation: Stochastic models and their application to some problems in forest surveys and other sampling investigations. Meddelanden Fran Statens Skogsforskningsinstitut, vol. 49, Stockholm (1960)
78. Matheron, G.: Random Sets and Integral Geometry . Wiley Series in Probability and Mathematical Statistics (Wiley, New York, 1975)
79. J. Mecke, Stationäre zufällige Masse auf lokalkompakten Abelschen Gruppen. Z. Wahrscheinlichkeitstheorie und Verw. Gebiete 9 , 36-58 (1967)
80. J. Mecke, On the relationship between the 0-cell and the typical cell of a stationary random tessellation. Pattern Recogn. 32 , 1645-1648 (1999)
81. R. Meesters, R. Roy, Continuum Percolation (Cambridge University Press, New York, 1996)
82. J.L. Meijering, Interface area, edge length and number of vertices in crystal aggregates with random nucleation. Philips Res. Rep. 8 , 270-90 (1953)
83. R.E. Miles, Random polygons determined by random lines in a plane I. Proc. Natl. Acad. Sci. U S A 52 , 901-907 (1964)
84. R.E. Miles, Random polygons determined by random lines in a plane II. Proc. Natl. Acad. Sci. U S A 52 , 1157-1160 (1964)
85. R.E. Miles, The random division of space. Suppl. Adv. Appl. Probab. 4 , 243-266 (1972)
86. R.E. Miles, The various aggregates of random polygons determined by random lines in a plane. Adv. Math. 10 , 256-290 (1973)
87. R.E. Miles, Estimating aggregate and overall characteristics from thich sections by transmission microscopy. J. Microsc. 107 , 227-233 (1976)
88. J. Møller, Random tessellations in R d . Adv. Appl. Probab. 21 , 37-73 (1989)
89. J. Møller, Random Johnson-Mehl tessellations. Adv. Appl. Probab. 24 , 814-844 (1992)
90. J. Møller, Lectures on Random Voronoi Tessellations . Lecture Notes in Statistics, vol. 87 (Springer, New York, 1994)
91. A. Müller, D. Stoyan, Comparison Methods for Stochastic Models and Risks . Wiley Series in Probability and Statistics (Wiley, Chichester, 2002)


<!-- p:54 -->


92. W. Nagel, V. Weiss, Crack STIT tessellations: characterization of stationary random tessellations stable with respect to iteration. Adv. Appl. Probab. 37 , 859-883 (2005)
93. J. Neveu, Processus ponctuels, in École d'été de Probabilités de Saint-Flour . Lecture Notes in Mathematics, vol. 598 (Springer, Berlin, 1977), pp. 249-445
94. New Advances in Geostatistics. Papers from Session Three of the 1987 MGUS Conference held in Redwood City, California, April 13-15, 1987 . Mathematical Geology, vol. 20 (Kluwer Academic/Plenum Publishers, Dordrecht, 1988), pp. 285-475
95. New Perspectives in Stochastic Geometry , ed. by W.S. Kendall, I. Molchanov (Oxford University Press, Oxford, 2010)
96. C. Palm, Intensitätsschwankungen im Fernsprechverkehr. Ericsson Technics 44 , 1-189 (1943)
97. M. Penrose, On a continuum percolation model. Adv. Appl. Probab. 23 , 536-556 (1991)
98. M. Penrose, Non-triviality of the vacancy phase transition for the Boolean model (2017). https://arxiv.org/abs/1706.02197
99. R.E. Pfiefer, The historical development of J. J. Sylvester's four point problem. Math. Mag. 62 , 309-317 (1989)
100. H. Poincaré, Calcul des probabilités (Gauthier-Villars, Paris, 1912)
101. J. Quintanilla, S. Torquato, Clustering in a continuum percolation model. Adv. Appl. Probab. 29 , 327-336 (1997)
102. C. Redenbach, On the dilated facets of a Poisson-Voronoi tessellation. Image Anal. Stereol. 30 , 31-38 (2011)
103. M. Reitzner, Stochastical approximation of smooth convex bodies. Mathematika 51 , 11-29 (2004)
104. M. Reitzner, Central limit theorems for random polytopes. Probab. Theory Relat. Fields 133 , 483-507 (2005)
105. M. Reitzner, The combinatorial structure of random polytopes. Adv. Math. 191 , 178-208 (2005)
106. M. Reitzner, Random polytopes, in New Perspectives in Stochastic Geometry , ed. by W.S. Kendall, I. Molchanov (Oxford University Press, Oxford, 2010), pp. 45-76
107. A. Rényi, R. Sulanke, Über die konvexe Hülle von n zufällig gewählten Punkten. Z. Wahrscheinlichkeitsth. verw. Geb. 2 , 75-84 (1963)
108. A. Rényi, R. Sulanke, Über die konvexe Hülle von n zufällig gewählten Punkten. II. Z. Wahrscheinlichkeitsth. verw. Geb. 3 , 138-147 (1964)
109. R. Schneider, Convex Bodies: The Brunn-Minkowski Theory (Cambridge University Press, Cambridge, 1993)
110. L.A. Santaló, Integral Geometry and Geometric Probability . Encyclopedia of Mathematics and its Applications, vol. 1 (Addison-Wesley, Reading, 1976)
111. R. Schneider, Random hyperplanes meeting a convex body. Z. Wahrsch. Verw. Gebiete 61 , 379-387 (1982)
112. R. Schneider, Integral geometric tools for stochastic geometry, in Stochastic Geometry , ed. by W. Weil. Lectures Given at the C.I.M.E. Summer School held in Martina Franca. Lecture Notes in Mathematics, vol. 1892 (Springer, Berlin, 2007), pp. 119-184
113. R. Schneider, W. Weil, Stochastic and Integral Geometry (Springer, Berlin, 2008)
114. R. Schneider, J.A. Wieacker, Random polytopes in a convex body. Z. Wahrsch. Verw. Gebiete 52 , 69-73 (1980)
115. J. Serra, Image Analysis and Mathematical Morphology (Academic, London, 1984)
116. L.A. Shepp, Covering the circle with random arcs. Isr. J. Math. 11 , 328-345 (1972)
117. A.F. Siegel, Random space filling and moments of coverage in geometrical probability. J. Appl. Probab. 15 , 340-355 (1978)
118. A.F. Siegel, L. Holst, Covering the circle with random arcs of random sizes. J. Appl. Probab. 19 , 373-381 (1982)
119. H. Solomon, Geometric Probability. CBMS-NSF Regional Conference Series in Applied Mathematics, vol. 28 (SIAM, Philadelphia, 1978)
120. J. Steiner, Über parallele Flächen. Monatsber. Preuss. Akad. Wiss., Berlin (1840), pp. 114118


<!-- p:55 -->


1

121. W.L. Stevens, Solution to a geometrical problem in probability. Ann. Eugenics 9 , 315-320 (1939)
122. D. Stoyan, Applied stochastic geometry: a survey. Biometrical J. 21 , 693-715 (1979)
123. J.J. Sylvester, Problem 1491. The Educational Times, London (April, 1864)
124. P. Valtr, Probability that n random points are in convex position. Discret. Comput. Geom. 13 , 637-643 (1995)
125. P. Valtr, The probability that n random points in a triangle are in convex position. Combinatorica 16 , 567-573 (1996)
126. V.H. Vu, Sharp concentration of random polytopes. Geom. Funct. Anal. 15 , 1284-1318 (2005)
127. W. Weil, Point processes of cylinders, particles and flats. Acta Appl. Math. 9 , 103-136 (1987)
128. V. Weiss, R. Cowan, Topological relationships in spatial tessellations. Adv. Appl. Probab. 43 , 963-984 (2011)
129. J.G. Wendel, A problem in geometric probability. Math. Scand. 11 , 109-111 (1962)
130. W.A. Whitworth, Choice and Chance (D. Bell, Cambridge, 1870)
131. F. Willot, D. Jeulin, Elastic behavior of composites containing Boolean random sets of inhomogeneities. Int. J. Eng. Sci. 47 , 313-324 (2009)


<!-- p:56 -->


## Chapter 2 Understanding Spatial Point Patterns Through Intensity and Conditional Intensities

Jean-François Coeurjolly and Frédéric Lavancier

Abstract This chapter deals with spatial statistics applied to point patterns. As well as in many specialized books, spatial point patterns are usually treated elaborately in books devoted to spatial statistics or stochastic geometry. Our aim is to propose a different point of view as we intend to present how we can understand and analyze a point pattern through intensity and conditional intensity functions. We present these key-ingredients theoretically and in an intuitive way. Then, we list some of the main spatial point processes models and provide their main characteristics, in particular, when available the form of their intensity and conditional intensity functions. Finally, we provide a non exhaustive list of statistical methodologies to estimate these functions and discuss the pros and cons of each method.

### 2.1 Introduction

Spatial point patterns arise in a broad range of applications. We are faced with such data for instance when we want to model the locations of trees in a forest, the locations of disease cases in a region, the locations of cells in a biological tissue, the locations of sunspots on the surface of the sun, the fixations of the retina (acquired with an eye-tracker) superimposed on an image or video a subject is looking at, etc. With the ability to acquire spatial data, the number of applications is increasing and the amount of data is becoming huge.

The objective of this chapter is to analyze spatial point processes through the notion of intensity. The word intensity here has to be understood in a very large sense, since it can be a simple intensity function, often interpreted as the local probability to observe a point at a fixed location, or a conditional intensity function.

J.-F. Coeurjolly ( envelopeback )

Université du Québec à Montréal, Département de Mathématiques, Montréal, QC, Canada e-mail: coeurjolly.jean-francois@uqam.ca

F. Lavancier

Université de Nantes, Laboratoire de Mathématiques Jean Leray, Nantes, France

[e-mail: frederic.lavancier@univ-nantes.fr](mailto:frederic.lavancier@univ-nantes.fr)

©Springer Nature Switzerland AG 2019

<!-- p:57 -->


Again, the term conditional intensity can gather several concepts: the intensity of the process given that the process has a point at the location x (or more generally n points at x 1 , . . . , xn ), or the intensity of the process given that the rest of the configuration is fixed.

Section 2.2 presents the main notation of the paper, some background on spatial point processes (general definition, characterization of the distribution), and specifically the concepts of intensity functions, Palm intensities and Papangelou conditional intensities for a spatial point process. These characteristics are introduced from a theoretical and intuitive point of view. In Sect. 2.3, we review classical models of spatial point processes: Poisson point processes, Gibbs point processes, Cox processes and determinantal point processes. This list is not exhaustive but these four classes are clearly the main models used in applications to model aggregation or repulsiveness in a point pattern. For these models, we state their main properties and report, when available, the form of intensity, Palm intensity and Papangelou conditional intensity functions.

Sections 2.4 and 2.5 are devoted to statistics. In Sect. 2.4 we focus on the intensity function and present different methodologies to estimate it. We first consider the case where this function is constant (in which case the point process is assumed to be stationary). In the inhomogeneous case, we first consider the non parametric estimation of the intensity. Then, and more intensively, we review a few methods designed to estimate a parametric form of the intensity function. The presentation is not exhaustive but gathers the main methods, for which we try to give the pros and cons for their practical use. Section 2.5 focuses on the estimation of conditional intensities and especially on the Papangelou conditional intensity and, to a lesser extent, on the one-point Palm intensity. Our purpose is here again to provide the reader the key-ingredients of each method, its advantages and drawbacks. Numerical aspects concerning the methods of Sects. 2.4 and 2.5 are briefly discussed and some illustrations are provided.

Spatial point pattern analysis constitutes the topic of many specialized books. Our aim in this chapter is to propose a different way of reading. Most of the material presented in this chapter can be found in the following books or reviews (see also the references cited in Sects. 2.4 and 2.5). For theoretical and methodological aspects, we refer the reader to Daley and Vere-Jones [28], Møller and Waagepetersen [58] and to Illian et al. [45]; see also the recent reviews by Møller and Waagepetersen [59, 60]. The reader interested in numerical and computational aspects and who simply wants to analyze spatial point patterns with R is definitely invited to read the complete and excellent book by Baddeley et al. [5]. To obtain a broader perspective, the interested reader is referred to the earliest book by Ripley [67], Kingman's monograph on Poisson processes [48], Lieshout's work on Markov models [76], the accessible introduction by Diggle [35], or the work of the American school as exemplified by Cressie [25], Cressie and Wikle [26], see also the connections to random sets and random measures as presented in Chiu et al. [12].


<!-- p:58 -->


### 2.2 Intensity and Conditional Intensity Functions

#### 2.2.1 Definition and Theoretical Characterization of a Spatial Point Process

In this chapter, we consider spatial point processes in R d . For ease of exposition, we view a point process as a random locally finite subset X of a Borel set S ⊆ R d , d ≥ 1. For readers interested in measure theoretical details, we refer to e.g. [58] or [28], or to Chap. 5 by David Dereudre. This setting implies the following facts. First, we consider simple point processes (two points cannot occur at the same location). Second, we exclude manifold-valued point processes (like circular or spherical point processes), spatio-temporal point processes and marked point processes, even if most of the concepts and methodologies presented hereafter exist or can be straightforwardly adapted in such contexts.

We denote by X B = X ∩ B the restriction of X to a set B ⊆ S and by | B | the volume of any bounded B ⊂ S . Local finiteness of X means that X B is finite almost surely (a.s.), that is the number of points N(B) of X B is finite a.s., whenever B is bounded. We let N stand for the state space consisting of the locally finite subsets (or point configurations) of S . For x ∈ N , we let | x | denote the number of elements of x . Furthermore, B 0 is the family of all bounded Borel subsets of S .

The counting variables N(B) = | X ∩ B | for B ∈ B 0 play a central role in the characterization, modelling and analysis of spatial point patterns. The distribution of X is uniquely determined by the joint distribution of N(B 1 ), . . . , N(Bm ) for any B 1 , . . . , Bm ∈ B 0 and any m ≥ 1. Surprisingly, the distribution is also equivalently determined by its void probabilities, i.e. by the probabilities P ( X K = ∅ ) = P (N(K) = 0 ), K ⊆ S compact, see again e.g. [28] for a proof of this result.

The reference model is the Poisson point process often defined as follows.

Definition 2.1 Let ρ be a locally integrable function on S . A point process X satisfying the following statements is called the Poisson point process on S with intensity function ρ :

- for any m ≥ 1, and for any disjoint and bounded B 1 , . . . , Bm ⊂ S , the random variables X B 1 , . . . , X Bm are independent;
- N(B) follows a Poisson distribution with parameter ∫ B ρ(u) d u for any bounded B ⊂ S .

It is easily checked that the void probabilities of a Poisson point process are given by P ( X K = ∅ ) = exp ( - ∫ K ρ(u) d u) for any compact set K ⊂ S . We also have that, for any B ∈ B 0 and any non-negative measurable function h on { x ∩ B | x ∈ N }

$$E h ( X _ { B } ) = \sum _ { n = 0 } ^ { \infty } \frac { \exp ( - | B | ) } { n ! } \int _ { B } \dots \int _ { B } h ( \{ u _ { 1 } , \dots , u _ { n } \} ) \rho ( u _ { 1 } ) \dots \rho ( u _ { n } ) d u _ { 1 } \dots d u _ { n } ,$$

where for n = 0 the term is read as exp ( -| B | )h( ∅ ) .


<!-- p:59 -->


Next sections will provide additional properties of Poisson point processes and in particular will make clearer why this model generates points without any interaction.

The nice theoretical characterization of a general spatial point process X does not help to define new models and/or to understand interaction between points. Next sections will present more useful ways of analyzing the dependence between points. We will review the concept of intensity function and conditional intensities (actually Palm intensities and Papangelou conditional intensities). There are clearly other ways of characterizing and understanding the interaction in a point pattern. Some of them are directly based on intensities like the pair correlation function (see Sect. 2.2.2). But most of them are not: e.g. the Ripley's K function, the L -function or distance based summary statistics like the F - G - and J -functions. We refer the interested reader to such summary statistics to [45, 58-60].

#### 2.2.2 Moment Measures Factorial Moment Measures and Intensity Functions

For n = 1 , 2 , . . . and Bi ∈ B 0, the n -th order moment measure μ (n) and the n -th order factorial moment measure α (n) are defined by

$$\mu ^ { ( n ) } ( B _ { 1 } \times B _ { 2 } \times \dots \times B _ { n } ) = E \sum _ { u _ { 1 } , \dots , u _ { n } \in \mathbb { X } } 1 ( u _ { 1 } \in B _ { 1 } , \dots , u _ { n } \in B _ { n } )$$

$$\alpha ^ { ( n ) } ( B _ { 1 } \times B _ { 2 } \times \dots \times B _ { n } ) = E \sum _ { u _ { 1 } , \dots , u _ { n } \in X } ^ { \neq } 1 ( u _ { 1 } \in B _ { 1 } , \dots , u _ { n } \in B _ { n } ) ,$$

where 1 ( · ) denotes the indicator function and ̸= over the summation sign means that u 1 , . . . , un are pairwise distinct. We focus on α (n) in the following which is clearly more useful. If α (n) has a density ρ (n) with respect to the Lebesgue measure, ρ (n) is called the n -th order joint intensity function and is determined up to a Lebesgue null set. Therefore, we can assume that ρ (n) (u 1 , . . . , un) is invariant under permutations of u 1 , . . . , un , and we need only to consider the case where u 1 , . . . , un ∈ S are pairwise distinct. Then ρ (n) (u 1 , . . . , un) d u 1 · · · d un can be interpreted as the approximate probability for X having a point in each of infinitesimally small regions around u 1 , . . . , un of volumes d u 1 , . . . d un , respectively. We also write ρ(u) for the intensity function ρ ( 1 ) (u) . The Campbell-Mecke theorem gives an integral representation of ρ (n) : for any function h such that | h | ρ (n) is integrable with respect to the Lebesgue measure on S n , then

$$E \sum _ { u _ { 1 } , \dots , u _ { n } \in \mathbf X } ^ { \neq } h ( u _ { 1 } , \dots , u _ { n } ) = \int _ { S } \dots \int _ { S } h ( u _ { 1 } , \dots , u _ { n } ) \rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) d u _ { 1 } \cdots d u _ { n } .$$


<!-- p:60 -->


If X is a Poisson point process on S with intensity function ρ , it is straightforwardly seen that the n -th order intensity function satisfies

$$\rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) = \prod _ { i = 1 } ^ { n } \rho ( u _ { i } ) , \ \forall u _ { 1 } , \dots , u _ { n } \in S .$$

From this, when n = 2 it is natural to focus on the pair correlation function, which is the function g : S × S → R + given for any u, v ∈ S such that ρ(u)ρ(v) &gt; 0 (otherwise we set g(u, v) = 0) by

$$g ( u , v ) = \frac { \rho ^ { ( 2 ) } ( u , v ) } { \rho ( u ) \rho ( v ) } .$$

The pair correlation function gives ideas on how a point process X deviates from the Poisson case since in this situation g(u, v) = 1, ∀ u, v ∈ S .

At this stage, it is pertinent to recall that when S = R d , a point process X is said to be stationary (respectively isotropic) if its distribution is invariant under translations (respectively under rotations). In such a case the intensity function is necessarily constant, and the pair correlation function g depends through ρ ( 2 ) only on u - v when X is stationary and on ‖ u - v ‖ when X is isotropic. Point process models with an inhomogeneous intensity function and a pair correlation function invariant by translation are called second-order reweighted stationary point processes (see e.g. [58]). This class of processes is often considered to derive asymptotic results for parametric inference methods.

Figure 2.1 illustrates this section and reports intensity function for homogeneous and inhomogeneous models and for different classes of point processes. From Fig. 2.1a-c, we clearly see what homogeneity (i.e. constant intensity) means and that this notion is independent of the fact that the points interact with each other or not. Figure 2.1d-i show that more points are observed when the intensity function is high.

#### 2.2.3 Palm Distributions and Palm Intensities

For any measurable F ⊆ N , define the n -th order reduced Campbell measure C (n) ! as the measure on S n × N given by

$$C ^ { ( n ) ! } ( B _ { 1 } \times B _ { 2 } \times \cdots \times B _ { n } \times F ) \\ = E \sum _ { x _ { 1 } , \dots , x _ { n } \in X } 1 ( x _ { 1 } \in B _ { 1 } , \dots , x _ { n } \in B _ { n } , X \ \{ x _ { 1 } , \dots , x _ { n } \} \in F ) .$$


<!-- p:61 -->


Fig. 2.1 Realization of a Poisson point process ( a ), ( d ), ( g ), a log-Gaussian Cox process ( b ), ( e ), ( h ) and a determinantal point process ( c ), ( f ), ( i ). The intensity is constant for ( a )-( c ) and equals 200. For ( d )-( f ), the intensity has the form log ρ cubic (u) = β + u 1 + u 3 1 / 2. The latent image corresponds to the map of ρ cubic . For ( g )-( i ), we use covariates accompanying the dataset bei (giving locations of a specific species of trees) of the R package spatstat . These covariates correspond to the elevation and slope of elevation fields of a part of the forest in Barro Colorado Island. The domain of observation is W bei = [ 0 , 1000 ] × [ 0 , 500 ] . The model for the intensity is log ρ grad ( u ) = β + . 5 z(u) where z(u) is the slope of elevation at location u . The points are superimposed to the 3-dimensional map of the elevation field. The parameter β is adjusted to get E N(W) = 200 for ( d )-( f ) and 800 for ( g )-( i ); the latent Gaussian field defining the LGCP model has an exponential covariance function with variance 2 and scale parameter 0.02; the kernel defining the DPP is a Gaussian kernel with parameters 0.035 for ( c ) and 0.025 for ( f ) and ( i ). LGCPs and DPPs are presented in detail in Sects. 2.3.3.1 and 2.3.4

Note that C (n) ! ( · × F) , as a measure on S n , is absolutely continuous with respect to α (n) , with a density P ! x 1 ,...,xn (F) which is determined up to an α (n) null set, and α (n) (B 1 × · · · × Bn) = C (n) ! (B 1 × B 2 × · · · × Bn × N ) . By the socalled Campbell-Mecke formula/theorem, we can assume that P ! x 1 ,...,xn ( · ) is a point process distribution on N , called the n -th order reduced Palm distribution given x 1 , . . . , xn (see e.g. [29]). We denote by X ! x 1 ,...,xn a point process distributed according to P ! x 1 ,...,xn . Again we need only to consider the case where x 1 , . . . , xn are pairwise distinct. Then P ! x 1 ,...,xn can be interpreted as the conditional distribution of X \ { x 1 , . . . , xn } given that x 1 , . . . , xn ∈ X .


<!-- p:62 -->


If ρ (n) exists, then by standard measure theoretical arguments we obtain the extended Campbell-Mecke formula. For any non-negative function h defined on S n × N

$$E \sum _ { x _ { 1 } , \dots , x _ { n } \in X } ^ { \neq } h ( x _ { 1 } , \dots , x _ { n } , X \ \{ x _ { 1 } , \dots , x _ { n } \} ) \\ = \int _ { S } \cdots \int _ { S } E h ( x _ { 1 } , \dots , x _ { n } , X _ { x _ { 1 } , \dots , x _ { n } } ^ { ! } ) \rho ^ { ( n ) } ( x _ { 1 } , \dots , x _ { n } ) d x _ { 1 } \cdots d x _ { n } .$$

Suppose ρ (m + n) exists for an m ≥ 1 and n ≥ 1. Then, for pairwise distinct u 1 , . . . , um, x 1 , . . . , xn ∈ S , it follows easily by expressing α (m + n) as an expectation of the form (2.3) that X ! x 1 ,...,xn has m -th order joint intensity function

$$\rho _ { x _ { 1 } , \dots , x _ { n } } ^ { ( m ) } ( u _ { 1 } , \dots , u _ { m } ) = \begin{cases} \frac { \rho ^ { ( m + n ) } ( u _ { 1 } , \dots , u _ { m } , x _ { 1 } , \dots , x _ { n } ) } { \rho ^ { ( n ) } ( x _ { 1 } , \dots , x _ { n } ) } & \text {if } \rho ^ { ( n ) } ( x _ { 1 } , \dots , x _ { n } ) > 0 , \\ 0 & \text {otherwise.} \end{cases}$$

We also write ρx 1 ...,xn for the intensity function ρ ( 1 ) x 1 ...,xn . The function ρ (m) x 1 ,...,xn is called the m -th order n -point Palm intensity. Obviously, when X is a Poisson point process, we have the equality ρ (m) x 1 ,...,xn (u 1 , . . . , um) = ∏ m i = 1 ρ(ui) ; the knowledge that ' x 1 , . . . , xn ∈ X ' does not bring any information on the probability to observe points at u 1 , . . . , um .

When m = n = 1, we speak of the one-point Palm intensity function or even simpler the Palm intensity function. We can check that for any pairwise distinct u, x ∈ S , ρx(u) = ρ(u)g(u, x) . From that, we observe first, that the Palm intensity function ρx is independent on x for any x ∈ S if and only if g = 1 (note that this is not equivalent to say that X is a Poisson point process). Second, if X is a stationary point process (resp. isotropic point process), the Palm intensity ρx( · ) depends only on x -· (respectively on ‖ x -·‖ ).

Equation (2.4) provides a natural interpretation of Palm intensities: ρ (m) x 1 ,...,xn (u 1 , . . . , um) d u 1 . . . d um can be interpreted as the approximate probability for X having a point in each of infinitesimally small regions around x 1 , . . . , xn, u 1 , . . . , um of volumes d x 1, . . . , d xn , d u 1,. . . , d um respectively divided by the approximate probability for X having a point in each of infinitesimally small regions around x 1 , . . . , xn of volumes d x 1, . . . , d xn . In other words, this is also the approximate conditional probability for X having a point in each of infinitesimally small regions around u 1 , . . . , um of volumes d u 1, . . . , d um conditionnally on X having a point in each of infinitesimally small regions around x 1 , . . . , xn of volumes d x 1, . . . , d xn .

Figure 2.2 illustrates this section and plots, for a homogeneous and inhomogeneous LGCP, the one-point Palm intensity function ρx(u) for some fixed point x represented by a cross. This class of models is presented in details in Sect. 2.3.3.1. When the LGCP is defined through an exponential (more generally a positive) covariance function, as made in Fig. 2.2, the model produces attractive patterns. The one-point Palm intensity attests this characteristic, as it is high in the neighbourhood of the fixed point x .


<!-- p:63 -->


Fig. 2.2 Point patterns represented in ( a ) (respectively ( b, c )) correspond to the LGCP from Fig. 2.1b, and e respectively (see Fig. 2.1 for details on the parameters of the LGCP). The latent image corresponds to the Palm intensity function ρx(u) where x is the point represented by a cross ( × ) and located at the center of the square sub-window of each plot. For ( a ), ρx (u) = 200 g(u, x) while for ( b, c ), ρx(u) = ρ cubic (u)g(u, x) ; see Fig. 2.1 and Sect. 2.3.3.1 for details on ρ cubic and g . Figure ( d )-( f ) are zooms of the square sub-windows (with side-length 0.2) depicted in ( a ), ( b ) and ( c )

#### 2.2.4 Papangelou Conditional Intensities

Let Z be a unit rate Poisson point process on S and assume, first, that S is bounded ( | S | &lt; ∞ ). We say that a spatial point process X has a density f if the distribution of X is absolutely continuous with respect to the one of Z and with density f . Thus, for any non-negative measurable function h defined on N , E h( X ) = E (f ( Z )h( Z )) . By (2.1)

$$E h ( X ) = \sum _ { n = 0 } ^ { \infty } \frac { \exp ( - | S | ) } { n ! } \int _ { B } \dots \int _ { B } h ( \{ u _ { 1 } , \dots , u _ { n } \} ) f ( \{ u _ { 1 } , \dots , u _ { n } \} ) d u _ { 1 } \dots d u _ { n } .$$


<!-- p:64 -->


Now, suppose that f is hereditary , i.e., for any pairwise distinct u 0 , u 1 , . . . , un ∈ S , f( { u 1 , . . . , un } ) &gt; 0 whenever f( { u 0 , u 1 , . . . , un } ) &gt; 0. We can then define the so-called n -th order Papangelou conditional intensity by

$$\lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , \mathbf x ) = f ( \mathbf x \cup \{ u _ { 1 } , \dots , u _ { n } \} ) / f ( \mathbf x )$$

for pairwise distinct u 1 , . . . , un ∈ S and x ∈ N \ { u 1 , . . . , un } , setting 0 / 0 = 0. By the interpretation of f , λ (n) (u 1 , . . . , un, x ) d u 1 · · · d un can be considered as the conditional probability of observing one event in each of the infinitesimally small balls Bi centered at ui with volume d ui , conditional on that X outside ∪ n i = 1 Bi agrees with x . When n = 1, we simply write λ(u, x ) and call this function the Papangelou conditional intensity of u given x . When f is hereditary, there is a oneto-one correspondence between f and λ .

Because the notion of density for Z when S = R d makes no sense, the Papangelou conditional intensity cannot be defined through a ratio of densities in R d . But it still makes sense as the n -th order Papangelou conditional intensity can actually be defined at the Radon-Nykodym derivative of P ! x 1 ,...,xn with respect to P (see [28]).

APoisson point process on S with intensity function ρ has n -th order Papangelou conditional intensity equal to

$$\lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , x ) = \prod _ { i = 1 } ^ { n } \rho ( u _ { i } ) ,$$

shedding again light on the fact that there is no interaction between points in a pattern generated by a Poisson point process.

Without further details, we mention the celebrated Georgii-Nguyen-Zessin formula (see [38, 62]), which states that for any h : S n × N → R (such that the following expectations are finite)

$$E \sum _ { u _ { 1 } , \dots , u _ { n } \in X } ^ { \neq } h ( u _ { 1 } , \dots , u _ { n } , X \ \{ u _ { 1 } , \dots , u _ { n } \} ) \\ = \int _ { S } \dots \int _ { S } E \left ( h ( u _ { 1 } , \dots , u _ { n } , X ) \lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , X ) \right ) d u _ { 1 } \dots d u _ { n } .$$

By identification of (2.2) and (2.7), we see a link between the n -th order intensity and the n -th order Papangelou conditional intensity: for any pairwise distinct u 1 , . . . , un ∈ S

$$\rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) = E \left ( \lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , \mathbf X ) \right ) .$$

We will return to the GNZ equation formula in connection to Gibbs processes in Sects. 2.3 and 2.5.


<!-- p:65 -->


Figure 2.3 illustrates this section. For three different patterns exhibiting either repulsiveness (Fig. 2.3a,b) or attraction (Fig. 2.3c), the right plots represent the Papangelou conditional intensity λ(u, x ) for all u ∈ W . Specifically, Fig. 2.3a depicts a realization of a Strauss hard-core model, a Gibbs model for which points are pushed to be at a distance δ apart and repel up to a distance R &gt; δ , see Sect. 2.3.2 for details. Figure 2.3b,c show realizations of an area-interaction Gibbs model, see again Sect. 2.3.2 for details, that produces repulsive (resp. attractive) patterns when the underlying parameter θ is negative (resp. positive). To interpret the right plots of Fig. 2.3, think of where a new point is likely to appear: clearly in areas where λ(u, x ) is high, i.e. in the white areas. Figure 2.3a is very pedagogical. We see that outside the balls with radius R centered in x , the Papangelou conditional intensity is constant, as expected. We also observe that a new point is forbidden within a distance δ to the point pattern. The Papangelou conditional intensity for an areainteraction point process is slightly more complex but the interpretation is similar: When θ &lt; 0, the repulsive case of Fig. 2.3b, a new point is likely to appear in the white areas, i.e. far from the points of x . This is the converse for the attractive case of Fig. 2.3c where a new point is likely to appear close to the points of x .

### 2.3 Examples on Standard Models of Spatial Point Processes

We describe in this section some widely used models of spatial point processes and we specify for each of them the intensities, Palm intensities and Papangelou conditional intensities, if these are explicitly known. Table 2.1 is a summary.

#### 2.3.1 Poisson Point Process

The Poisson point process on S has already been introduced in Definition 2.1 and some realizations are shown in Fig. 2.1. This is the model for independence of the location of the events. It is characterized by its intensity function ρ , from which we deduce, see Sect. 2.2, the n -th order intensity function

$$\rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) = \prod _ { i = 1 } ^ { n } \rho ( u _ { i } ) , \ \forall u _ { 1 } , \dots , u _ { n } \in S ,$$

the m -th order n -point Palm intensity function, given x 1 , . . . , xn in S ,

$$\rho _ { x _ { 1 } , \dots , x _ { n } } ^ { ( m ) } ( u _ { 1 } , \dots , u _ { m } ) = \prod _ { i = 1 } ^ { m } \rho ( u _ { i } ) , \quad \forall u _ { 1 } , \dots , u _ { m } \in S ,$$


<!-- p:66 -->


2

Fig. 2.3 Left plots: realization of point patterns in W from a Strauss hard-core model ( a ) and an area interaction point process ( b, c ). See Sect. 2.3.2 for a definition of these models. Right plots: Papangelou conditional intensity of the models, given the point pattern in the left hand side, see (2.12) and (2.13)

<!-- p:67 -->


Table 2.1 Intensity function ρ(u) , one-point Palm intensity ρx(u) and first order Papangelou conditional intensity λ(u, x ) for: a Poisson point process with intensity ρ ; A Gibbs model with energy function H and activity parameter z ; A log-Gaussian Cox process (LGCP) associated to a Gaussian random field with mean μ(u) and covariance c(u, v) ; A Neymann Scott process (NSP) where the clusters' centres have intensity κ , the mean number of points per cluster is γ and the dispersion kernel is k 0; A determinantal point process (DPP) with kernel C(u,v)

| Models   | ρ(u)                     | ρ x (u)                                   | λ(u, x )                            |
|----------|--------------------------|-------------------------------------------|-------------------------------------|
| Poisson  | ρ(u)                     | ρ(u)                                      | ρ(u)                                |
| Gibbs    | NA                       | NA                                        | z exp ( - (H( x ∪{ u } ) - H( x ))) |
| LGCP     | exp (μ(u) + c(u, u)/ 2 ) | exp (μ(u) + c(u, u)/ 2 + c(u, x))         | NA                                  |
| NSP      | κγ                       | κγ + γ ∫ R d k 0 (z)k 0 (x - u + z) d z   | NA                                  |
| DPP      | C(u, u)                  | C(u, u) -&#124; C(u, x) &#124; 2 /C(x, x) | NA in general                       |

The entries NA correspond to the cases where the formulas are not available in closed form

the one-point Palm intensity given x ∈ S

$$\rho _ { x } ( u ) = \rho ( u ) , \ \forall u \in S ,$$

and the n -th order Papangelou conditional intensity

$$\lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , x ) = \prod _ { i = 1 } ^ { n } \rho ( u _ { i } ) , \quad \forall u _ { 1 } , \dots , u _ { n } \in S , \, \forall x \in \mathcal { N } \ \{ u _ { 1 } , \dots , u _ { n } \} .$$

Note that the conditioning on x 1 , . . . , xn in the Palm intensity and the conditioning on x in the Papangelou conditional intensity have no effect on the form of these functions. Morever all joint intensities and joint conditional intensities reduce to a product form. These observations confirm the independence property of the Poisson point process.

It is worth emphasizing that the Poisson point process is the only model for which we have an explicit and tractable expression for all characteristics above.

#### 2.3.2 Gibbs Point Processes

Gibbs point processes have been widely treated in the literature. For a comprehensive presentation of Gibbs point processes as well as a detailed list of references, we refer to Chap.5 by David Dereudre in this volume. These processes are characterized by an energy function H (or Hamiltonian) that maps any finite point configuration to R ∪ {∞} . Specifically, if | S | &lt; ∞ , a Gibbs point process on S associated to H and with activity z &gt; 0 admits the following density with respect to the unit rate Poisson process:

$$f ( \mathbf x ) \, \infty \, z ^ { | \mathbf x | } e ^ { - H ( \mathbf x ) } ,$$


<!-- p:68 -->


2

where ∝ means 'proportional to'. This definition makes sense under some regularity conditions on H , typically non degeneracy ( H( ∅ ) &lt; ∞ ) and stability (there exists A ∈ R such that H( x ) ≥ A | x | for any x ∈ N ). Consequently, configurations x having a small energy H( x ) are more likely to be generated by a Gibbs point process than by a Poisson point process, and conversely for configurations having a high energy. In the extreme case where H( x ) = ∞ , then x cannot, almost surely, be the realization of a Gibbs point process associated to H .

If | S | = ∞ , the above definition does not make sense in general since H( x ) can be infinite or even undefined if | x | = ∞ . In this case a Gibbs point process is defined through its local specifications, which are the conditional densities on any bounded set Δ , given the outside configuration on Δ c , with respect to the unit rate Poisson process on Δ . These conditional densities take a similar form as in (2.8), where now the Hamiltonian H becomes a family of Hamiltonian functions HΔ that quantify the energy of x Δ given the outside configuration x Δ c . Some supplementary regularity assumptions on the family of HΔ 's are necessary to ensure the existence of a point process satisfying these local specifications. Again, we refer to Chap. 5 by David Dereudre for more details. The interpretation nonetheless remains similar: a (infinite) Gibbs point process associated to HΔ tends to favor configurations x Δ on Δ having a small value HΔ( x ) .

Gibbs point processes offer a great flexibility of modelling, depending on the choice of the energy function H that favors or penalizes some point patterns' features. This function can in particular encode inhibition between the points, or attraction, or even both inhibition and attraction depending on the distance between the points. Let us give two popular examples. They are defined hereafter for simplicity on a bounded set S , but their definition extends to S = R d , provided we carefully account for edge effects in the conditional specifications.

Strauss Hard-Core Model on a Bounded Set S This model is a particular case of a pairwise interaction model, for which

$$H ( x ) = \sum _ { \{ u , v \} \in \mathbf x } \phi ( u - v ) ,$$

where φ is a symmetric function called the pair potential. The potential of a hardcore Strauss model depends on some hardcore parameter δ ≥ 0, some interaction parameter θ ≥ 0 and some range of interaction R &gt; δ in the following way

$$\phi ( u ) & = \begin{cases} \infty & \text {if} \quad | u | < \delta , \\ \theta & \text {if} \quad \delta \leq | u | < R , \\ 0 & \text {if} \quad | u | \geq R . \end{cases} \\ \intertext { t h e p o t e n t i a l , $ this $ model only a l l w o w s }$$

As encoded in the potential, this model only allows configurations where all points are δ -apart. Moreover it penalizes configurations with too many pairs of points that are R -apart. This model thus generates inhibitive point patterns. A realization is shown in Fig. 2.3.


<!-- p:69 -->


Area-Interaction Model on a Bounded Set S The Hamiltonian H of the areainteraction process is defined for the radius R ≥ 0 and the interacting parameter θ ∈ R by

$$H ( x ) = \theta \left | \bigcup _ { u \in x } B ( u , R ) \right | , & & ( 2 . 1 1 ) \\ \intertext { h e a l l c e r t e d i n e r t a u t w i t h r a d i s u r $ R . $ D e pending o n t h e s i n g o f }$$

where B(u, R) is the ball centered at u with radius R . Depending on the sign of θ , this model yields inhibition or clustering. If θ &gt; 0, a small value of H( x ) is achieved if the union of balls in (2.11) has a small area, which happens when many balls intersect or equivalently if the points of x are close to each other. Conversely if θ &lt; 0, this model generates configurations with a large area in (2.11), which means that some inhibition occurs between the points to avoid intersections between the associated balls. Some realizations (in both cases) are represented in Fig. 2.3.

As illustrated in the above examples, Gibbs models provide a clear and interpretable way to introduce interactions between the points of a point pattern, these interactions being encoded in the energy function. Unfortunately, very few characteristics of a Gibbs process are explicitly known. The main reason is that the normalizing constant in (2.8) is in general intractable, making impossible the computation of the intensities and of the Palm intensities of a Gibbs process. However, from (2.6) and (2.8), this normalization cancels in the n -th order Papangelou conditional intensity to provide

$$\lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , \mathbf x ) = z \, e ^ { - ( H ( \mathbf x \cup \{ u _ { 1 } , \dots , u _ { n } \} ) - H ( \mathbf x ) ) } .$$

For instance, when n = 1, we obtain for a pair potential (2.9)

$$\lambda ( u , x ) = z \, e ^ { - \theta \sum _ { v \in \mathbf X } \phi ( v - u ) }$$

for all u ∈ S and x ∈ N such that H( x ) &lt; ∞ , while λ(u, x ) = 0 if H( x ) = ∞ . This becomes for the Strauss hard-core model (2.10), denoting by nR(u, x ) the number of R -closed neighbours of u in x ,

$$\lambda ( u , \mathbf x ) = z \, e ^ { - \theta n _ { R } ( u , \mathbf x ) }$$

if all points in x ∪{ u } are δ -apart and λ(u, x ) = 0 otherwise. For the area interaction model (2.11), we get

$$\lambda ( u , \mathbf x ) = z \, e ^ { - \theta \left ( \left | \bigcup _ { v \in \mathbf x ( u ) } B ( v , R ) \right | - \left | \bigcup _ { v \in \mathbf x } B ( v , R ) \right | \right ) } .$$


<!-- p:70 -->


#### 2.3.3 Cox Processes

Let (Λ(u))u ∈ S be a non-negative random field. A point process is a Cox process driven by Λ if conditional on Λ , it is a Poisson point process with intensity Λ . The existence is ensured if Λ is locally integrable almost surely, i.e. ∀ B ∈ B 0, ∫ B Λ(u) d u &lt; ∞ almost surely.

If the random field Λ is not a constant random variable over S , the realization of a Cox process generates clusters of points, located around the highest values of the realization of Λ .

In general, very few mathematical properties are available for a Cox process. For instance we easily obtain that the n -th order intensity function is

$$\rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) = E \left ( \prod _ { i = 1 } ^ { n } \Lambda ( u _ { i } ) \right )$$

but this expectation is in general not tractable. We focus below on two special cases of Cox processes, namely the log-Gaussian Cox processes (LGCP) and the shot noise Cox processes (SNCP) for which (2.14) become computable. On the other hand, the density of a Cox process on a bounded S ( | S | &lt; ∞ ) with respect to the unit rate Poisson process is

$$f ( x ) = E \left \{ \exp \left ( | S | - \int _ { S } \Lambda ( u ) d u \right ) \prod _ { u \in \mathbb { X } } \Lambda ( u ) \right \}$$

which is intractable, even for the LGCP and SNCP detailed below. Consequently the Papangelou conditional intensity is unknown for these models.

##### 2.3.3.1 Log-Gaussian Cox Processes

These processes correspond to the particular case Λ(u) = exp (Y(u)) , u ∈ S , where Y is a Gaussian random field with mean function μ(u) and covariance function c(u, v) . These models are often used for modelling spatially correlated latent uncertainty. Some realizations are shown in Figs. 2.1 and 2.2.

For an LGCP, (2.14) becomes tractable, see [61]. We obtain for n = 1 that the intensity function is given by

$$\rho ( u ) = \exp ( \mu ( u ) + c ( u , u ) / 2 ) , \quad \forall u \in S ,$$

and combined with the case n = 2, we deduce the pair correlation function

$$g ( u , v ) = \exp ( c ( u , v ) ) , \quad \forall u , v \in S .$$


<!-- p:71 -->


We have that g ≥ 1 if c(u, v) ≥ 0, confirming the clustering property of an LGCP. Note that this attractive interaction is controlled through the second order moment of Y , which is a global feature, and not through the local interaction between pairs of points, as it is the case for pairwise interaction Gibbs point process with the energy function. For this reason an LGCP is not a mechanistic model in the sense that it does not describe the physical process generating the points.

More generally, the n -th order intensity function writes

$$\rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) = \prod _ { i = 1 } ^ { n } \rho ( u _ { i } ) \prod _ { 1 \leq i < j \leq n } g ( u _ { i } , u _ { j } ) , \ \forall u _ { 1 } , \dots , u _ { n } \in S .$$

From (2.4), we further obtain the m -th order n -point Palm intensity function, given x 1 , . . . , xn in S ,

$$\rho _ { x _ { 1 } , \dots , x _ { n } } ^ { ( m ) } ( u _ { 1 } , \dots , u _ { m } ) = \prod _ { i = 1 } ^ { m } \rho _ { x _ { 1 } , \dots , x _ { n } } ( u _ { i } ) \prod _ { 1 \leq i < j \leq m } g ( u _ { i } , u _ { j } ) , \quad \forall u _ { 1 } , \dots , u _ { m } \in S ,$$

where

$$\rho _ { x _ { 1 } , \dots , x _ { n } } ( u ) = \rho ( u ) \prod _ { i = 1 } ^ { n } g ( u , x _ { i } ) , \quad \forall u \in S ,$$

corresponds to the case m = 1. In particular the one-point Palm intensity given x ∈ S is

$$\rho _ { x } ( u ) = \rho ( u ) g ( u , x ) , \quad \forall u \in S .$$

The Palm intensities can also be derived from a stronger result proved in [24], which establishes that the n -th order reduced Palm distribution of an LGCP, given x 1 , . . . , xn in S , is still an LGCP associated to the Gaussian field (Y(u) + ∑ n i = 1 c(u, xi ))u ∈ S .

##### 2.3.3.2 Shot Noise Cox Processes

They are Cox processes associated to

$$\Lambda ( u ) = \sum _ { ( c , \gamma ) \in \Phi } \gamma \, k ( c , u )$$

where Φ is a Poisson point process on S ×[ 0 , ∞ ) with intensity measure ζ and k is a kernel on S 2 , i.e. k(c, .) is a density function on S for all c ∈ S .


<!-- p:72 -->


2

An SNCP can be viewed as a Poisson cluster process where the random set of centres (or parents) consists in the set of c 's and k(c, .) stands for a dispersion density around the centre c . The intensity of each cluster is encoded in γ . From this point of view, unlike LGCPs, an SNCP is a mechanistic model that provides a clear interpretation of the generating process.

It is verified in [56, Proposition 1] that the first intensity function of an SNCP is

$$\rho ( u ) = \int \gamma \, k ( c , u ) d \zeta ( c , \gamma ) , \ \forall u \in S ,$$

and the pair correlation function writes

$$g ( u , v ) = 1 + \frac { \beta ( u , v ) } { \rho ( u ) \rho ( v ) } , \ \forall u , v \in S$$

$$\beta ( u , v ) = \int \gamma ^ { 2 } \, k ( c , u ) k ( c , v ) d \zeta ( c , \gamma ) ,$$

provided these integrals are finite. The fact that g ≥ 1 confirms the clustering property of an SNCP. We deduce the one-point Palm intensity given x ∈ S

$$\rho _ { x } ( u ) = \rho ( u ) g ( u , x ) , \quad \forall u \in S .$$

Higher order intensities and Palm intensities are less tractable.

A widely used class of SNCP is the class of Neymann Scott processes defined on S = R d . They correspond to the case k(c, u) = k 0 (u - c) , where k 0 is a density, and Φ = Φc × { γ } where γ &gt; 0 and Φc is a homogeneous Poisson process with intensity κ &gt; 0. So the point process of intensities is constant equal to γ and is independent of the locations of the centres. The resulting process is stationary. The Thomas process is the special case where k 0 is a zero-mean normal density, and the Matérn cluster process is the example where k 0 is a uniform density on a ball centered at the origin. For Neymann Scott processes the above formulae become

$$\rho ( u ) = \kappa \gamma , \quad \forall u \in \mathbb { R } ^ { d } ,$$

where

and given x ∈ R d ,

$$\rho _ { x } ( u ) = \kappa \gamma + \gamma \int _ { \mathbb { R } ^ { d } } k _ { 0 } ( z ) k _ { 0 } ( x - u + z ) d z , \quad \forall u \in \mathbb { R } ^ { d } .$$


<!-- p:73 -->


#### 2.3.4 Determinantal Point Processes

Determinantal point processes (DPPs) are models for inhibitive point patterns, introduced in their general form by Macchi [51]. We refer to [49] for their main statistical properties. They are defined through a kernel C which is a function from S × S to C . A point process is a DPP on S with kernel C if for any n , its n -th order intensity function takes the form

$$\rho ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } ) = \det [ C ] ( u _ { 1 } , \dots , u _ { n } ) ,$$

for every (u 1 , . . . , un) ∈ S n , where [ C ] (u 1 , . . . , un) denotes the matrix with entries C(ui, uj ) , 1 ≤ i, j ≤ n . Sufficient conditions for existence are that C be a continuous covariance function on R d × R d and further satisfies a spectral condition. In the homogeneous case where C(u,v) = C 0 (v - u) , this spectral condition is C 0 ∈ L 2 ( R d ) and F (C 0 ) ≤ 1 where F denotes the Fourier transform. In the inhomogeneous case, a sufficient condition is that there exists a covariance function C 0 as before such that C 0 (v - u) - C(u,v) remains a covariance function.

Repulsiveness of a DPP is deduced from (2.16): by continuity of C and the determinant, ρ (n) (u 1 , . . . , un) tends to 0 whenever ui ≈ uj for some i ̸= j , showing that a DPP is unlikely to generate too close points. The intensity and the pair correlation of a DPP are easily deduced

$$\rho ( u ) = C ( u , u ) , \quad g ( u , v ) = 1 - \frac { | C ( u , v ) | ^ { 2 } } { C ( u , u ) C ( v , v ) } ,$$

and the repulsiveness property is confirmed by the fact that g ≤ 1. These two expressions also give a clear interpretation of the kernel C : the diagonal of C encodes the intensity of the process, while the off-diagonal encodes the interaction between two points of the process. Like for LGCPs, this interaction is only controlled globally through the second order moment of the process, so DPPs are not mechanistic models. Finally, a DPP cannot be extremely inhibitive. In particular, a DPP cannot include a hardcore distance δ (this is a consequence of [69], Corollary 1.4.13), a situation where all points are at least δ -apart. The most repulsive DPP (in a certain sense) is determined in [49] and [11], where it is demonstrated that DPPs can nonetheless model a large class of point patterns exhibiting inhibition. Realizations of DPPs where C is a Gaussian covariance function are represented in Fig. 2.1c, f, and i.

An appealing feature of DPPs is that many theoretical properties are available. In particular, by the definition (2.16), the n -th order intensity function is explicitly known. Further, the m -th order n -point Palm intensity function, given x 1 , . . . , xn in S , is deduced from (2.4) and (2.16) and becomes after some algebra (see [71] Corollary 6.6)

$$\rho _ { x _ { 1 } , \dots , x _ { n } } ^ { ( m ) } ( u _ { 1 } , \dots , u _ { m } ) = \det [ C _ { x _ { 1 } , \dots , x _ { n } } ] ( u _ { 1 } , \dots , u _ { m } ) , \quad \forall u _ { 1 } , \dots , u _ { m } \in S ,$$


<!-- p:74 -->


2

where

$$C _ { x _ { 1 } , \dots , x _ { n } } ( u , v ) = \frac { 1 } { \det [ C ] ( x _ { 1 } , \dots , x _ { n } ) } \det \left [ \begin{array} { c c c c } C ( u , v ) & C ( u , x _ { 1 } ) & \dots & C ( u , x _ { n } ) \\ C ( x _ { 1 } , v ) & C ( x _ { 1 } , x _ { 1 } ) & \dots & C ( x _ { 1 } , x _ { n } ) \\ \vdots & \vdots & \ddots & \vdots \\ C ( x _ { n } , v ) & C ( x _ { n } , x _ { 1 } ) & \dots & C ( x _ { n } , x _ { n } ) \end{array} \right ] .$$

.

This expression shows that the n -th order reduced Palm distribution of a DPP, given x 1 , . . . , xn , is still a DPP with kernel Cx 1 ,...,xn . In particular, the one-point Palm intensity given x ∈ S is

$$\rho _ { x } ( u ) = C ( u , u ) - \frac { | C ( u , x ) | ^ { 2 } } { C ( x , x ) } , \ \forall u \in S .$$

Concerning the n -th order Papangelou conditional intensity, its expression is

$$\lambda ^ { ( n ) } ( u _ { 1 } , \dots , u _ { n } , x ) = \det [ \tilde { C } ] ( x \cup \{ u _ { 1 } , \dots , u _ { n } \} ) / \det [ \tilde { C } ] ( x ) ,$$

which depends on a new kernel  ̃ C related to C by the integral equation

$$\tilde { C } ( u , v ) - \int _ { S } \tilde { C } ( u , t ) C ( t , v ) d t = C ( u , v ) , \quad \forall u , v \in S .$$

The solution  ̃ C is in general unknown and for this reason the Papangelou conditional intensity of a DPP does not straightforwardly follow from the knowledge of C . However, some approximations in the case where S is a rectangular region and C(u,v) = C 0 (v - u) are available, see [49].

### 2.4 Estimating the Intensity Function

In Sects. 2.4 and 2.5, we are given the realization of a spatial point process X defined on S . We will present very briefly asymptotic results. Asymptotics is understood as increasing-domain asymptotics. So, we assume that X is well-defined on R d and is observed in Wn , where (Wn)n ≥ 1 is a sequence of bounded regular domains with | Wn | → ∞ as n → ∞ . According to the problems, contexts and estimators, assumptions for the sequence (Wn)n ≥ 1 are different, but to ease the presentation think Wn as the domain [- n, n ] d . To lighten the text, we will also assume that the quantities used hereafter are well-defined; for instance, if an estimator has a variance depending on the pair correlation function g , it is intrinsically assumed that the second order intensity of X is well-defined.

In this section, we focus on estimating the intensity function. Three different settings will be considered: first, we consider the case when ρ is constant; second, the case where ρ is a d -dimensional function not specified by any parameter; third, the case where ρ is a function with a parametric form.


<!-- p:75 -->


Because the different methodologies often start from methodologies for the reference model, i.e. the Poisson process, we mention the following result. Let X be a Poisson point process with intensity function ρ defined on R d and observed in Wn , then X restricted to Wn admits a density w.r.t the unit rate Poisson process defined on Wn and the density, denoted by f , writes for x ∈ N

$$f ( x ) = \exp \left ( | W _ { n } | - \int _ { W _ { n } } \rho ( u ) d u \right ) \, \prod _ { u \in X } \rho ( u ) .$$

#### 2.4.1 Constant Intensity

##### 2.4.1.1 Poisson Case

When ρ is constant and X is a Poisson point process, the density reduces to f( x ) = exp ( | Wn | - ρ | Wn | )ρ | x | and the maximum likelihood estimator (MLE) of ρ is therefore ˆ ρ = N(Wn)/ | Wn | . It is of course an unbiased estimator of ρ , with variance ρ/ | Wn | and as n →∞ , | Wn | 1 / 2 ( ˆ ρ - ρ) → N( 0 , ρ) in distribution. To build asymptotic confidence intervals, the variance stabilizing transform is sometimes used. In this setting, this leads to | Wn | 1 / 2 ( √ ˆ ρ - √ ρ) → N( 0 , 1 ) in distribution. The MLE is, as expected, the optimal estimator, among unbiased estimators. To end this paragraph, we mention the work by Clausel et al. [14] which provides a Stein estimator of ρ . A Stein estimator is a biased estimator with mean-squared error smaller than the one of the MLE. The authors considered in particular the following estimator obtained as a small perturbation of ˆ ρ : assume here that | Wn | = B( 0 , 1 ) (the d -dimensional Euclidean ball)

$$\tilde { \rho } = \hat { \rho } - \gamma \, D _ { k } ( 1 - D _ { k } )$$

where γ is a real parameter and where Dk is the squared distance to zero of the k -th closest point to zero (set to 1 if k is larger than the number of observed points). Clausel et al. [14] showed that it is possible to adjust k and γ such that the meansquared error of  ̃ ρ is smaller than the one of ˆ ρ . Note that the bias of  ̃ ρ , depending on ρ , can in principle be estimated. However, the resulting 'debiased' estimator is not guaranteed to outperform the MLE in terms of mean-squared error.

##### 2.4.1.2 General Case

In the general case, the estimator ˆ ρ = N(Wn)/ | Wn | is the standard estimator: it actually corresponds to the estimator obtained from the following estimating equation

$$\sum _ { u \in X \cap W _ { n } } 1 - \int _ { W _ { n } } \rho d u = N ( W _ { n } ) - \rho | W _ { n } |$$


<!-- p:76 -->


2

an equation which is easily shown to be unbiased using (2.2), leading to an estimator that is also unbiased. Under mixing conditions on X and the assumption that X is a second-order reweighted stationary point process [44], have shown that | Wn | 1 / 2 ( ˆ ρ - ρ) → N( 0 , σ 2 ) where

$$\sigma ^ { 2 } = \rho + \rho ^ { 2 } \int _ { \mathbb { R } ^ { d } } ( g ( u , o ) - 1 ) d u ,$$

where o is the origin of R d . Equation (2.17) reveals an interesting fact: when g(u, v) &gt; 1 (respectively g(u, v) &lt; 1) for any u, v , i.e. for attractive (respectively repulsive) patterns, the asymptotic variance is larger (respectively smaller) than ρ , the asymptotic variance in the Poisson case. Heinrich and Prokešová [44] also provided the following estimator of σ 2 and established its asymptotic mean-squared error:

$$\widehat { \sigma } ^ { 2 } = \widehat { \rho } + \sum _ { u , v \in X \cap W _ { n } } \frac { \# } { | ( W _ { n } - u ) \cap ( W _ { n } - v ) | } \\ - | W _ { n } | b _ { n } ^ { d } \hat { \rho } ( \hat { \rho } - | W _ { n } | ^ { - 1 } ) \int _ { W _ { n } } \ker ( u ) \, d u \\$$

where ker : R d → [ 0 , ∞ ) plays the role of a kernel and (bn)n ≥ 1 is a sequence of real numbers playing the role of a bandwidth.

We end this section with a recent work by Coeurjolly [15] dealing with a robust estimator of ρ . Assume the domain of observation Wn can be decomposed as Wn = ∪ k ∈ K n Cn,k where the cells Cn,k are non-overlapping and equally sized with volume cn = | Cn,k | and where K n is a subset of Z d with finite cardinality kn = | K n | . The standard estimator of ρ obviously satisfies ˆ ρ = k - 1 n ∑ k ∈ K n N( X ∩ Cn,k)/cn since | Wn | = kncn , i.e. ˆ ρ is nothing else than the sample mean of intensity estimators computed in cells Cn,k . The strategy adopted by Coeurjolly [15] is to replace the sample mean by the sample median, which is known to be more robust to outliers. Quantile estimators based on count data or more generally on discrete data can cause some troubles in the asymptotic theory (see e.g. [30]). To bypass the discontinuity problem of the count variables N( X ∩ Cn,k ) , we follow a well-known technique (e.g. [52]) which introduces smoothness. Let (Uk, k ∈ K n) be a collection of independent and identically distributed random variables, distributed as U ∼ U ( [ 0 , 1 ] ) . Then, for any k ∈ K n , we define Jn,k = N( X ∩ Cn,k) + Uk and J = (Jn,k , k ∈ K n) . The jittering effect shows up right away: the Jn,k admit a density at any point. The jittered median-based estimator of ρ is finally defined by

$$\hat { \rho } ^ { \text {med} } = \frac { \widehat { M e } ( J ) } { c _ { n } }$$


<!-- p:77 -->


where ̂ Me ( J ) stands for the sample median based on J . The estimator ˆ ρ med is shown to be consistent and asymptotically normal and from a numerical point of view to be more robust to outliers (areas where points are unnaturally too abundant or absent). First results were mainly available for Neymann-Scott processes and LGCPs. Biscio and Coeurjolly [10] have extended them to DPPs.

#### 2.4.2 Non Parametric Estimation of the Intensity Function

To estimate non parametrically the intensity function, the standard estimator is a kernel estimator. The analogy proposed by Baddeley et al. [5, Section 6.5.1] gives a very nice intuition of kernel intensity estimation: 'imagine placing one square of chocolate on each data point. Using a hair dryer, we apply heat to the chocolate so that it melts slightly. The result is an undulating surface of chocolate; the height of the surface represents the estimated intensity function. The total mass of the chocolate is unchanged'.

Let ker : R d → [ 0 , ∞ ) be a symmetric kernel function with integral one (over R d ) and let (bn)n ≥ 1 be a sequence of real numbers playing the role of bandwidths. Example of kernels are: the Gaussian kernel ( 2 π) - d/ 2 exp ( -‖ y ‖ 2 / 2 ) or the product of Epanecnikov kernels ∏ d i = 1 3 4 1 ( | yi | ≤ 1 )( 1 -| yi | 2 ) . Let ker bn (w) = ker (w/bn)b - d n , w ∈ R d . The standard estimators are the uniformly corrected ˆ ρ U (see [6, 34]), and the locally corrected ˆ ρ L (suggested by Van Lieshout [77]). These estimators are respectively given for u ∈ Wn by

$$\hat { \rho } ^ { U } ( u ) = \frac { 1 } { e ( u ) } \sum _ { v \in X \cap W _ { n } } \ker _ { b _ { n } } ( v - u ) \quad \text {and} \quad \hat { \rho } ^ { L } ( u ) = \sum _ { v \in X \cap W _ { n } } \frac { \ker _ { b _ { n } } ( v - u ) } { e ( v ) }$$

where e is an edge correction factor given by e(w) = ∫ Wn ker bn (w - t) d t , for w ∈ Wn . As first outlined by Diggle [34], non parametric intensity estimators of the intensity have obvious similarities with probability density estimators introduced by Rosenblatt [68]. The distinction relies on the edge-correction factor and on the more subtle distinction that for point process data the observation domain is Wn but (most of the time) the model exists in R d but is unobserved on R d \ Wn . A further difference is that the points of a sample pattern can in general no longer be seen as an i.i.d. sample from a common probability density.

We want to give hereafter the main idea why it works. Consider the non parametric estimator ˆ ρ U . By the Campbell-Mecke formula (2.2)

$$E \hat { \rho } ^ { U } ( u ) & = e ( u ) ^ { - 1 } \int _ { W _ { n } } \ker _ { b _ { n } } ( v - u ) \rho ( v ) d v \\ & = e ( u ) ^ { - 1 } \int _ { ( W _ { n } - u ) / b _ { n } } \ker ( w ) \rho ( b _ { n } w + u ) d w$$


<!-- p:78 -->


2

Fig. 2.4 Diggle's non parametric estimation of the intensity function ρ = ρ cubic described in Fig. 2.1 for the point patterns from Fig. 2.1d-f. The kernel used is the Gaussian kernel and the bandwidth is chosen using (Poisson) likelihood cross-validation (argument bw.ppl in the density.ppp function). ( a ) Poisson. ( b ) LGCP. ( c ) DPP

$$\approx e ( u ) ^ { - 1 } \int _ { ( W _ { n } - u ) / b _ { n } } \ker ( w ) \, \rho ( u ) d w = e ( u ) ^ { - 1 } \rho ( u ) \int _ { W _ { n } } \ker _ { b _ { n } } ( v ) d v = \rho ( u ) \\$$

where the approximation is valid for bn small and under regularity conditions on ρ . A similar argument can be used for ˆ ρ L . Van Lieshout [77] showed that ˆ ρ L has better statistical performance than ˆ ρ U . As usual, the choice of bandwidth involves a tradeoff between bias and variance. Several data-driven procedures exist to select the optimal bandwidth, see e.g. [5, 6] or the recent promising work by Cronie and Van Lieshout [27] that offers a non-model based way of choosing this parameter.

Many other methods have been introduced to estimate ρ like spatially adaptive smooting, nearest-neighbour based methods, tessellations based approaches, Bayesian estimation. We refer the interested reader to [5] and the many references therein. Following the analogy with density estimation, non parametric estimates of ρ can be obtained using the function density in the spatstat R package. This section is illustrated by Fig. 2.4.

#### 2.4.3 Parametric Estimation of the Intensity Function

In this section, we assume that the intensity function has a parametric form, and in particular we assume that its form is log-linear:

$$\log \rho ( u ; \theta ) = \theta ^ { \top } z ( u )$$

where p ≥ 1, θ ∈ Θ , Θ is an open bounded set of R p and z (u) = (z 1 (u), . . . , zp(u)) ⊤ , u ∈ R d . The functions zi : R d → R play the role of basis functions or covariates. For instance, the models for the intensity functions of Fig. 2.1c-e and h, i are respectively given by:

- p = 3, θ = (β, 1 , . 5 ) ⊤ , z (u) = ( 1 , u 1 , u 3 1 ) ⊤ .
- p = 2, θ = (β, . 5 ) ⊤ , z (u) = ( 1 , grad (u)) ⊤ , where grad is the covariate corresponding to the slope of elevation.


<!-- p:79 -->


##### 2.4.3.1 Poisson Likelihood Estimator

For an inhomogeneous Poisson point process with log-linear intensity function ρ parameterized by θ , the likelihood function (up to a normalizing constant) reads

$$\ell ( \theta ) = \sum _ { u \in \mathbb { X } \cap W _ { n } } \theta ^ { \top } z ( u ) - \int _ { W _ { n } } \exp ( \theta ^ { \top } z ( u ) ) d u .$$

[66] showed that the maximum likelihood estimator is consistent, asymptotically normal and asymptotically efficient as the sample region goes to R d .

Let θ 0 be the true parameter vector. By applying Campbell theorem (2.2) to the score function, i.e. the gradient vector of l( θ ) denoted by l ( 1 ) ( θ ) , we have

$$\mathbb { E } \ell ^ { ( 1 ) } ( \theta ) = \int _ { W _ { n } } z ( u ) ( \exp ( \theta _ { 0 } ^ { \top } z ( u ) ) - \exp ( \theta ^ { \top } z ( u ) ) ) d u = 0$$

when θ = θ 0. So, the score function of the Poisson log-likelihood appears to be an unbiased estimating equation, even though X is not a Poisson point process. The estimator maximizing (2.21) is referred to as the Poisson likelihood estimator. The properties of the Poisson estimator have been carefully studied. Schoenberg [70] showed that the Poisson estimator is still consistent for a class of spatio-temporal point process models. The infill asymptotic normality was obtained by Waagepetersen [78] while [41] established asymptotic normality under an increasing domain assumption and for suitable mixing point processes.

To improve the Poisson likelihood estimator when X is not a Poisson point process [42], proposed to consider the weighted Poisson log-likelihood function

$$\ell ( w ; \theta ) = \sum _ { u \in X \cap W _ { n } } w ( u ) \log \rho ( u ; \theta ) - \int _ { W _ { n } } w ( u ) \rho ( u ; \theta ) \text {d} u ,$$

where w : R d → R is a weight surface whose objective is to reduce the asymptotic covariance matrix. Its score

$$\ell ^ { ( 1 ) } ( w ; \theta ) = \sum _ { u \in X \cap W _ { n } } w ( u ) z ( u ) - \int _ { W _ { n } } w ( u ) z ( u ) \rho ( u ; \theta ) \mathrm d u ,$$

is easily seen to be again an unbiased estimating equation by Campbell theorem. Guan and Shen [42] proved that, under some conditions, the parameter estimates are consistent and asymptotically normal. In particular, it is shown that, in distribution

$$\Sigma ^ { - 1 / 2 } ( \hat { \theta } - \theta _ { 0 } ) \to N ( 0 , \mathbf I _ { p } ) \text { where } \Sigma = A ^ { - 1 } ( \mathbf B + C ) A ^ { - 1 }$$


<!-- p:80 -->


2

with

$$A = \int _ { W _ { n } } w ( u ) z ( u ) z ( u ) ^ { \top } \rho ( u ; \theta _ { 0 } ) d u , \quad B = \int _ { W _ { n } } w ( u ) ^ { 2 } z ( u ) z ( u ) ^ { \top } \rho ( u ; \theta _ { 0 } ) d u ,$$

$$C = \int _ { W _ { n } } \int _ { W _ { n } } w ( u ) w ( v ) z ( u ) z ( v ) ^ { \top } \rho ( u ; \theta _ { 0 } ) \rho ( v ; \theta _ { 0 } ) \left ( g ( u , v ) - 1 \right ) d u d v .$$

Guan and Shen [42] defined the optimal weight surface as the function w minimizing the trace of the asymptotic covariance matrix Σ . They also came up with the following estimate of the optimal weight surface

$$\hat { w } ( u ) = \left ( 1 + \rho ( u ; \hat { \theta } ) ( \hat { K } ( r ) - | B ( 0 , r ) | ) \right ) ^ { - 1 }$$

where r is the practical range of interaction the model (typically estimated by examining an empirical pair correlation function plot), | B( 0 , r) | is the volume of the d -dimensional Euclidean ball centered at 0 with radius r and ˆ K(r) is the inhomogeneous K -function estimator (see e.g. [58]).

The problem of estimating the asymptotic covariance matrix is crucial to derive confidence intervals. The problem is not straightforward as Σ involves unknown second-order characteristics of X . Guan [40], Guan and Shen [42] considered a block bootstrap procedure to achieve this problem while [17] extended (2.18) to the inhomogeneous case.

Figure 2.5 illustrates this section and depicts for the three different patterns parametric estimated intensities and relative errors.

##### 2.4.3.2 Numerical Implementation of the Weighted Poisson Log-Likelihood

[7] developed a numerical quadrature method to approximate the Poisson likelihood (the method is actually the same for the weighted Poisson likelihood) Suppose we approximate the integral term in (2.22) by Riemann sum approximation

$$\int _ { W _ { n } } w ( u ) \rho ( u ; \theta ) d u \approx \sum _ { i = 1 } ^ { M } v _ { i } w ( u _ { i } ) \rho ( u _ { i } ; \theta )$$

where ui , i = 1 , . . . , M are points in Wn consisting of the | x | data points and M - | x | dummy points. The quadrature weights vi &gt; 0 sum to Wn . Examples of such weights are the volumes of the Voronoi cells obtained from the quadrature points ui , i = 1 , . . . , M , see e.g. [5]. Thus, the weighted Poisson log-likelihood function (2.22) can be approximated and rewritten as

$$\ell ( w ; \theta ) \approx \sum _ { i = 1 } ^ { M } v _ { i } w _ { i } \{ y _ { i } \log \rho _ { i } - \rho _ { i } \} ,$$


<!-- p:81 -->


Fig. 2.5 Point patterns considered in this figure are the ones from Fig. 2.1d-f. The first row correponds to the estimated intensity function while the second one depicts the relative errors, i.e. the image with values (ρ(u ; θ ) - ρ(u ; ˆ θ ))/ρ(u ; θ ) . The intensity functions are parametrically estimated using the Poisson likelihood estimator based on (2.21). ( a ) Poisson. ( b ) LGCP. ( c ) DPP. ( d ) Poisson. ( e ) LGCP. ( f ) DPP

where yi = v - 1 i 1 (ui ∈ x ), wi = w(ui) and ρi = ρ(ui ; θ ) . Equation (2.24) corresponds to a quasi Poisson log-likelihood function. Maximizing (2.24) under the log-linear assumption (2.20) is equivalent to fitting a weighted Poisson generalized linear model, which can be performed using standard statistical software. This fact is in particular exploited in the ppm function in the spatstat R package [5] with option method="mpl" .

##### 2.4.3.3 Logistic Regression Likelihood

To perform well, the Berman-Turner approximation requires a large number of dummypoints, actually a much larger number than the number of data points. Fitting such generalized linear models can be computationally intensive. Waagepetersen [79] proposed to consider the following contrast

$$\sum _ { u \in X \cap W _ { n } } w ( u ) \log \left ( \frac { \rho ( u ; \theta ) } { \delta ( u ) + \rho ( u ; \theta ) } \right ) + \sum _ { u \in Y \cap W _ { n } } w ( u ) \log \left ( \frac { \delta ( u ) } { \rho ( u ; \theta ) + \delta ( u ) } \right ) ,$$

where Y is a spatial point process with intensity function δ , independent of X . When the intensity function δ is very large, it can be shown that (2.25) tends to (2.22). So,


<!-- p:82 -->


2

both criterions are actually not so far one from each other. However, (2.25) has two advantages: first, if ρ(u ; θ) cannot be evaluated for u / ∈ ( X ∪ Y ) ∩ Wn , (2.22) cannot be computed. Second and most important, conditional on X ∪ Y , (2.25) corresponds to the weighted likelihood function for Bernoulli trials with probability, π(u) = P ( 1 { u ∈ X } = 1 ) for u ∈ X ∪ Y , with π(u) = ρ(u ; θ )/(δ(u) + ρ(u ; θ ) . Precisely, (2.25) is a weighted logistic regression with offset term - log δ . Thus, again, parameter estimates can be straightforwardly obtained using standard software for generalized linear models. This approach is provided in the spatstat package in R by calling the ppm function with option method="logi" [4, 5]. The estimator derived from the logistic regression likelihood, studied theoretically by Waagepetersen [79], is in general less efficient than the weighted Poisson likelihood estimator but does not suffer from the Berman-Turner approximation, which for specific situations can be very interesting. Waagepetersen [79] actually considered the case w = 1; an estimation of the optimal weight surface w for the logistic regression has recently been proposed by Choiruddin et al. [13] following Guan and Shen [42].

##### 2.4.3.4 Quasi-Likelihood

Guan and Jalilian [43] extended the estimating function (2.23) by considering the following class of estimating equations

$$\sum _ { u \in X \cap W _ { n } } \mathbf h ( u ; \theta ) - \int _ { W _ { n } } \mathbf h ( u ; \theta ) \rho ( u ; \theta ) d u ,$$

where h is a test function to be chosen. The authors considered the Godambe information criterion, which is the inverse of the asymptotic covariance matrix, as the criterion to optimize. By denoting T the integral operator acting on R p valued functions h defined by

$$T h ( u ) = \int _ { W _ { n } } h ( v ) \rho ( v ; \theta ) \left \{ g ( v - u ) - 1 \right \} d v$$

where g is the pair correlation function (assumed to be invariant under translations) [43], showed that the optimal function h is the solution of the Fredholm equation

$$h ( \cdot ) + T h ( \cdot ) = \frac { \rho ^ { ( 1 ) } ( \cdot ; \theta ) } { \rho ( \cdot ; \theta ) } . \\$$

The estimator derived from the estimating Eq. (2.26) with this optimal choice of h was shown to be consistent and asymptotically Gaussian. The procedure results in a slightly more efficient estimator than the one obtained by Guan and Shen [42] especially for very clustered patterns. The counterpart is that the derived estimator is more computationally expensive, essentially because it cannot be fitted using an analogy with generalized linear models.


<!-- p:83 -->


##### 2.4.3.5 Variational Approach

Previous methods require either d -dimensional integral discretization or the simulation of an extra dummy point process. This can be problematic when d is large and/or when the number of points is large. All methods share the characteristic to be implemented using optimization procedures and require z (u) to be observed over the whole window (or on a dense set for the logistic regression method). Coeurjolly and Møller [19] proposed an alternative to bypass all these criticisms. The authors first obtained the following equation

$$E \sum _ { u \in X \cap W _ { n } } h ( u ) \theta ^ { \top } \text {div} \, z ( u ) = - E \sum _ { u \in X \cap W _ { n } } \text {div} \, h ( u )$$

where div z (u) = ( div zi (u), i = 1 , . . . , p) ⊤ and div zi (u) = ∑ d j = 1 ∂zi(u)/∂uj , for any function h compactly supported on Wn (and such that the above quantities are well-defined). Coeurjolly and Møller [19] exploited (2.27) and proposed the estimator ˆ θ = - A - 1 b with

$$A = \sum _ { u \in X \cap W _ { n } } \eta ( u ) d i v \, z ( u ) d i v \, z ( u ) ^ { \top } \quad \text {and} \quad \mathfrak { b } = \sum _ { u \in X \cap W _ { n } } \text {div } ( \eta ( u ) d i v \, z ( u ) )$$

where η is a smooth compactly supported function (which can be set to 1 in the case where the zi are compactly supported). This estimator is called variational estimator. Such a variational approach was first introduced by Baddeley and Dereudre [2] to estimate the Papangelou conditional intensity of a Gibbs point process.

We indeed observe that the variational estimator is explicit, does not require any integral discretization and depends only on (derivatives of) the zi where the points are observed. When the zi correspond to covariates (like Fig. 2.1h, i) the first and second derivatives can be estimated using finite differences locally around the data points.

### 2.5 Higher-Order Interaction Estimation via Conditional Intensity

Conditional intensities encode the interactions of the process. In a parametric setting, they are key quantities arising in several estimating equations and contrast estimating functions to estimate the interaction parameters of the model. We describe these estimating methods in the following, whether they depend on the Papangelou conditional intensity (Sect. 2.5.1) or the Palm likelihood (Sect. 2.5.2). The statistical setting is the same as in Sect. 2.4, i.e. we observe X on Wn and the asymptotic results are in the sense of an increasing domain. In view of Table 2.1, the procedures based on the Papangelou conditional intensity are mainly devoted to the estimation of Gibbs models, while the methods based on the Palm likelihood are used to estimate the parameters in some Cox and DPP models. Note that for these models, maximum likelihood estimation is generally not considered in practice: the density of a Cox model is indeed intractable, see (2.15), and the density of a Gibbs model involves an intractable normalizing constant, see (2.8). However, for some Gibbs models, this normalizing constant may be approximated by MCMC methods, in which case maximum likelihood estimation becomes a viable alternative, see [39, 55] and [32].


<!-- p:84 -->


Beyond this parametric framework, a natural concern could be the non parametric estimation of conditional intensities, similarly as the methods described in Sect. 2.4.2 for the intensity. For Gibbs models [36], focused on the class of pairwise interaction models and proposed a non parametric estimation of the pairwise interaction function, leading to a non parametric estimation of the Papangelou conditional intensity (within the class of pairwise interaction models). For the Palm intensity, by exploiting that ρx(u) = ρ(u)g(u, x) , a non parametric estimation of ρx could be obtained by combining a non parametric estimation of the intensity function ρ and of the pair correlation function g , a classical problem in spatial statistics, see e.g. [45, 58]. This approach has, nevertheless, never been studied in the literature. Following the previous comments, we note that non parametric estimation of conditional intensities thus remains largely unexplored and the following subsections do not treat this aspect.

#### 2.5.1 Parametric Estimation with the Papangelou Conditional Intensity

Weassume at many places in the following that the Papangelou conditional intensity has a log-linear parametric form

$$\log \lambda ( u , x ; \theta ) = \theta ^ { \top } t ( u , x ) ,$$

for some function t (u, x ) = (t 1 (u, x ), . . . , tp(u, x )) ⊤ , u ∈ R d , x ∈ N , and where θ ∈ Θ , Θ is an open bounded set of R p . These models are sometimes called exponential models. This is a common assumption made in the literature to investigate the asymptotic properties of the estimation methods. In this setting, the inference procedures can also be much faster. Many standard models belong to the family of exponential models, see [9]. For example, the Strauss model and the area-interaction model are exponential models for the parameters ( log z, θ) but not for the range parameter R or the hard-core parameter δ .


<!-- p:85 -->


##### 2.5.1.1 Maximum Pseudo-Likelihood Estimator

The pseudo-likelihood function, given the observation of X on Wn , is

$$P L ( \theta ) = e ^ { - \int _ { W _ { n } } \lambda ( u , X ; \theta ) d u } \prod _ { u \in X \cap W _ { n } } \lambda ( u , X ; \theta ) .$$

The concept of pseudo-likelihood was introduced by Besag [8] for Markov random fields on a lattice, in which case it is the product of the conditional densities of the field at each site of the lattice, given the neighbor sites. The extension to point processes first appears in [67], Section 4.2, where (2.30) is informally derived by a limiting argument. Specifically, given a lattice on Wn , the Markov random field consisting of the count process on each cell of the lattice is introduced. The pseudolikelihood of this random field, in the sense of [8], tends to (2.30) as each cell of the lattice is refined to an infinitesimal point. This approach is rigorously justified in [47].

The log pseudo-likelihood (LPL) function reads

$$L P L ( \theta ) = \sum _ { u \in X \cap W _ { n } } \log \lambda ( u , X ; \theta ) - \int _ { W _ { n } } \lambda ( u , X ; \theta ) d u ,$$

which becomes for exponential models

$$L P L ( \theta ) = \sum _ { u \in X \cap W _ { n } } \theta ^ { \top } t ( u , X ) - \int _ { W _ { n } } \exp { ( \theta ^ { \top } t ( u , X ) ) } d u .$$

The parallel with the Poisson log-likelihood (2.21) is immediate. In virtue of the GNZ equation (2.7), the score of the LPL equation appears to be an unbiased estimating equation for X . The estimator obtained as the maximum of LPL ( θ ) over Θ is the maximum pseudo-likelihood estimator.

From a theoretical point of view, the consistency of the maximum pseudolikelihood estimator has been proved for stationary exponential models in [47], [53] and [9], and extended to general (possibly non hereditary) interactions in [31]. The asymptotic normality for this estimator is established in [46, 54] and [9] for stationary exponential models having a finite range interaction, i.e. there exists R such that λ(u, X ; θ ) = λ(u, X B(u,R) ; θ ) . An extension to finite range nonexponential models is carried out in [16], while the case of infinite range exponential models is treated in [18]. For finite range exponential models, a fast and consistent estimation of the asymptotic covariance matrix of the estimator is proposed in [21].

As detailed hereafter, due to the similarity between (2.31) and (2.21), the numerical approximations to get the maximum pseudo-likelihood estimator and the Poisson likelihood estimator are analogous. The ideas to improve their efficiency also follow the same lines.


<!-- p:86 -->


2

However, an important difference between (2.31) and (2.21) is the presence of edge effects in (2.32). Whereas all terms in the Poisson likelihood function only depend on the observation of X on Wn , the LPL function involves λ(u, X ; θ ) that may depend on the unobserved point pattern X ∩ W c n . Standard solutions to deal with this issue are: (1) to replace X by X Wn in (2.31), thus accounting for the empty set configuration outside Wn ; (2) to apply a periodic expansion of XWn in W c n , up to some distance, in order to account for a more realistic outside configuration than the empty set; (3) to apply the border correction, which consists in replacing Wn in (2.31) by Wn ⊖ R for some R &gt; 0, that is Wn eroded by R . This border correction is particularly adapted when the interaction is finite-range with a range less than R , in which case λ(u, X ; θ ) , for u ∈ Wn ⊖ R , is equal to λ(u, X Wn ; θ ) . Other edge corrections are possible. The ppm function of the spatstat package in R offers six different choices, including the three options detailed above, see [3] and [5].

Beyond the edge effects, the integral in (2.31) has to be approximated. A straightforward but somewhat costly solution consists in applying a Monte-Carlo approximation of this integral. Alternatively, as pointed out and developed by Baddeley and Turner [3], the [7] device can be applied in the exact same way as described in Sect. 2.4.3.2, where ρ(ui ; θ ) is replaced by λ(ui, X ; θ ) . For a log-linear Papangelou conditional intensity, the maximisation of the resulting approximated LPL function reduces to fit a (weighted) Poisson generalized linear model. This is how the maximum pseudo-likelihood estimator is derived by default in the ppm function of spatstat .

The limitations of the Berman-Turner approximation are the same as for the Poisson likelihood estimation. The number of dummy points has to be large to hope for a good approximation. This is all the more important in presence of a Gibbs model generating strong interactions. If not, the Berman-Turner approximation may lead to a significant bias. This is illustrated in [4], where a logistic regression pseudo-likelihood is introduced as an alternative, in the same vein as the logistic regression likelihood of Sect. 2.4.3.3. The logistic regression pseudo-likelihood contrast function reads in the present case

$$\sum _ { u \in X \cap W _ { n } } \log \left ( \frac { \lambda ( u , X ; \theta ) } { \delta ( u ) + \lambda ( u , X ; \theta ) } \right ) + \sum _ { u \in Y \cap W _ { n } } \log \left ( \frac { \delta ( u ) } { \lambda ( u , X ; \theta ) + \delta ( u ) } \right ) , \quad ( 2 . 3 3 )$$

where Y is a spatial point process with intensity function δ , independent of X . By application of the GNZ equation and the Campbell formula, it is easily seen that the associated score function is an unbiased estimating function. As for (2.31), an edge correction must be applied to be able to compute λ(u, X ; θ ) . The advantages of this approach are again similar to those described in Sect. 2.4.3.3 for the estimation of the intensity. In particular, for a log-linear Papangelou conditional intensity, the estimates can be simply derived using standard GLM procedures. Moreover the result does not suffer from the artificial bias of the Berman-Turner approximation. The asymptotic properties of the method, including an estimation of the variance, are studied in [4].


<!-- p:87 -->


Fig. 2.6 Point patterns considered in this figure correspond to the ones from Fig. 2.3d-f. The first row corresponds to the estimated Papangelou conditional intensity function while the second one depicts the relative errors, i.e. the image with values (λ(u, x ; θ ) - λ(u, x ; ˆ θ ))/λ(u, x ; θ ) . The Papangelou conditional intensity functions are parametrically estimated using the maximum pseudo-likelihood method. ( a ) Strauss hard-core. ( b ) Area-interaction, θ = - 2 . 3. ( c ) Areainteraction, θ = 0 . 7. ( d ) Strauss hard-core. ( e ) Area-interaction, θ = - 2 . 3. ( f ) Area-interaction, θ = 0 . 7

This Sect. 2.5.1 is illustrated by Fig. 2.6 which depicts for three different patterns the estimated Papangelou conditional intensities and the associated relative errors.

##### 2.5.1.2 Takacs-Fiksel Estimator

Just like the quasi-likelihood estimator (Sect. 2.4.3.4) extends the Poisson likelihood estimator of the intensity function by fully exploiting the Campbell theorem, the Takacs-Fiksel estimator extends the pseudo-likelihood estimator of the Papangelou conditional intensity function by fully exploiting the GNZ formula (2.7). Specifically, from the GNZ formula, for any q -dimensional ( q ≥ p ) function h (provided the following terms exist and admit an expectation), the equation

$$e _ { h } ( \theta ) \coloneqq \int _ { W _ { n } } \mathbf h ( u , X ; \theta ) \lambda ( u , X ; \theta ) d u - \sum _ { u \in X \cap W _ { n } } \mathbf h ( u , X \ \{ u \} ; \theta )$$

is an unbiased estimating equation for θ . The choice h (u, X ; θ ) = ∂ log λ(u, X ; θ )/ ∂ θ corresponds to the score function of the pseudo-likelihood procedure.

In its initial form [37, 73], the Takacs-Fiksel estimator is obtained by minimizing the norm of e h ( θ ) . An alternative (see [5]) consists in adopting the estimating


<!-- p:88 -->


2

equation approach to solve e h ( θ ) = 0 with q = p . In both cases, the strength and flexibility of the method lies in the possibility to choose the function h , as discussed now. The asymptotic properties of the Takacs-Fiksel estimator for stationary models are mainly studied by Coeurjolly et al. [22].

The first interest is to be able to find specific choices of h which may lead to an explicit estimator (unlike the pseudo-likelihood estimator), or may allow estimation in situations where the pseudo-likelihood estimator is unusable. We give two examples, originated from [22]. For the Strauss model, an explicit estimator of (z, θ) follows from the choice h = (h 1 , h 2 ) with

$$h _ { 1 } ( u , X ; \theta ) & = \begin{cases} 1 & \text {if } | X \cap B ( u , R ) | = 0 \\ 0 & \text {otherwise} \end{cases} , \quad h _ { 2 } ( u , X ; \theta ) = \begin{cases} e ^ { \theta } & \text {if } | X \cap B ( u , R ) | = 1 \\ 0 & \text {otherwise} \end{cases} . \\ \\ \text {It is not diffucntl to verify that } e _ { 2 } ( \theta ) = ( z V _ { 0 } - N _ { 0 } \ z V _ { 1 } - e ^ { \theta } N _ { 1 } ) \text { whose norm } | e _ { 2 } ( \theta ) | \Big |$$

It is not difficult to verify that e h (θ) = (zV 0 - N 0 , zV 1 - e θ N 1 ) whose norm ‖ e h (θ) ‖ is minimal for

$$\hat { z } = N _ { 0 } / V _ { 0 } , \ \hat { \theta } = \log ( V _ { 1 } / N _ { 1 } ) - \log ( V _ { 0 } / N _ { 0 } ) ,$$

where Nk , k = 0 , 1, denotes the number of points u ∈ X Wn such that | B(u, R) ∩ X | = k + 1, and Vk denotes the volume of the set { u ∈ Wn, | B(u, R) ∩ X | = k } . For the second example, consider the area interaction process where only the union of balls Γ ( X Wn ) := ⋃ u ∈ X Wn B(u, R) is observed, but not all individual points in X Wn . This setting comes from stochastic geometry, where the spots in a binary images can be modeled by a union of balls, see [33, 57]. In this case a pseudo-likelihood estimator cannot be applied because this estimator needs the locations of all points of X Wn to be computed. In contrast, it is possible to find specific choices of h such that e h (θ) becomes computable, even if each quantity in the sum term of e h (θ) is unavailable. Define

$$h _ { 1 } ( u , X ; \theta ) = \mathcal { P } \left ( B ( u , R ) \cap \{ \Gamma ( X ) \} ^ { c } \right ) , \\ \\$$

where P denotes the perimeter. Neglecting edge effects, we obtain that

$$\sum _ { u \in X \cap W _ { n } } h _ { 1 } ( u , X \ \{ u \} ; \theta ) = \mathcal { P } ( \Gamma ( X _ { W _ { n } } ) )$$

which is a quantity computable from the observation of Γ( X Wn ) . Another choice is possible by considering isolated balls:

$$h _ { 2 } ( u , X ; \theta ) = \begin{cases} 1 & \text {if } B ( u , R ) \cap \Gamma ( X ) = \emptyset , \\ 0 & \text {otherwise.} \end{cases}$$


<!-- p:89 -->


Then

$$\sum _ { u \in X \cap W _ { n } } h _ { 2 } ( u , X \ \{ u \} ; \theta ) = N _ { i s o } ( \Gamma ( X _ { W _ { n } } ) ) ,$$

where N iso (Γ ( X Wn )) denotes the number of isolated balls in Γ( X Wn ) . Besides, the integrals terms in eh 1 (θ) and eh 2 (θ) do not suffer from the same unobservability issue as the sum terms, and they can be computed numerically. Therefore the estimation of (z, θ) in the area interaction model can be carried out using the Takacs-Fiksel estimator associated to h = (h 1 , h 2 ) , with the observation of Γ( X Wn ) only.

Another interest of the Takacs-Fiksel approach is the possibility to optimize the estimating equation in h , specifically by minimizing the associated Godambe information. This problem has been studied in [23], where the authors notice that the minimization of the Godambe information is a too difficult problem in practice. Instead they suggest a 'semi-optimal' procedure, where the Godambe information is replaced by a close approximation. Let T x be the integral operator acting on R p valued functions g

$$T _ { x } \, g ( u ) = \int _ { W _ { n } } g ( v ) ( \lambda ( v , x ; \theta ) - \lambda ( v , x \cup \{ u \} ; \theta ) ) d v .$$

Coeurjolly and Guan [23] show that their semi-optimal test function h is the solution of the Fredholm equation

$$h ( . , x ; \theta ) + T _ { x } \mathbf h ( . , x ; \theta ) = \frac { \lambda ^ { ( 1 ) } ( . , x ; \theta ) } { \lambda ( . , x ; \theta ) }$$

where λ ( 1 ) (., x ; θ ) = ∂λ(., x ; θ )/∂ θ . In practice, this solution is obtained numerically. As a result [23], show that the Takacs-Fiksel estimator based on this semi-optimal test function outperforms the pseudo-likelihood estimator in most cases. However the gain might appear not sufficiently significant in view of the computational cost to implement the method.

##### 2.5.1.3 Variational Estimator

An alternative inference method based on the Papangelou conditional intensity consists in a variational approach, in the same spirit as in Sect. 2.4.3.5 for the estimation of the intensity. This idea originates from [2]. We assume in this section that the Papangelou conditional intensity admits a log-linear form as in (2.29). To stress the peculiar role of the activity parameter z in this expression, we rather write

$$\log \lambda ( u , x ; \theta ) = \log z + \theta ^ { \top } t ( u , x ) .$$


<!-- p:90 -->


2

where θ ∈ R p gathers all parameters but the activity parameter. We further assume that u ↦→ t (u, x ) is differentiable. Then, an integration by part in the GNZ formula shows that for any real function h on R d × N , which is differentiable and compactly supported with respect to the first variable and such that the following expectations are well-defined,

$$E \sum _ { u \in X } h ( u , X \ \{ u \} ) \theta ^ { \top } d i v _ { u } \mathfrak { t } ( u , X ) = - E \sum _ { u \in X } d i v _ { u } h ( u , X \ \{ u \} )$$

where divu t (u, X ) = ( divu t 1 (u, X ), . . . , divu tp(u, X ) ) ⊤ . Considering the empirical version of this equation for p different test functions h 1 , . . . , hp , we obtain a system of linear equations that yields the estimator

$$\hat { \theta } = - A ^ { - 1 } b$$

where A is the matrix with entries ∑ u ∈ X Wn hi (u, X \ { u } ) divu tj (u, X ) , i, j = 1 , . . . , p and b is the vector with entries ∑ u ∈ X Wn divu hi (u, X \ { u } ) , i = 1 , . . . , p . Here we have assumed that A is invertible. Note that if z (or log z ) was part of θ , that is (2.29) holds instead of (2.34), then its associated t 0 (u, X ) function would be constant equal to 1, so divu t 0 (u, X ) = 0 and A would not be invertible. In fact, this procedure does not make the estimation of the activity parameter possible.

The asymptotic properties of (2.35) for stationary models are studied in [2]. The main interest of this variational estimator is its simple and explicit form. As to the choice of the test functions hi , some recommendations are suggested in [2]. For pairwise exponential models, they consider hi (u, X ) = divu ti(u, X ) . A simulation study carried out with this choice for the Lennard-Jones model [50] demonstrates the efficiency of the procedure, especially in presence of strong interactions. In this situation the variational estimator outperforms the pseudo-likelihood estimator, both in terms of accuracy and computational cost, see [2].

The assumption that u ↦→ ti(u, x ) is differentiable is the main restriction of this procedure. For instance, for the Strauss model (2.12), t 1 (u, x ) = - nR(u, x ) is not differentiable, even not continuous in u . The other restriction, as noted before, is the impossibility to estimate z . However, note that given ˆ θ in (2.35) for the exponential model (2.34), a natural procedure to get an estimation of z is to apply the Takacs-Fiksel estimator associated to the test function h = e - ˆ θ ⊤ t (u, x ) . This two-step procedure provides

$$\hat { z } = \frac { 1 } { | W _ { n } | } \sum _ { u \in X _ { W _ { n } } } e ^ { - \hat { \theta } ^ { \top } t ( u , x ) } .$$

For finite-range Gibbs models, [20], also proposed the estimator ˆ z = N 0 /V 0 (see Sect. 2.5.1.2 for the definitions of N 0 , V 0).


<!-- p:91 -->


#### 2.5.2 Palm Likelihood Estimation

Palm likelihood refers to the estimation procedures based on the first order Palm intensity ρx(u) . For this reason Palm likelihood only applies to models for which we have a closed form expression of the Palm intensity. This is the case for the LGCP, SNCP and DPP models, see Table 2.1.

The first contribution exploiting the properties of ρx(u) , namely in [63], was not intended to estimate the parameters in one of these models, but to estimate the fractal dimension of the point pattern. For isotropic models, implying that ρx(u) = ρ 0 (u) only depends on | u | and is independent of x , this estimation boils down to estimate the parameter H ∈ [ 0 , 2 ] in the (assumed) asymptotic behavior ρ 0 (u) - ρ ∼ κ | u | - H as | u | → ∞ , where κ &gt; 0 and ρ denotes the intensity parameter. To get an estimation of H [63], suggested a non parametric and a parametric method. In the non parametric approach, they estimate ρ 0 (u) for | u | ∈ [ r 1 , r 2 ] by the number of pairs at a distance belonging to the annular region A (r 1 , r 2 ) divided by the area of A (r 1 , r 2 ) . Then the slope of the (approximated) line in the log-log plot of ˆ ρ 0 (u) - ˆ ρ with respect to | u | provides an estimate of H . For their parametric approach, they assume that ρ 0 (u) = ρ 0 (u ; θ ) = ρ + κ | u | - H where θ = (ρ, κ, H ) and they estimate θ by maximizing the Palm likelihood

$$\sum _ { u , v \in X _ { w _ { n } } , \| u - v \| < R } ^ { \neq } \log ( \rho _ { 0 } ( u - v ; \theta ) ) - | X _ { W _ { n } } | \int _ { B ( 0 , R ) } \rho _ { 0 } ( u ; \theta ) d u ,$$

where R is a tuning parameter that is typically small relative to the size of Wn . The Palm likelihood is informally motivated in [63] by the fact that the point process consisting of pairs of points R -apart in X Wn is approximately an inhomogeneous Poisson process with intensity | X Wn | ρ 0 (u) . The Palm likelihood is thus deduced from the associated Poisson likelihood (2.22).

The Palm likelihood (2.36) has been used in [74] to estimate the parameters of stationary Neymann Scott processes. The method can also be applied to other models like LGCPs and DPPs. The theoretical aspects (consistency and asymptotic normality) have been studied in the stationary case by Prokešová and Jensen [64], where the authors used the fact that the score associated to (2.36) is nearly an unbiased estimating equation. Specifically, it follows from the Campbell theorem that the score associated to the modified Palm likelihood

$$\sum _ { u \in X _ { W _ { n } \ominus R } , v \in W _ { n } , \| u - v \| < R } \log ( \rho _ { 0 } ( u - v ; \theta ) ) - | X _ { W _ { n } \ominus R } | \int _ { B ( 0 , R ) } \rho _ { 0 } ( u ; \theta ) d u ,$$

that accounts for edge effects, is an unbiased estimating equation. The difference between this modified Palm likelihood and (2.36) is proved to be asymptotically negligible in [64].


<!-- p:92 -->


Several generalizations of (2.36) in the setting of inhomogeneous models are possible. In [65], a two step procedure is proposed for the estimation of secondorder intensity-reweighted stationary models. For these models, the pair correlation is invariant by translation, g(u, v) = g 0 (v - u) , while the intensity ρ(x) is not constant, whence ρx(u) = ρ(u)g 0 (x - u) . In [65], ρ(u) is estimated by the Poisson likelihood method to yield ˆ ρ(u) , and the remaining parameters θ are then estimated by the following Palm likelihood

$$\sum _ { u , v \in X _ { w _ { n } } , \| u - v \| < R } ^ { \neq } \log ( \hat { \rho } ( v ) g _ { 0 } ( u - v ; \theta ) ) - \sum _ { u \in X _ { w _ { n } } } \int _ { B ( u , R ) } \hat { \rho } ( v ) g _ { 0 } ( u - v ; \theta ) d v .$$

Note that if ρ(v) = ρ is constant, replacing ˆ ρ(v) by ρ in the above formula gives (2.36). As an alternative generalization of (2.36) [65] also considers the Palm likelihood

$$\sum _ { u \in X _ { w _ { n } \in R } , \, v \in W _ { n } , \, \| u - v \| < R } ^ { \neq } \log ( \hat { \rho } ( u ) \hat { \rho } ( v ) g _ { 0 } ( u - v ; \theta ) ) \\ & - \int _ { W _ { n } \in R } \int _ { B ( u , R ) } \hat { \rho } ( u ) \hat { \rho } ( v ) g _ { 0 } ( u - v ; \theta ) d u d v . \\ \intertext { The asymptotic properties of this two step method, with either generalization of }$$

The asymptotic properties of this two step method, with either generalization of the Palm likelihood, are established in [65], with a focus on SNCPs. For general inhomogeneous models, a natural proposition would be to use the Palm likelihood

$$\sum _ { u \in X _ { w _ { n } \in R } , v \in W _ { n } , \| u - v \| < R } \log ( \rho _ { v } ( u ; \theta ) ) - \sum _ { v \in X _ { w _ { n } \in R } } \int _ { B ( v , R ) } \rho _ { v } ( u ; \theta ) d u ,$$

whose score function is an unbiased estimating function. The estimation of all parameters could be handled in one step. Such a methodology has not been investigated so far.

### 2.6 Conclusion

In this chapter, we have proposed an analysis of spatial point patterns through intensity functions and conditional intensity functions. As demonstrated in the last two sections, many methods are available to estimate these quantities. However, we think there are still challenging questions that deserve to be studied.

Most inference procedures presented in this chapter are devoted to the parametric estimation of spatial point process models. We think that efficient non parametric procedures to estimate the Papangelou conditional intensity or the Palm intensity are missing. This of course can be viewed as a first step to the choice of a parametric model, but it constitutes an informative characteristic to understand the interactions in a point pattern. As briefly exploited in [63], a non parametric estimation can also serve as a basis for the estimation of specific characteristic, as the fractal index in [63], or the long-range interaction parameter, a (still open) issue raised in [72, pp. 202-210].


<!-- p:93 -->


Modern spatial statistics face complex data sets, with a possibly huge amount of information (millions of points, thousands of covariables). Inference methods able to handle these aspects must be developed. This demands efficient numerical methods and requires the development of regularization methods [13, 75]. Similarly, the stationarity assumption is rarely realistic for complex data. There is a need to develop inference methods for inhomogeneous (conditional) intensity functions, as local Papangelou and local Palm likelihood [1].

Acknowledgements Apart of the material presented here is the fruit of several collaborations. We take the opportunity to thank our main collaborators David Dereudre, Jesper Møller, Ege Rubak and Rasmus Waagepetersen. We are also grateful to Christophe Biscio, Achmad Choiruddin, Rémy Drouilhet, Yongtao Guan and Frédérique Letué. This contribution has been partly supported by the program ANR-11-LABX-0020-01.

## Chapter 3

## Stochastic Methods for Image Analysis

Agnès Desolneux

Abstract These lectures about stochastic methods for image analysis contain three parts. The first part is about visual perception and the non-accidentalness principle. It starts with an introduction to the Gestalt theory, that is a psychophysiological theory of human visual perception. It can be translated into a mathematical framework thanks to a perception principle called the non-accidentalness principle, that roughly says that 'we immediately perceive in an image what has a low probability of coming from an accidental arrangement'. The second part of these lectures is about the so-called 'a contrario method' for the detection of geometric structures in images. The a contrario method is a generic method, based on the nonaccidentalness principle, to detect meaningful geometric structures in images. We first show in details how it works in the case of the detection of straight segments. Then, we show some other detection problems (curves, vanishing points, etc.) The third part of these lectures is about stochastic models of images for the problem of modeling and synthesizing texture images. It gives an overview of some methods of texture synthesis. We also discuss two models of texture images: stationary Gaussian random fields and shot noise random fields.

### 3.1 Visual Perception and the Non-accidentalness Principle

Figure 3.1 presents a pure noise image: in this image we don't perceive any visual structure. This lack of perception is called Helmholtz principle , also called, in its stronger form, the non-accidentalness principle . This principle can be stated in two different ways:

1. The first way is common sensical. It simply states that 'we do not perceive any structure in a uniform random image'. (In this form, the principle was first stated by Attneave [3] in 1954.)

<!-- p:98 -->


Fig. 3.1 A pure noise image. It is of size 64 × 64 pixels, and the grey levels are independent samples of the uniform distribution on { 0 , 1 , . . . , 255 }

Fig. 3.2 The same alignment of dots is present in the two images. On the left, there are 30 points, and there are 80 on the right. According to the non-accidentalness principle, we don't perceive the alignment in the right image (hide the left image with your hand, not to be influenced by it) because the probability of having 8 almost aligned points just by chance when you have 80 random points is quite high, whereas it is very small when there are 30 random points

2. In its stronger form, it states that whenever some large deviation from randomness occurs, a structure is perceived. In other words 'we immediately perceive whatever has a low likelihood of resulting from accidental arrangement'. (Under this form, the principle was stated in Computer Vision by Zhu [43] or Lowe [27].)

On Fig. 3.2, we illustrate the non-accidentalness principle on an example with aligned dots.


<!-- p:99 -->


Now, not all possible structures are relevant for visual perception. The 'interesting' structures are geometric patterns, and they have been extensively studied and defined by the so-called Gestalt School of Psychophysiology.

#### 3.1.1 Gestalt Theory of Visual Perception

The aim of Gestalt theory (Wertheimer [42], Metzger [28] and Kanizsa [25]) is to answer questions such as: How do we perceive geometric objects in images? What are the laws and principles of visual construction? In other words, how do you go from pixels (or retina cells) to visual objects (lines, triangles, etc.)?

Before Gestalt theory, the study of visual perception was done through opticgeometric illusions. See Fig. 3.3 for an example. The goal of these illusions is to ask: 'what is the reliability of our visual perception?'

But Gestalt theory does not continue on the same line. The question is not why we sometimes don't see parallel lines when they are; the question is why we do see a line at all. This perceived line is the result of a construction process. And it is the aim of Gestalt theory to establish the laws of this construction process. Gestalt theory starts with the assumption that there exists a small list of active grouping laws in visual perception: vicinity, same attribute (like color, shape, size or orientation for instance), alignment, good continuation, symmetry, parallelism, convexity, closure, constant width, amodal completion, T-junctions, X-junctions, Y-junctions.

The above listed grouping laws belong, according to Kanizsa, to the so-called primary process, opposed to a more cognitive secondary process.

These different grouping laws are illustrated on the following figures (that are replications of some of the many illustrations of the book of Kanizsa [25]): on Fig. 3.4 for vicinity (we group objects that are spatially close), Fig. 3.5 for same attribute (we immediately perceive groups of objects that have the same attribute, like here color, size or orientation), Fig. 3.6 for symmetry (our visual perception is very sensitive to symmetry, we immediately perceive it when it is present), Fig. 3.7-left for good continuation (we perceive smooth curves) and Fig. 3.7-

Fig. 3.3 An example of an optic-geometric illusion: Zoellner's illusion (1860). The diagonal lines are not perceived as being parallel, but they are! An explanation is that, in some way, they partly 'inherit' the horizontal or vertical orientation of the smaller segments that are on them. Therefore, their perceived orientation is not the same as their real orientation

<!-- p:100 -->


Fig. 3.4 Elementary grouping law: vicinity. We clearly perceive here two groups of 'objects'

Fig. 3.5 Elementary grouping law: the objects have a common attribute and this allows us to perceive immediately vertical lines of similar objects. From left to right, the common attribute is: same color, same size and same orientation

Fig. 3.6 Elementary grouping law: symmetry. Our visual perception is very sensitive to symmetry. We immediately perceive it when it is present

<!-- p:101 -->


3

58

Fig. 3.7 Left: Elementary grouping law of Good Continuation. We perceive here two 'smooth' curves, one in the horizontal direction and one in the vertical one. Right: Elementary grouping law of Closure. We perceive here two closed curves, and not an '8', as it would have been the case if we had kept the good continuation grouping of the left figure

Fig. 3.8 On the left: T-junctions. They allow us to perceive occlusions. On the right: an X-junction that is typical of the transparency phenomenon

right for closure (we perceive closed curves). This last figure has to be compared with Fig. 3.7-left that illustrates good continuation. It is a typical example of conflict between grouping laws: here we can say that 'closure wins against good continuation'. But one may build examples where the converse will be true. It is one of the properties of the Gestalt grouping laws: there is no hierarchy in this small set of grouping laws, and there are sometimes conflicts between different possible interpretations of a figure.

The three types of junctions are illustrated on Figs. 3.8, 3.9 and 3.10. The Tjunctions indicate occlusion (an object is partly hidden by another one). The Xjunctions occur when there is some transparency. The Y-junctions indicate a 3D perspective effect (they come from the planar representation of the three principal orientations of the 3D space).

Amodal completion is one of the most applied grouping laws for our visual perception. Objects are often partly hidden by other objects (this is the occlusion phenomenon), but we are able to infer the missing contours. This is for instance illustrated on Fig. 3.11, where we 'see' a black rectangle partly covered by five white shapes. Now there is no black rectangle in this figure, there are only black


<!-- p:102 -->


Fig. 3.9 A famous illustration of the power of T-junctions by Kanizsa. On the left, there are no T-junctions, and no occlusion is perceived. On the right: the three added bands create T-junctions, allowing contours completion across occlusions. The 3D cube is immediately perceived, whereas in the first figure one only sees strange 'Y' shapes

0

Fig. 3.10 The famous Penrose fork: an impossible figure. In this figure, the perspective effect is created by Y-junctions. This figure also illustrates the fact that visual grouping laws can be stronger than physical sense

Fig. 3.11 Amodal completion: what do you see here? A black rectangle (see text)

pixels that we group according to their same color, and then thanks to alignment and T-junctions we complete the missing parts of the black rectangle.

The fact that in Fig. 3.11 we perceive a rectangle and not another shape (with round corners for instance), comes from the collaboration of several Gestalt laws, as good continuation, simplicity and 'past experience'. This last 'law' is also part of Gestalt theory: our visual perception is very sensitive to 'known shapes': digits, letters, geometric shapes, but also faces, cars, etc. This is something that is much more difficult to translate in mathematical terms.


<!-- p:103 -->


Fig. 3.12 The recursivity of Gestalt grouping laws: black pixels are grouped (thanks to vicinity and same color) to form small rectangles. These small rectangles are grouped (thanks to parallelism and vicinity) to form 'bars', that are again grouped to form larger bars, then parallel rectangles, and so on . . .

|    |   1 |    |    |
|----|-----|----|----|
|  1 |     |    |    |
|    |   1 |    |    |
|    |     |  1 |  1 |
|  1 |   1 |    |  1 |
|    |   1 |    |    |
|    |  11 |  1 |  1 |
|    |   1 |    |    |
|  1 |     |    |    |
|    |     |    | 1. |
|  1 |   1 |    |    |
|    |  11 |    |    |
|  1 |  11 |    |    |

All grouping Gestalt laws are recursive : they can be applied first to atomic inputs and then in the same way to partial groups already constituted. See for instance Fig. 3.12 where grouping laws are recursively applied. On this figure, the same partial Gestalt laws namely alignment, parallelism, constant width and proximity, are recursively applied not less than six times.

#### 3.1.2 The Non-accidentalness Principle

Under its strong form, the Helmholtz or non-accidentalness principle states that we immediately perceive any regular structure that has a low probability to be there just by chance. This principle is used all the time in vision, but not only in vision, in our every day life also. For instance, if you play dice and you obtain a sequence 6 , 6 , 6 , 6 , 6 , 6 , 6-you will certainly notice it-and start wondering why!

In Computer Vision, the non-accidentalness principle is used to compute detectability thresholds , and this will be explained in details in the following sections.

Now to give a first simple example of computation, let us consider a black square appearing in a pure binary noise image, as illustrated on Fig. 3.13.

Let U be a random image of size N × N pixels, and such that pixels are black (with probability p ) or white (with probability 1 - p ), all independently. What is the probability that U contains a k × k square of all black pixels? There is no easy exact answer to this question, since it involves counting events that may overlap. Now, let R be the random variable counting the number of k × k black squares in U . As just explained, we cannot easily compute exactly P (R ⩾ 1 ) , but thanks to Markov Inequality , we can bound it by the expectation of R :


<!-- p:104 -->


Fig. 3.13 Left: a pure binary noise image of size 64 × 64 pixels. It contains several 3 × 3 black squares, and we don't pay any special attention to them. Right: the same image but containing now a 8 × 8 black square. We immediately perceive it. The probability of observing such a square in a pure binary noise image is less than 2 × 10 - 16

$$\mathbb { P } ( R \geqslant 1 ) = \sum _ { r = 1 } ^ { + \infty } \mathbb { P } ( R = r ) \leqslant \sum _ { r = 0 } ^ { + \infty } r \mathbb { P } ( R = r ) = \mathbb { E } ( R ) .$$

And now E (R) is much easier to compute since

$$\mathbb { E } ( R ) = \mathbb { E } ( \sum _ { s q u a r e s } 1 _ { b l a c k } ) = N _ { s q } \mathbb { P } \left ( s q u a r e s \text { is all black} \right ) = N _ { s q } \, p ^ { k ^ { 2 } } ,$$

where Nsq = (N - k + 1 ) 2 is the number of k × k squares in a N × N grid.

This formula for E (R) allows us to compute thresholds, such as the minimal value of k such that E (R) becomes very small, that is less than ε , with ε = 10 - 3 for instance.

Let us consider the example of Fig. 3.13. Here we have N = 64 and p = 0 . 5. Then for k = 3, we can explicitly compute E (R) ≃ 7 . 5, and for k = 8 we get E (R) ≃ 2 × 10 - 16 . See the comment of the figure.

Now the link between thresholds computed this way and perceptual thresholds that could be tested by psychophysicists is a difficult, but interesting question. Some studies on this have been performed for instance by Blusseau, Grompone and collaborators in [4].


<!-- p:105 -->


### 3.2 A Contrario Method for the Detection of Geometric Structures in Images

The above simple computation is a first example of a general methodology to detect geometric structures in images. This methodology is called the a contrario method and it is closely related to statistical hypothesis testing. The aim here is not to have a statistical model of what an image is and use it as a prior in computations. Instead, we just need a simple statistical model (called the noise model, or background model, or a contrario model) of what the image is not , and we will perform tests to find the structures that show the image does not follow this noise model.

In this section, we will first give the general formulation of the a contrario methodology, and then we will give several instances of application of the methodology for detection purposes.

#### 3.2.1 General Formulation of a Contrario Methods

We give here the general formulation of the a contrario methodology. Here are the different steps:

- Given n geometric objects O 1 , . . . , On , let Xi be a random variable describing an attribute of the object Oi (for instance: its position, its color, its orientation, or its size, etc . . . ).
- Define an hypothesis H 0 (also called background distribution or noise model or a contrario model ): X 1 , . . . , Xn are independent identically distributed, following a 'simple' distribution (the uniform one in general).
- Observe an event E on a realization x 1 , . . . , xn of X 1 , . . . , Xn (for example: there is k such that x 1 , . . . , xk are very similar). Ask the question: Can this observed event happen by chance? (i.e. how likely is it under the null hypothesis H 0?)
- Perform a test. First define the Number of False Alarm of the event E by:

NFA (E) := E H 0 [ nb of occurrences of E ] .

$$\ N F A ( E ) \leqslant \varepsilon ,$$

where ε is a small number (less than 1).

- If the test is positive, then the observed event E is said to be an ε -meaningful event.

This a contrario methodology is very general and can be applied in several different frameworks. However each case is not straightforward, and we need to define precisely what are the objects, the attributes, the noise model and the observed events.

And then test


<!-- p:106 -->


#### 3.2.2 Detection of Alignments in an Image

Detecting alignments (i.e. straight segments) in an image is often one of the first steps for higher level object recognition. To do this task in the a contrario framework, we need to precisely define the considered events. An alignment in a grey level image will be defined as a group of aligned pixels such that the orientations of the image at these pixels are also aligned (at least approximately). For more details about this section, see [11] and [14].

##### 3.2.2.1 Definitions and First Properties

Let us consider a discrete grey level image u of size N × N pixels. At each pixel x = (x, y) we can compute the gradient of u by

$$\nabla u ( \mathbf x ) \coloneqq \frac { 1 } { 2 } \begin{pmatrix} u ( x + 1 , y + 1 ) + u ( x + 1 , y ) - u ( x , y + 1 ) - u ( x , y ) \\ u ( x + 1 , y + 1 ) + u ( x , y + 1 ) - u ( x + 1 , y ) - u ( x , y ) \end{pmatrix} .$$

Then, the direction at a point x is defined as

$$d ( x ) = \frac { \nabla u ( x ) ^ { \perp } } { \| \nabla u ( x ) \| } . \\$$

It is a vector of unit length, and we can write it, using complex number notations, as d ( x ) = e iθ( x ) , where θ( x ) ∈ [ 0 , 2 π) is then called the orientation at x . In the image, the gradient is orthogonal to level lines ('objects' in the image), and therefore the direction d will represent the tangent to the objects. Notice that here we forget the gradient amplitude, only its orientation is considered. This implies that we will detect straight segments independently of their contrast.

We define a discrete oriented segment S of length l as a sequence { x 1 , x 2 , . . . , x l } of l aligned pixels (meaning that there is an underlying continuous line going through them, see Fig. 3.14), that are 2-adjacent (meaning that we take them not contiguous, but at distance 2 such that their gradient are computed on disjoint neighborhoods). Such a segment is determined by its starting point (pixel) x 1 and its ending point (pixel) x l . As a consequence, the total number of segments in the image is finite. If we denote it by NS , then

$$N _ { S } = N ^ { 2 } ( N ^ { 2 } - 9 ) \simeq N ^ { 4 } ,$$

since an oriented segment is determined by its first point ( N 2 choices) and its last point ( N 2 - 9 choices because it cannot be an immediate neighbor of the first point).


<!-- p:107 -->


3

Fig. 3.14 A discrete oriented segment S , seen as a sequence { x 1 , x 2 , . . . , x l } of aligned pixels. Each pixel has an orientation θ( x ) , that is then compared to the orientation θ S of the segment S

Let us fix a precision p , that is a number in ( 0 , 1 / 4 ] (in general, it is taken in practice to be equal to 1 / 16). We say that a point x is aligned with a direction v up to precision p if

$$| \text {Angle} ( \mathbf d ( x ) , \mathbf v ) | \leqslant p \pi .$$

On a given segment S of length l , we count the number of points of S that are aligned with the direction of S up to precision p . If this number is high enough to be very unlikely under the null hypothesis H 0 (that we need to define), we will 'keep' the segment, as being a large deviation from randomness.

The null hypothesis H 0 is here: The orientations at the pixels are independent and uniformly distributed on [ 0 , 2 π) . Then, as a consequence, we have

$$\mathbb { P } _ { H _ { 0 } } [ \mathbf d ( \mathbf x ) \text { is aligned with } \mathbf v \text { up to precision } p ] = \frac { 2 \pi p } { 2 \pi } = p .$$

Lemma 3.1 If U is a white noise image (meaning that the grey levels are i.i.d. N (μ, σ 2 ) ), then the orientations θ( x ) are uniformly distributed on [ 0 , 2 π) . They are moreover independent at points taken at distance larger than 2 .

Proof Let us compute the law of ∇ U at a point x = (x, y) . Thanks to Formula (3.1), we have ∇ U( x ) = AX where X ∈ R 4 is the vector (U(x, y), U(x + 1 , y), U(x, y +


<!-- p:108 -->


1 ), U(x + 1 , y + 1 )) and A is the 2 × 4 matrix given by A = 1 2 ( - 1 1 - 1 1 - 1 - 1 1 1 ) . When

Let S = { x 1 , . . . , x l } be a discrete segment of length l (counted in independent points, i.e. at distance 2) in an image following the null hypothesis H 0 (that is for instance a Gaussian white noise image of size N × N ).

U is a white noise image of law N (μ, σ 2 ) , then X is a Gaussian vector of mean (μ, μ, μ, μ) and covariance σ 2 I 4 (where for n ⩾ 1, I n denotes the identity matrix of size n × n ). Therefore ∇ U( x ) is a Gaussian vector of mean A(μ,μ,μ,μ) = ( 0 , 0 ) and of covariance σ 2 AA T = σ 2 I 2. This shows that the gradient is an isotropic Gaussian vector, and as a consequence its orientation is uniformly distributed on [ 0 , 2 π) (and its amplitude follows a Rayleigh distribution of parameter σ ). ⊓ ⊔

Let Xi = 1 | θ S - θ( x i ) | ⩽ pπ be the random variable that has value 1 if x i is aligned with S up to precision p , and 0 otherwise. Then the Xi are independent and thanks to Eq. (3.2), they all follow a Bernoulli distribution of parameter p .

Let Sl = ∑ l i = 1 Xi be the number of aligned points with the direction of S , then:

$$\mathbb { P } _ { H _ { 0 } } [ S _ { l } = k ] = \binom { l } { k } p ^ { k } ( 1 - p ) ^ { l - k }$$

and then P H 0 [ Sl ⩾ k ] = B(l, k, p) := ∑ j ⩾ k ( l j ) p j ( 1 - p) l - j ,

where B(l, k, p) denotes the tail of the binomial distribution of parameters l and p . We can now give the main definition, that is the one of ε -meaningful segments.

Definition 3.1 Let S be a segment of length l( S ) containing k( S ) aligned points (for the precision p ). The number of false alarms (NFA) of S is defined by

$$\ N F A ( S ) & = N F A ( l ( S ) , k ( S ) ) \colon = N ^ { 4 } \times B ( l ( S ) , k ( S ) , p ) \\ & = N ^ { 4 } \times \sum _ { k = k ( S ) } ^ { l ( S ) } \binom { l ( S ) } { k } p ^ { k } ( 1 - p ) ^ { l ( S ) - k } .$$

$$k = k ( S )$$

Let ε &gt; 0, be a (small) positive number. When NFA ( S ) ⩽ ε , then the segment is said ε -meaningful. This is equivalent to have k( S ) ⩾ k min (l( S )) , where

$$k _ { \min } ( l ) \colon = \min \left \{ k \in \mathbb { N } , \ B ( l , k , p ) \leqslant \frac { \varepsilon } { N ^ { 4 } } \right \} .$$

The main property of ε -meaningful segments is that, on the average, we will not observe more than ε such segments in images following the H 0 hypothesis (for instance in a Gaussian white noise image). More precisely, we have the following proposition.


<!-- p:109 -->


3

Proposition 3.1 The expectation of the number of ε -meaningful segments in a random image of size N × N pixels following the null hypothesis H 0 , is less than ε .

Proof Let NS be the number of segments in the N × N image. Let ei = 1 if the i -th segment of the image is ε -meaningful, and 0 otherwise. Let R be the number of ε -meaningful segments in the image. Then

$$\mathbb { E } _ { H _ { 0 } } [ R ] & = \sum _ { i = 1 } ^ { N _ { S } } \mathbb { E } [ e _ { i } ] = \sum _ { i = 1 } ^ { N _ { S } } \mathbb { P } _ { H _ { 0 } } [ S _ { l _ { i } } \geqslant k _ { \min } ( l _ { i } ) ] \\ & = \sum _ { i = 1 } ^ { N _ { S } } B ( l _ { i } , k _ { \min } ( l _ { i } ) , p ) \leqslant N _ { S } \times \frac { \varepsilon } { N ^ { 4 } } \leqslant \varepsilon .$$

⊓ ⊔

The number NFA ( S ) measures the degree of confidence, or the 'meaningfulness' of an observed alignment. The smaller NFA ( S ) is, the more meaningful the segment S is, since it has a smaller probability of having arised just by chance.

Notice also that the NFA ( S ) is related to the so-called Per Family Error Rate in Statistics, when multiple tests are performed and a Bonferroni correction is applied.

Using elementary properties of the binomial distribution, we can easily deduce some elementary properties of the NFA, such that:

1. NFA (l, 0 ) = N 4 . It means that a segment containing 0 aligned points will never be meaningful (this is quite natural and expected!).
2. NFA (l, l) = N 4 p l . It implies that, in order to be ε -meaningful, a segment has to be of length larger than 4 log N - log ε - log p . For instance for N = 512, p = 1 / 16 and ε = 1, we have l ⩾ 9 (that is a 'true' length of at least 18 pixels).
3. NFA (l, k + 1 ) &lt; NFA (l, k). It means that when two segments have the same length, the most meaningful one (i.e. the one with the smallest NFA) is the one that has the largest number of aligned points. Again this is quite normal and expected.
4. NFA (l, k) &lt; NFA (l + 1 , k) . It can be interpreted by saying that if one considers a segment, and then extends it with a non-aligned point, then one increases the NFA. Also, if one removes a non-aligned point from a segment, one decreases its NFA.
5. NFA (l + 1 , k + 1 ) &lt; NFA (l, k) . This is the opposite situation: here, if one extends the segment with an aligned point, then one decreases its NFA. Or, also, if one removes an aligned point from a segment, one increases its NFA.

##### 3.2.2.2 Maximality

In the previous section, we have seen the definition of meaningful segments. Now, when a segment S is 'very' meaningful (that is NFA ( S ) ≪ ε ), then many segments that contain it or that are contained in it, will also be meaningful. Therefore the detections that we obtain in an image are redundant, and some of the detected segments are just the consequence of a very meaningful segment. This is why we need to introduce a notion of 'maximality', that is defined as follows (see also [13] for more details about this part).


<!-- p:110 -->


Definition 3.2 A segment S is said maximal meaningful if it is meaningful and if

∀ segment S ′ ⊂ S , NFA ( S ′ ) ⩾ NFA ( S ), ∀ segment S ′ ⊃ S , NFA ( S ′ ) &gt; NFA ( S ).

In other words, maximal meaningful segments are local minima of the NFA for the relationship of inclusion.

Thanks to the elementary properties of the NFA, we immediately have the two following properties of maximal meaningful segments:

- The two ending points of S are aligned with S ,
- The two 'adjacent' points to S (i.e. one 'before' and one 'after' S ), are not aligned with S .

The difference between meaningful segments and maximal meaningful ones is illustrated on Fig. 3.15.

In fact, maximal meaningful segments have strong structural properties, mainly the one of being disjoint when lying on the same straight line. This property has been numerically checked for segments of length l up to 256 (see [14]), but the general result is still an open conjecture that can be stated as follows:

Conjecture If S 1 and S 2 are two distinct meaningful segments lying on the same straight line, and such that S 1 ∩ S 2 ̸= ∅ , then

min ( NFA (S 1 ∪ S 2 ), NFA (S 1 ∩ S 2 )) &lt; max ( NFA (S 1 ), NFA (S 2 )).

Fig. 3.15 From left to right: an image, all its ε -meaningful segments (with ε = 10 - 3 ), its maximal meaningful segments

<!-- p:111 -->


3

Fig. 3.16 Left: an original image (a painting by Uccello). Middle: the maximal meaningful segments. Right: result of the LSD algorithm (only the middle line of the meaningful regions are shown)

As a direct consequence of this conjecture, we would have that indeed two maximal meaningful segments lying on the same straight line cannot meet.

Let us also remark that the above conjecture is equivalent to say that

$$\min ( B ( l _ { 1 } + l _ { 2 } - l _ { \cap } , k _ { 1 } + k _ { 2 } - k _ { \cap } , \, p ) , \, B ( l _ { \cap } , k _ { \cap } , p ) ) \, < \max ( B ( l _ { 1 } , k _ { 1 } , \, p ) , \, B ( l _ { 2 } , k _ { 2 } , \, p ) ) ,$$

where l ∩ and k ∩ (resp. l ∪ and k ∪ ) denote the length and the number of aligned points of S 1 ∩ S 2 (resp. of S 1 ∪ S 2). Such a result may seem simple, it is however not so easy, and we haven't found a proof for it (see [14] for developments on this conjecture).

As shown on Figs. 3.15 and 3.16 (middle), the maximal meaningful segments found in an image are 'satisfactory' from a perceptual viewpoint. Now, since the method is based on an almost exhaustive testing of all segments of the image (there are however some properties that can be used to have a not so complex algorithm), it has the drawbacks that it is quite slow, and we often get 'bundles' of segments. An elegant solution to these two points has been proposed by Grompone et al. in [21]. It is based on the idea of considering directly 'thick' segments (rectangles), and it is explained in the following subsection.

##### 3.2.2.3 The Line Segment Detector Algorithm

The Line Segment Detector (LSD) Algorithm proposed by Grompone et al. in [21] can be summarized the following way:

1. Partition of the image (of size N × N pixels) into Line-Support Regions (connected sets of pixels sharing the same orientation up to precision pπ ).
2. Approximate these sets by rectangular regions.
3. Compute the NFA of each region: for a region (rectangle) r containing l( r ) points with k( r ) of them aligned with it (i.e. aligned with the principal orientation of r up to precision pπ ), define

$$N F A ( \mathbf r ) = N ^ { 5 } \times B ( l ( \mathbf r ) , k ( \mathbf r ) , p ) .$$

4. The rectangular regions r such that NFA ( r ) &lt; 1 are kept (meaningful regions).


<!-- p:112 -->


The definition of meaningful regions in the LSD algorithm is very similar to the one of meaningful segments given in Definition 3.1. Here ε is fixed to 1, and the number of tests is now N 5 , that is (approximately) the number of possible rectangles in a N × N image. Thanks to its first step, the LSD algorithm is able to directly identify the candidate meaningful regions, without the need of an exhaustive search. It makes therefore the algorithm much faster than the one of meaningful segments, and the results are much 'cleaner'. This is illustrated on Fig. 3.16.

The LSD algorithm can be tested online [22] on the website of the Image Processing On Line (IPOL) journal (http://www.ipol.im/), whose aim is to emphasize the role of mathematics as a source for algorithm design and the reproducibility of the research .

Remark The methodology and the definitions for meaningful segments (or rectangles) can be easily extended to other parametric curves, such as arcs of circle for instance. More generally, the a contrario methodology can be used to find meaningful peaks in the so-called Hough Transform (see [23] for an historical viewpoint on the Hough Transform).

#### 3.2.3 Detection of Contrasted or Smooth Curves

##### 3.2.3.1 Meaningful Boundaries

It is a classical problem in Image Processing to find the boundaries (contours) in an image. This problem is generally called the edge detection problem. In order to apply the a contrario methodology to this problem, we first need to consider 'test objects', that will be curves here. Now, we don't want to restrict ourselves to parametric curves, and it is also impossible to consider all possible curves in an image. Since we are interested in curves that will have a contrast across them, some natural candidates are the level lines of the image (or pieces of them). Let us first recall how they are defined.

Definition 3.3 Let Ω be a discrete domain (rectangle of Z 2 ), and let u : Ω → R be a grey level image. The upper- and lower-level sets of u are respectively the sets defined for all λ ∈ R by

$$\chi _ { \lambda } ( u ) = \{ x \in \Omega \, ; \, u ( x ) \geqslant \lambda \} \quad \text {and} \quad \chi ^ { \lambda } ( u ) = \{ x \in \Omega \, ; \, u ( x ) \leqslant \lambda \} .$$

The level lines of u are then defined as being the (discrete) topological boundaries of its level sets.

Notice that the upper-level sets are decreasing: ∀ λ ⩽ μ, χμ ⊂ χλ , whereas the lower-level sets are increasing: ∀ λ ⩽ μ, χ λ ⊂ χ μ . The knowledge of all the upper (resp. lower)-level sets is enough to reconstruct u by for instance

$$u ( x ) = \sup \{ \lambda \, ; \, x \in \chi _ { \lambda } \} .$$


<!-- p:113 -->


Fig. 3.17 Left: an image (the church of Valbonne, source: INRIA). The grey levels are taking value in the range { 0 , 1 , . . . , 255 } . Right: the level lines corresponding to levels λ multiple of 6

Another interesting property of the level sets is that they are globally invariant to contrast changes. More precisely, if g is a change of contrast (i.e. an increasing function), then u and g(u) globally have the same level sets, since ∀ λ ∃ μ such that χλ(u) = χμ(g(u)) .

On Fig. 3.17, we show an example of an image and some of its level lines. We don't show all the level lines because they would cover entirely the image. A reader interested in making its own experiments on level lines can use the Image Processing On Line demo on 'Image Curvature Microscope' [9].

Let u be a discrete grey level image of size N × N and let Nll be the (finite) number of level lines it contains. Let L be a level line of u . It is a sequence of pixels such that each of them is neighbor of the previous one. In this sequence, we keep only points at distance 2, and then identify L with this sub-sequence of pixels, that is L = { x 1 , . . . , x l } , and l is called the length of L . We define the contrast of u at a point x by

$$c ( x ) = \| \nabla u ( x ) \| ,$$

where ∇ u is the gradient of u (computed for instance on a 2 × 2 neighbourhood as in the case of segments). Notice that we only consider here the amplitude of the gradient. Its orientation is almost already known, since it is orthogonal to the level lines (at least when considering an underlying continuous framework).

We can now define meaningful boundaries in an image. More details about all this can be found in [12]. Roughly speaking, a meaningful boundary is a level line that is long enough and contrasted enough not to appear just by chance. It is more precisely defined the following way.


<!-- p:114 -->


Definition 3.4 Let u be an image of size N × N , containing Nll level lines. Let H be the empirical gradient amplitude distribution in u given by

$$H ( \mu ) = \frac { 1 } { N ^ { 2 } } \, \# \{ x \, ; \, \| \nabla u ( x ) \| \geqslant \mu \}$$

We define the Number of False Alarms of a level line L with discrete length l and minimal contrast μ = min x ∈ L c( x ) by

$$\ N F A ( L ) = N _ { l l } \times H ( \mu ) ^ { l } .$$

The level line L is said to be an ε -meaningful boundary iff NFA (L) ⩽ ε .

Here the underlying a contrario model H 0 is given by: the contrasts at points taken at distance at least 2 are independent and distributed according to H (that is given by Eq. (3.3)). Notice that this is a noise model on the contrasts but not on the image itself. It is indeed not clear what image noise model it corresponds to (if it exists).

Meaningful boundaries have several interesting properties, that are direct consequences of their definition:

- The ε -meaningful boundaries are invariant under affine contrast changes (that is u and g(u) have exactly the same ε -meaningful boundaries when g is of the form g(t) = at + b , with a &gt; 0).
- If μ ⩽ μ ′ and l is fixed, then H(μ) l ⩾ H(μ ′ ) l . Therefore if two level lines have the same length, the most contrasted one has the smallest NFA.
- If l ⩽ l ′ and μ is fixed, then H(μ) l ⩾ H(μ) l ′ . Therefore if two level lines have the same contrast, the longest one has the smallest NFA.
- A level line with minimal contrast μ is ε -meaningful iff its length is larger than

$$l _ { \min } ( \mu ) = \frac { \log \varepsilon - \log N _ { l l } } { \log H ( \mu ) } .$$

- A level line with length l is ε -meaningful iff its minimal contrast μ is larger than

$$\mu _ { \min } ( l ) = H ^ { - 1 } \left ( \left ( \frac { \varepsilon } { N _ { l l } } \right ) ^ { 1 / l } \right ) .$$

As in the case of segments, meaningful level lines are often organized in 'bundles'. When a contrasted 'object' is present in the image, many parallel level lines representing the contour of this object will be detected (see for instance Fig. 3.18-middle). Therefore, we also need to define here a notion of maximality. As for segments, maximal meaningful level lines will be defined as being local


<!-- p:115 -->


3

Fig. 3.18 On the left, the original image. On the middle, all meaningful boundaries with ε = 1. On the right, all maximal meaningful boundaries with ε = 1

minima of the NFA for the relationship of inclusion. Here the natural organization of level sets (and therefore of level lines) is a tree structure, and we will consider 'branches' in this tree. More precisely, the definition of maximal meaningful boundaries is the following.

Definition 3.5 Amonotonicbranch in the tree of level lines is a branch along which the grey level is monotonic and such that each level line has a unique child. A monotonic branch is maximal if it is not contained in another monotonic branch. A level line is a maximal meaningful boundary if it is meaningful and if its NFA is minimal in its maximal monotonic branch of the tree of level lines.

An example of an image, its meaningful boundaries and the maximal meaningful ones is given on Fig. 3.18. On this figure, one can clearly see how the notion of maximality helps to describe in an 'optimal' way the set of meaningful boundaries of the image.

##### 3.2.3.2 Meaningful Good Continuations

The goal here will be to look for 'smooth' curves in the image, without considering the contrast along the curve. The content of this section is taken from the work of Cao in [7].

Since all curves are discrete (they are sequences of pixels), the definition of smoothness has to be adapted. Here a discrete curvature will be defined, and a smooth curve will be a curve such that its curvature is 'small'. The precise value of 'small' will be obtained by applying the a contrario methodology.


<!-- p:116 -->


Fig. 3.19 A discrete curve Γ is a sequence of points p 0 , . . . , p l + 1, and we define its maximal discrete curvature by Eq. (3.4)

The framework is the following. Let Γ = (p 0 , . . . , p l + 1 ) be a discrete curve of length l , and let κ be its maximal discrete curvature defined by

$$\kappa _ { \Gamma } = \max _ { 1 \leqslant i \leqslant l } | \text {Angle} ( p _ { i + 1 } - p _ { i } , p _ { i } - p _ { i - 1 } ) | = \max _ { 1 \leqslant i \leqslant l } | \theta _ { i } | ,$$

as illustrated on Fig. 3.19.

The a contrario noise model H 0 is here: the angles θi are i.i.d. with uniform law on [- π, π) , i.e. the curve is a discrete 'random walk'. Under the a contrario noise model, the probability of having l angles θi smaller than an observed value κ is

$$\mathbb { P } ( \forall 1 \leqslant i \leqslant l , \ | \theta _ { i } | \leqslant \kappa ) = \prod _ { i = 1 } ^ { l } \mathbb { P } ( | \theta _ { i } | \leqslant \kappa ) = \left ( \frac { \kappa } { \pi } \right ) ^ { l } .$$

As in all other applications of the a contrario methodology, we have to take into account the total number of 'tests' that are made. Let thus Nc be the number of considered curves in the image. In practice, it will be the number of pieces of level lines in the image. We can now state the definition of meaningful good continuations.

Definition 3.6 We say that a discrete curve Γ is an ε -meaningful good continuation if

$$\kappa _ { \Gamma } < \frac { \pi } { 2 } \quad \text {and} \quad N F A ( \Gamma ) = N _ { c } \left ( \frac { \kappa _ { \Gamma } } { \pi } \right ) ^ { l } \leqslant \varepsilon .$$

As for segments, a meaningful good continuation with a very small NFA (i.e. much less than ε ) will generate many other meaningful good continuations that are else contained or included in it. Therefore we again need here to define a notion of maximality.

Definition 3.7 Let G be a set of (discrete) curves. A meaningful good continuation Γ ∈ G is maximal meaningful if it is meaningful and if

$$\forall \Gamma ^ { \prime } \subset \Gamma , \, N F A ( \Gamma ^ { \prime } ) \geq N F A ( \Gamma ) \quad \text {and} \quad \forall \Gamma ^ { \prime } \supseteq \Gamma , \, N F A ( \Gamma ^ { \prime } ) > N F A ( \Gamma ) .$$


<!-- p:117 -->


3

Fig. 3.20 Left: Image of the Church of Valbonne. Middle: Maximal meaningful good continuations. Right: Maximal meaningful contrasted boundaries

As a consequence, if G is the set of connected pieces of level lines of an image, then if Γ and Γ ′ are two maximal meaningful good continuations belonging to the same level line, we necessarily have that

$$\Gamma \cap \Gamma ^ { \prime } = \emptyset .$$

This directly comes from the fact that if Γ ∩ Γ ′ ̸= ∅ , then the curve Γ ∪ Γ ′ is an element of G . It has a length larger than l and l ′ with a maximal curvature less than κΓ or κΓ ′ . Therefore its NFA is less than the one of Γ or of Γ ′ , which contradicts the maximality of Γ or of Γ ′ .

An example of maximal meaningful good continuations on an image is given on Fig. 3.20-middle, where we also show, for comparison, the maximal meaningful boundaries. What is quite remarkable is that for good continuations we recover the boundaries of the 'hand-made' objects present in the image (the church, the cars, but not the tree!), independently of their contrast. Indeed this is a direct consequence of the (in general) smoothness of hand-made objects. A not so smooth object would not be detected.

In the case of meaningful straight segments detection, we saw that the LSD algorithm was an elegant, efficient and fast solution to obtain a 'clean' set of segments. Similarly here for good continuations, Grompone and Randall have proposed a smooth contour detection algorithm, that can be tested online [20].


<!-- p:118 -->


#### 3.2.4 Detection of Vanishing Points

In the a contrario methodology, one often has to compute the probability of appearance of such or such geometric event. These are typical questions of stochastic geometry. One of the main and characteristic example is the detection of vanishing points in an image, that we are going to develop in this section and that is inspired by the paper of Almansa et al. [2].

In a pinhole camera model, parallel straight lines in 3D are projected on the image plane as 2D lines that intersect at a single point. This principle is used, for instance by painters, to create perspective effects in paintings. The intersection points are called vanishing points . To detect them, we start from elementary straight segments detected in the image (by the LSD algorithm of Sect. 3.2.2.3 for instance), and then we look for regions in the image plane (inside or outside the image domain), such that 'a lot of' segments converge towards these regions. As in the other examples, we will use the a contrario methodology to define 'a lot of' as a mathematical threshold.

Let Ω be the image domain and let N be the number of elementary segments detected in the image. Let D 1 , . . . DN be the support lines of the N segments. We define a noise model H 0, that is here: 'The N lines are i.i.d. uniform'. Then, we will look for regions that are intersected by significantly more support lines than the number expected under H 0. We first need to explain what is the uniform distribution on the lines of the image. A line G of the plane is parametrized by its two polar coordinates: ρ ⩾ 0 and θ ∈ [ 0 , 2 π) . That is

$$G = G ( \rho , \theta ) = \{ ( x , y ) \in \mathbb { R } ^ { 2 } \ s . t . \ x \cos \theta + y \sin \theta = \rho \} .$$

Then, there exists a unique (up to a positive multiplicative constant) measure on the set of lines that is invariant under translations and rotations. It is the Poincaré measure given by (see for instance the book of Santalo [37]):

$$d \mu = d \rho \, d \theta .$$

This measure will be called the uniform measure on lines.

To detect meaningful vanishing regions, and since it is impossible to test all possible regions of the plane, we choose a partition of the plane R 2 into a finite number M of regions (we will see later how to construct this partition):

$$\mathbb { R } ^ { 2 } = \bigcup _ { j = 1 } ^ { M } V _ { j } .$$


<!-- p:119 -->


3

Definition 3.8 Let Vj be a region and let kj = # { Di s.t. Di ∩ Vj ̸= ∅} . The Number of False Alarms of Vj is defined by

$$N F A ( V _ { j } ) \coloneqq M \times B ( N , k _ { j } , p _ { j } ) = M \times \sum _ { k = k _ { j } } ^ { N } \binom { N } { k } p _ { j } ^ { k } ( 1 - p _ { j } ) ^ { N - k } ,$$

where pj is the probability that a random line (under dμ ) going through the image domain Ω also meets Vj . When NFA (Vj ) ⩽ ε , then we say that the region Vj is ε -meaningful.

As usual in the a contrario methodology, we have the main property that, under H 0, the expected number of ε -meaningful regions is less than ε .

Now, two questions remain: determine a 'good partition' of the plane, and compute pj . Computing pj is a typical question of stochastic geometry. It uses the following results (that can be found in [37]):

- Let K ⊂ R 2 be a bounded closed convex set with non-empty interior. Then

$$\mu \left ( \{ ( \rho , \theta ) \ s . t . \ G ( \rho , \theta ) \cap K \neq \emptyset \} \right ) = \text {Per} ( K ) ,$$

where Per (K) is the perimeter of K (= length of the boundary).

- Let K 1 and K 2 be two bounded closed convex sets with non-empty interior. Then

$$\mu \left ( \{ ( \rho , \theta ) \ s . t . \ G ( \rho , \theta ) \cap K _ { 1 } \neq \emptyset \, \text { and } G \cap K _ { 2 } \neq \emptyset \} \right ) \\ = \begin{cases} \text {Per} ( K _ { 1 } ) & \text { if } K _ { 1 } \subset K _ { 2 } , \\ L _ { i } - L _ { e } & \text { if } K _ { 1 } \cap K _ { 2 } = \emptyset , \\ \text { Per} ( K _ { 1 } ) + \text { Per} ( K _ { 2 } ) - L _ { e } & \text { otherwise.} \end{cases} \\ \text {where } L _ { i } \text { and } L _ { e } \text { respectively denote the interior perimeter and the exterior}$$

where Li and Le respectively denote the interior perimeter and the exterior perimeter of K 1 and K 2 (see Fig. 3.21).

Fig. 3.21 The exterior perimeter is the perimeter of the convex hull of K 1 ∪ K 2. For the interior perimeter, the definition is less simple, but one can see it as the length of an elastic band drawing an '8' around K 1 and K 2

<!-- p:120 -->


To choose the plane partition, we want to satisfy two constraints. The first one is that we would like to have all pj equal. This will imply that all regions are equally detectable, meaning that they require the same minimal number of lines passing through them in order to become meaningful. The second constraint is about angular precision. Indeed, because of the pixelization of the image, the support line of a segment of length l (counted in pixels) is rather a cone of angle dθ = arcsin 1 l ≃ 1 l . Therefore, regions that are far away from the image domain Ω need to be larger than regions inside or close to Ω .

Finally, using the two above constraints, we propose (see [2]) to construct the partition of the plane the following way. We assume that the image domain is a disk of radius R , centered at the origin 0, that is Ω = D( 0 , R) (otherwise we include it in such a disk). We fix an angle θ . The interior regions are simply chosen as squares of side length 2 R sin θ . This implies by Eq. (3.5) that

$$p _ { j } = \frac { \text {Per} ( V _ { j } ) } { \text {Per} ( \Omega ) } = \frac { 4 \sin \theta } { \pi } \colon = p _ { \theta } .$$

The exterior regions are then defined as portions of circular sectors with angle 2 θ and determined by two distances d and d ′ .

Given a region Vd,d ′ , portion of a circular sector between the distances d and d ′ &gt; d , then we can compute the probability that a random line intersects it knowing that it intersects Ω . Thanks to Eqs. (3.5) and (3.6) (see also Fig. 3.22) it is given by

$$p _ { V _ { d , d ^ { \prime } } } = \frac { L _ { i } - L _ { e } } { \text {Per} ( \Omega ) } = \frac { 1 } { \pi } \left ( \tan \beta - \tan \beta ^ { \prime } + \frac { 1 } { \cos \beta ^ { \prime } } - \frac { 1 } { \cos \beta } + \beta ^ { \prime } - \beta + 2 \theta \right ) ,$$

where β = arccos ( R d cos θ ) and β ′ = arccos ( R d ′ cos θ ) .

Fig. 3.22 Constructing the regions Vj of the partition of the plane

<!-- p:121 -->


We can now exactly determine the exterior regions: we start with d 1 = R , then set d 2 &gt; d 1 such that pVd 1 ,d 2 = pθ , then d 3 &gt; d 2 such that pVd 2 ,d 3 = pθ , and so on, until being larger than d ∞ , that is finite and characterized by

$$\forall d ^ { \prime } > d _ { \infty } , \ p _ { V _ { d _ { \infty } , d ^ { \prime } } } < p _ { \theta } .$$

The last region is thus infinite and its probability is &lt; pθ .

Now, how to choose θ ? In order to have a good balance between detectability and localization, we don't fix a single value for θ , we instead use several values, having thus a multiscale approach. More precisely, we choose n angular values θs = 2 π 2 s with s = 4 , 5 , . . . , n + 3. For each θs , we have a 'partition' (there is some overlap between interior and exterior regions near the boundary of Ω ) of the image plane into Ms regions: R 2 = ∪ Ms j = 1 Vj,s .

Definition 3.9 The number of false alarms of a region is then defined as

$$N F A ( V _ { j , s } ) = n \cdot M _ { s } \cdot B ( N _ { s } , k ( V _ { j , s } ) , p _ { \theta _ { s } } ) ,$$

where Ns is the number of segments (among the N ) having a precision at least θs and k(Vj,s ) is the number of support lines (among the Ns ) that meet the region Vj,s . The region Vj,s is said ε -meaningful iff NFA (Vj,s ) ⩽ ε .

As in all other applications of the a contrario methodology, we need to define a notion of maximality, related to local minima of the NFA. Indeed, when a lot of lines pass through a region Vj,s , then the neighbouring regions are also intersected by a lot of lines. We therefore need to select 'the best regions'.

Definition 3.10 The region Vj,s is said maximal ε -meaningful if it is ε -meaningful and if

$$\forall s ^ { \prime } \in [ s _ { 1 } , \dots , s _ { n } ] , \quad \forall j ^ { \prime } \in [ 1 , \dots , M _ { s ^ { \prime } } ] , \\ \overline { V _ { j ^ { \prime } , s ^ { \prime } } } \cap \overline { V _ { j , s } } \neq \emptyset \Longrightarrow \partial F A ( V _ { j , s } ) \leqslant N F A ( V _ { j ^ { \prime } , s ^ { \prime } } ) .$$

Examples of results of maximal meaningful regions are shown on Fig. 3.23. This example also allows us to vizualise the partition of the plane that is used.

#### 3.2.5 Detection of the Similarity of a Scalar Attribute

Wehavealready seen several instances of application of the a contrario methodology with the definition of a Number of False Alarms (NFA) in each case: detection of segments, of contrasted curves (boundaries), of good continuations and of vanishing regions. Let us here be interested in the detection of the elementary Gestalt grouping law of similarity of a scalar attribute like grey level, or orientation, or size for instance.


<!-- p:122 -->


-log 10 (NFA) = 90.7943, angular precision = 256

Fig. 3.23 An image (a building in Cachan), and its maximal meaningful regions. The most meaningful region is far away from the image domain, it is at 'infinity' and corresponds to the set of (almost) parallel vertical lines in this image. For the two other maximal meaningful regions, the figures allow us to also see where they are among the exterior regions of the partition of the plane

The framework is the following. We assume we have M 'objects', and each of them has an 'attribute' q ∈ { 1 , 2 , . . . , L } . It can be its grey level, its orientation, its size. Let us consider the group Ga,b of objects that have their scalar attribute q such that a ⩽ q ⩽ b . Let k(a, b) denote the cardinal of Ga,b . Then, we can define its Number of False Alarm by

$$\ N F A ( G _ { a , b } ) = \text {NFA} ( [ a , b ] ) = \frac { L ( L + 1 ) } { 2 } \cdot B \left ( M , k ( a , b ) , \frac { b - a + 1 } { L } \right ) ,$$

where, as in Sect. 3.2.2, B(M,k,p) denotes the tail of the binomial distribution of parameters M and p . The number of tests is here L(L + 1 ) 2 , it corresponds to the number of discrete intervals in { 1 , 2 , . . . , L } . Here again we can define a notion of maximality, saying that an interval (and therefore the corresponding group of objects) is maximal meaningful if its number of false alarms is minimal among the ones of all intervals that contain it or are contained in it.


<!-- p:123 -->


3

0

50

100

150

200

300

250

Fig. 3.24 Left: the original image. Middle: the histogram of grey levels. It contains one maximal meaningful interval, the interval [ 70 , 175 ] . Right: quantized image obtained by quantifying the grey levels of the original image by the quantization function g given by g(λ) = 0 (black) if λ &lt; 70, g(λ) = 128 (grey) if 70 ⩽ λ ⩽ 175, and g(λ) = 255 (white) if λ &gt; 175

Afirst example of application is the study of the grey level histogram of an image. The 'objects' here are simply the pixels of the image, and their attribute is their grey level. Looking for the maximal meaningful intervals is a way to obtain an automatic histogram segmentation, and therefore a grey level quantization, as illustrated on Fig. 3.24.

A second example of application is a key point in the Gestalt theory: the recursivity of elementary grouping laws. The example is presented on Fig. 3.25. Here the considered attribute is the size (area) of the objects that are blobs detected thanks to their meaningful boundaries (Sect. 3.2.3.1).

#### 3.2.6 Discussion

In the previous sections we have seen many examples of detection of geometric structures in images, based on the a contrario methodology. This methodology is a powerful computational tool that is the result of the combination of the nonaccidentalness principle (Helmholtz principle) with the Gestalt theory of grouping laws. But beyond these detection problems, the a contrario framework has also been used for many other tasks in image processing such as: shape recognition (Musé et al. [31]), image matching (Rabin et al. [35]), epipolar geometry(Moisan and Stival [30]), motion detection and analysis (Veit et al. [41]), clustering (Cao et al. [8]), stereovision (Sabater et al. [36]), image denoising by grain filters (Coupier et al. [10]), etc.


<!-- p:124 -->


Fig. 3.25 Gestalt grouping principles at work for building an 'order 3' gestalt (alignment of blobs of the same size). First row: original DNA image (left) and its maximal meaningful boundaries (right). Second row: left, barycenters of all meaningful regions whose area is inside the only maximal meaningful mode of the histogram of areas; right, meaningful alignments of these points

### 3.3 Stochastic Models of Images: The Problem of Modeling and Synthesizing Texture Images

In the previous sections about a contrario methodology, we needed to define a model of what the image was not (the so-called a contrario noise model). In most cases, the model was just 'generalized uniform noise' (roughly saying that grey levels, orientations, lines, etc. are i.i.d. uniform). Here, at the opposite, we want to build models of what an image is. A typical example of the problem of modeling 'natural' images in a stochastic framework is the case of texture images.

Many illustrations and parts of the text of this section have been prepared by Bruno Galerne 1 (MAP5, Université Paris Descartes), and are taken from the lectures that we give in the Master 2 program MVA (Mathematics, Vision, Learning) at the ENS Cachan, Université Paris-Saclay.

1 Many thanks to him!


<!-- p:125 -->


#### 3.3.1 What is a Texture Image?

There is no clear mathematical unique definition of what a texture image is. We can just give a very general definition: a texture image is the realization of a random field, where a (more or less) random pattern is repeated in a (more or less) random way.

In fact, one of the main difficulties with texture images is that they have a huge variety of appearance. They can be roughly divided in two main classes: micro-textures (constitued of small non-discernible objects) and macro-textures (constitued of small but discernible objects). As illustrated on Fig. 3.26, a same scene, depending on the scale of observation, can generate images of various aspects, going from a micro-texture to a macro-texture, and even to an image that is not a texture anymore.

#### 3.3.2 Texture Synthesis

One of the main question with texture images is the problem of texture synthesis. This problem can be stated as follows: given an input texture image, produce a new output texture image being both visually similar to and pixel-wise different from the input texture. The output image should ideally be perceived as another part of the same large piece of homogeneous material the input texture is taken from (see Fig. 3.27). Texture synthesis is a very common issue in Computer Graphics, and it has a lot of applications for animated films or video games.

Fig. 3.26 Depending on the viewing distance (the scale), the same scene can be perceived either as from left to right: ( a ) a micro-texture, ( b ) a macro-texture, or ( c ) a collection of individual objects (some pebbles)

<!-- p:126 -->


Fig. 3.27 The problem of texture synthesis: produce an image that should be perceived as another part of the same large piece of homogeneous material the input texture is taken from

Texture synthesis algorithms can be roughly divided in two main classes: the neighborhood-based synthesis algorithms (or 'copy-paste' algorithms) and the statistical constraints-based algorithms.

The general idea of neighborhood-based synthesis algorithms ('copy-paste' algorithms) is to compute sequentially an output texture such that each patch of the output corresponds to a patch of the input texture. Many variants have been proposed by: changing the scanning orders, growing pixel by pixel or patch by patch, doing a multiscale synthesis, choosing a different optimization procedure, etc. The main properties of these algorithms is that they synthesize well macro-textures, but they can have some speed and stability issues, and it is difficult to set the parameters values.

The 'father' of all these algorithms is the famous Efros-Leung algorithm [16]. Its general idea relies on the Markov property assumption for the texture image I , and its aim is to provide an estimate of the probability of I ( x ) knowing I (N( x )) , where N( x ) denotes a neighborhood of x . To do this, it just searches in the input original image all similar neighborhoods, and that is then used as an estimate of the probability distribution of I ( x ) knowing its neighborhood. Finally, to sample from this probability distribution, it just picks one match at random. More precisely, the algorithm works as follows:

1. Input: original texture image I 0, size of the output image I , size of the neighborhood, precision parameter ε ( = 0 . 1 in general).
2. Initialize I : take a random patch from I 0 and put it somewhere in I .
3. While the output I is not filled:
4. (a) Pick an unknown pixel x in I with maximal known neighbor pixels, denoted N( x ) .


<!-- p:127 -->


###### (b) Compute the set of y in I 0 such that

$$d ( I _ { 0 } ( N ( y ) ) , I ( N ( \mathbf x ) ) ) \leqslant ( 1 + \varepsilon ) \min _ { \mathfrak z } d ( I _ { 0 } ( N ( \mathbf z ) ) , I ( N ( \mathbf x ) ) ) ,$$

where d is the L 2 distance.

- (c) Randomly pick one of these y and set I ( x ) = I 0 ( y ) .

The mathematical analysis of this algorithm has been performed in [26], where they write it as a nonparametric algorithm for bootstrapping a stationary random field, and they show consistency results.

On Fig. 3.28, we show some examples of results obtained by this algorithm. In general, the results are visually impressive. They are however very sensitive to the size of the neighborhood, and one can sometimes observe two main failings of the method: it can produce 'garbage' (it has 'lost' the structures of the image and generates things that look like 'noise') and it also often produces verbatim copy of the original image (large parts of the original image are reproduced as they are in the output image, resulting in a very limited statistical innovation).

Fig. 3.28 Some results of the Efros-Leung texture synthesis algorithm, obtained from IPOL online demo [1]. Left column, the original input images: pebbles (size 128 × 128), cells (size 64 × 64) and fabric (size 256 × 256). Second and third column: outputs (all of size 256 × 256) generated by the Efros-Leung algorithm, with respective neighborhood size 5 × 5 and 11 × 11

<!-- p:128 -->


In the other class of texture synthesis algorithms (the ones based on statistical constraints), the aim is to try to build a statistical model of the image. In a generic way, these algorithms work as follows:

1. Extract some meaningful statistics from the input image (e.g. distribution of colors, of Fourier coefficients, of wavelet coefficients , . . . ).
2. Compute a random output image having the same statistics: start from a white noise and alternatively impose the statistics of the input.

The main properties of these algorithms are: they are perceptually stable (the outputs always have the same visual aspect), they allow mathematical computations, but they are generally not good enough for macro-textures (that have long-range interactions that are difficult to capture with statistics). The main representatives of these algorithms are: the Heeger-Bergen algorithm [24] (the considered statistics are the histograms of responses to multiscale and multi-orientation filters), the PortillaSimoncelli algorithm [33] (the considered statistics are the correlations between multiscale and multi-orientation filters responses), and the Random Phase Noise [17] of Galerne et al. (that will be detailed in the next section, and where the considered statistics are the Fourier modulus). Some examples of results with these three algorithms are shown on Fig. 3.29.

To end this section, let us mention that the literature on texture synthesis methods is quite huge, and many algorithms exist that cannot be simply classified as being else 'copy-paste' algorithms or 'statistics-based' algorithms. They generally mix several ideas. Just to mention a few of them: [34, 39] and the recent successful algorithm of Gatys et al. [19] that uses convolutional neural networks.

#### 3.3.3 Discrete Fourier Transform and the RPN Algorithm

We work here with digital images u : Ω → R where Ω is a rectangle of Z 2 centered at 0 = ( 0 , 0 ) and of size M × N where M and N are both assumed to be odd (this is just an assumption to make some formulas simpler, and of course things can also be written with even image sizes). We thus write: Ω = {- M - 1 2 , . . . , 0 , . . . , M - 1 2 } × {- N - 1 2 , . . . , 0 , . . . , N - 1 2 } . The discrete Fourier transform (DFT) of u is defined by

$$\forall \xi \in \Omega , \ \widehat { u } ( \xi ) = \sum _ { x \in \Omega } u ( x ) e ^ { - 2 i \pi \langle x , \xi \rangle } ,$$


<!-- p:129 -->


3

Fig. 3.29 Some results of statistics-based texture synthesis algorithm. The original input images are not shown here, they are the same as in Fig. 3.28. Left column: results of the Heeger-Bergen algorithm (obtained with the IPOL online demo [6]). Middle column: results of the PortillaSimoncelli algorithm (obtained with the code provided by the authors). Right column: results of the RPN algorithm (obtained with the IPOL online demo [18])

where the inner product between x = (x 1 , x 2 ) and ξ = (ξ 1 , ξ 2 ) is defined by 〈 x , ξ 〉 = 1 M x 1 ξ 1 + 1 N x 2 ξ 2. As usual, the image u can be recovered from its Fourier transform u by the Inverse Discrete Fourier Transform:

$$\forall x \in \Omega , \ u ( x ) = \frac { 1 } { | \Omega | } \sum _ { \xi \in \Omega } \widehat { u } ( \xi ) e ^ { 2 i \pi ( x , \xi ) } , \\$$

̂

where | Ω | = MN is the size of the domain Ω .

The modulus | ̂ u | is called the Fourier modulus (or Fourier amplitude) of u and arg ( ˆ u ) is the Fourier phase of u . Since u is real-valued, its Fourier modulus is even while its Fourier phase is odd. The Fourier modulus and the Fourier phase of an image play very different roles, in the sense that they 'capture' different features of the image. Indeed, geometric contours are mostly contained in the phase [32], while (micro-)textures are mostly contained in the modulus. This fact can be experimentally checked by taking two images and by exchanging their Fourier modulus or their Fourier phases. See Figs. 3.30 and 3.31 for some illustrations of this.

We can now describe the RPN (Random Phase Noise) algorithm [17]. It is based on the above observation: for micro-textures, only the Fourier modulus is important, the Fourier phase can be randomly changed. The RPN algorithm works as follows:


<!-- p:130 -->


Fig. 3.30 Exchanging Fourier modulus or phases of two images. This is an experimental check that geometric contours are mostly contained in the phase, while textures are mostly contained in the modulus. First line: Images Im1, Im2, Im3 and Im4. Second line, images obtained by taking respectively: the modulus of Im1 with the phase of Im2, the modulus of Im2 with the phase of Im1, the modulus of Im3 with the phase of Im4, the modulus of Im4 with the phase of Im3

Fig. 3.31 The image that has the Fourier modulus of Im4 and the Fourier phase of Im1. This image has captured the geometry of Im1 and the texture of Im4

1. Let u 0 be the original input image. To avoid artefacts in the Fourier transform due to the boundaries of Ω , replace u 0 by its periodic component [29].


<!-- p:131 -->


2. Compute the Discrete Fourier Transform u 0 of the input u 0.
4. Set Z = | u 0 | e iΘ (or Z = u 0 e iΘ ).
3. ̂ 3. Compute a random phase Θ , with the Θ( ξ ) being independent, uniformly distributed on [ 0 , 2 π) with the constraint that Θ( - ξ ) = - Θ( ξ ) .
4. ̂ ̂ ̂ ̂ 5. Return Z the inverse Fourier transform of Z .

̂ Examples of results obtained by this algorithm were shown on Fig. 3.29. As expected, this algorithm performs well on micro-textures, but fails on macrotextures that contain geometric patterns (that are lost when randomizing the phase) and long-range interactions (that are difficult to model by statistics).

As written above, the RPN algorithm generates an image Z that has the same size as the input image u 0. To obtain an output image of an arbitrary large size, one can just start by smoothly extending u 0 by a constant outside its domain (see [17] for more details) and then perform the RPN algorithm with the new extended input.

The RPN algorithm can be adapted to the case of color images, by adding the same random phase to the three channels. More precisely, if the input image u is a color image, meaning that u = (u 1 , u 2 , u 3 ) (for the Red, Green and Blue channels) with each uk being Ω → R , then the RPN algorithm generates one random phase Θ and three output images given by ̂ Zk = ̂ uke iΘ . Therefore we have that for all k, j = 1 , 2 or 3, ̂ Zk ̂ Zj = ̂ uk ̂ uj , showing that it keeps the Fourier modulus of each channel but also the cross-channel Fourier correlation. This fact is related to the link between the Fourier modulus and the empirical covariance, as we will explain it in the following section.

#### 3.3.4 Gaussian Models for Texture Images

Given two images u : Ω → R and v : Ω → R , we can define the convolution of u and v as the image u ⋆ v : Ω → R given by

$$\forall x \in \Omega , \ \ ( u * v ) ( x ) = \sum _ { y \in \Omega } u ( y ) \, v ( x - y ) ,$$

where v( x ) can be defined for any x ∈ Z 2 by considering x modulo Ω (i.e. x 1 modulo M and x 2 modulo N ). This amounts to extend v on Z 2 by periodicity. The convolution is described more simply in the Fourier domain since the convolution/product exchange property states that

$$\forall \xi \in \Omega , \ \widehat { u ^ { * } v } ( \xi ) = \widehat { u } ( \xi ) \widehat { v } ( \xi ) .$$

̂ ̂ ̂ Stationary Gaussian textures are widely used as models of (micro)-textures, and they are well characterized in Fourier domain. Indeed, we have the following proposition.


<!-- p:132 -->


Proposition 3.2 Let (U( x )) x ∈ Ω be a real-valued random field on Ω , and let Ω + = { ξ = (ξ 1 , ξ 2 ) ; ξ 1 &gt; 0 or (ξ 1 = 0 and ξ 2 &gt; 0 ) } . Then (U( x )) x ∈ Ω is a centered Gaussian periodic stationary random field if and only if the random variables

$$\{ \widehat { U } ( 0 ) , R e \, \widehat { U } ( \xi ) , \text {Im} \, \widehat { U } ( \xi ) ; \xi \in \Omega _ { + } \} \\ \intertext { c e n t e r e d \ G a u s s i a n \ v a r i a b l e s . \ M o r e o v e r ; \, i n \ t h i s \ c }$$

are independent centered Gaussian variables. Moreover, in this case, if Γ denotes the covariance of U defined by Γ( x ) = Cov (U( x ), U( 0 )) for all x ∈ Ω , then

$$Var ( \widehat { U } ( 0 ) ) = | \Omega | \cdot \widehat { \Gamma } ( 0 ) \quad \text {and} \quad \text {Var} ( \text {Re} \, \widehat { U } ( \xi ) ) = \text {Var} ( \text {Im} \, \widehat { U } ( \xi ) ) = \frac { 1 } { 2 } | \Omega | \cdot \widehat { \Gamma } ( \xi ) \\ \intertext { f o r all } \xi \in \Omega + \text { } \Omega$$

for all ξ ∈ Ω + .

Proof The proof is based on the fact that the Fourier transform is a linear transform. Therefore if U is a centered Gaussian periodic stationary random field, then the variables { Re ̂ U( ξ ), Im ̂ U( ξ ) ; ξ ∈ Ω } are a centered Gaussian vector. To compute its covariance, let us for instance compute E ( Re ̂ U( ξ ) Re ̂ U( ξ ′ )) for ξ and ξ ′ in Ω . Let Γ denote the covariance of U . We have

$$\text {Let} \, \overline { \ } d o m e \, \text {covariance of} \, U \colon \text { we have} \\ \mathbb { E } ( \text {Re} \, \widehat { U } ( \xi ) \, \text {Re} \, \widehat { U } ( \xi ^ { \prime } ) ) & = \mathbb { E } \left ( \sum _ { x } \sum _ { y } U ( x ) \cos ( 2 \pi \left ( x , \xi \right ) ) U ( y ) \cos ( 2 \pi \left ( y , \xi ^ { \prime } \right ) ) \right ) \\ & = \sum _ { x } \sum _ { z } \mathbb { E } ( I ( x ) U ( x + z ) ) \cos ( 2 \pi \left ( x , \xi \right ) ) \cos ( 2 \pi \left ( x + z , \xi ^ { \prime } \right ) ) \\ & = \frac { | \Omega | } { 2 } \left ( 1 _ { \xi } = \pm \xi ^ { \prime } \neq 0 \sum _ { z } \Gamma ( z ) \cos ( 2 \pi \left ( x , \xi \right ) ) + 2 1 _ { \xi = \xi ^ { \prime } = 0 } \sum _ { z } \Gamma ( z ) \right ) .$$

Therefore, since Γ( z ) = Γ( - z ) and Re ̂ U( ξ ) = Re ̂ U( - ξ ) (because U is real), we deduce that if ξ ̸= ξ ′ ∈ Ω + , then E ( Re ̂ U( ξ ) Re ̂ U( ξ ′ )) = 0 (these two Gaussian random variables are thus independent), E ( Re ̂ U( 0 ) 2 ) = | Ω | ̂ Γ( 0 ) and E ( Re ̂ U( ξ ) 2 ) = | Ω | 2 ̂ Γ( ξ ) for ξ ̸= 0. Analogous computations hold with ( Re ̂ U( ξ ), Im ̂ U( ξ ′ )) and ( Im ̂ U( ξ ), Im ̂ U( ξ ′ )) , and this ends the proof of the proposition. ⊓ ⊔

The above proposition gives a characterization of periodic stationary Gaussian textures. Indeed, we have that

- The Fourier phases (φ( ξ )) ξ ∈ Ω + are independent identically distributed uniformly on [ 0 , 2 π) and independent from the Fourier amplitudes ( | U( ξ ) | ) ξ ∈ Ω + .
- ̂ · And U( 0 ) follows a centered normal distribution with variance | Ω | Γ( 0 ) .
- ̂ · The Fourier amplitudes ( | ̂ U( ξ ) | ) ξ ∈ Ω + are independent random variables following a Rayleigh distribution of parameter √ 1 2 | Ω | Γ( ξ ) .

̂ ̂ The simplest case of a Gaussian stationary random field is the white noise (of variance 1): the U( x ) are i.i.d. following the standard normal distribution N ( 0 , 1 ) .


<!-- p:133 -->


3

Then, in this case Γ ( x ) = δ 0 ( x ) (the indicator function of { 0 } ), and thus ̂ Γ( ξ ) = 1 for all ξ ∈ Ω . Therefore the Fourier transform ̂ U (restricted to Ω + ) is also a (complex) white noise (of variance | Ω | ).

In the following, we will denote by GT (Γ ) (GT stands for Gaussian Texture) the law of the centered Gaussian periodic stationary random field with covariance function Γ .

Starting from an original image u 0, that is assumed to have zero mean on Ω (otherwise we just add a constant to it), we can compute its empirical covariance as

$$\forall x \in \Omega , \ C _ { u _ { 0 } } ( x ) = \frac { 1 } { | \Omega | } \sum _ { y \in \Omega } u _ { 0 } ( y ) u _ { 0 } ( y + x ) .$$

Thanks to the convolution/product property of the Fourier transform, we have that

$$\forall \xi \in \Omega , \ \widehat { C _ { u _ { 0 } } } ( \xi ) = \frac { 1 } { | \Omega | } | \widehat { u _ { 0 } } ( \xi ) | ^ { 2 } . \\$$

Now, let W be a white noise image of variance σ 2 = 1 / | Ω | on Ω (i.e. all W( x ) , x ∈ Ω , are i.i.d N ( 0 , σ 2 ) ). Let us consider

$$U = u _ { 0 } * W .$$

Then, by computing its covariance, we obtain that U follows a GT (Cu 0 ) distribution. Conversely if Γ is a covariance and U follows a GT (Γ ) distribution, then by Proposition 3.2 that characterizes U , we have that U can be written as

$$e s \ U , \, w e \text { have that } U \\ U = u _ { \Gamma } * W , \\ 2 \quad ( 2 )$$

where W is white noise (of variance σ 2 = 1 / | Ω | ) and uΓ is any image such that

$$\forall \xi \in \Omega , \ | \widehat { u _ { \Gamma } } ( \xi ) | = \sqrt { | \Omega | \widehat { \Gamma } ( \xi ) } .$$

̂ ̂ Notice that since Γ is a covariance, the ̂ Γ( ξ ) are positive (see also Proposition 3.2, where they appear as variances). There are many such uΓ images, since one can choose any Fourier phase for it. However some choices appear to be better than others, in the sense that the image uΓ is more 'concentrated'. This is in particular the choice of uΓ being simply the inverse Fourier transform of | ̂ uΓ | = √ | Ω | ̂ Γ (having thus an identically null Fourier phase). This particular image, called the texton , is analyzed in more details in [15].

Starting from an image u 0, we can generate two samples: one with the RPN algorithm, that is given by ̂ U RPN = ̂ u 0 e iΘ where Θ is an i.i.d uniform phase field, and another one that is a sample of GT (Cu 0 ) that can be written as U GT = u 0 ⋆ W (where W is white noise of variance σ 2 ), or equivalently ̂ U GT = ̂ u 0 ̂ W = ̂ u 0 Re iΦ , where Φ is an i.i.d uniform phase field, independent of the R( ξ ) that are i.i.d following a Rayleigh distribution of parameter √ 1 / 2. The formula for these two samples are very similar, they have both random phases, and there is just an additional Rayleigh random variable in the Gaussian texture. However, this Rayleigh term doesn't make any visual difference, as illustrated on Fig. 3.32.


<!-- p:134 -->


Fig. 3.32 Gaussian textures and the RPN algorithm. Left column: original images u 0 ('snake' and 'wood'). Middle column: samples from the Gaussian Texture model with covariance Cu 0 . Right column: samples from the RPN algorithm, using the same random phase as for the Gaussian samples. It shows that the random Rayleigh factor in the modulus of the Gaussian textures doesn't visually make a difference

As for the RPN algorithm, Gaussian textures can be defined from an input color image u = (u 1 , u 2 , u 3 ) by simply considering the convolution of each channel of u with the same (real-valued) white noise W . This results in a random Gaussian color image such that the covariance between the channels is the same as the empirical covariance between the channels of u .

#### 3.3.5 Shot Noise Model and Dead Leaves Model

As it was shown by Galerne et al. in [17], as a consequence of the Central Limit Theorem, the Gaussian texture model GT (Cu 0 ) , where u 0 is a (centered) given input image, is the limit, as n goes to infinity of the discrete spot noise model given by

$$U ( \mathbf x ) = \frac { 1 } { \sqrt { n } } \sum _ { j = 1 } ^ { n } u _ { 0 } ( \mathbf x - \mathbf y _ { j } ) ,$$

where the y j are independent, uniformly distributed on Ω .


<!-- p:135 -->


The spot noise model was introduced by van Wijk in Computer Graphics [40], and its general definition in a continuous setting is called shot noise random field . It is (in dimension 2) a random field X : R 2 → R given by

$$\forall x \in \mathbb { R } ^ { 2 } , \ X ( x ) = \sum _ { i \in I } g _ { m _ { i } } ( x - x _ { i } ) ,$$

where the { x i } i ∈ I is a Poisson point process of intensity λ &gt; 0 in R 2 , the { mi } i ∈ I are independent 'marks' with distribution F(dm) on R d , and independent of { x i } i ∈ I , and the functions gm are real-valued functions, called spot functions , and such that ∫ R d ∫ R n | gm( y ) | d y F(dm) &lt; +∞ .

This shot noise model can be used as a model for natural images made of 'objects', and it is for instance used by A. Srivastava et al. in [38] as forms for 'modelling image probabilities'. They write it as

$$\forall x \in \mathbb { R } ^ { 2 } , \ X ( x ) = \sum _ { i } \beta _ { i } \, g _ { i } \left ( \frac { 1 } { r _ { i } } ( x - x _ { i } ) \right ) ,$$

where gi is an 'object', x i its position, βi its grey level or color and ri is a scaling factor (related to the distance at which the object is).

Such a model is also a nice model for macro-textures modelling. Now, in this model the different objects are just added, whereas in natural texture images, objects are partially hidden, in particular when some other objects are in front of them. To take into account this so-called occlusion phenomenon , a more 'realistic' model is given by the dead leaves model introduced by G. Matheron and studied for instance in [5]. In the dead leaves model, the function gi are indicator functions of a 'grain', and an additional random variable t i is introduced that models the time at which the grain falls. The value at a point x is then defined as being the value of the first grain that covers x . Two examples of respectively a shot noise random field and a dead leaves model are given on Fig. 3.33.

Fig. 3.33 Two examples of macro-textures: on the left, a sample of a shot noise random field, and on the right, a sample of a dead leaves model with the same color 'grains'

<!-- p:136 -->


### References

1. C. Aguerrebere, Y. Gousseau, G. Tartavel, Exemplar-based texture synthesis: the Efros-Leung algorithm. Image Process. Line 3 , 223-241 (2013). https://doi.org/10.5201/ipol.2013.59
2. A. Almansa, A. Desolneux, S. Vamech, Vanishing point detection without any a priori information. IEEE Trans. Pattern Anal. Mach. Intell. 25 (4), 502-507 (2003)
3. F. Attneave, Some informational aspects of visual perception. Psychol. Rev. 61 , 183-193 (1954)
4. S. Blusseau, A. Carboni, A. Maiche, J.-M. Morel, R. Grompone von Gioi, A psychophysical evaluation of the a contrario detection theory, in Proceedings of the 2014 IEEE International Conference on Image Processing (ICIP) (IEEE, Piscataway, 2014), pp. 1091-1095
5. C. Bordenave, Y. Gousseau, F. Roueff, The dead leaves model: an example of a general tesselation. Adv. Appl. Probab. 38 (1), 31-46 (2006)
6. T. Briand, J. Vacher, B. Galerne, J. Rabin, The Heeger &amp; Bergen pyramid based texture synthesis algorithm. Image Process. Line 4 , 276-299 (2014). https://doi.org/10.5201/ipol.2014. 79
7. F. Cao, Good continuation in digital images, in Proceedings of the International Conference on Computer Vision (ICCV) (2003), pp. 440-447
8. F. Cao, J. Delon, A. Desolneux, P. Musé, F. Sur, A unified framework for detecting groups and application to shape recognition. J. Math. Imaging Vis. 27 (2), 91-119 (2007).
9. A. Ciomaga, P. Monasse, J.-M. Morel, The image curvature microscope: accurate curvature computation at subpixel resolution. Image Process. Line 7 , 197-217 (2017). https://doi.org/10. 5201/ipol.2017.212
10. D. Coupier, A. Desolneux, B. Ycart, Image denoising by statistical area thresholding. J. Math. Imaging Vis. 22 (2-3), 183-197 (2005)
11. A. Desolneux, L. Moisan, J.-M. Morel, Meaningful alignments. Int. J. Comput. Vis. 40 (1), 7-23 (2000)
12. A. Desolneux, L. Moisan, J.-M. Morel, Edge detection by Helmholtz principle. J. Math. Imaging Vis. 14 (3), 271-284 (2001)
13. A. Desolneux, L. Moisan, J.-M. Morel, Maximal meaningful events and applications to image analysis. Ann. Stat. 31 (6), 1822-1851 (2003)
14. A. Desolneux, L. Moisan, J.-M. Morel, From Gestalt Theory to Image Analysis: A Probabilistic Approach (Springer, Berlin, 2008)
15. A. Desolneux, L. Moisan, S. Ronsin, A compact representation of random phase and Gaussian textures, in 2012 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP) (IEEE, Piscataway, 2012), pp. 1381-1384
16. A.A. Efros, T.K. Leung, Texture synthesis by non-parametric sampling, in Proceedings of the IEEE International Conference on Computer Vision (ICCV 1999) , vol. 2 (IEEE, Piscataway, 1999), pp. 1033-1038
17. B. Galerne, Y. Gousseau, J.-M. Morel, Random phase textures: theory and synthesis. IEEE Trans. Image Process. 20 (1), 257-267 (2011)
18. B. Galerne, Y. Gousseau, J.-M. Morel, Micro-texture synthesis by phase randomization. Image Process. Line 1 , 213-237 (2011). https://doi.org/10.5201/ipol.2011.ggm\_rpn
19. L.A. Gatys, A.S. Ecker, M. Bethge, Texture synthesis using convolutional neural networks, in Proceedings of the Conference on Neural Information Processing Systems, 2015 (2015), pp. 262-270
20. R. Grompone von Gioi, G. Randall, Unsupervised smooth contour detection. Image Process. Line 6 , 233-267 (2016). https://doi.org/10.5201/ipol.2016.175
21. R. Grompone von Gioi, J. Jakubowicz, J.-M. Morel, G. Randall, A fast line segment detector with a false detection control. IEEE Trans. Pattern Anal. Mach. Intell. 32 , 722-732 (2010)
22. R. Grompone von Gioi, J. Jakubowicz, J.-M. Morel, G. Randall, LSD: a line segment detector. Image Process. Line 2 , 35-55 (2012). https://doi.org/10.5201/ipol.2012.gjmr-lsd


<!-- p:137 -->


23. P.E. Hart, How the Hough transform was invented. IEEE Signal Process. Mag. 26 (6), 18-22 (2009)
24. D.J. Heeger, J.R. Bergen, Pyramid-based texture analysis/synthesis, in Proceedings of the Conference SIGGRAPH '95 (IEEE, Piscataway, 1995), pp. 229-238
25. G. Kanizsa, Grammatica del Vedere/La Grammaire du Voir (Bologna/Éditions Diderot, Arts et Sciences, IL Mulino, 1980/1997)
26. E. Levina, P.J. Bickel, Texture synthesis and nonparametric resampling of random fields. Ann. Stat. 35 (4), 1751-1773 (2006)
27. D. Lowe, Perceptual Organization and Visual Recognition (Kluwer Academic Publishers, Dordecht, 1985)
28. W. Metzger, Gesetze des Sehens (Kramer, Frankfurt, 1953).
29. L. Moisan, Periodic plus smooth image decomposition. J. Math. Imaging Vis. 39 (2), 161-179 (2011)
30. L. Moisan, B. Stival, A probabilistic criterion to detect rigid point matches between two images and estimate the fundamental matrix. Int. J. Comput. Vis. 57 (3), 201-218 (2004)
31. P. Musé, F. Sur, F. Cao, Y. Gousseau, Unsupervised thresholds for shape matching, in Proceedings 2003 International Conference on Image Processing (ICIP 2003) , vol. 2 (IEEE, Piscataway, 2003), pp. 647-650
32. A.V. Oppenheim, J.S. Lim, The importance of phase in signals. IEEE Proc. 69 , 529-541 (1981)
33. J. Portilla, E.P. Simoncelli, A parametric texture model based on joint statistics of complex wavelet coefficients. Int. J. Comput. Vis. 40 (1), 49-71 (2000)
34. L. Raad, A. Desolneux and J.-M. Morel, A conditional multiscale locally Gaussian texture synthesis algorithm. J. Math. Imaging Vis. 56 (2), 260-279 (2016)
35. J. Rabin, J. Delon, Y. Gousseau, A statistical approach to the matching of local features. SIAM J. Imag. Sci. 2 (3), 931-958 (2009)
36. N. Sabater, A. Almansa, J.-M. Morel, Meaningful matches in stereovision. IEEE Trans. Pattern Anal. Mach. Intell. 34 (5), 930-942 (2012)
37. L. Santalo, Integral Geometry and Geometric Probability , 2nd edn. (Cambridge University Press, Cambridge, 2004)
38. A. Srivastava, X. Liu, U. Grenander, Universal analytical forms for modeling image probabilities. IEEE Trans. Pattern Anal. Mach. Intell. 24 (9), 1200-1214 (2002)
39. G.Tartavel, Y. Gousseau, G. Peyré, Variational texture synthesis with sparsity and spectrum constraints. J. Math. Imaging Vis. 52 (1), 124-144 (2015)
40. J.J. van Wijk, Spot noise texture synthesis for data visualization, in Proceedings of the 18th Annual Conference on Computer Graphics and Interactive Techniques, SIGGRAPH '91 (ACM, New York, 1991), pp. 309-318
41. T. Veit, F. Cao, P. Bouthemy, An a contrario decision framework for region-based motion detection. Int. J. Comput. Vis. 68 (2), 163-178 (2006)
42. M. Wertheimer, Unterzuchungen zur lehre der gestalt. Psychol. Forsch. 4 (1), 301-350 (1923)
43. S.C. Zhu, Embedding gestalt laws in markov random fields. IEEE Trans. Pattern Anal. Mach. Intell. 21 (11), 1170-1187 (1999)


<!-- p:138 -->


## Chapter 4 Introduction to Random Fields and Scale Invariance

####### Hermine Biermé

Abstract In medical imaging, several authors have proposed to characterize roughness of observed textures by their fractal dimensions. Fractal analysis of 1D signals is mainly based on the stochastic modeling using the famous fractional Brownian motion for which the fractal dimension is determined by its so-called Hurst parameter. Lots of 2D generalizations of this toy model may be defined according to the scope. This lecture intends to present some of them. After an introduction to random fields, the first part will focus on the construction of Gaussian random fields with prescribed invariance properties such as stationarity, self-similarity, or operator scaling property. Sample paths properties such as modulus of continuity and Hausdorff dimension of graphs will be settled in the second part to understand links with fractal analysis. The third part will concern some methods of simulation and estimation for these random fields in a discrete setting. Some applications in medical imaging will be presented. Finally, the last part will be devoted to geometric constructions involving Marked Poisson Point Processes and shot noise processes.

### 4.1 Random Fields and Scale Invariance

We recall in this section definitions and properties of random fields. Most of them can also be found in [22] but we try here to detail some important proofs. We stress on invariance properties such as stationarity, isotropy, and scale invariance and illustrate these properties with typical examples.

<!-- p:139 -->


#### 4.1.1 Introduction to Random Fields

As usual when talking about randomness, we let (Ω, A , P ) be a probability space, reflecting variability.

##### 4.1.1.1 Definitions and Distribution

Let us first recall the general definition of a stochastic process. For this purpose we have to consider a set of indices T . In this lecture we assume that T ⊂ R d for some dimension d ≥ 1.

Definition 4.1 A (real) stochastic process indexed by T is just a collection of real random variables meaning that for all t ∈ T , one has Xt : (Ω, A ) → ( R , B ( R )) measurable.

Stochastic processes are very important in stochastic modeling as they can mimic numerous natural phenomena. For instance, when d = 1, one can choose T ⊂ R (seen as time parameters) and consider Xt(ω) as the real value of heart frequency at time t ∈ T with noise measurement or for an individual ω ∈ Ω . Note that, in practice data are only available on a discrete finite subset S of T , for instance each millisecond. When d = 2, choosing T = [ 0 , 1 ] 2 , the value Xt(ω) may correspond to the grey level of a picture at point t ∈ T . Again, in practice, data are only available on pixels S = { 0 , 1 /n, . . . , 1 } 2 ⊂ T for an image of size (n + 1 ) × (n + 1 ) . In general we talk about random fields when d &gt; 1 and keep the terminology stochastic process only for d = 1. Since we have actually a map X from Ω × T with values in R we can also consider it as a map from Ω to R T . We equip R T with the smallest σ -algebra C such that the projections πt : ( R T , C ) → ( R , B ( R )) , defined by πt (f ) = f(t) are measurable. It follows that X : (Ω, A ) → ( R T , C ) is measurable and its distribution is defined as the image measure of P by X , which is a probability measure on ( R T , C ) . An important consequence of Kolmogorov's consistency theorem (see [37, p. 92]) is the following equivalent definition.

Definition 4.2 The distribution of (Xt )t ∈ T is given by all its finite dimensional distribution (fdd) i.e. the distribution of all real random vectors

$$( X _ { t _ { 1 } } , \dots , X _ { t _ { k } } ) \text { for } k \geq 1 , t _ { 1 } , \dots , t _ { k } \in T .$$

Note that joint distributions for random vectors of arbitrary size k are often difficult to compute. However we can infer some statistics of order one and two by considering only couples of variables.

Definition 4.3 The stochastic process (Xt )t ∈ T is a second order process if E (X 2 t ) &lt; + ∞ , for all t ∈ T . In this case we define

- its covariance function KX : (t, s) ∈ T × T → Cov (Xt , Xs ) ∈ R .
- its mean function mX : t ∈ T → E (Xt ) ∈ R ;


<!-- p:140 -->


4

A particular case arises when mX = 0 and the process X is said centered. Otherwise the stochastic process Y = X - mX is also second order and now centered with the same covariance function KY = KX . Hence we will mainly consider centered stochastic processes. The covariance function of a stochastic process must verify the following properties.

Proposition 4.1 A function K : T × T → R is a covariance function iff

2. K is non-negative definite: ∀ k ≥ 1 , t 1 , . . . , tk ∈ T, : λ 1 , . . . , λk ∈ R ,
1. K is symmetric i.e. K(t, s) = K(s,t) for all (t, s) ∈ T × T ;

$$\sum _ { i , j = 1 } ^ { k } \lambda _ { i } \lambda _ { j } K ( t _ { i } , t _ { j } ) \geq 0 .$$

Proof The first implication is trivial once remarked the fact that Var ( ∑ k i = 1 λi Xti ) = ∑ k i,j = 1 λi λj K(ti , tj ) . For the converse, we need to introduce Gaussian processes.

##### 4.1.1.2 Gaussian Processes

As far as second order properties are concerned the most natural class of processes are given by Gaussian ones.

Definition 4.4 A stochastic process (Xt )t ∈ T is a Gaussian process if for all k ≥ 1 and t 1 , . . . , tk ∈ T

$$( X _ { t _ { 1 } } , \dots , X _ { t _ { k } } ) \text { is a Gaussian vector of } \mathbb { R } ^ { k } ,$$

which is equivalent to the fact that for all λ 1 , . . . , λk ∈ R , the real random variable k ∑ i = 1 λi Xti is a Gaussian variable (eventually degenerate i.e. constant).

Note that this definition completely characterizes the distribution of the process in view of Definition 4.2.

Proposition 4.2 When (Xt )t ∈ T is a Gaussian process, (Xt )t ∈ T is a second order process and its distribution is determined by its mean function mX : t ↦→ E (Xt ) and its covariance function KX : (t, s) ↦→ Cov (Xt , Xs ) .

This comes from the fact that the distribution of the Gaussian vector (Xt 1 , . . . , X tk ) is characterized by its mean ( E (Xt 1 ), . . . , E (Xtk )) = (mX(t 1 ), . . . , mX(tk)) and its covariance matrix ( Cov (Xti , Xtj ) ) 1 ≤ i,j ≤ k = ( KX(ti, tj ) ) 1 ≤ i,j ≤ k .

Again Kolmogorov's consistency theorem (see [37, p. 92] for instance) allows to prove the following existence result that finishes to prove Proposition 4.1.

⊓

⊔


<!-- p:141 -->


Theorem 4.1 Let m : T → R and K : T × T → R a symmetric and non-negative definite function, then there exists a Gaussian process with mean m and covariance K .

Let us give some insights of construction for the fundamental example of Gaussian process, namely the Brownian motion. We set here T = R + and consider (Xk)k ∈ N a family of independent identically distributed second order random variables with E (Xk) = 0 and Var (Xk) = 1. For any n ≥ 1, we construct on T the following stochastic process

$$S _ { n } ( t ) = \frac { 1 } { \sqrt { n } } \sum _ { k = 1 } ^ { [ n t ] } X _ { k } . \\$$

By the central limit theorem (see [28] for instance) we clearly have for t &gt; 0, √ n [ nt ] Sn(t) d -→ n →+∞ N ( 0 , 1 ) so that by Slutsky's theorem (see [15] for instance) Sn(t) d -→ n →+∞ N ( 0 , t) . Moreover, for k ≥ 1, if 0 &lt; t 1 &lt; . . . &lt; tk , by independence of marginals,

$$( S _ { n } ( t _ { 1 } ) , S _ { n } ( t _ { 2 } ) - S _ { n } ( t _ { 1 } ) , \dots , S _ { n } ( t _ { k } ) - S _ { n } ( t _ { k - 1 } ) ) \underset { n \to + \infty } { \stackrel { d } { \longrightarrow } } Z = ( Z _ { 1 } , \dots , Z _ { k } ) ,$$

with Z ∼ N ( 0 , KZ) for KZ = diag (t 1 , t 2 - t 1 , . . . , tk - tk - 1 ) . Hence identifying the k × k matrix Pk = ⎛ ⎜ ⎜ ⎜ ⎝ 1 0 . . . 0 1 1 . . . . . . 1 . . . . . . 1 ⎞ ⎟ ⎟ ⎟ ⎠ with the corresponding linear application on R k ,

$$( S _ { n } ( t _ { 1 } ) , S _ { n } ( t _ { 2 } ) , \dots , S _ { n } ( t _ { k } ) ) & = P _ { k } ( S _ { n } ( t _ { 1 } ) , S _ { n } ( t _ { 2 } ) - S _ { n } ( t _ { 1 } ) , \dots , S _ { n } ( t _ { k } ) \\ & - S _ { n } ( t _ { k - 1 } ) ) \\ & \stackrel { \frac { d } { n \to + \infty } } { \longrightarrow } P _ { k } Z ,$$

with PkZ ∼ N ( 0 , Pk KZP ∗ k ) and PkKZP ∗ k = ( min (ti , t j ) ) 1 ≤ i,j ≤ k . In particular the function

$$K ( t , s ) = \min ( t , s ) = \frac { 1 } { 2 } \left ( t + s - | t - s | \right )$$

is a covariance function on the whole space R + × R + and (Sn)n converges in finite dimensional distribution to a centered Gaussian stochastic process X = (Xt ) t ∈ R +


<!-- p:142 -->


4

1

Fig. 4.1 Sample paths of a Brownian motion on [ 0 , 1 ] . The realization is obtained using fast and exact synthesis presented in Sect. 4.3.1.1

with covariance K , known (up to continuity of sample paths) as the standard Brownian motion on R + .

Now we can extend this process on R by simply considering X ( 1 ) and X ( 2 ) two independent centered Gaussian processes on R + with covariance function K and defining Bt := X ( 1 ) t for t ≥ 0, Bt := X ( 2 ) - t for t &lt; 0. Computing the covariance function of B yields the following definition.

Definition 4.5 A (standard) Brownian motion on R (Fig. 4.1) is a centered Gaussian process (Bt )t ∈ R with covariance function given by

$$K _ { B } ( t , s ) = C o v ( B _ { t } , B _ { s } ) = \frac { 1 } { 2 } \left ( | t | + | s | - | t - s | \right ) , \, \forall t , s \in \mathbb { R } .$$

From Gaussian stochastic processes defined on R we can define Gaussian random fields defined on R d in several ways. We give some possibilities in the next section.

##### 4.1.1.3 Gaussian Fields Defined from Processes

Weconsider on R d the Euclidean norm, denoted by ‖·‖ with respect to the Euclidean scalar product x · y for x, y ∈ R d . The unit sphere { θ ∈ R d ; ‖ θ ‖ = 1 } is denoted as S d - 1 and we let (ei ) 1 ≤ i ≤ d stand for the canonical basis of R d .

A first example of construction is given in the following proposition.


<!-- p:143 -->


Proposition 4.3 Let K : R × R → R be a continuous covariance function. For all μ non-negative finite measure on the unit sphere S d - 1 , the function defined by

$$( x , y ) \in \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } & \mapsto \int _ { S ^ { d - 1 } } K ( x \cdot \theta , y \cdot \theta ) d \mu ( \theta ) \in \mathbb { R } ,$$

is a covariance function on R d × R d .

Proof According to Proposition 4.1, it is enough to check symmetry and nonnegative definiteness. Symmetry is clear and for all k ≥ 1, x 1 , . . . , xk ∈ R d , λ 1 , . . . , λk ∈ R ,

$$\sum _ { i , j = 1 } ^ { k } \lambda _ { i } \lambda _ { j } \int _ { S ^ { d - 1 } } K ( x _ { i } \cdot \theta , x _ { j } \cdot \theta ) d \mu ( \theta ) & = \int _ { S ^ { d - 1 } } \left ( \sum _ { i , j = 1 } ^ { k } \lambda _ { i } \lambda _ { j } K ( x _ { i } \cdot \theta , x _ { j } \cdot \theta ) \right ) \\ & \times d \mu ( \theta ) \geq 0 , \\$$

since for all θ ∈ S d - 1 , x 1 · θ, . . . , xk · θ ∈ R with K non-negative definite on R × R and μ non-negative measure. ⊓ ⊔

As an example we can note that ∫ S d - 1 | x · θ | dθ = cd ‖ x ‖ , with cd = ∫ S d - 1 | e 1 · θ | dθ for e 1 = ( 1 , 0 , . . . , 0 ) ∈ S d - 1 . Then, for KB the covariance function of a standard Brownian motion on R we get

$$\int _ { S ^ { d - 1 } } K _ { B } ( x \cdot \theta , y \cdot \theta ) d \theta = \frac { c _ { d } } { 2 } \left ( \| x \| + \| y \| - \| x - y \| \right ) .$$

Definition 4.6 A (standard) Lévy Chentsov field on R d (Fig. 4.2) is a centered Gaussian field (Xx) x ∈ R d with covariance function given by

$$C o v ( X _ { x } , X _ { y } ) = \frac { 1 } { 2 } \left ( \| x \| + \| y \| - \| x - y \| \right ) , \, \forall x , y \in \mathbb { R } ^ { d } .$$

Let us note that (Xtθ )t ∈ R is therefore a standard Brownian motion for all θ ∈ S d - 1 . Another example is given using a sheet structure according to the following proposition.

Proposition 4.4 Let K 1 , K 2 , . . . , Kd be covariance functions on R × R , then the function defined by

$$( x , y ) \in \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } \mapsto \prod _ { i = 1 } ^ { d } K _ { i } ( x \cdot e _ { i } , y \cdot e _ { i } ) \in \mathbb { R } ,$$

is a covariance function on R d × R d .


<!-- p:144 -->


4

Fig. 4.2 Sample paths of a Lévy Chentsov field on [ 0 , 1 ] 2 . The realization is obtained using fast and exact synthesis presented in Sect. 4.3.1.3. On the left we draw the obtained surface, on the right the two corresponding images with colors or gray levels given according to the values on each points

Proof Since for 1 ≤ i ≤ d , the function Ki is a covariance function on R × R we may consider independent centered Gaussian processes X (i) = (X (i) t )t ∈ R with covariance given by Ki . For x = (x 1 , . . . , x d ) ∈ R d , we may define the random variable Xx = ∏ d i = 1 X (i) x · ei so that the random field X = (Xx) x ∈ R d is second order (but no more Gaussian!), centered, with covariance given by

$$C o v ( X _ { x } , X _ { y } ) = \mathbb { E } \left ( X _ { x } X _ { y } \right ) = \prod _ { i = 1 } ^ { d } \mathbb { E } \left ( X _ { x \cdot e _ { i } } ^ { ( i ) } X _ { y \cdot e _ { i } } ^ { ( i ) } \right ) = \prod _ { i = 1 } ^ { d } K _ { i } ( x _ { i } , y _ { i } ) ,$$

by independence of X ( 1 ) , . . . , X (d) .

⊓

⊔

This leads to the second fundamental extension of Brownian motion on the whole space R d , by choosing Ki = KB for all 1 ≤ i ≤ d .

Definition 4.7 A (standard) Brownian sheet on R d is a centered Gaussian field (Xx) x ∈ R d with covariance function given by

$$C o v ( X _ { x } , X _ { y } ) = \prod _ { i = 1 } ^ { d } \frac { 1 } { 2 } ( | x \cdot e _ { i } | + | y \cdot e _ { i } | - | x \cdot e _ { i } - y \cdot e _ { i } | ) , \ \forall x , y \in \mathbb { R } ^ { d } .$$

Note that it implies that this field is equal to 0 on the axes { x ∈ R d ; ∃ i ∈ { 1 , . . . , d } , x · ei = 0 } and corresponds to a Brownian motion (non-standard) when restricted to { x + tei ; t ∈ R } , for x ∈ R d with x · ei = 0. The following section will focus on some invariance properties.

#### 4.1.2 Stationarity and Invariances

When considering stochastic modeling of homogeneous media it is usual to assume an invariance of distributions under translation (stationarity) or vectorial rotation (isotropy).


<!-- p:145 -->


##### 4.1.2.1 Stationarity and Isotropy

Definition 4.8 The random field X = (Xx) x ∈ R d is (strongly) stationary if, for all x 0 ∈ R d , the random field (Xx + x 0 ) x ∈ R d has the same distribution than X .

It implies a specific structure of second order moments.

Proposition 4.5 If X = (Xx) x ∈ R d is a stationary second order random field, then,

- its mean function is constant mX(x) = mX , for all x ∈ R d and some mX ∈ R ;
- its covariance may be written as KX(x,y) = cX(x - y) with cX : R d → R an even function satisfying
- (i) cX( 0 ) ≥ 0 ;

(iii) cX is of non-negative type ie ∀ k ≥ 1 , x 1 , . . . , xk ∈ R d , λ 1 , . . . , λk ∈ C ,

- (ii) | cX(x) | ≤ cX( 0 ) ∀ x ∈ R d ;

$$\sum _ { j , l = 1 } ^ { k } \lambda _ { j } \overline { \lambda _ { l } } c _ { X } ( x _ { j } - x _ { l } ) \geq 0 .$$

Let us remark that the two above properties characterize the weak (second-order) stationarity. Note also that they imply strong stationarity when the field is assumed to be Gaussian. This is because mean and covariance functions characterize the distribution of Gaussian fields.

Proof Since Xx d = X 0 we get mX(x) = E (Xx) = E (X 0 ) := mX . For the covariance structure we set cX(z) = KX(z, 0 ) , for all z ∈ R d , and remark that for y ∈ R d , one has (Xz + y , Xy ) d = (Xz, X 0 ) so that Cov (Xz + y , Xy ) = cX(z) . Hence for z = x - y we obtain KX(x,y) = cX(x - y) . Since (Xx, X 0 ) d = (X 0 , X - x ) , the function cX is even. The first point comes from the fact that cX( 0 ) = Var (X 0 ) = Var (Xx) ≥ 0, the second one is obtained using Cauchy-Schwarz inequality to bound | Cov (Xx, X 0 ) | . The last one is just a reformulation of the non-negative definiteness of KX when λ 1 , . . . , λk ∈ R . Otherwise, it follows writing λj = aj + ibj since we have R (λj λl ) = aj al + bj bl and I (λj λl ) = bj al - bl aj with cX even. ⊓ ⊔

By Bochner's theorem (1932), a continuous function of non-negative type is a Fourier transform of a non-negative finite measure. This can be rephrased as the following theorem.

Remark that when a function c : R d → R satisfies (4.1), then c must be even and satisfy points (i) and (ii) . Actually, (i) is obtained for k = 1, λ 1 = 1 and x 1 = 0. Considering k = 2, x 1 = 0 and x 2 = x ∈ R d , we first obtain for λ 1 = 1 and λ 2 = i that 2 c( 0 ) + ic(x) - ic( - x) ≥ 0 hence c is even, while for λ 1 = λ 2 = 1 it yields - c(x) ≤ c( 0 ) and for λ 1 = 1 = - λ 2 we get c(x) ≤ c( 0 ) so that (ii) is satisfied.

Theorem 4.2 (Bochner) A continuous function c : R d → R is of non-negative type if and only if c( 0 ) ≥ 0 and there exists a symmetric probability measure ν on


<!-- p:146 -->


4

R d such that

$$\forall x \in \mathbb { R } ^ { d } , \ c ( x ) = c ( 0 ) \int _ { \mathbb { R } ^ { d } } e ^ { i x \cdot \xi } d \nu ( \xi ) .$$

In other words there exists a symmetric random vector Z on R d such that

$$\forall x \in \mathbb { R } ^ { d } , \ c ( x ) = c ( 0 ) \mathbb { E } ( e ^ { i x \cdot Z } ) .$$

When c = cX is the covariance of a random field X , the measure ν = νX is called the spectral measure of X . This strong result implies in particular that we may define stationary centered Gaussian random field with a covariance function given by the characteristic function of a symmetric random vector.

Proof Note that the converse implication is straightforward so we will only prove the first one. We may assume that c( 0 ) &gt; 0, otherwise there is nothing to prove. The first step is to assume that c ∈ L 1 ( R d ) . Note that in view of (ii), since c is bounded we also have c ∈ L 2 ( R d ) . We will prove that its Fourier transform ˆ c ∈ L 2 ( R d ) is necessarily non-negative. To this end remark that, approximating by Riemann sums for instance, we necessarily have

$$\int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } g ( x ) \overline { g ( y ) } c ( x - y ) d x d y \geq 0 ,$$

for all g ∈ S ( R d ) , the Schwartz class of infinitely differentiable function with rapid decreasing. We denote as usual ˆ g(ξ) = ∫ R d e - ix · ξ g(x)dx , the Fourier transform, that may be extended to any L 2 ( R d ) function. We may rewrite ∫ R d ∫ R d g(x)g(y)c(x - y)dxdy = ∫ R d g(x)c ∗ g(x)dx , where ∗ is the usual convolution product on L 1 ( R d ) and c ∗ g ∈ L 2 ( R d ) since c ∈ L 1 ( R d ) and g ∈ S ( R d ) ⊂ L 2 ( R d ) . Hence, by Plancherel's theorem (see [55] for instance), we have

$$\frac { 1 } { ( 2 \pi ) ^ { d } } \int _ { \mathbb { R } ^ { d } } \hat { c } ( \xi ) | \hat { g } ( - \xi ) | ^ { 2 } d \xi = \int _ { \mathbb { R } ^ { d } } g ( x ) c * \overline { g } ( x ) d x ,$$

where the right hand side is non-negative in view of (4.2). Now, for σ &gt; 0, let us denote by hσ the density of a centered Gaussian vector of R d with covariance σ 2 Id ie hσ (x) = 1 σ d ( 2 π) d/ 2 e - ‖ x ‖ 2 2 σ 2 . Its characteristic function is given by the Fourier transform ˆ hσ (ξ) = e - σ 2 ‖ ξ ‖ 2 2 . In this way (hσ )σ is an approximation of identity and c ∗ hσ (x) → c(x) , as σ → 0, since c is continuous. Moreover, ˆ c is also continuous as the Fourier transform of an L 1 ( R d ) function, so that we also have ˆ c ∗ hσ (ξ) → ˆ c(ξ) . Now we will prove that ˆ c ≥ 0. Let us take gσ (x) = σ d/ 2 2 d/ 4 π 3 d/ 4 e - σ 2 ‖ x ‖ 2 such that


<!-- p:147 -->


| ˆ gσ | 2 = hσ , by (4.2) and (4.3), we obtain that for all σ &gt; 0

$$\hat { c } * h _ { \sigma } ( 0 ) = \int _ { \mathbb { R } ^ { d } } \hat { c } ( \xi ) h _ { \sigma } ( \xi ) d \xi = ( 2 \pi ) ^ { d } \int _ { \mathbb { R } ^ { d } } g _ { \sigma } ( x ) c * \overline { g _ { \sigma } } ( x ) d x \geq 0 .$$

Letting σ tend to 0 we get ˆ c( 0 ) ≥ 0. But for all ξ ∈ R d , the function e - iξ · c is an L 1 ( R d ) function satisfying (4.1). Hence its Fourier transform is non-negative at point 0, according to previously. But this is exactly ˆ c(ξ) and therefore ˆ c is nonnegative. Using Fatou Lemma in (4.1), for g = hσ as σ tends to 0 we also obtain that ∫ R d ˆ c(ξ)dξ ≤ c( 0 ) ensuring that ˆ c ∈ L 1 ( R d ) . Then, by the Fourier inversion theorem, since c and ˆ c are even, we get

$$c ( x ) = \frac { 1 } { ( 2 \pi ) ^ { d } } \int _ { \mathbb { R } ^ { d } } e ^ { i x \cdot \xi } \hat { c } ( \xi ) d \xi ,$$

with c( 0 ) = 1 ( 2 π) d ∫ R d ˆ c(ξ)dξ . Hence we can choose Z a random vector with density given by ˆ c/(( 2 π) d c( 0 )) .

For the general case we remark that c ˆ hσ is also a function of non-negative type. Actually, since ˆ hσ is the Fourier transform of a non-negative function, by converse of Bochner's theorem it is of non-negative type and we may consider Xσ a centered stationary Gaussian random field with covariance ˆ hσ . Let us also consider X a centered stationary Gaussian random field with covariance c , independent from Xσ . Then the random field XXσ is stationary and admits c ˆ hσ for covariance function. Since c is bounded by (ii) , the function c ˆ hσ is in L 1 ( R d ) and we may find Zσ such that [ c ˆ hσ ] = c( 0 ) E (e ix · Zσ ) . But c ˆ hσ tends to c which is continuous at 0 as σ tends to 0. Hence, by Lévy's theorem (see [28] for instance), there exists a random vector Z such that Zσ d -→ σ → 0 Z and ν = P Z is convenient. Let us finally conclude that Z is symmetric since c is even. ⊓ ⊔

Examples of stationary Gaussian processes are given by Ornstein Uhlenbeck processes constructed on R with a parameter θ &gt; 0 and B a standard Brownian motion on R + (Fig. 4.3), by

$$X _ { t } = e ^ { - \theta t } B _ { e ^ { 2 \theta t } } , \forall t \in \mathbb { R } .$$

Then X = (Xt )t is clearly a centered Gaussian process with covariance

$$C o v ( X _ { t } , X _ { s } ) = e ^ { - \theta | t - s | } \colon = c _ { X } ( t - s ) , \ \forall t , s \in \mathbb { R } .$$

Hence it is weakly stationary and also strongly since it is Gaussian. Now the spectral measure is given by νX(dt) = θ 2 π(θ 2 + t 2 ) dt , or equivalently cX(t) = E (e it · Zθ ) , with Zθ a random variable with Cauchy distribution of parameter θ .


<!-- p:148 -->


4

Fig. 4.3 Sample paths of Ornstein Uhlenbeck process on [ 0 , 1 ] , using fast and exact synthesis via circulant embedding matrix method

Definition 4.9 The random field X = (Xx) x ∈ R d is isotropic if, for all R rotation of R d , the random field (XRx) x ∈ R d has the same distribution than X .

Note that, contrarily to the stationarity, the notion of isotropy is useless in dimension 1! We already have seen one example of isotropic random field when considering the Lévy Chentsov random field. Actually, for all R rotation of R d ,

$$C o v ( X _ { R x } , X _ { R y } ) = \frac { 1 } { 2 } \left ( \| R x \| + \| R y \| - \| R x - R y \| \right ) = C o v ( X _ { x } , X _ { y } ) .$$

Since X is centered and Gaussian this implies that (XRx) x ∈ R d has the same distribution than X . However X is not stationary (note that X( 0 ) = 0 a.s.). An example of stationary and isotropic random field may be given by considering Gaussian covariances ˆ hσ , for σ &gt; 0 (with Zσ ∼ N ( 0 , σ Id ) in Bochner's theorem). Let us also remark that considering the covariance function kσ (t, s) = e - σ 2 (t - s)/ 2 on R × R we also have

$$K _ { \sigma } ( x , y ) = \hat { h } _ { \sigma } ( x - y ) = \prod _ { i = 1 } ^ { d } k _ { \sigma } ( x \cdot e _ { i } , y \cdot e _ { i } ) ,$$

so that this field has also a sheet structure as in Proposition 4.4. Since ˆ hσ is isotropic, we also have Kσ(Rx,Ry) = Kσ(x,y) for x, y ∈ R d , and this allows to define a stationary isotropic centered Gaussian field with covariance Kσ (Fig. 4.4).

Another very important invariance property is the scale invariance also called self-similarity for random fields.

##### 4.1.2.2 Self-Similarity or Scale Invariance

Definition 4.10 The random field X = (Xx) x ∈ R d is self-similar of order H &gt; 0 if, for all λ &gt; 0, the random field (Xλx) x ∈ R d has the same distribution than λ H X = (λ H Xx) x ∈ R d .


<!-- p:149 -->


=

Fig. 4.4 Sample paths of center Gaussian random fields with Gaussian covariances on [ 0 , 1 ] 2 , obtained using circulant embedding matrix method (see [53] for details)

Note that the Lévy Chentsov field, and in particular the Brownian motion ( d = 1), is self-similar of order H = 1 / 2 since

$$C o v ( X _ { \lambda x } , X _ { \lambda y } ) & = \frac { 1 } { 2 } \left ( \| \lambda x \| + \| \lambda y \| - \| \lambda x - \lambda y \| \right ) \\ & = \lambda C o v ( X _ { x } , X _ { y } ) = C o v ( \lambda ^ { 1 / 2 } X _ { x } , \lambda ^ { 1 / 2 } X _ { y } )$$

Recall that X is isotropic but not stationary. Actually, there does not exist a nontrivial stationary self-similar second order field since we should have Var (Xx) = Var (Xλx) = λ 2 H Var (Xx) for all λ &gt; 0 and x ∈ R d , implying that Var (Xx) = 0. In order to define self-similar fields for homogeneous media we must relax stationary property. This is done throughout the notion of stationary increments.

##### 4.1.2.3 Stationary Increments

Definition 4.11 The random field X = (Xx) x ∈ R d has (strongly) stationary increments if, for all x 0 ∈ R d , the random field (Xx + x 0 - Xx 0 ) x ∈ R d has the same distribution than (Xx - X 0 ) x ∈ R d .

Of course a stationary random field X has stationary increments but this class is larger: it also contents X - X 0 for instance that can not be stationary except if it is almost surely equal to 0. An example of field with stationary increments is given by the Levy Chentsov field X since we have

$$C o v ( X _ { x + x _ { 0 } } - X _ { x _ { 0 } } , X _ { y + x _ { 0 } } - X _ { x _ { 0 } } ) = C o v ( X _ { x } - X _ { 0 } , X _ { y } - X _ { 0 } ) ,$$

using the fact that X 0 = 0 a.s. We have an analogous of Proposition 4.5 concerning second order structure of fields with stationary increments.

1


<!-- p:150 -->


4

Proposition 4.6 If X = (Xx) x ∈ R d is a second order centered random field with stationary increments and X 0 = 0 a.s., then its covariance function may be written as

$$K _ { X } ( x , y ) = \frac { 1 } { 2 } \left ( v _ { X } ( x ) + v _ { X } ( y ) - v _ { X } ( x - y ) \right ) ,$$

with the function vX(x) = Var (Xx + x 0 - Xx 0 ) = Var (Xx - X 0 ) = Var (Xx) called variogram satisfying

1. vX( 0 ) = 0
3. vX is conditionally of negative type ie ∀ k ≥ 1 , x 1 , . . . , xk ∈ R d , λ 1 , . . . , λk ∈ C ,
2. vX(x) ≥ 0 and vX( - x) = vX(x)

$$\sum _ { j = 1 } ^ { k } \lambda _ { j } = 0 \Rightarrow \sum _ { j , l = 1 } ^ { k } \lambda _ { j } \overline { \lambda _ { l } } v _ { X } ( x _ { j } - x _ { l } ) \leq 0 .$$

Note that when X 0 does not vanish a.s. this proposition applies to X - X 0.

Proof Compute Var (Xx - Xy) = Var (Xx) + Var (Xx) + 2 KX(x,y) and note that Xx - Xy d = Xx - y - X 0 = Xx - y to get KX with respect to vX . We clearly have vX ≥ 0 as a variance and vX( 0 ) = 0 since X 0 = 0 a.s. The evenness comes from X - x = X - x - X 0 d = X 0 - Xx = - Xx . The last property follows from the fact that

$$V _ { \left ( \sum _ { j = 1 } ^ { k } \lambda _ { j } X _ { x _ { j } } \right ) } = \frac { 1 } { 2 } \sum _ { j , l = 1 } ^ { k } \lambda _ { j } \lambda _ { l } \left ( v _ { X } ( x _ { j } ) + v _ { X } ( x _ { l } ) - v _ { X } ( x _ { j } - x _ { l } ) \right ) \geq 0 ,$$

for λ 1 , . . . , λk ∈ R , using the expression of KX(xj,xl) with respect to vX . The inequality is extended for λ 1 , . . . , λk ∈ C as in Proposition 4.5 since vX is also even. ⊓ ⊔

In order to define centered Gaussian random fields we can use the following result.

Theorem 4.3 (Schoenberg) Let v : R d → R be a function such that v( 0 ) = 0 . The following are equivalent.

- i) v is conditionally of negative type;
2. ii) K : (x, y) ∈ R d × R d ↦→ 1 2 (v(x) + v(y) - v(x - y)) is a covariance function;
3. iii) For all λ &gt; 0 , the function e - λv is of non-negative type.

Proof To prove that i) ⇒ ii) , we use Proposition 4.1. Symmetry comes from the fact that v is even. Actually, taking k = 2, λ 1 = i = - λ 2 and x 1 = x , x 2 = 0 we obtain that v(x) ≤ v( - x) since v( 0 ) = 0, such that replacing x by - x we get v(x) = v( - x) . For the second point let k ≥ 1, x 1 , . . . , xk ∈ R d , λ 1 , . . . , λk ∈ R


<!-- p:151 -->


and set λ 0 = - ∑ k i = 1 λi and x 0 = 0. We compute k ∑ i,j = 1 λi λj K(xi, xj ) as

$$and set \lambda _ { 0 } = - \sum _ { i = 1 } ^ { k } \lambda _ { i } \text { and } x _ { 0 } = 0 . \text { We compute } \sum _ { i , j = 1 } ^ { k } \lambda _ { i } \lambda _ { j } K ( x _ { i } , x _ { j } ) \text { as } \\ \sum _ { i , j = 1 } ^ { k } \lambda _ { i } \lambda _ { j } v ( x _ { i } ) - \frac { 1 } { 2 } \sum _ { i , j = 1 } ^ { k } \lambda _ { i } \lambda _ { j } v ( x _ { i } - x _ { j } ) = - \lambda _ { 0 } \sum _ { i = 1 } ^ { k } \lambda _ { i } v ( x _ { i } ) \\ - \frac { 1 } { 2 } \sum _ { j = 1 } ^ { k } \lambda _ { j } \sum _ { i = 1 } ^ { k } \lambda _ { i } v ( x _ { i } - x _ { j } ) \\ = - \frac { 1 } { 2 } \lambda _ { 0 } \sum _ { i = 1 } ^ { k } \lambda _ { i } v ( x _ { i } ) \\ - \frac { 1 } { 2 } \sum _ { j = 0 } ^ { k } \lambda _ { j } \sum _ { i = 1 } ^ { k } \lambda _ { i } v ( x _ { i } - x _ { j } ) \\ = - \frac { 1 } { 2 } \sum _ { j = 0 } ^ { k } \lambda _ { j } \sum _ { i = 0 } ^ { k } \lambda _ { i } v ( x _ { i } - x _ { j } ) \geq 0 , \\ \intertext { s i n c v e r s } \text { since } v \text { is even and conditionally of negative type. } \\ \text { Let us now consider } i i \right \} \Rightarrow i i \text { . Let } ( X ^ { ( n ) } ) _ { i } \text { be a sequence of } i d \text { centered Gaussian } \\ \text { random fields with covariance function } g \text { given by } K \text { and } N \text { independent Poisson }$$

since v is even and conditionally of negative type.

Let us now consider ii) ⇒ iii) . Let (X (n) )n be a sequence of iid centered Gaussian random fields with covariance function given by K and N an independent Poisson random variable of parameter λ &gt; 0. We may define a new random field Y = ∏ N n = 1 X (n) , with the convention that ∏ 0 n = 1 = 1. Therefore, for all x, y ∈ R d , we get

$$\mathbb { E } ( Y _ { x } Y _ { y } ) & = \sum _ { k = 0 } ^ { + \infty } \mathbb { E } ( Y _ { x } Y _ { y } | N = k ) \mathbb { P } ( N = k ) \\ & = \sum _ { k = 0 } ^ { + \infty } \mathbb { E } ( \prod _ { n = 1 } ^ { k } X _ { x } ^ { ( n ) } X _ { y } ^ { ( n ) } ) e ^ { - \lambda } \frac { \lambda ^ { k } } { k ! } \\ & = \sum _ { k = 0 } ^ { + \infty } K ( x , y ) ^ { k } e ^ { - \lambda } \frac { \lambda ^ { k } } { k ! } = e ^ { - \lambda ( 1 - K ( x , y ) ) } , \\$$

by independence. Now remark that E (Y 2 x ) = e - λ( 1 - K(x,x)) = e - λ( 1 - v(x)) . Hence defining the random field Z by setting Zx = Yx √ E (Y 2 x ) e λ/ 2 we get

$$\mathbb { E } ( Z _ { x } Z _ { y } ) = \frac { e ^ { \lambda } } { e ^ { - \lambda ( 1 - \frac { 1 } { 2 } ( v ( x ) + v ( y ) ) ) } } e ^ { - \lambda ( 1 - K ( x , y ) ) } = e ^ { - \frac { \lambda } { 2 } v ( x - y ) } .$$


<!-- p:152 -->


4

As a consequence, for all k ≥ 1, x 1 , . . . , xk ∈ R d and λ 1 , . . . , λk ∈ R

$$\sum _ { j , l } ^ { k } \lambda _ { j } \lambda _ { l } e ^ { - \frac { \lambda } { 2 } v ( x _ { j } - x _ { l } ) } = \mathbb { E } \left ( \left ( \left ( \sum _ { j } ^ { k } \lambda _ { j } Z _ { x _ { j } } \right ) ^ { 2 } \right ) \geq 0 . \\ \\$$

Note that v must be even since K(x, 0 ) = K( 0 , x) by symmetry of a covariance function and v( 0 ) = 0 so that the previous inequality extends to λ 1 , . . . , λk ∈ C . This finishes to prove iii).

The last implication iii) ⇒ i) comes from the fact for k ≥ 1, λ 1 , . . . , λk ∈ C s.t. ∑ k j = 1 λj = 0, x 1 , . . . , xk ∈ R d , we may write for all ε &gt; 0,

$$\sum _ { j , l = 1 } ^ { k } \lambda _ { j } \overline { \lambda } _ { l } v ( x _ { j } - x _ { l } ) \frac { 1 } { \varepsilon } \int _ { 0 } ^ { \varepsilon } e ^ { - \lambda v ( x _ { j } - x _ { l } ) } d \lambda = \frac { 1 } { \varepsilon } \sum _ { j , l = 1 } ^ { k } \lambda _ { j } \overline { \lambda } _ { l } ( 1 - e ^ { - \varepsilon v ( x _ { j } - x _ { l } ) } ) \geq 0 ,$$

since ∑ k j = 1 λj = 0 and e - εv is of non-negative type. Hence letting ε tend to 0 we get the result. ⊓ ⊔

An important corollary for the construction of self-similar fields with stationary increments is the following one due to J. Istas in [35].

As an application of this result we may deduce that the function v(x) = ‖ x ‖ 2 is a variogram. Actually, this easily follows from bi-linearity of the Euclidean product since v(x - y) = ‖ x ‖ 2 + ‖ y ‖ 2 - 2 x · y . But we can also remark that for all σ&gt; 0, the function e - σ 2 2 v is the Gaussian covariance function which implies that v is conditionally of negative type. Let us remark that this variogram corresponds to a kind of trivial field since choosing Z ∼ N ( 0 , Id ) , one can define the centered Gaussian random field Xx = x · Z , for x ∈ R d , that admits v for variogram.

Corollary 4.1 If v : R d → R + is a variogram then the function v H is also a variogram for all H ∈ ( 0 , 1 ] .

Proof There is nothing to prove for H = 1 and when H ∈ ( 0 , 1 ) , it is sufficient to remark that, by a change of variable, one has for t ≥ 0,

$$t ^ { H } = c _ { H } \int _ { 0 } ^ { + \infty } \frac { 1 - e ^ { - \lambda t } } { \lambda ^ { H + 1 } } d \lambda ,$$

for c - 1 H = ∫ +∞ 0 1 - e - λ λ H + 1 dλ ∈ ( 0 , +∞ ) . Hence, for k ≥ 1, λ 1 , . . . , λk ∈ C s.t. ∑ k j = 1 λj = 0, x 1 , . . . , xk ∈ R d , we get

$$\sum _ { j , l = 1 } ^ { k } \lambda _ { j } \overline { \lambda } _ { l } v ( x _ { j } - x _ { l } ) ^ { H } & = - c _ { H } \int _ { 0 } ^ { + \infty } \sum _ { j , l = 1 } ^ { k } \lambda _ { j } \overline { \lambda } _ { l } e ^ { - \lambda v ( x _ { j } - x _ { l } ) } \lambda ^ { - H - 1 } d \lambda \leq 0 , \\$$

in view of Schoenberg's theorem since v is a variogram.

⊓

⊔


<!-- p:153 -->


Fig. 4.5 Sample paths realizations of fractional Brownian fields on [ 0 , 1 ] 2 for different values of H , obtained using the fast and exact synthesis method presented in Sect. 4.3.1.3

It follows that for all H ∈ ( 0 , 1 ] the function vH(x) = ‖ x ‖ 2 H is conditionally of negative type and leads to the next definition.

Definition 4.12 A(standard) fractional Brownian field on R d (Fig. 4.5), with Hurst parameter H ∈ ( 0 , 1 ] , is a centered Gaussian field (BH ) x ∈ R d with covariance function given by

$$C o v ( B _ { H } ( x ) , B _ { H } ( y ) ) = \frac { 1 } { 2 } \left ( \| x \| ^ { 2 H } + \| y \| ^ { 2 H } - \| x - y \| ^ { 2 H } \right ) , \, \forall x , y \in \mathbb { R } ^ { d } .$$

Of course when H = 1 / 2, we recognize B 1 / 2 as the Lévy Chentsov field. The order of self-similarity is now given by H . Note also that the case H = 1 corresponds to a degenerate case where B 1 = (x · Z)x for Z ∼ N ( 0 , Id ) .

Proposition 4.7 Up to a constant, the fractional Brownian field of order H ∈ ( 0 , 1 ] is the unique isotropic centered Gaussian field with stationary increments which is self-similar of order H .

Proof This comes from the fact that the distribution of a centered Gaussian field X with stationary increments is characterized by its variogram vX as soon as X( 0 ) = 0 a.s. Self-similarity implies that X( 0 ) = 0 and therefore, for all λ &gt; 0 we have vX(λx) = Var (Xλx) = Var (λ H Xx) = λ 2 H Var (Xx) = λ 2 H vX(x) . Hence for all x ̸= 0, vX(x) = ‖ x ‖ 2 H vX( x ‖ x ‖ ) . But isotropy also implies that Xθ d = Xe 1 for all θ ∈ S d - 1 and e 1 = ( 1 , 0 , . . . , 0 ) ∈ S d - 1 . Hence vX(θ) = vX(e 1 ) and X d = √ vX(e 1 )BH . ⊓ ⊔

Let us also remark that we cannot find a second order field with stationary increments that is self-similar for an order H &gt; 1. Actually, by triangular inequality for ‖ · ‖ 2 := √ Var ( · ) , when X is a second order field, we have ‖ X 2 x ‖ 2 ≤ ‖ X 2 x - Xx ‖ 2 + ‖ Xx ‖ 2, for all x ∈ R d . Self-similarity of order H &gt; 0 implies that X 0 = 0 a.s. and ‖ X 2 x ‖ 2 = 2 H ‖ Xx ‖ 2, while stationary increments imply that


<!-- p:154 -->


4

‖ X 2 x - Xx ‖ 2 = ‖ Xx - X 0 ‖ 2 = ‖ Xx ‖ 2. Therefore we must have 2 H - 1 ‖ Xx ‖ 2 ≤ 1 and H ≤ 1 or Xx = 0 for all x ∈ R d .

In dimension d = 1, it is called fractional Brownian motion, implicitly introduced in [41] and defined in [47]. The order of self-similarity H is also called Hurst parameter. Hence the fractional Brownian field is an isotropic generalization of this process. Other constructions using sheet structure are known as fractional Brownian sheets but these fields loose stationary increments (see e.g. [22]).

Anisotropy may be an interesting property in applications (see [16] for instance). We also refer to [2] for many examples of anisotropic variograms. For instance, we can consider several anisotropic generalizations of fractional Brownian motions by keeping self-similarity and stationary increments properties following Proposition 4.3. Let H ∈ ( 0 , 1 ) and vH : t ∈ R ↦→| t | 2 H be the variogram of a fractional Brownian motion that is conditionally of negative type. If μ is a finite positive measure on S d - 1 , we may define on R d ,

$$v _ { H , \mu } ( x ) = \int _ { S ^ { d - 1 } } v _ { H } ( x \cdot \theta ) \mu ( d \theta ) = \int _ { S ^ { d - 1 } } | x \cdot \theta | ^ { 2 H } \mu ( d \theta ) = c _ { H , \mu } \left ( \frac { x } { \| x \| } \right ) \| x \| ^ { 2 H } ,$$

that is now a conditionally of negative type function on R d . Hence we may consider XH,μ = (XH,μ(x)) x ∈ R d a centered Gaussian random field with stationary increments and variogram given by vH,μ . This new random field is still self-similar of order H but may not be isotropic according to the choice of μ . The function cH,μ , describing anisotropy, is called topothesy function as in [25].

For instance, when d = 2 we can choose μ(dθ) = 1 ( - α,α)(θ)dθ for some α ∈ ( 0 , π/ 2 ] . Let β H (t) = ∫ t 0 u H - 1 / 2 ( 1 - u) H - 1 / 2 du , t ∈ [ 0 , 1 ] , be a Beta incomplete function. Then the corresponding topothesy function denoted now by cH,α is a π periodic function defined on ( - π/ 2 , π/ 2 ] by

$$c _ { H , \alpha } ( \theta ) = 2 H \begin{cases} \beta _ { H } \left ( \frac { 1 - \sin ( \alpha - \theta ) } { 2 } \right ) + \beta _ { H } \left ( \frac { 1 + \sin ( \alpha + \theta ) } { 2 } \right ) & \text {if } - \alpha \leq \theta + \frac { \pi } { 2 } \leq \alpha \\ \beta _ { H } \left ( \frac { 1 + \sin ( \alpha - \theta ) } { 2 } \right ) + \beta _ { H } \left ( \frac { 1 - \sin ( \alpha + \theta ) } { 2 } \right ) & \text {if } - \alpha \leq \theta - \frac { \pi } { 2 } \leq \alpha \\ \left | \beta _ { H } \left ( \frac { 1 - \sin ( \alpha - \theta ) } { 2 } \right ) - \beta _ { H } \left ( \frac { 1 + \sin ( \alpha + \theta ) } { 2 } \right ) \right | & \text {otherwise} \end{cases} \\ \text {We refer to } [ 1 4 ] \text { for computations details and to Fig. 4.6 for plots of these functions.} \\ \text {The associated Gaussian random field denoted by } Y _ { \cdot } \text { , is called } \text { elementary} .$$

We refer to [14] for computations details and to Fig. 4.6 for plots of these functions.

The associated Gaussian random field denoted by XH,α is called elementary anisotropic fractional Brownian field. Several realizations are presented in Fig. 4.7 for different values of parameters α and H . Note that when α = π/ 2 the random field XH,α is isotropic and therefore corresponds to a non-standard fractional Brownian field.

Another anisotropic generalization is obtained by considering a generalization of the self-similarity property that allows different scaling behavior according to directions.


<!-- p:155 -->


Fig. 4.6 Topothesy functions of some elementary anisotropic fractional Brownian fields

Fig. 4.7 Sample paths realizations of some elementary anisotropic fractional Brownian fields on [ 0 , 1 ] 2 using Turning band method presented in Sect. 4.3.1.2 (see also [14])

##### 4.1.2.4 Operator Scaling Property

Definition 4.13 Let E be a real d × d matrix with eigenvalues of positive real parts and H &gt; 0. The random field X = (Xx) x ∈ R d is (E, H) -operator scaling if for all λ &gt; 0, the random field (X λ E x ) x ∈ R d has the same distribution than λ H X = (λ H Xx) x ∈ R d , where λ E = exp (E log λ) with exp (A) = ∑ ∞ k = 0 A k k ! the matrix exponential.


<!-- p:156 -->


4

Note that when E is the identity matrix we recover the definition of self-similarity of order H . Note also that (E, H) -operator scaling property is equivalent to (E/H, 1 ) operator scaling property. We refer to [9] for general cases and focus here on a simple example where the matrix E is assumed to be diagonalizable. In particular when E is a diagonal matrix, this property may be observed for limit of aggregated discrete random fields (see [42, 52] for instance). In the general case where E is diagonalizable, we assume that its eigenvalues, denoted by α - 1 1 , . . . , α - 1 d , are all greater than 1. They are also eigenvalues of the transpose matrix E t and we denote by θ 1 , . . . , θd the corresponding eigenvectors such that E t θi = α - 1 i θi . We obtained in [7] the following proposition.

Proposition 4.8 For H ∈ ( 0 , 1 ] , the function defined on R d by

$$v _ { H , E } ( x ) = \tau _ { E } ( x ) ^ { 2 H } = \left ( \sum _ { i = 1 } ^ { d } | x \cdot \theta _ { i } | ^ { 2 \alpha _ { i } } \right ) ^ { H } = \left ( \sum _ { i = 1 } ^ { d } v _ { \alpha _ { i } } ( x \cdot \theta _ { i } ) \right ) ^ { H } ,$$

is a variogram.

Proof According to Corollary 4.1, it is enough to prove that τ E (x) 2 is a variogram but this follows from the fact that vαi (x · θi ) is the variogram of ( B (i) αi (x · θi ) ) x ∈ R d , where B ( 1 ) α 1 , . . . , B (d) αd are d independent fractional Brownian motions on R with Hurst parameter given by α 1 , . . . , αd ∈ ( 0 , 1 ] . ⊓ ⊔

Some realizations of operator scaling self-similar random fields are presented in Fig. 4.9. Note that the case where α = 1 corresponds to the isotropic case, whereas the case where H = 1 is a degenerate one obtained by adding two independent fractional Brownian processes.

Therefore, we can consider a centered Gaussian random field XH,E = (XH,E(x)) x ∈ R d with stationary increments and variogram given by vH,E . Then, XH,E is (E, H) operator scaling since vH,E(λ E x) = λ 2 H vH,E(x) for all x ∈ R d . When α 1 = . . . = αd = α ∈ ( 0 , 1 ] , or equivalently when E = α - 1 Id , the random field XH,E is actually αH ∈ ( 0 , 1 ) self-similar with topothesy function given by vH,E( x ‖ x ‖ ) . Now considering (θi ) 1 ≤ i ≤ d = (ei ) 1 ≤ i ≤ d , the canonical basis, such fields are examples of Minkowski fractional Brownian fields (see Proposition 3.3 in [49]). In particular, when d = 2, we get the topothesy functions as the π -periodic functions θ ↦→ ( | cos (θ) | 2 α +| sin (θ) | 2 α ) H (see Fig. 4.8 for some plots).

The realizations of Fig. 4.10 are no more self-similar but when restricting to horizontal, respectively vertical, lines we get fractional Brownian motions of order Hα 1, respectively Hα 2. The sheet structure appearing as H increases to 1 should come from the reduction of dependency between directions. The vertical gradient comes from the fact that the self-similarity exponent Hα 2 is chosen greater than the horizontal one. This is also linked to sample paths regularity as we will see in the following section.

,


<!-- p:157 -->


Fig. 4.8 Topothesy functions of self-similar fields XH,E obtained for E = α - 1 Id

Fig. 4.9 Sample paths realizations of self-similar fields XH,E obtained for E = α - 1 Id and Hα = 0 . 5, using the simulation method presented in Sect. 4.3.1.3

Fig. 4.10 Sample paths realizations of operator scaling fields XH,E obtained for E = diag (α - 1 1 , α - 1 2 ) with Hα 1 = 0 . 5 and Hα 2 = 0 . 6, using the simulation method presented in Sect. 4.3.1.3

<!-- p:158 -->


### 4.2 Sample Paths Properties

In this section we focus on Hölder sample paths properties related to fractal properties of Gaussian random fields. In particular we will see that self-similarity properties induce such fractal behaviors.

#### 4.2.1 Sample Paths Regularity

Before considering sample paths continuity we must introduce the weak notion of stochastic continuity.

Definition 4.14 Let X = (Xx) x ∈ R d be a random field. We say that X is stochastically continuous at point x 0 ∈ R d if

$$\forall \varepsilon > 0 , \lim _ { x \to x _ { 0 } } \mathbb { P } ( | X _ { x } - X _ { x _ { 0 } } | > \varepsilon ) = 0 .$$

Let us emphasize that a centered Gaussian random field with stationary increments is stochastically continuous as soon as its variogram is continuous at point 0, according to Bienaymé Chebyshev's inequality. Since we have only defined random fields as a collection of real variables (Xx) x ∈ R d , when studying the functions x ↦→ Xx(ω) for some typical ω ∈ Ω , we can in general only state results for a modification of X .

Definition 4.15 Let X = (Xx) x ∈ R d be a random field. We say that  ̃ X = (  ̃ Xx) x ∈ R d is a modification of X if

$$\forall x \in \mathbb { R } ^ { d } , \mathbb { P } ( X _ { x } = \tilde { X } _ { x } ) = 1 .$$

Note that it follows that X and  ̃ X have the same distribution since (Xx 1 , . . . , Xxk ) = (  ̃ Xx 1 , . . . ,  ̃ Xxk ) a.s. for all k ≥ 1 and x 1 , . . . , xk ∈ R d . This implies a weaker notion.

Definition 4.16 Let X = (Xx) x ∈ R d be a random field. We say that  ̃ X = (  ̃ Xx) x ∈ R d is a version of X if X and  ̃ X have the same finite dimensional distributions.

We refer to Chapter 9 of [56] for the interested reader.

##### 4.2.1.1 Hölder Regularity

Definition 4.17 Let K = [ 0 , 1 ] d . Let γ ∈ ( 0 , 1 ) . A random field X = (Xx) x ∈ R d is γ -Hölder on K if there exists a finite random variable A such that a.s.

$$\left | X _ { x } - X _ { y } \right | \leq A \| x - y \| ^ { \gamma } , \forall x , y \in K .$$


<!-- p:159 -->


Note that it implies that X is a.s. continuous on K . The following theorem gives a general criterion to ensure the existence of an Hölder modification, particularly helpful for Gaussian fields, generalizing the one dimensional case (see [39, p. 53]).

Theorem 4.4 (Kolmogorov-Chentsov 1956) If there exist 0 &lt; β &lt; δ and C &gt; 0 such that

$$\mathbb { E } \left ( | X _ { x } - X _ { y } | ^ { \delta } \right ) & \leq C \| x - y \| ^ { d + \beta } , \forall x , y \in K , \\ \tilde { \ } r a c { K }$$

then there exists  ̃ X a modification of X γ -Hölder on K , for all γ &lt; β/δ .

Let us note that the assumption clearly implies stochastic continuity of X on K in view of Markov's inequality. We give the constructing proof of this result.

Proof Step 1. For k ≥ 1 we introduce the dyadic points of [ 0 , 1 ] d

$$\mathcal { D } _ { k } = \left \{ \frac { j } { 2 ^ { k } } ; \, j = ( j _ { 1 } , \dots , j _ { d } ) \in \mathbb { N } ^ { d } \text { with } 0 \leq j _ { i } \leq 2 ^ { k } \text { for all } 1 \leq i \leq d \right \} .$$

Note that for x ∈ [ 0 , 1 ] d , there exists xk ∈ D k with ‖ x - xk ‖∞ ≤ 2 - k so that D k is a 2 - k net of K for ‖ · ‖∞ , where ‖ x ‖∞ = max 1 ≤ i ≤ d | x · ei | . The sequence ( D k )k is clearly increasing.

Let γ ∈ ( 0 , β/δ) . For i, j ∈ [ 0 , 2 k ] d ∩ N d with i ̸= j define the measurable set

$$E _ { i , j } ^ { k } = \{ \omega \in \Omega ; | X _ { i / 2 ^ { k } } ( \omega ) - X _ { j / 2 ^ { k } } ( \omega ) | > \| i / 2 ^ { k } - j / 2 ^ { k } \| _ { \infty } ^ { \gamma } \} .$$

By assumption and Markov's inequality

$$\mathbb { P } ( E _ { i , j } ^ { k } ) \leq 2 ^ { - k ( d + \beta - \gamma \delta ) } \| i - j \| _ { \infty } ^ { d + \beta - \gamma \delta } .$$

$$E ^ { k } = \bigcup _ { ( i , j ) \in [ 0 , 2 ^ { k } ] ; 0 < \| i - j \| _ { \infty } \leq 5 } E _ { i , j } ^ { k } .$$

Set

It follows that

$$\mathbb { P } ( E ^ { k } ) & \leq 5 ^ { d + \beta - \gamma \delta } 2 ^ { - k ( d + \beta - \gamma \delta ) } \# ( i , j ) \in [ 0 , 2 ^ { k } ] ; \, 0 < \| i - j \| _ { \infty } \leq 5 \} \\ & \leq 5 ^ { d + \beta - \gamma \delta } 1 0 ^ { d } 2 ^ { - k ( \beta - \gamma \delta ) } .$$

Hence, by Borel-Cantelli Lemma we get P ( lim sup k E k ) = 0 so that the event  ̃ Ω = ∪ k ∩ l ≥ kΩ ∖ E l satisfies P (  ̃ Ω) = 1. Hence, for ω ∈  ̃ Ω , there exists k ∗ (ω) such that for all l ≥ k ∗ (ω) and x, y ∈ D l with 0 &lt; ‖ x - y ‖∞ ≤ 5 × 2 - l , we have

$$| X _ { x } ( \omega ) - X _ { y } ( \omega ) | \leq \| x - y \| _ { \infty } ^ { \gamma } .$$


<!-- p:160 -->


4

Step 2. Let us set D = ∪ k D k . For x, y ∈ D with 0 &lt; ‖ x - y ‖∞ ≤ 2 - k ∗ (ω) , there exists a unique l ≥ k ∗ (ω) with

$$2 ^ { - ( l + 1 ) } < \| x - y \| _ { \infty } \leq 2 ^ { - l } .$$

Moreover, one can find n ≥ l + 1 such that x, y ∈ D n and for all k ∈ [ l, n - 1 ] , there exist xk, yk ∈ D k with ‖ x - xk ‖∞ ≤ 2 - k and ‖ y - yk ‖∞ ≤ 2 - k . We set xn = x and yn = y . Therefore

$$\| x _ { l } - y _ { l } \| _ { \infty } & \leq \| x _ { l } - x \| _ { \infty } + \| x - y \| _ { \infty } + \| y - y _ { l } \| _ { \infty } \\ & \leq 2 \times 2 ^ { - l } + \| x - y \| _ { \infty } .$$

But 2 - l &lt; 2 ‖ x - y ‖∞ and ‖ xl - yl ‖∞ ≤ 5 ‖ x - y ‖∞ ≤ 5 × 2 - l and since l ≥ k ∗ (ω)

$$| X _ { x _ { l } } ( \omega ) - X _ { y _ { l } } ( \omega ) | \leq \| x _ { l } - y _ { l } \| _ { \infty } ^ { \gamma } \leq 5 ^ { \gamma } \| x - y \| _ { \infty } ^ { \gamma } .$$

But for all k ∈ [ l, n - 1 ] , ‖ xk - xk + 1 ‖∞ ≤ 2 - k + 2 - (k + 1 ) ≤ 3 × 2 - (k + 1 ) so that

$$| X _ { x _ { k } } ( \omega ) - X _ { x _ { k + 1 } } ( \omega ) | \leq \| x _ { k } - x _ { k + 1 } \| _ { \infty } ^ { \gamma } \leq ( 3 / 2 ) ^ { \gamma } 2 ^ { - k \gamma } .$$

Similarly,

It follows that

$$It follows that \\ | X _ { x } ( \omega ) - X _ { y } ( \omega ) | \leq \sum _ { k = l } ^ { n - 1 } | X _ { x _ { k } } ( \omega ) - X _ { x _ { k + 1 } } ( \omega ) | + | X _ { x _ { l } } ( \omega ) - X _ { y _ { l } } ( \omega ) | \\ + \sum _ { k = l } ^ { n - 1 } | X _ { y _ { k } } ( \omega ) - X _ { y _ { k + 1 } } ( \omega ) | \\ & \leq \frac { 2 \times 3 ^ { \gamma } } { 2 ^ { \gamma } - 1 } \times 2 ^ { - l \gamma } + 5 ^ { \gamma } \| x - y \| _ { \infty } ^ { \gamma } \\ & \leq c _ { \gamma } \| x - y \| _ { \infty } ^ { \gamma } . \\ \intertext { Step 3. By chaining, we obtain that for all $x , y \in \mathcal { D } $ }$$

Step 3. By chaining, we obtain that for all x, y ∈ D

$$| X _ { x } ( \omega ) - X _ { y } ( \omega ) | \leq c _ { \gamma } 2 ^ { k ^ { * } ( \omega ) } \| x - y \| _ { \infty } ^ { \gamma } ,$$

and we set A(ω) = cγ 2 k ∗ (ω) . Hence we have proven that for all ω ∈  ̃ Ω , x, y ∈ D ,

$$| X _ { x } ( \omega ) - X _ { y } ( \omega ) | \leq A ( \omega ) \| x - y \| _ { \infty } ^ { \gamma } .$$

$$| X _ { y _ { k } } ( \omega ) - X _ { y _ { k + 1 } } ( \omega ) | \leq \| y _ { k } - y _ { k + 1 } \| _ { \infty } ^ { \gamma } \leq ( 3 / 2 ) ^ { \gamma } 2 ^ { - k \gamma } .$$


<!-- p:161 -->


We set  ̃ Xx(ω) = 0 if ω / ∈  ̃ Ω . For ω ∈  ̃ Ω , if x ∈ D we set  ̃ Xx(ω) = Xx(ω) . Otherwise, there exists (xk)k a sequence of dyadic points such that xk → x . Therefore (Xxk (ω)) is a Cauchy sequence and we define  ̃ Xx(ω) as its limit. By stochastic continuity we have

$$\mathbb { P } ( \tilde { X } _ { x } = X _ { x } ) = 1 ,$$

ensuring that  ̃ X is a modification. ⊓ ⊔

In order to get the best regularity we can use the notion of critical Hölder exponent, as defined in [16].

##### 4.2.1.2 Critical Hölder Exponent

Definition 4.18 Let γ ∈ ( 0 , 1 ) . A random field (Xx) x ∈ R d admits γ as critical Hölder exponent on [ 0 , 1 ] d if there exists  ̃ X a modification of X such that:

- (a) ∀ s &lt; γ , a.s.  ̃ X satisfies H(s) : ∃ A ≥ 0 a finite random variable such that ∀ x, y ∈ [ 0 , 1 ] d ,

$$| X _ { x } - X _ { y } | & \leq A \| x - y \| ^ { s } . \\ \intertext { i s t i s f y } \hat { H } ( s ) &$$

- (b) ∀ s &gt; γ , a.s.  ̃ X fails to satisfy H(s) .

For centered Gaussian random fields it is enough to consider second order regularity property as stated in the next proposition (see also [1]).

Proposition 4.9 Let (Xx) x ∈ R d be a centered Gaussian random field. If for all ε &gt; 0 , there exist c 1 , c 2 &gt; 0 , such that, for all x, y ∈ [ 0 , 1 ] d ,

$$c _ { 1 } \| x - y \| ^ { 2 \gamma + \varepsilon } \leq \mathbb { E } \left ( X _ { x } - X _ { y } \right ) ^ { 2 } \leq c _ { 2 } \| x - y \| ^ { 2 \gamma - \varepsilon } , \\$$

then the critical Hölder exponent of X on [ 0 , 1 ] d is equal to γ .

Proof The upper bound allows to use Kolmogorov-Chentsov theorem since for all k ∈ N ∗ and ε &gt; 0, using the fact that X is Gaussian, one can find c with

$$\mathbb { E } \left ( X _ { x } - X _ { y } \right ) ^ { 2 k } = \frac { ( 2 k - 1 ) ! } { 2 ^ { k - 1 } ( k - 1 ) ! } \left ( \mathbb { E } \left ( X _ { x } - X _ { y } \right ) ^ { 2 } \right ) ^ { k } \leq c \| x - y \| ^ { 2 \gamma k - \varepsilon } .$$

Hence considering  ̃ X the modification of X constructed in the previous proof we see that  ̃ X is a.s. s -Hölder for all s &lt; 2 γk - ε 2 k . But since 2 γk - ε 2 k → γ , this is true for all s &lt; γ . Note that according to the lower bound, for any s &gt; γ , choosing ε = s - γ , for any x ̸= y , the Gaussian random variable  ̃ Xx -  ̃ Xy ‖ x - y ‖ s admits a variance greater than


<!-- p:162 -->


4

c 1 ‖ x - y ‖ - (s - γ) , that tends to infinity as x tends to y . Therefore it is almost surely unbounded as ‖ x - y ‖ → 0. ⊓ ⊔

We have therefore a very simple condition on variogram for Gaussian random fields with stationary increments.

Corollary 4.2 Let X be a centered Gaussian field with stationary increments. If for all ε &gt; 0 , there exist c 1 , c 2 &gt; 0 , such that for all x ∈ [- 1 , 1 ] d ,

$$c _ { 1 } \| x \| ^ { 2 \gamma + \varepsilon } \leq v _ { X } ( x ) = \mathbb { E } ( ( X _ { x } - X _ { 0 } ) ^ { 2 } ) \leq c _ { 2 } \| x \| ^ { 2 \gamma - \varepsilon } ,$$

then X has critical Hölder exponent on [ 0 , 1 ] d equal to γ .

This allows to compute critical exponents of several examples presented above.

- Fractional Brownian fields with variogram vH (x) = ‖ x ‖ 2 H and 2-dimensional elementary anisotropic fractional Brownian fields with variogram vH,α(x) = cH,α(x/ ‖ x ‖ ) ‖ x ‖ 2 H for α ∈ ( 0 , π/ 2 ] have critical Hölder exponent given by H (see Figs. 4.5 and 4.7).
- Stationary Ornstein Uhlenbeck processes have variogram given by vX(t) = 2 (cX( 0 ) - cX(t)) = 2 ( 1 - e - θ | t | ) . It follows that their critical Hölder exponent is given by 1 / 2 as for Brownian motion (see Fig. 4.3).
- Operator scaling random fields with variogram given by vH,E(x) = ( ∑ d i = 1 | x · θi | 2 αi ) H admit H min1 ≤ i ≤ d αi for critical Hölder exponent (see Figs. 4.9 and 4.10).

Note that this global regularity does not capture anisotropy of these last random fields. In order to enlighten it we can consider regularity along lines.

##### 4.2.1.3 Directional Hölder Regularity

Considering a centered Gaussian random field with stationary increments X , one can extract line processes by restricting values along some lines. For x 0 ∈ R d and θ ∈ S d - 1 , the line process is defined by Lx 0 ,θ(X) = (X(x 0 + tθ)) t ∈ R . It is now a one-dimensional centered Gaussian process with stationary increments and variogram given by vθ (t) = E ( (X(x 0 + tθ) - X(x 0 )) 2 ) = vX(tθ).

Definition 4.19 ([16]) Let θ ∈ S d - 1 . We say that X admits γ(θ) ∈ ( 0 , 1 ) as directional regularity in the direction θ if, for all ε &gt; 0, there exist c 1 , c 2 &gt; 0, such that

$$c _ { 1 } | t | ^ { 2 \gamma ( \theta ) + \varepsilon } \leq v _ { \theta } ( t ) = v _ { X } ( t \theta ) \leq c _ { 2 } | t | ^ { 2 \gamma ( \theta ) - \varepsilon } , \ \forall t \in [ - 1 , 1 ] .$$

It follows that the process Lx 0 ,θ(X) admits γ(θ) as critical Hölder exponent. Actually, by stationarity of increments, the directional regularity-if exists- may not have more than d values as stated in the following proposition.


<!-- p:163 -->


Proposition 4.10 ([16]) If there exists γ : S d - 1 → ( 0 , 1 ) such that for all θ ∈ S d - 1 , X admits γ(θ) as directional regularity in the direction θ , then γ takes at most d values. Moreover, if γ takes k values γk &lt; . . . &lt; γ 1 , there exists an increasing sequence of vectorial subset { 0 } = V 0 ⊊ V 1 ⊊ . . . ⊊ Vk := R d such that

$$\gamma ( \theta ) = \gamma _ { i } \Leftrightarrow \theta \in ( V _ { i } \smallsetminus V _ { i - 1 } ) \cap S ^ { d - 1 } .$$

In our previous examples we get the following results.

- For fractional Brownian fields with variogram vH (x) = ‖ x ‖ 2 H and 2dimensional elementary anisotropic fractional Brownian fields with variogram vH (x) = cH,α(x/ ‖ x ‖ ) ‖ x ‖ 2 H : for all θ ∈ S d - 1 , the directional Hölder regularity in direction θ is given by H and hence is constant.
- For operator scaling fields with variogram vH,E(x) = ( ∑ d i = 1 | x · θi | 2 αi ) H , for all 1 ≤ i ≤ d , the directional Hölder regularity in direction  ̃ θi is given by Hαi where  ̃ θi is an eigenvector of E associated with the eigenvalue α - 1 i ie E  ̃ θi = α - 1 i  ̃ θi . Moreover, assuming for instance that α 1 &gt; α 2 &gt; .. . &gt; αd , the strict subspaces defined by Vk = span (α 1 , . . . , α k ) for 1 ≤ k ≤ d illustrate the previous proposition by choosing γk = Hαk for 1 ≤ k ≤ d . For example, in Fig. 4.10, the greater directional regularity is given by Hα 2 = 0 . 4 only in vertical directions θ = ± e 2. For any other direction, the directional regularity is given by Hα 1 = 0 . 3. We refer to [44] for more precise results and to [24] for a general setting.

Hölder regularity properties are often linked with fractal properties as developed in the following section.

#### 4.2.2 Hausdorff Dimension of Graphs

We will see in this section how to compute Hausdorff dimension of some Gaussian random fields graphs. The fractal nature comes from the fact that the dimension will not be an integer as usual. We shall recall basic facts on Hausdorff measures and dimensions before.

##### 4.2.2.1 Hausdorff Measures and Dimensions

We follow [27] Chapter 2 for these definitions. Let U ⊂ R d be a bounded Borel set and ‖ · ‖ be a norm on R d . For δ &gt; 0, a finite or countable collection of subsets (Bi )i ∈ I of R d is called a δ -covering of U if diam (Bi ) ≤ δ for all i and U ⊂ ∪ i ∈ I Bi . Then, for s ≥ 0, we set

$$\mathcal { H } _ { \delta } ^ { s } ( U ) = \inf \left \{ \sum _ { i \in I } \text {diam} ( B _ { i } ) ^ { s } ; ( B _ { i } ) _ { i \in I } \ \delta - \text {covering of } U \right \} .$$


<!-- p:164 -->


4

Note that for all δ &lt; δ ′ , since a δ covering is also a δ ′ -covering we get H s δ (U) ≥ H s δ ′ (U) . The sequence ( H s δ (U))δ being monotonic we can give the following definition.

Definition 4.20 The s -dimensional Hausdorff measure of U is defined by

$$\mathcal { H } ^ { s } ( U ) = \lim _ { \delta \to 0 } \mathcal { H } _ { \delta } ^ { s } ( U ) \in [ 0 , + \infty ] .$$

Note that Hausdorff measures define measures on ( R d , B ( R d )) that generalize Lebesgue measures so that H 1 (U) gives the length of a curve U , H 2 (U) gives the area of a surface U , etc... Let us also remark that for s ′ &gt; s and (Bi)i ∈ I a δ -covering of U we easily see that for all δ &gt; 0

$$\sum _ { i \in I } \text {diam} ( B _ { i } ) ^ { s ^ { \prime } } \leq \delta ^ { s ^ { \prime } - s } \sum _ { i \in I } \text {diam} ( B _ { i } ) ^ { s } ,$$

so that H s ′ δ (U) ≤ δ s ′ - s H s δ (U) ≤ δ s ′ - s H s (U) . Hence, if H s (U) &lt; +∞ , we get H s ′ (U) = 0. Conversely, if H s ′ (U) &gt; 0, we obtain that H s (U) = +∞ . Actually, the function s ∈ [ 0 , +∞ ) ↦→ H s (U) jumps from +∞ to 0.

Definition 4.21 The Hausdorff dimension of U is defined as

$$\dim _ { H } ( U ) = \inf \left \{ s \geq 0 ; \mathcal { H } ^ { s } ( U ) = 0 \right \} = \sup \left \{ s \geq 0 ; \mathcal { H } ^ { s } ( U ) = + \infty \right \} .$$

For instance, when U = [ 0 , 1 ] d , choosing ‖ · ‖∞ , we can cover U by cubes δi +[ 0 , δ ] d of diameter δ , for i ∈ N d satisfying 0 ≤ ik ≤ δ - 1 - 1. Hence we need around δ - d such cubes to cover U so that H s δ (U) ≤ cδ - d × δ s . It follows that for s ≥ d , H s (U) &lt; +∞ and dim H(U) ≤ d . But if (Bi )i ∈ I is a δ covering of U with diam (Bi ) = ri we get 1 = L eb(U) ≤ ∑ i ∈ I r d i and therefore H d (U) &gt; 0 and dim H(U) ≥ d . In conclusion we obtain that dim H(U) = d . This can be generalized as in the following Proposition (see [27] for instance).

Let us emphasize that in general we do not know the value of H s ∗ (U) ∈ [ 0 , +∞] at s ∗ = dim H(U) . But we always have that H s (U) &gt; 0 implies dim H(U) ≥ s , while H s (U) &lt; +∞ implies that dim H(U) ≤ s , allowing to compute dim H(U) .

Proposition 4.11 If U is a non-empty open bounded set of R d then dim H(U) = d .

Following similar computations we can deduce an upper bound of Hausdorff dimension for graphs of Hölder functions.

##### 4.2.2.2 Upper Bound of Graphs Hausdorff Dimension

Let f : [ 0 , 1 ] d → R and denote its graph by

$$\mathcal { G } _ { f } = \{ ( x , f ( x ) ) ; x \in [ 0 , 1 ] ^ { d } \} \subset \mathbb { R } ^ { d + 1 } .$$


<!-- p:165 -->


Note that we clearly have dim H G f ≥ d . An upper bound may be set according to the Hölder regularity of the function.

Proposition 4.12 If there exist γ ∈ ( 0 , 1 ] and C &gt; 0 such that for all x, y ∈ [ 0 , 1 ] d one has | f(x) - f(y) | ≤ C ‖ x - y ‖ γ ∞ , then dim H G f ≤ d + 1 - γ .

Proof Write [ 0 , 1 ] d ⊂ Nδ ∪ i = 1 ( xi +[ 0 , δ ] d ) , where we can choose Nδ of the order of - d N d

δ and xi ∈ δ for 1 ≤ i ≤ Nδ as previously. Then

$$\mathcal { G } _ { f } & \subset \bigcup _ { i = 1 } ^ { N _ { \delta } } \left ( x _ { i } + [ 0 , \delta ] ^ { d } \right ) \times \left ( f ( x _ { i } ) + [ - C \delta ^ { \gamma } , C \delta ^ { \gamma } ] \right ) \\ & \subset \bigcup _ { i = 1 } ^ { N _ { \delta } } \bigcup _ { j = 1 } ^ { N _ { \delta } ^ { \gamma } } \left ( x _ { i } + [ 0 , \delta ] ^ { d } \right ) \times \left ( f ( x _ { i } ) + I _ { j } ( \delta ) \right ) , \\$$

choosing N γ δ intervals (Ij (δ))j of size δ to cover [- Cδ γ , Cδ γ ] , with N γ δ of the order of δ γ - 1 . Hence H s δ ( G f ) ≤ NδN γ δ δ s ≤ cδ - d + γ - 1 + s . Therefore choosing s &gt; d + 1 - γ implies that H s ( G f ) = 0 and dim H G f ≤ s . Since this holds for all s &lt; d + 1 - γ we obtain that dim H G f ≤ d + 1 - γ . ⊓ ⊔

Lower bounds for Hausdorff dimension are usually more difficult to obtain.

##### 4.2.2.3 Lower Bound of Graphs Hausdorff Dimension

One usual way to get lower bounds is to use Frostman criteria [27]. For second order random fields, this can be formulated as in the following theorem (see Lemma 2 of [3]).

Theorem 4.5 Let (Xx) x ∈ R d be a second order field a.s. continuous on [ 0 , 1 ] d such that there exists s ∈ (d, d + 1 ] ,

$$\int _ { [ 0 , 1 ] ^ { d } \times [ 0 , 1 ] ^ { d } } \mathbb { E } \left ( \left ( | X _ { x } - X _ { y } | ^ { 2 } + \| x - y \| ^ { 2 } \right ) ^ { - s / 2 } \right ) d x d y < + \infty ,$$

then a.s. dim H G X ≥ s .

For Gaussian random fields this can be used in the following way.

Corollary 4.3 Let (X(x)) x ∈ R d be a Gaussian random field. If there exists γ ∈ ( 0 , 1 ) such that for all ε &gt; 0 , there exist c 1 , c 2 &gt; 0 ,

$$c _ { 1 } \| x - y \| ^ { 2 \gamma + \varepsilon } \leq \mathbb { E } \left ( X ( x ) - X ( y ) \right ) ^ { 2 } \leq c _ { 2 } \| x - y \| ^ { 2 \gamma - \varepsilon } ,$$

then, for any continuous modification  ̃ X of X , one has

$$d i m _ { H } \mathcal { G } _ { \tilde { X } } = d + 1 - \gamma \ a . s .$$


<!-- p:166 -->


4

Proof The upper bound allows to construct a modification  ̃ X of X that is β - Hölder on [ 0 , 1 ] d for any β &lt; γ in view of Kolmogorov-Chentsov theorem so that dim H G  ̃ X ≤ d + 1 - γ a.s. according to the previous part. Following [3] and [4], since X is Gaussian, one can prove that for any s &gt; 1 and β &gt; γ , there exists c &gt; 0 such that

$$\mathbb { E } \left ( \left ( | X _ { x } - X _ { y } | ^ { 2 } + \| x - y \| ^ { 2 } \right ) ^ { - s / 2 } \right ) \leq c \| x - y \| ^ { 1 - \beta - s } ,$$

using the fact that E (X(x) - X(y)) 2 ≥ c 1 ‖ x - y ‖ 2 β by assumption. It follows that for 1 - β - s + d &gt; 0 the integral in Theorem 4.5 is finite. Hence a.s. dim H G  ̃ X ≥ s . Since this holds for all β &gt; γ and s &lt; d + 1 - β we get the desired lower bound and then the result. ⊓ ⊔

Note that in particular we obtain that the Hausdorff dimension of fractional Brownian fields graphs, respectively 2-dimensional elementary anisotropic fractional Brownian fields graphs, with Hurst parameter H ∈ ( 0 , 1 ) , is given by d + 1 - H / ∈ N , respectively 2 + 1 - H / ∈ N . For (E, H) -operator scaling random fields graphs, it is given by d + 1 - H min1 ≤ i ≤ d αi / ∈ N , where (α - 1 i ) 1 ≤ i ≤ d are the eigenvalues of E (see [9]).

### 4.3 Simulation and Estimation

This section focuses on some exact methods of simulation for some previously studied Gaussian random fields. We also give one way of estimation for fractal roughness and some applications in medical imaging.

#### 4.3.1 Simulation

In order to simulate a centered Gaussian random field X on [ 0 , 1 ] d for instance, the first step is to choose the mesh of discretization, let say 1 /n for some n ∈ N . Then one want to simulate the centered Gaussian random vector (Xk/n) k ∈[[ 0 ,n ]] d that is of size (n + 1 ) d . Choleski's method for diagonalizing the covariance matrix becomes quickly unpractical as n increases. Some helpful results concerning diagonalization of circulant matrices by discrete Fourier transforms may be sometimes used under an assumption of stationarity implying a Toeplitz structure of the covariance matrix. We refer to [26] for general framework and only illustrate these ideas to set fast and exact algorithms for some fractional or operator scaling 2-dimensional fields. The first step is to simulate one-dimensional fractional Brownian motion.


<!-- p:167 -->


##### 4.3.1.1 Fast and Exact Synthesis of Fractional Brownian Motion

Let H ∈ ( 0 , 1 ) and BH = (BH(t))t ∈ R be a fractional Brownian motion and recall that for n ∈ N we want to simulate (BH (k/n)) 0 ≤ k ≤ n . By self-similarity,

for k ≥ 1, since BH( 0 ) = 0 a.s. Hence, let us define the fractional Gaussian noise as Yj = BH(j + 1 ) - BH(j) , for j ∈ Z . Since BH has stationary increments, (Yj )j ∈ Z is a centered stationary Gaussian sequence with covariance given by

$$\text {recall that for } n \in \mathbb { N } \text { we want to simulate } ( B _ { H } ( k / n ) ) _ { 0 \leq k \leq n } . \text { by semi-similarity,} \\ ( B _ { H } ( k / n ) ) _ { 0 \leq k \leq n } \stackrel { d } { = } n ^ { - H } ( B _ { H } ( k ) ) _ { 0 \leq k \leq n } , \text { with } B _ { H } ( k ) = \sum _ { j = 0 } ^ { k - 1 } ( B _ { H } ( j + 1 ) - B _ { H } ( j ) ) \\ \text {for } k \geq 1 , \text { since } B _ { H } ( 0 ) = 0 \, a . s . \text { Hence, let us define the fractional Gaussian noise as}$$

$$c _ { k } = C o v ( Y _ { k + j } , Y _ { j } ) = \frac { 1 } { 2 } \left ( | k + 1 | ^ { 2 H } - 2 | k | ^ { 2 H } + | k - 1 | ^ { 2 H } \right ) , \forall k \in \mathbb { Z } .$$

It follows that the Gaussian vector Y = (Y 0 , . . . , Yn) has a Toeplitz covariance

matrix method [26] is to embed KY in the symmetric circulant matrix S = circ(s) of size 2 n with

matrix given by KY = ⎛ ⎜ ⎜ ⎜ ⎜ ⎝ c 0 c 1 . . . cn . . . . . . . . . c 1 c 0 ⎞ ⎟ ⎟ ⎟ ⎟ ⎠ . The idea of the circulant embedding

$$s = ( c _ { 0 } \, c _ { 1 } \dots \, c _ { n } \, c _ { n - 1 } \dots c _ { 1 } ) = ( s _ { 0 } \, s _ { 1 } \dots s _ { n } \, s _ { n + 1 } \dots s _ { 2 n - 1 } ) ,$$

and more precisely

$$S = \left ( \begin{array} { c c c c } s _ { 0 } & s _ { 2 n - 1 } & \cdots & s _ { 2 } & s _ { 1 } \\ s _ { 1 } & s _ { 0 } & s _ { 2 n - 1 } & s _ { 2 } & \\ \vdots & \vdots & s _ { 1 } & s _ { 0 } & \ddots & \vdots \\ s _ { 2 n - 2 } & \ddots & \ddots & s _ { 2 n - 1 } & \\ s _ { 2 n - 1 } & s _ { 2 n - 2 } & \cdots & s _ { 1 } & s _ { 0 } \end{array} \right ) = \left ( \begin{array} { c c c } K _ { Y } & S _ { 1 } \\ S _ { 1 } ^ { t } & S _ { 2 } \end{array} \right ) .$$

Then S = 1 2 n F ∗ 2 n diag (F 2 ns)F 2 n with F 2 n = ( e 2 iπ(j - 1 )(k - 1 ) 2 n ) 1 ≤ j,k ≤ 2 n the matrix of

discrete Fourier transform.

The symmetric matrix S may be used as a covariance matrix as soon as its eigenvalues are non-negative, which is equivalent to the fact that F 2 ns ≥ 0. This is in general difficult to establish and sometimes only checked numerically. However as far as fractional Gaussian noises are concerned we have a theoretical positive result established in [23, 51]. So we may consider a square root of S given by R 2 n = 1 √ 2 n F ∗ 2 n diag (F 2 ns) 1 / 2 ∈ M 2 n( C ) . Hence, choosing two independent centered Gaussian vectors ε ( 1 ) , ε ( 2 ) with covariance matrix I 2 n (hence iid marginals


<!-- p:168 -->


4

Fig. 4.11 Simulation of (BH (k/n)) 0 ≤ k ≤ n for n = 2 12 using circulant embedding matrix method

of standard Gaussian variables), we get using the fact that R 2 nR ∗ 2 n = S ,

$$R _ { 2 n } [ \varepsilon ^ { ( 1 ) } + i \varepsilon ^ { ( 2 ) } ] = Z ^ { ( 1 ) } + i Z ^ { ( 2 ) } ,$$

with Z ( 1 ) , Z ( 2 ) iid N ( 0 , S) . It follows that

$$Y \stackrel { d } { = } \left ( Z _ { k } ^ { ( 1 ) } \right ) _ { 0 \leq k \leq n } \stackrel { d } { = } \left ( Z _ { k } ^ { ( 2 ) } \right ) _ { 0 \leq k \leq n } \sim \mathcal { N } ( 0 , K _ { Y } ) .$$

Choosing n = 2 p we can use fast discrete Fourier transforms to get a cost of simulation O(n log (n)) to compare with O(n 3 ) for Choleski method. On Fig. 4.11, we can now illustrate previous results on the regularity and graphs Hausdorff dimension of fractional Brownian motions given respectively by H and 2 - H in dimension 1.

When considering 2-dimensional Gaussian fields, several extensions are possible. For instance, if (Yk 1 ,k 2 ) (k 1 ,k 2 ) ∈ Z 2 is stationary, its covariance function may be written as Cov (Yk 1 + l 1 ,k 2 + l 2 , Yl 1 ,l 2 ) = rk 1 ,k 2 . Hence we may use a block Toeplitz covariance matrix with Toeplitz blocks and embed in a block circulant matrix (see [21, 26]). When only stationary increments are assumed one can still try to simulate the increments but in dimension d &gt; 1 the initial conditions now correspond to values on axis and are correlated with increments [38].

We present two other possible generalizations for considered random fields based on more general ideas.

##### 4.3.1.2 Turning Band Method for 2-Dimensional Anisotropic Self-Similar Fields

The turning band method was introduced by Matheron in [48]. It is mainly based on similar ideas developed in Proposition 4.3 when considering isotropic fields constructed from processes. Actually, when Y is a centered second order stationary process with covariance KY(t, s) = cY (t - s) one can define the field

$$Z ( x ) = Y ( x \cdot U ) \text { for } x \in \mathbb { R } ^ { 2 } ,$$


<!-- p:169 -->


by choosing U ∼ U (S 1 ) independent from Y . It follows that Z is a centered stationary isotropic field such that identifying θ ∈ [- π, π ] with u(θ) = ( cos (θ), sin (θ)) ∈ S 1 ,

$$c _ { Z } ( x ) = C o v ( Z ( x + y ) , Z ( y ) ) = \frac { 1 } { \pi } \int _ { - \pi / 2 } ^ { \pi / 2 } c _ { Y } ( x \cdot u ( \theta ) ) d \theta . \\$$

Let us note that even if Y is Gaussian Z is not a Gaussian field. Assuming that we are able to simulate Y one can define for K ≥ 1, θ 1 , . . . , θK ∈ [- π/ 2 , π/ 2 ] and λ 1 , . . . , λK ∈ R + , an approximated field

$$Z _ { K } ( x ) = \sum _ { i = 1 } ^ { K } \sqrt { \lambda _ { i } } Y ^ { ( i ) } ( x \cdot u ( \theta _ { i } ) ) , \\$$

with Y ( 1 ) , . . . , Y (K) independent realizations of Y . The field ZK is a centered stationary field with covariance

$$c _ { Z _ { K } } ( x ) & = \sum _ { i = 1 } ^ { K } \lambda _ { i } c _ { Y } ( x \cdot u ( \theta _ { i } ) ) , \\ \vdots & \quad \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \vdots \$$

such that choosing convenient weights it can be an approximation of the covariance cZ . For Gaussian random field, Matheron proposes to use the central limit theorem and considers 1 √ N (Z ( 1 ) K + . . . + Z (N) K ) , with Z ( 1 ) K , . . . , Z (N) K independent realizations of ZK . In [14] we have exploited these ideas to propose simulations of anisotropic self-similar fields. Let H ∈ ( 0 , 1 ) , μ be a finite non-negative measure on S 1 , and XH,μ = (XH,μ(x)) x ∈ R 2 be a centered Gaussian random field with stationary increments and variogram given by

$$v _ { H , \mu } ( x ) = \int _ { S ^ { 1 } } | x \cdot \theta | ^ { 2 H } \mu ( d \theta ) = C _ { H , \mu } \left ( \frac { x } { \| x \| } \right ) \| x \| ^ { 2 H } .$$

We recall that XH,μ is self-similar of order H . Note also that choosing μ the uniform measure on S 1 , the corresponding field XH,μ is isotropic and therefore it is a fractional Brownian field. When μK is a discrete measure ie μK = ∑ K i = 1 λi δθi for some θ 1 , . . . , θK ∈ S 1 and λ 1 , . . . , λK ∈ R + , we get

$$v _ { H , \mu _ { K } } ( x ) = \sum _ { i = 1 } ^ { K } \lambda _ { i } | x \cdot \theta _ { i } | ^ { 2 H } = \sum _ { i = 1 } ^ { K } \lambda _ { i } \text {Var} ( B _ { H } ( x \cdot \theta _ { i } ) ) . \\$$

Hence, considering, (B (i) H ) 1 ≤ i ≤ K independent realizations of the one dimensional H -fractional Brownian motion,

$$X _ { H , \mu _ { K } } ( x ) \colon = \sum _ { i = 1 } ^ { K } \sqrt { \lambda _ { i } } B _ { H } ^ { ( i ) } ( x \cdot \theta _ { i } ) , \, x \in \mathbb { R } ^ { 2 } ,$$


<!-- p:170 -->


4

is a centered Gaussian random field with stationary increments and variogram vH,μK .

Hence the simulation of these random fields depends on the simulation of BH on some specific points. We can exploit further on this fact using specific choices of lines and weights. Actually, to simulate ( XH,μK ( k 1 n , k 2 n )) 0 ≤ k 1 ,k 2 ≤ n one has to simulate for 1 ≤ i ≤ K ,

$$B _ { H } ^ { ( i ) } \left ( \frac { k _ { 1 } } { n } \cos ( \theta _ { i } ) + \frac { k _ { 2 } } { n } \sin ( \theta _ { i } ) \right ) \text { for } 0 \leq k _ { 1 } , k _ { 2 } \leq n .$$

When cos (θi ) ̸= 0, by choosing θi with tan (θi ) = pi qi for pi ∈ Z and qi ∈ N , using self-similarity we get

$$\left ( B _ { H } ^ { ( i ) } \left ( \frac { k _ { 1 } } { n } \cos ( \theta _ { i } ) + \frac { k _ { 2 } } { n } \sin ( \theta _ { i } ) \right ) \right ) _ { k _ { 1 } , k _ { 2 } } \stackrel { f a d } { = } \left ( \frac { \cos ( \theta _ { i } ) } { n q _ { i } } \right ) ^ { H } \left ( B _ { H } ^ { ( i ) } \left ( k _ { 1 } q _ { i } + k _ { 2 } p _ { i } \right ) \right ) _ { k _ { 1 } , k _ { 2 } } .$$

Using the previous algorithm we are able to simulate this with a cost given by O(n( | pi |+ qi ) log (n( | pi |+ qi ))) . For μ(dθ) = c(θ)dθ , in particular for elementary anisotropic fractional fields (see Fig. 4.7), Riemann approximation for convenient μK yields to error bounds between the distribution of XH,μK and the distribution of XH,μ so that XH,μK may be used as an approximation to simulate XH,μ . Note that contrarily to the original Turning band method, the simulated fields are all Gaussian, with stationary increments, and self-similar of order H . We refer to Fig. 4.12 where we can see the effect of the number of chosen lines on induced realizations as well as on corresponding variograms.

Fig. 4.12 Top: realizations of XH,μK with H = 0 . 2 to approximate the isotropic field XH,μ for μ(dθ) = dθ and n = 512; Bottom: corresponding variograms vH,μK (see [14])

<!-- p:171 -->


Actually, a fast and exact method of simulation has been set up in [57] for isotropic fractional Brownian fields XH,μ . This is based on a local stationary approximation of this field by considering a stationary field with compactly supported covariance function for which the 2-dimensional circulant embedding matrix algorithm is running. These ideas have also been exploited in [29] and may be partially used for more general operator scaling random field [7]. We briefly present this in the following section.

##### 4.3.1.3 Stein Method for 2-Dimensional Operator Scaling fields

For the sake of simplicity we consider here the diagonal case and set E = diag(α - 1 1 , α - 1 2 ) for some α 1 , α 2 ∈ ( 0 , 1 ] and τ E (x) 2 := | x 1 | 2 α 1 + | x 2 | 2 α 2 . Recall that, by Proposition 4.8, for H ∈ ( 0 , 1 ] we can define XH,E = (XH,E(x)) x ∈ R 2 a centered Gaussian random field with stationary increments and variogram given by

$$v _ { H , E } ( x ) = \tau _ { E } ( x ) ^ { 2 H } = \left ( | x _ { 1 } | ^ { 2 \alpha _ { 1 } } + | x _ { 2 } | ^ { 2 \alpha _ { 2 } } \right ) ^ { H } ,$$

so that XH,E is (E, H) -operator scaling. Let us also note that for α 1 = α 2 = α ∈ ( 0 , 1 ] , the field XH,E is αH -self-similar but it is isotropic only when the common value α is equal to 1. In this case XH,E corresponds to a fractional Brownian field of order αH = H . In [7], we extend the procedure developed in [57] for fast and exact synthesis of these last fields. Let us define for cH = 1 - H , the real compactly supported function

$$K _ { H , E } ( x ) = \begin{cases} c _ { H } - \tau _ { E } ( x ) ^ { 2 H } + ( 1 - c _ { H } ) \tau _ { E } ( x ) ^ { 2 } & \text {if } \tau _ { E } ( x ) \leq 1 \\ 0 & \text {else} \end{cases} \quad \text {for } x \in \mathbb { R } ^ { 2 } .$$

Assuming that KH,E is a covariance function on R 2 we can define YH,E a stationary centered Gaussian random field with covariance KH,E . Then, computing covariance functions we get that

$$\left \{ X _ { H , E } ( x ) ; x \in [ 0 , M ] ^ { 2 } \right \} \\ \\ H , E ( 0 ) + \sqrt { 1 - c _ { H } B _ { \alpha _ { 1 } } ^ { ( 1 ) } ( x _ { 1 } ) + \sqrt { 1 - c _ { H } } B _ { \alpha _ { 2 } } ^ { ( 2 ) } ( x _ { 2 } ) ; x \in [ 0 , M ] ^ { 2 } } \right \} ,$$

$$\stackrel { f d d } { = } \left \{ Y _ { H , E } ( x ) - Y _ { H , E } ( 0 ) + \sqrt { 1 - c _ { H } } B _ { \alpha _ { 1 } } ^ { ( 1 ) } ( x _ { 1 } ) + \sqrt { 1 - c _ { H } } B _ { \alpha _ { 2 } } ^ { ( 2 ) } ( x _ { 2 } ) ; \, x \in [ 0 , M ] ^ { 2 } \right \} ,$$

for M = max { 0 ≤ r ≤ 1 ; r 2 α 1 + r 2 α 2 ≤ 1 } and B ( 1 ) α 1 , B ( 2 ) α 2 two standard independent 1-dimensional fractional Brownian motions, independent from YH,E . Since we are already able to simulate ( B (i) αi (k/n) ) 0 ≤ k ≤ n in view of Sect. 4.3.1.1, it is enough to simulate (YH,E(k 1 /n, k 2 /n)) 0 ≤ k 1 ,k 2 ≤ n in order to simulate (XH,E(k 1 /n, k 2 /n)) 0 ≤ k 1 ,k 2 ≤ Mn But if KH,E is a covariance function, since it


<!-- p:172 -->


4

has compact support in [- 1 , 1 ] 2 , its periodization

$$K _ { H , E } ^ { p e r } ( x ) = \sum _ { k _ { 1 } , k _ { 2 } \in \mathbb { Z } ^ { 2 } } K _ { H , E } ( x _ { 1 } + 2 k _ { 1 } , x _ { 2 } + 2 k _ { 2 } ) ,$$

will also be a periodic covariance function on R 2 . Denoting by Y per H,E a stationary periodic centered Gaussian random field with covariance function K per H,E and remarking that KH,E(x) = KH,E( | x 1 | , | x 2 | ) , the random vector ( Y per H,E ( k 1 n , k 2 n )) 0 ≤ k 1 ,k 2 ≤ 2 n has a block circulant covariance matrix diagonalized by 2D discrete Fourier transform. Following [26], a fast and exact synthesis of ( YH,E ( k 1 n , k 2 n )) 0 ≤ k 1 ,k 2 ≤ n d = ( Y per H,E ( k 1 n , k 2 n )) 0 ≤ k 1 ,k 2 ≤ n is possible with a cost of the order O(n 2 log (n)) . Note that according to Theorem 4.2, by the Fourier inverse theorem, the function KH,E is a covariance matrix if and only if its Fourier transform, defined for ξ ∈ R 2 by ˆ KH,E(ξ) = ∫ R 2 e - ix · ξ KH,E(x)dx , is nonnegative. This was proven in [57] in the isotropic case for α 1 = α 2 = α = 1 and H ∈ ( 0 , 3 / 4 ) . Note also that in this case we simply have (B (i) αi (xi )) d = (xi N (i) ) with N (i) ∼ N ( 0 , 1 ) for i = 1 , 2. As long as we only want to synthesize the vector (XH,E(k 1 /n, k 2 /n)) 0 ≤ k 1 ,k 2 ≤ Mn it is actually sufficient to check numerically the non-negativeness of eigenvalues for the covariance matrix of ( Y per H,E ( k 1 n , k 2 n )) 0 ≤ k 1 ,k 2 ≤ 2 n . We refer to Figs. 4.13 and 4.14 for some realizations.

#### 4.3.2 Estimation

We describe here one way of estimation for Hölder directional regularity from a discretized sample paths observation. Our procedure is based on the variogram method for estimation of Hurst parameter of one-dimensional fractional Brownian motions.

##### 4.3.2.1 1D Estimation Based on Variograms

We first assume to observe (BH(k)) 0 ≤ k ≤ n for some large n , where BH = (BH (t))t ∈ R is a fractional Brownian motion with Hurst parameter H ∈ ( 0 , 1 ) . We exploit the stationarity of increments by considering the increments of BH with step u ∈ N

$$\Delta _ { u } B _ { H } ( k ) = B _ { H } ( k + u ) - B _ { H } ( k )$$


<!-- p:173 -->


Fig. 4.13 Top: realizations of anisotropic self-similar fields XH,E with E = α - 1 I 2 and Hα = 0 . 2 for n = 2 10 ; Bottom: corresponding variograms vH,E (see [7])

Fig. 4.14 Top: realizations of operator scaling fields XH,E with E = diag (α - 1 1 , α - 1 2 ) and Hα 1 = 0 . 2, Hα 2 = 0 . 3 for n = 2 10 ; Bottom: corresponding variograms vH,E (see [7])

<!-- p:174 -->


4

Note that the sequence (ΔuBH(k))k ∈ Z is a stationary Gaussian centered sequence, with common variance given by vH (u) = cH | u | 2 H . Hence, considering the statistics

$$V _ { n } ( u ) = \frac { 1 } { n - u } \sum _ { k = 0 } ^ { n - 1 - u } \Delta _ { u } B _ { H } ( k ) ^ { 2 } ,$$

we immediately see that E (Vn(u)) = vH (u) . Actually, since ΔuBH is Gaussian and Cov (ΔuBH(k),ΔuBH( 0 )) -→ k →+∞ 0, this sequence is ergodic (see [45]) so that Vn(u) is a strongly consistent estimator of vH (u) meaning that Vn(u) -→ n →+∞ vH (u) a.s. This naturally leads us to consider for two different steps u ̸= v , the statistic

$$\widehat { H } _ { n } = \frac { 1 } { 2 } \log \left ( \frac { V _ { n } ( u ) } { V _ { n } ( v ) } \right ) / \log \left ( \frac { u } { v } \right ) . \\ \\ F _ { \ } U _ { n } + ( \varrho _ { 1 } ) _ { 1 } + ( \widehat { H } _ { 1 } ) _ { 1 } \cdot \widehat { H } _ { 1 } + ( \varrho _ { 2 } ) _ { 2 } + ( \widehat { H } _ { 2 } ) _ { 2 } + ( \varrho _ { 3 } ) _ { 3 } + ( \varrho _ { 4 } ) _ { 4 } + ( \varrho _ { 5 } ) _ { 5 } + ( \varrho _ { 6 } ) _ { 6 } \right )$$

Theorem 4.6 For H ∈ ( 0 , 1 ) , the statistic ̂ Hn is a strongly consistent estimator of H . Moreover for H ∈ ( 0 , 3 / 4 ) it is also asymptotically normal.

Proof The consistency is immediate once remarked that H = 1 2 log ( vH (u) vH (v) ) / log ( u v ) . To prove asymptotic normality, the first step is a central limit theorem for

$$\frac { V _ { n } ( u ) } { v _ { H } ( u ) } = \frac { 1 } { n - u } \sum _ { k = 0 } ^ { n - 1 - u } X _ { u } ( k ) ^ { 2 } \text { with } X _ { u } ( k ) = \frac { \Delta _ { u } B _ { H } ( k ) } { \sqrt { v _ { H } ( u ) } } ,$$

so that (Xu(k))k is a centered stationary Gaussian sequence with unit variance. Then, denoting H 2 (x) = x 2 - 1 the Hermite polynomial of order 2 we consider

$$Q _ { n } ( u ) \colon = \sqrt { n - u } \left ( \frac { V _ { n } ( u ) } { v _ { H } ( u ) } - 1 \right ) = \frac { 1 } { \sqrt { n - u } } \sum _ { k = 0 } ^ { n - 1 - u } H _ { 2 } \left ( X _ { u } ( k ) \right ) . \\$$

We will use a general result of Breuer Major [17] giving a summability condition on the covariance sequence to get asymptotic normality.

Proposition 4.13 ([17]) If (ρu(k))k = ( Cov (Xu(k), Xu( 0 )))k satisfies

$$\sigma _ { u } ^ { 2 } = \sum _ { k \in \mathbb { Z } } \rho _ { u } ( k ) ^ { 2 } < + \infty , \ t h e n$$

$$i i ) \ \frac { Q _ { n } ( u ) } { \sqrt { V a r ( Q _ { n } ( u ) ) } } \stackrel { d } { \rightarrow } N , w i t h \, N \sim \mathcal { N } ( 0 , 1 ) .$$

i) Var (Qn(u)) → 2 σ 2 u ;


<!-- p:175 -->


But since Xu(k) = ΔuBH (k) √ vH (u) we obtain that

$$\rho _ { u } ( k ) = \frac { 1 } { 2 } \left ( | k + u | ^ { 2 H } - 2 | k | ^ { 2 H } + | k - u | ^ { 2 H } \right ) = O _ { | k | \to + \infty } ( | k | ^ { - 2 ( 1 - H ) } ) .$$

Hence, we check that ∑ k ∈ Z ρu(k) 2 &lt; +∞ for H &lt; 3 / 4, and by Slutsky's theorem Qn(u) d → N ( 0 , σ 2 u ). By Delta-method (see [58] for instance), asymptotic normality of ̂ Hn will follow from asymptotic normality of the couple (Qn(u), Qn(v)) . Note that we already have checked it for each marginal. However since Qn(u) and Qn(v) are in the same Wiener chaos of order two we can use a very strong result of [50] saying that if Cov (Qn(u), Qn(v)) → σuv , asymptotic normality of marginals imply asymptotic normality of the couple namely

that concludes the proof.

⊓

⊔

In order to get rid of the upper bound H &lt; 3 / 4 for asymptotic normality, Istas and Lang [36] have proposed to consider generalized quadratic variations. In particular we can replace ΔuBH(k) by second order increments

$$\Delta _ { u } ^ { ( 2 ) } B _ { H } ( k ) = B _ { H } ( k + 2 u ) - 2 B _ { H } ( k + u ) + B _ { H } ( k )$$

so that we keep a centered Gaussian stationary sequence with a similar variance given by v ( 2 ) H (u) = Var (Δ ( 2 ) u BH(k)) = c ( 2 ) H | u | 2 H but now the covariance sequence is Ok →+∞ ( | k | - 2 ( 2 - H) ) ensuring asymptotic normality for Q ( 2 ) n (u) , obtained by replacing Xu by X ( 2 ) u = Δ ( 2 ) u BH √ v ( 2 ) H (u) in (4.7) and, as a consequence for ̂ H ( 2 ) n for all

H ∈ ( 0 , 1 ) . This way of estimation is particularly robust and consistency as well as asymptotic normality still hold for infill or high frequency estimation where we now assume to observe (BH (k/n)) 0 ≤ k ≤ n instead of (BH (k)) 0 ≤ k ≤ n . In this framework we have to replace Δ ( 2 ) u BH(k) by

$$\Delta _ { u / n } ^ { ( 2 ) } B _ { H } ( k / n ) = B _ { H } \left ( \frac { k + 2 u } { n } \right ) - 2 B _ { H } \left ( \frac { k + u } { n } \right ) + B _ { H } \left ( \frac { k } { n } \right ) .$$

Let us note that by self-similarity (Δ ( 2 ) u/n BH(k/n))k d = (n - H Δ ( 2 ) u BH(k))n but we can also replace the self-similar process BH by Y a centered Gaussian process with stationary increments such that

$$v _ { Y } ( u ) = \mathbb { E } \left ( ( Y ( t + u ) - Y ( t ) ) ^ { 2 } \right ) = c _ { Y } | u | ^ { 2 H } + O _ { | u | \to 0 } \left ( | u | ^ { 2 H + \varepsilon } \right ) .$$


<!-- p:176 -->


4

Fig. 4.15 A realization of a 2-dimensional random field and two line processes. In green for the horizontal direction θ = ( 1 , 0 ) . In red for the vertical one θ = ( 0 , 1 )

Asymptotic normality still hold assuming that ε &gt; 1 / 2 but now, under our assumption, we get an estimator of Hölder regularity of Y , given by H in view of Proposition 4.9. We refer to [12] for more details and to [6] for complements.

##### 4.3.2.2 Application to Random Fields by Line Processes

This framework may be used when considering random fields (X(x)) x ∈ R d instead of one-dimensional processes. Actually, for x 0 ∈ R d and θ ∈ S d - 1 we can consider the line process Lx 0 ,θ(X) = { X(x 0 + tθ) ; t ∈ R } already defined in Sect. 4.2.1.3 (Fig. 4.15).

Recall that when X is a centered stationary Gaussian random field with stationary increments and variogram vX , the process Lx 0 ,θ(X) is centered Gaussian with stationary increments and variogram

$$v _ { \theta } ( t ) = \mathbb { E } \left ( ( X ( x _ { 0 } + t \theta ) - X ( x _ { 0 } ) ) ^ { 2 } \right ) = v _ { X } ( t \theta ) , \, t \in \mathbb { R } .$$

When moreover X is self-similar of order H ∈ ( 0 , 1 ) , we clearly get that vθ (t) = vX(θ) | t | 2 H , ensuring that Lx 0 ,θ(X) - Lx 0 ,θ (X)( 0 ) is also self-similar of order H ∈ ( 0 , 1 ) and therefore it is a (non-standard) fractional Brownian motion with Hurst parameter H . Hence estimators set up in previous section may be used to estimate H . Note also that when X is isotropic we must have θ ∈ S d - 1 ↦→ vX(θ) a constant function. Finally, let us remark that considering (E, H) -operator scaling fields with α 1 , . . . , αd ∈ ( 0 , 1 ] , H ∈ ( 0 , 1 ) and E the diagonal matrix diag (α - 1 1 , . . . , α - 1 d ) , for any 1 ≤ i ≤ d , the line process Lx 0 ,ei (X) - Lx 0 ,ei (X)( 0 ) is a fractional Brownian motion with Hurst parameter Hαi , where (ei ) 1 ≤ i ≤ d is the canonical basis of R d . This follows from the fact that vei (t) = v H,E (tei ) = | t | αi H since v H,E (x) = ( | x 1 | α 1 + . . . +| xd | αd ) 2 H . Hence we are able to estimate α 1 H,...,αdH (see [7] for numerical results).


<!-- p:177 -->


We can illustrate this with some applications in medical imaging.

#### 4.3.3 Application in Medical Imaging Analysis

There are numerous methods and studies around what is called fractal analysis in medical imaging. We refer to [46] for a good review. The main goal is to characterized self-similarity of images with a fractal index H ∈ ( 0 , 1 ) to extract some helpful information for diagnosis. Our point of view consists in considering an image (I (k 1 , k 2 )) 1 ≤ k 1 , k 2 ≤ n as a realization of a random field. Then,

- Extract a line from the image (Lθ (k)) 1 ≤ k ≤ nθ for θ a direction.
- = · Average along several lines of the same direction vθ (u) and compute ̂ Hθ(u,v) = 1 2 log ( vθ (u) vθ (v) ) / log ( u v ) .

$$& \quad \cdot \quad \text {Extract a line from the image } ( L _ { \theta } ( k ) ) _ { 1 \leq k \leq n _ { \theta } } \text { for } \theta \text { a direction.} \\ & \quad \cdot \quad \text {Compute } v _ { \theta } ( u ) = \frac { 1 } { n _ { \theta } - u } \sum _ { k = 1 } ^ { n _ { \theta } - u } \left ( L _ { \theta } ( k + u ) - L _ { \theta } ( k ) \right ) ^ { 2 } . \\ & \quad \cdot \quad \text {Average along several lines of the same direction } \overline { v _ { \theta } } ( u ) \text { and compute}$$

Of course there are several implementation issues according to the chosen direction. It follows that considering estimation on oriented lines without interpolation does not allow to reach any direction. Moreover precision is not the same in all directions (Fig.4.16). However the procedure is successful when considering horizontal and vertical direction and may also be compared with diagonal directions. We present in the following some results obtained with two kind of medical images: bone radiographs and mammograms.

Fig. 4.16 Available directions on a square lattice

Black = out of lattice. Precision of red = 1, green = √ 2


<!-- p:178 -->


##### 4.3.3.1 Osteoporosis and Bone Radiographs

According to experts from the World Health Organization, osteoporosis is a disease affecting many millions of people around the world. It is characterized by low bone mass and micro-architectural deterioration of bone tissue, leading to bone fragility and a consequent increase in risk of fracture. Bone mineral density allows to measure low bone mass and is used for diagnosis while micro-architectural deterioration is not quantify. Several medical research teams have been working on micro-architectural deterioration assessment from bone radiographs, an easiest and cheapest clinical exam. Several authors have proposed to use fractal analysis with different methods of analysis for instance for calcaneous bone in [31], and cancellous bone in [20]. In [5], it allows to discriminate between osteoporotic cases Hmean = 0 . 679 ± 0 . 053 and control cases Hmean = 0 . 696 ± 0 . 030, by coupling with bone mineral density.

In [10], we have considered a data set composed of 211 numeric radiographs high-resolution of calcaneum (bone heel) with standardized acquisition of region of interest (ROI) 400 × 400 of Inserm unit U658 [43] (see Fig. 4.17). Figure 4.18 gives the results we obtained for horizontal and vertical directions. Log-log plots are linear for small scales in adequation with a self-similarity property valid for small scales. Estimated values are greater in the vertical direction than in the horizontal

ROI

control case

osteoporotic case

Fig. 4.17 Standardized acquisition of region of interest (ROI) of Inserm unit U658 [43]

1 =( 1 , 0 ) , H 1 = 0 . 51 ± 0 . 08

±

Fig. 4.18 Mean of log-log plot of mean quadratic variations in horizontal and vertical direction. The last plot indicates estimated values of couple (Hθ 1 , Hθ 2 ) for each 211 images (see [10])


<!-- p:179 -->


dense breast tissue

Fig. 4.19 Region of interest extracted from real mammograms

fatty breast tissue

direction contradicting an isotropic or self-similar model. Similar results were recently obtained using different kinds of estimators in [32]. Moreover, comparisons with diagonal direction lead us to think that operator scaling random fields could be used for modeling.

##### 4.3.3.2 Mammograms and Density Analysis

Fractal analysis has also been used in mammograms analysis. In particular, it was used for the characterization and classification of mammogram density [19]. Actually, breast tissues are mainly composed of two kinds of tissues called dense and fatty (see Fig. 4.19) and the amount of dense tissues is believed to be a risk factor for developing breast cancer [19, 33].

In [33], the hypothesis of a self-similar behavior is validated using a power spectrum method with an estimated fractal index range H ∈ [ 0 . 33 , 0 . 42 ] . Based on the variogram method presented above we also found a local self-similar behavior with similar values H = 0 . 31 ± 0 . 05 on a data set of 58 cases with 2 mammograms (left and right) ROI of size 512 × 512 in [8]. Note that, contrarily to bones data, we do not have a standardized procedure to extract ROI. Very interesting results were obtained in [40] who manages to discriminate between dense and fatty breast tissues using the Wavelet Transform Modulus Maxima method with respective fractal indices given by H ∈ [ 0 . 55 , 0 . 75 ] and H ∈ [ 0 . 2 , 0 . 35 ] . Fractal analysis is also linked with lesion detectability in mammogram textures. Actually, as observed in [18], it may be more difficult to detect lesion in dense tissues than in fatty tissues. This was mathematically proven in [30], using a-contrario model, for textures like isotropic fractional Brownian fields, showing that size and contrast of lesions are linearly linked in log-log plot with a slope depending on the H index. This is illustrated in Fig. 4.20, where we have added a spot with an increasing radius on two simulations of fractional Brownian fields of size 512 × 512 for H = 0 . 3, corresponding to values of fatty tissues, and for H = 0 . 7, corresponding to values of dense tissues. Contrarily to white noise images, obtained with independent identically distributed Gaussian variables on each pixel, in fractal images the more the radius increases, the less the spot is observable.


<!-- p:180 -->


Fig. 4.20 Examples of simulated spots with various sizes (radius 5, 10, and 50) but similar contrast in a white noise texture (top row) and in fractional Brownian fields H = 0 . 3 and H = 0 . 7 (bottom row)

### 4.4 Geometric Construction

We present here geometric construction for some fractional Brownian fields based on Chentsov's representation of random fields using a random measure and a particular class of Borel sets indexed by points of R d . This is particularly interesting as it yields possible extensions, in particular beyond the Gaussian framework.

#### 4.4.1 Random Measures

A random measure will be defined as a stochastic process indexed by some Borel set. We still consider (Ω, A , P ) a probability space. Let k ≥ 1 and μ be a σ -finite non-negative measure on ( R k , B ( R k )) . Let set

$$\mathcal { E } _ { \mu } = \{ A \in \mathcal { B } ( \mathbb { R } ^ { k } ) \text { such that } \mu ( A ) < + \infty \} ,$$


<!-- p:181 -->


Definition 4.22 A random measure M is a stochastic process M = { M(A) ; A ∈ E μ } satisfying

- For A 1 , . . . , An ∈ E μ disjoint sets the random variables M(A 1 ), . . . , M(An) are independent;
- For all A ∈ E μ , M(A) is a real random variable on (Ω, A ) ;
- For (An)n ∈ N disjoint sets such that ∪ n ∈ N An ∈ E μ ,

$$M ( \cup _ { n \in \mathbb { N } } A _ { n } ) = \sum _ { n \in \mathbb { N } } M ( A _ { n } ) \ a . s .$$

Let us emphasize that this definition does not ensure that almost surely M is a measure. However some random measures may be almost surely measures.

Definition 4.23 A Poisson random measure N with intensity μ is a random measure such that for any A ∈ E μ , the random variable N(A) follows a Poisson distribution of intensity μ(A) ie N(A) ∼ P (μ(A)) .

In this case N is a random discrete measure given by N = ∑ i ∈ I δTi , where Φ = (Ti )i ∈ I is a countable family of random variables with values in R k called Poisson point process on R k with intensity μ (see [37] for instance). For example, when k = 1 and μ = λ × Lebesgue for some λ &gt; 0, (N( [ 0 , t ] )) t ≥ 0 is the classical Poisson process of intensity λ and Φ corresponds to the jumps of the Poisson process.

Definition 4.24 A Gaussian random measure W with intensity μ is a random measure such that for any A ∈ E μ , the random variable W(A) follows a normal distribution with mean 0 and variance μ(A) , ie W(A) ∼ N ( 0 , μ(A)).

In this case, W is not an a.s. measure. It is a centered Gaussian stochastic process (sometimes called set-indexed process, see [34] for instance) with covariance given by

$$C o v \left ( W ( A ) , W ( B ) \right ) = \mu ( A \cap B ) = \frac { 1 } { 2 } \left ( \mu ( A ) + \mu ( B ) - \mu ( A \Delta B ) \right ) ,$$

for all A,B ∈ E μ , with AΔB = (A ∩ B c ) ⋃ (B ∩ A c ) . Let us note that this is also the covariance function of any second order random measure M satisfying Var (M(A)) = μ(A) and so for N a Poisson random measure of intensity μ . For example, when k = 1 and μ = λ × Lebesgue for some λ &gt; 0, (W( [ 0 , t ] )) t ≥ 0 is the classical (non-standard) Brownian motion with diffusion λ , up to continuity of sample paths. Conversely, considering a Brownian motion (Bt )t ∈ R one can define a Gaussian random measure on R given by W(A) = ∫ +∞ -∞ 1 A(t)dBt .

measure with intensity n × μ . By the central limit theorem we immediately deduce

The link between Poisson and Gaussian measures is given by the central limit theorem. Actually, if N ( 1 ) , . . . , N (n) are independent Poisson random measures with the same intensity μ , by superposition principle n ∑ i = 1 N (i) is a Poisson random


<!-- p:182 -->


4

that for A ∈ E μ

$$\frac { 1 } { \sqrt { n } } \left ( \sum _ { i = 1 } ^ { n } N ^ { ( i ) } ( A ) - n \mu ( A ) \right ) _ { n \rightarrow + \infty } \frac { d } { W ( A ) } \, W ( A ) .$$

More generally we have the following normal approximation for Poisson measures in high intensity.

Proposition 4.14 If Nλ is a Poisson random measure with intensity λ × μ and W is a Gaussian random measure with the same intensity μ , then

$$\left ( \lambda ^ { - 1 / 2 } \left ( N _ { \dot { \lambda } } ( A ) - \lambda \mu ( A ) \right ) \right ) _ { A \in \mathcal { E } _ { \mu } } \stackrel { f d d } { \longrightarrow } \left ( W ( A ) \right ) _ { A \in \mathcal { E } _ { \mu } } .$$

#### 4.4.2 Chentsov's Representation: Lévy and Takenaka Constructions

Chentsov's type representation (see [56]) consists in constructing a random field X with M a random measure with intensity μ on R k and V = { Vx ; x ∈ R d } a class of sets of E μ indexed by R d for d ≥ 1, by setting

$$X _ { x } = M ( V _ { x } ) , \ x \in \mathbb { R } ^ { d } .$$

Then X is called Chentsov random field associated with M and V . If M is a second order random measure satisfying Var (M(A)) = μ(A) then X is a second order random field with

$$\forall x , y \in \mathbb { R } ^ { d } , \ V a r ( X _ { x } - X _ { y } ) = \mu ( V _ { x } \Delta V _ { y } ) .$$

Then invariance properties of X imply several relations on μ and V . If X has stationary increments then we must have μ(VxΔVy) = μ(Vx - y ΔV 0 ) for all x, y ∈ R d ; If X is isotropic and X 0 = 0 a.s. then μ(VRx) = μ(Vx) , for all vectorial rotations R ; Finally if X is H -self-similar and X 0 = 0 a.s. then we obtain μ(Vcx) = c 2 H μ(Vx) , for all c &gt; 0. It follows that for X to be isotropic, H selfsimilar with stationary increments, we necessarily have μ(VxΔVy) = μ(Vx - y) = c ‖ x - y ‖ 2 H , t, s ∈ R d , for some constant c &gt; 0. This is only possible when H ∈ ( 0 , 1 / 2 ] . This comes from the fact that V 2 x ⊂ (V 2 x ΔVx) ∪ Vx . Hence, by increments stationarity, μ(V 2 x) ≤ μ(VxΔV 0 ) + μ(Vx) ≤ 2 μ(Vx) since μ(V 0 ) = Var (X 0 ) = 0. By self-similarity we obtain that 2 2 H μ(Vx) ≤ 2 μ(Vx) for all x ∈ R d , implying H ≤ 1 / 2. We describe in the following the different constructions given by Lévy and Chentsov (1948 &amp; 1957) for H = 1 / 2 and Takenaka (1987) for H ∈ ( 0 , 1 / 2 ) .


<!-- p:183 -->


Proposition 4.15 Let μ and V be defined on ( R d , B ( R d )) by

- μ(dz) = ‖ z ‖ - d + 1 dz

Then, μ(VxΔVy) = μ(Vx - y) = cd ‖ x - y ‖ , for all x, y ∈ R d .

- V = { Vx, x ∈ R d } with Vx = B ( x 2 , ‖ x ‖ 2 ) = { z ∈ R d : ∥ ∥ z - x 2 ∥ ∥ &lt; ‖ x ‖ 2 } , the ball of diameter [ 0 , x ] , for all x ∈ R d .

Proof For x ∈ R d , we may used polar coordinates to identify Vx with { (r, θ) ∈ R + × S d - 1 : 0 &lt; r &lt; θ · x } Then,

$$\mu ( V _ { x } ) = \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } _ { + } } 1 _ { \{ r < \theta \cdot x \} } d r d \theta = \frac { 1 } { 2 } \int _ { S ^ { d - 1 } } | \theta \cdot x | d \theta = \frac { c _ { d } } { 2 } \| x \| ,$$

with cd = ∫ S d - 1 | e 1 · x | dθ . Moreover, for y ̸= x ,

$$\mu ( V _ { x } \cap V _ { y } ^ { c } ) & = \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } _ { + } } 1 _ { \{ \theta \cdot y \leq r < \theta \cdot x \} } d r d \theta \\ & = \int _ { 0 < \theta \cdot y < \theta \cdot x } \theta \cdot ( x - y ) d \theta + \int _ { \theta \cdot y < 0 < \theta \cdot x } \theta \cdot x d \theta .$$

Similarly, by a change of variables,

$$\mu ( V _ { y } \cap V _ { x } ^ { c } ) = \int _ { \theta \cdot y < \theta \cdot x < 0 } | \theta \cdot ( x - y ) | d \theta + \int _ { \theta \cdot y < 0 < \theta \cdot x } ( - \theta \cdot y ) \, d \theta ,$$

so that

$$\mu ( V _ { x } \Delta V _ { y } ) = \frac { 1 } { 2 } \int _ { S ^ { d - 1 } } | \theta \cdot ( x - y ) | d \theta = \frac { c _ { d } } { 2 } \| x - y \| .$$

⊓ ⊔

One can therefore check that the Chentsov random field associated with a Gaussian measure W of intensity μ and V , given in Proposition 4.15 is a (non-standard) Levy Chentsov field, or equivalently, a fractional Brownian field of index H = 1 / 2. The construction for H ∈ ( 0 , 1 / 2 ) has been given by Takenaka and relies on the following proposition.

Proposition 4.16 Let H ∈ ( 0 , 1 / 2 ) , μ and V be defined on ( R d + 1 , B ( R d + 1 )) by

- V ={ Vx, x ∈ R d } with Vx = C x Δ C 0 where C x = { (z, r) ∈ R d × R : ‖ z - x ‖≤ r } , for all x ∈ R d .
- μH(dz,dr) = r 2 H - d - 1 1 r&gt; 0 dzdr for (z, r) ∈ R d × R ;

Then, μH(VxΔVy) = μH(Vx - y ) = cH,d ‖ x - y ‖ 2 H , for all x, y ∈ R d .


<!-- p:184 -->


4

Proof Let x ∈ R d with x ̸= 0. Let us note that μH( C x ) = +∞ but, integrating first with respect to r ,

$$\mu _ { H } ( \mathcal { C } _ { x } \cap \mathcal { C } _ { 0 } ^ { c } ) & = \frac { 1 } { d - 2 H } \int _ { \| z - x \| < \| z \| } \left ( \| z - x \| ^ { 2 H - d } - \| z \| ^ { 2 H - d } \right ) d z \\ & = c _ { H , d } \| x \| ^ { 2 H } = \mu _ { H } ( \mathcal { C } _ { 0 } \cap \mathcal { C } _ { x } ^ { c } ) ,$$

using translation invariance of Lebesgue's measure, where

$$c _ { H , d } = \frac { 1 } { d - 2 H } \int _ { \| z - e _ { 1 } \| < \| z \| } \left ( \| z - e _ { 1 } \| ^ { 2 H - d } - \| z \| ^ { 2 H - d } \right ) d z \in ( 0 , + \infty ) .$$

Again by translation invariance of Lebesgue's measure, for y ̸= x , we get μH( C x Δ C y ) = μH( C x - y Δ C 0 ) = cH,d ‖ x - y ‖ 2 H . The result follows once remarked that VxΔVy = C x Δ C y . ⊓ ⊔

Of course, considering an associated Gaussian random measure we obtain the Chentsov's representation of fractional Brownian fields for H ∈ ( 0 , 1 / 2 ) . Let us remark that it also allows to define self-similar symmetric α -stable fields considering an S α S random measure (see [56]) but we leave our second order framework in this way! However, considering instead a Poisson random measure, we can define a Poisson analogous of fractional Brownian fields when H ∈ ( 0 , 1 / 2 ) .

#### 4.4.3 Fractional Poisson Fields

When Nλ,H is a Poisson random measure on R d × R with intensity λ × μH for λ &gt; 0, and μH given by Proposition 4.16, we can define a Chentsov's field by

$$N _ { \lambda , H } ( \mathcal { C } _ { x } \Delta \mathcal { C } _ { 0 } ) = N _ { \lambda , H } ( \mathcal { C } _ { x } \cap \mathcal { C } _ { 0 } ^ { c } ) + N _ { \lambda , H } ( \mathcal { C } _ { x } ^ { c } \cap \mathcal { C } _ { 0 } ) , \ \forall x \in \mathbb { R } ^ { d } .$$

However, since Nλ,H ( C x Δ C 0 ) is a Poisson random variable of parameter λμH( C x Δ C 0 ) , this field is not a centered. But remarking that μH ( C x ∩ C c 0 ) = μH ( C c x ∩ C 0 ) , we may define the centered fractional Poisson field on R d by

$$F _ { \lambda , H } ( x ) = N _ { \lambda , H } ( \mathcal { C } _ { x } \cap \mathcal { C } _ { 0 } ^ { c } ) - N _ { \lambda , H } ( \mathcal { C } _ { x } ^ { c } \cap \mathcal { C } _ { 0 } ) , \, \forall x \in \mathbb { R } ^ { d } .$$

Actually, Fλ,H may also be defined as the stochastic integral with respect to the Poisson random measure Nλ,H as

$$F _ { \lambda , H } ( x ) & = \int _ { \mathbb { R } ^ { d } \times \mathbb { R } } \left ( 1 _ { \mathcal { C } _ { x } \cap \mathcal { C } _ { 0 } ^ { c } } ( z , r ) - 1 _ { \mathcal { C } _ { x } ^ { c } \cap \mathcal { C } _ { 0 } ^ { c } } ( z , r ) \right ) \, N _ { \lambda , H } ( d z , d r ) \\ & = \int _ { \mathbb { R } ^ { d } \times \mathbb { R } } \left ( 1 _ { B ( z , r ) } ( x ) - 1 _ { B ( z , r ) } ( 0 ) \right ) \, N _ { \lambda , H } ( d z , d r ) .$$


<!-- p:185 -->

1

Fig. 4.21 Convergence of a fractional Poisson field to a fractional Brownian field as the intensity increases

Heuristically, we can throw centers and radius with respect to a Poisson point process on R d × R of intensity λ × μH , meaning that centers are thrown uniformly in R d with intensity λ and independently marked with a radius. Then Fλ,H (x) will count the number of balls falling on x minus the number of balls falling on 0. It is close to a shot noise random field obtained as the sum of randomly dilated and translated contributions. We refer to [11] and [13] for more details. Then (Fλ,H (x)) x ∈ R d is centered, with stationary increments, isotropic with covariance

$$C o v ( F _ { \lambda , H } ( x ) , F _ { \lambda , H } ( y ) ) = \frac { \lambda c _ { H , d } } { 2 } \left ( \| x \| ^ { 2 H } + \| y \| ^ { 2 H } - \| x - y \| ^ { 2 H } \right ) .$$

This field is not self-similar but

$$( F _ { \lambda , H } ( c x ) ) _ { x \in \mathbb { R } ^ { d } } \stackrel { f d d } { = } ( F _ { \lambda c ^ { 2 H } , H } ( x ) ) _ { x \in \mathbb { R } ^ { d } } , \, \forall c > 0 .$$

Moreover, according to normal approximation of Poisson measures for high intensity we can prove that (λ - 1 / 2 Fλ,H (x)) x ∈ R d fdd -→ λ →+∞ ( √ CH,dBH(x)) x ∈ R d . This is illustrated in Fig. 4.21. Note that sharp contours of fractional Poisson fields disappear in the asymptotic Gaussian limits, that are Hölder continuous. Another interesting property of this field is that its distribution is also preserved along lines (and more generally along affine subspaces). More precisely, for x 0 ∈ R d and θ ∈ S d - 1 , defining the line process Lx 0 ,θ (Fλ,H ) = ( Fλ,H (x 0 + tθ) ) t ∈ R , computing characteristic functions we can prove that ( Lx 0 ,θ (t) - Lx 0 ,θ ( 0 ) ) t ∈ R has the same distribution than a fractional Poisson process (defined for d = 1), with the same H index and intensity given by cH,dλ where cH,d = ∫ R d - 1 ( 1 -‖ y ‖ 2 ) 1 / 2 - H 1 ‖ y ‖≤ 1 dy (see [11]). Hence, we can also use estimation based on variograms to build estimators of H . Consistency has been proven in [13]. Figure 4.22 presents sample paths comparison between Poisson and Gaussian cases. To conclude, let us note that, contrarily to the Gaussian case, one can prove that the increments E ( | Fλ,H (x) - Fλ,H (x) | q ) behave like ‖ x - y ‖ 2 H for any q ≥ 2 as ‖ x - y ‖ → 0. Such a feature still holds allowing some interactions for the radii as done in [54].


<!-- p:186 -->


1

Fig. 4.22 Sample paths of fractional Poisson process (top) vs fractional Brownian motion (bottom)

<!-- p:187 -->


Acknowledgements I would like to warmly thanks all my co-authors for the different works partially presented here, especially Clément Chesseboeuf and Olivier Durieu for their careful reading.

### References

1. R.J. Adler, The Geometry of Random Field (Wiley, Hoboken, 1981)
2. D. Allard, R. Senoussi, E. Porcu, Anisotropy models for spatial data. Math. Geosci. 48 (3), 305-328 (2016)
3. A. Ayache, F. Roueff, A Fourier formulation of the Frostman criterion for random graphs and its applications to wavelet series. Appl. Comput. Harmon. Anal. 14 , 75-82 (2003)
4. A. Benassi, S. Cohen, J. Istas, Local self-similarity and the Hausdorff dimension. C. R. Acad. Sci. 336 (3), 267-272 (2003)
5. C.L. Benhamou, S. Poupon, E. Lespessailles, S. Loiseau, R. Jennane, V. Siroux, W. Ohley, L. Pothuaud, Fractal analysis of radiographic trabecular bone texture and bone mineral density: two complementary parameters related to osteoporotic fractures. J. Bone Miner. Res. 16 (4), 697-704 (2001)
6. C. Berzin, A. Latour, J.R. León, Inference on the Hurst Parameter and the Variance of Diffusions Driven by Fractional Brownian Motion . Lecture Notes in Statistics , vol. 216 (Springer, Cham, 2014). With a foreword by Aline Bonami
7. H. Biermé, C. Lacaux, Fast and exact synthesis of some operator scaling Gaussian random fields. Appl. Comput. Harmon. Anal. (2018). https://doi.org/10.1016/j.acha.2018.05.004
8. H. Biermé, F. Richard, Statistical tests of anisotropy for fractional brownian textures: application to full-field digital mammography. J. Math. Imaging Vision 36 (3), 227-240 (2010)
9. H. Biermé, M.M. Meerschaert, H.P. Scheffler, Operator scaling stable random fields. Stoch. Process. Appl. 117 (3), 312-332 (2007)
10. H. Biermé, C.L. Benhamou, F. Richard, Parametric estimation for gaussian operator scaling random fields and anisotropy analysis of bone radiograph textures, in Proceedings of the International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI'09), Workshop on Probabilistic Models for Medical Imaging , ed. by K. Pohl, London, UK, September 2009, pp. 13-24
11. H. Biermé, A. Estrade, I. Kaj, Self-similar random fields and rescaled random balls models. J. Theor. Probab. 23 (4), 1110-1141 (2010)
12. H. Biermé, A. Bonami, J.R. León, Central limit theorems and quadratic variations in terms of spectral density. Electron. J. Probab. 16 (3), 362-395 (2011)
13. H. Biermé, Y. Demichel, A. Estrade, Fractional Poisson field and fractional Brownian field: why are they resembling but different? Electron. Commun. Probab. 18 , 11-13 (2013)
14. H. Biermé, L. Moisan, F. Richard, A turning-band method for the simulation of anisotropic fractional Brownian fields. J. Comput. Graph. Stat. 24 (3), 885-904 (2015)
15. M. Bilodeau, D. Brenner, Theory of Multivariate Statistics . Springer Texts in Statistics (Springer, New York, 1999)
16. A. Bonami, A. Estrade, Anisotropic analysis of some Gaussian models. J. Fourier Anal. Appl. 9 (3), 215-236 (2003)
17. P. Breuer, P. Major, Central limit theorems for nonlinear functionals of Gaussian fields. J. Multivar. Anal. 13 (3), 425-441 (1983)
18. A. Burgess, F. Jacobson, P. Judy, Human observer detection experiments with mammograms and power-law noise. Med. Phys. 28 (4), 419-437 (2001)
19. C. Caldwell, S. Stapleton, D. Holdsworth, et al., On the statistical nature of characterisation of mammographic parenchymal patterns by fractal dimension. Phys. Med. Biol. 35 (2), 235-247 (1990)


<!-- p:188 -->


20. C.B. Caldwell, J. Rosson, J. Surowiak, T. Hearn, Use of fractal dimension to characterize the structure of cancellous bone in radiographs of the proximal femur, in Fractals in Biology and Medicine (Birkhäuser, Basel, 1994), pp. 300-306
21. G. Chan, An effective method for simulating Gaussian random fields, in Proceedings of the Statistical Computing Section (American Statistical Association, Boston, 1999), pp. 133-138. www.stat.uiowa.edu/~grchan/
22. S. Cohen, J. Istas, Fractional Fields and Applications . Mathématiques &amp; Applications (Berlin) [Mathematics &amp; Applications] , vol. 73 (Springer, Heidelberg, 2013). With a foreword by Stéphane Jaffard
23. P.F. Craigmile, Simulating a class of stationary Gaussian processes using the Davies-Harte algorithm, with application to long memory processes. J. Time Ser. Anal. 24 (5), 505-511 (2003)
24. R. Dalang, D. Khoshnevisan, C. Mueller, D. Nualart, Y. Xiao, A Minicourse on Stochastic Partial Differential Equations . Lecture Notes in Mathematics , ed. by D. Khoshnevisan, F. Rassoul-Agha, vol. 1962 (Springer, Berlin, 2009). Held at the University of Utah, Salt Lake City, UT, May 8-19, 2006
25. S. Davies, P. Hall, Fractal analysis of surface roughness by using spatial data. J. R. Stat. Soc. Ser. B 61 , 3-37 (1999)
26. C.R. Dietrich, G.N. Newsam, Fast and exact simulation of stationary gaussian processes through circulant embedding of the covariance matrix. SIAM J. Sci. Comput. 18 (4), 10881107 (1997)
27. K.J. Falconer, Fractal Geometry (Wiley, Hoboken, 1990)
28. W. Feller, An Introduction to Probability Theory and Its Applications. Vol. II. 2nd edn. (Wiley, New York, 1971)
29. T. Gneiting, H. Sevciková, D.B. Percivala, M. Schlather, Y. Jianga, Fast and exact simulation of large gaussian lattice systems in R 2 : exploring the limits. J. Comput. Graph. Stat. 15 , 483-501 (1996)
30. B. Grosjean, L. Moisan, A-contrario detectability of spots in textured backgrounds. J. Math. Imaging Vision 33 (3), 313-337 (2009)
31. R. Harba, G. Jacquet, R. Jennane, T. Loussot, C.L. Benhamou, E. Lespessailles, D. Tourlière, Determination of fractal scales on trabecular bone X-ray images. Fractals 2 (3), 451-456 (1994)
32. K. Harrar, R. Jennane, K. Zaouchi, T. Janvier, H. Toumi, E. Lespessailles, Oriented fractal analysis for improved bone microarchitecture characterization. Biomed. Signal Process. Control 39 , 474-485 (2018)
33. J. Heine, R. Velthuizen, Spectral analysis of full field digital mammography data. Med. Phys. 29 (5), 647-661 (2002)
34. E. Herbin, E. Merzbach, The set-indexed Lévy process: stationarity, Markov and sample paths properties. Stoch. Process. Appl. 123 (5), 1638-1670 (2013)
35. J. Istas, On fractional stable fields indexed by metric spaces. Electron. Commun. Probab. 11 , 242-251 (2006)
36. J. Istas, G. Lang, Quadratic variations and estimation of the local Hölder index of a Gaussian process. Ann. Inst. Henri Poincaré Probab. Stat. 33 (4), 407-436 (1997)
37. O. Kallenberg, Foundations of Modern Probability . Probability and Its Applications (New York) (Springer, New York, 1997)
38. L.M. Kaplan, C.C.J. Kuo, An improved method for 2-d self-similar image synthesis. IEEE Trans. Image Process. 5 (5), 754-761 (1996)
39. I. Karatzas, E. Shreve, Brownian Motion and Stochastic Calculus (Springer, New York, 1998)
40. P. Kesterner, J.M. Lina, P. Saint-Jean, A. Arneodo, Waveled-based multifractal formalism to assist in diagnosis in digitized mammograms. Image Anal. Stereol. 20 , 169-174 (2001)
41. A.N. Kolmogorov, The local structure of turbulence in an incompressible viscous fluid for very large reynolds number. Dokl. Akad. Nauk SSSR 30 , 301-305 (1941)
42. R. Leipus, A. Philippe, D. Puplinskait ̇ e, D. Surgailis, Aggregation and long memory: recent developments. J. Indian Stat. Assoc. 52 (1), 81-111 (2014)


<!-- p:189 -->


43. E. Lespessailles, C. Gadois, I. Kousignian, J.P. Neveu, P. Fardellone, S. Kolta, C. Roux, J.P. DoHuu, C.L. Benhamou, Clinical interest of bone texture analysis in osteoporosis: a case control multicenter study. Osteoporos. Int. 19 , 1019-1028 (2008)
44. Y. Li, W. Wang, Y. Xiao, Exact moduli of continuity for operator-scaling Gaussian random fields. Bernoulli 21 (2), 930-956 (2015)
45. G. Lindgren, Stationary Stochastic Processes: Theory and Applications . Chapman &amp; Hall/CRC Texts in Statistical Science Series (CRC Press, Boca Raton, 2013)
46. R. Lopes, N. Betrouni, Fractal and multifractal analysis: a review. Med. Image Anal. 13 , 634649 (2009)
47. B.B. Mandelbrot, J. Van Ness, Fractional Brownian motion, fractionnal noises and applications. SIAM Rev. 10 , 422-437 (1968)
48. G. Matheron, The intrinsic random functions and their application. Adv. Appl. Probab. 5 , 439468 (1973)
49. I. Molchanov, K. Ralchenko, A generalisation of the fractional Brownian field based on nonEuclidean norms. J. Math. Anal. Appl. 430 (1), 262-278 (2015)
50. G. Peccati, C. Tudor, Gaussian limits for vector-valued multiple stochastic integrals. Séminaire de Probabilités XXXVIII , 247-262 (2004)
51. E. Perrin, R. Harba, R. Jennane, I. Iribarren, Fast and exact synthesis for 1-D fractional Brownian motion a nd fractional gaussian noises. IEEE Signal Process. Lett. 9 (11), 382-384 (2002)
52. V. Pilipauskait ̇ e, D. Surgailis, Scaling transition for nonlinear random fields with long-range dependence. Stochastic Process. Appl. 127 (8), 2751-2779 (2017)
53. C.E. Powell, Generating realisations of stationary gaussian random fields by circulant embedding (2014). Technical report
54. N. Privault, Poisson sphere counting processes with random radii. ESAIM Probab. Stat. 20 , 417-431 (2016)
55. W. Rudin, Real and Complex Analysis (McGraw-Hill, New York, 1986)
56. G. Samorodnitsky, M.S. Taqqu, Stable Non-Gaussian Random Processes: Stochastic Models with Infinite Variance . Stochastic Modeling (Chapman &amp; Hall, New York, 1994)
57. M.L. Stein, Fast and exact simulation of fractional Brownian surfaces. J. Comput. Graph. Stat. 11 (3), 587-599 (2002)
58. A.W. van der Vaart, Asymptotic Statistics . Cambridge Series in Statistical and Probabilistic Mathematics , vol. 3 (Cambridge University Press, Cambridge, 1998)


<!-- p:190 -->


## Chapter 5 Introduction to the Theory of Gibbs Point Processes

####### David Dereudre

Abstract The Gibbs point processes (GPP) constitute a large class of point processes with interaction between the points. The interaction can be attractive, repulsive, depending on geometrical features whereas the null interaction is associated with the so-called Poisson point process. In a first part of this mini-course, we present several aspects of finite volume GPP defined on a bounded window in R d . In a second part, we introduce the more complicated formalism of infinite volume GPP defined on the full space R d . Existence, uniqueness and non-uniqueness of GPP are non-trivial questions which we treat here with completely self-contained proofs. The DLR equations, the GNZ equations and the variational principle are presented as well. Finally we investigate the estimation of parameters. The main standard estimators (MLE, MPLE, Takacs-Fiksel and variational estimators) are presented and we prove their consistency. For sake of simplicity, during all the mini-course, we consider only the case of finite range interaction and the setting of marked points is not presented.

### 5.1 Introduction

The spatial point processes are well studied objects in probability theory and statistics for modelling and analysing spatial data which appear in several disciplines as statistical mechanics, material science, astronomy, epidemiology, plant ecology, seismology, telecommunication, and others [4, 10]. There exist many models of such random points configurations in space and the most popular one is surely the Poisson point process. It corresponds to the natural way of producing independent locations of points in space without interaction. For dependent random structures, we can mention for instance the Cox processes, determinantal point processes, Gibbs point processes, etc. None of them is established as the most relevant model

D. Dereudre ( envelopeback )

University Lille, Villeneuve-d'Ascq, France

<!-- p:191 -->


for applications. In fact the choice of the model depends on the nature of the dataset, the knowledge of (physical or biological) mechanisms producing the pattern, the aim of the study (theoretical, applied or numerical).

In this mini-course, we focus on Gibbs point processes (GPP) which constitute a large class of points processes, able to fit several kinds of patterns and which provide a clear interpretation of the interaction between the points, such as attraction or repulsion depending on their relative position. Note that this class is particularly large since several point processes can be represented as GPP (see [24, 33] for instance). The main disadvantage of GPP is the complexity of the model due to an intractable normalizing constant which appears in the local conditional densities. Therefore their analytical studies are in general based on implicit equilibrium equations which lead to complicated and delicate analysis. Moreover, the theoretical results which are needed to investigate the Gibbs point process theory are scattered across several publications or books. The aim of this mini-course is to provide a solid and self-contained theoretical basis for understanding deeply the Gibbs point process theory. The results are in general not exhaustive but the main ideas and tools are presented in accordance with modern and recent developments. The main strong restriction here involves the range of the interaction, which is assumed to be finite. The infinite range interaction requires the introduction of tempered configuration spaces and for sake of simplicity we decided to avoid this level of complexity. The mini-course is addressed for Master and Phd students and also for researchers who want to discover or investigate the domain. The manuscript is based on a mini-course given during the conference of GDR 3477 géométrie stochastique, at university of Nantes in April 2016.

In a first section, we introduce the finite volume GPP on a bounded window Λ ⊂ R d . They are simply defined as point processes in Λ whose the distributions are absolutely continuous with respect to the Poisson point process distribution. The unnormalized densities are of form z N e - βH , where z and β are positive parameters (called respectively activity and inverse temperature), N is the number of points and H an energy function. Clearly, these distributions favour (or penalize) configurations with low (or high) energy E . This distortion strengthens as β is large. The parameter z allows to tune the mean number of points. This setting is relatively simple since all the objects are defined explicitly. However, the intractable normalization constant is ever a problem and most of quantities are not computable. Several standard notions (DLR and GNZ equations, Ruelle's estimates, etc.) are treated in this first section as a preparation for the more complicated setting of infinite volume GPP developed in the second section. Note that we do not present the setting of marked Gibbs point processes in order to keep the notations as simple as possible. However, all the results can be easily extended in this case.

In a second section, we present the theory of infinite volume GPP in R d . There are several motivations for studying such infinite volume regime. Firstly, the GPP are the standard models in statistical physics for modelling systems with a large number of interacting particles (around 10 23 according to the Avogadro's number). Therefore, the case where the number of particles is infinite is an idealization of this setting and furnishes microscopic descriptions of gas, liquid or solid. Macroscopic


<!-- p:192 -->


5

quantities like the density of particles, the pressure and the mean energy are consequently easily defined by mean values or laws of large numbers. Secondly, in the spatial statistic context, the asymptotic properties of estimators or tests are obtained when the observation window tends to the full space R d . This strategy requires the existence of infinite volume models. Finally, since the infinite volume GPP are stationary (shift invariant) in R d , several powerful tools, as the ergodic theorem or the central limit Theorem for mixing field, are available in this infinite volume regime.

The infinite volume Gibbs measures are defined by a collection of implicit DLR equations (Dobrushin, Lanford and Ruelle). The existence, uniqueness and nonuniqueness are non trivial questions which we treat in depth with self-contained proofs in this second section. The phase transition between uniqueness and non uniqueness is one of the most difficult conjectures in statistical physics. This phenomenon is expected to occur for all standard interactions although it is proved rigorously only for few models. The area interaction is one of such models and the complete proof of its phase transition is given here. The GNZ equations, the variational principle are discussed as well.

In the last section, we investigate the estimation of parameters which appear in the distribution of GPP. For sake of simplicity we deal only with the activity parameter z and the inverse temperature β . We present several standard procedures (MLE, MPLE, Takacs-Fiksel procedure) and a new variational procedure. We show the consistency of estimators, which highlights that many theoretical results are possible in spite of lack of explicit computations. We will see that the GNZ equations play a crucial role in this task. For sake of simplicity the asymptotic normality is not presented but some references are given.

Let us finish this introduction by giving standard references. Historically, the GPP have been introduced for statistical mechanics considerations and an unavoidable reference is the book by Ruelle [47]. Important theoretical contributions are also developed in two Lecture Notes [20, 46] by Georgii and Preston. For the relations between GPP and stochastic geometry, we can mention the book [8] by Chiu et al. and for spatial statistic and numerical considerations, the book by Møller and Waagepetersen [42] is the standard reference. Let us mention also the book [51] by van Lieshout on the applications of GPP.

### 5.2 Finite Volume Gibbs Point Processes

In this first section we present the theory of Gibbs point process on a bounded set Λ ⊂ R d . A Gibbs point process (GPP) is a point process with interactions between the points defined via an energy functional on the space of configurations. Roughly speaking, the GPP produces random configurations for which the configurations with low energy have more chance to appear than the configurations with high energy (see Definition 5.2). In Sect. 5.2.1 we recall succinctly some definitions of point process theory and we introduce the reference Poisson point process. The energy functions are discussed in Sect. 5.2.2 and the definition of finite volume GPP is given in Sect. 5.2.3. Some first properties are presented as well. The central DLR equations and GNZ equations are treated in Sects. 5.2.4 and 5.2.5. Finally we finish the first section by giving Ruelle estimates in the setting of superstable and lower regular energy functions.


<!-- p:193 -->


#### 5.2.1 Poisson Point Process

In this first section, we describe briefly the setting of point process theory and we introduce the reference Poisson point process. We only give the main definitions and concepts and we suggest [10, 36] for a general presentation.

The space of configurations C is defined as the set of locally finite subsets in R d :

$$\mathcal { C } = \{ \gamma \subset \mathbb { R } ^ { d } , \gamma _ { \Lambda } \colon = \gamma \cap \Lambda \text { is finite for any bounded set } \Lambda \subset \mathbb { R } ^ { d } \} .$$

Note that we consider only the simple point configurations, which means that the points do not overlap. We denote by C f the space of finite configurations in C and by C Λ the space of finite configurations inside Λ ⊂ R d .

The space C is equipped with the sigma-field FC generated by the counting functions NΛ for all bounded measurable Λ ⊂ R d , where NΛ : γ ↦→ # γΛ . A point process Γ is then simply a measurable function from any probability space (Ω, F , P ) to ( C , FC ) . As usual, the distribution (or the law) of a point process Γ is defined by the image of P to ( C , FC ) by the application Γ . We say that Γ has finite intensity if, for any bounded set Λ , the expectation μ(Λ) := E(NΛ(Γ )) is finite. In this case, μ is a sigma-finite measure called intensity measure of Γ . When μ = ζλ d , where λ d is the Lebesgue measure on R d and ζ ≥ 0 a positive real, we simply say that Γ has finite intensity ζ .

The main class of point processes is the family of Poisson point processes, which furnish the natural way of producing independent points in space. Let μ be a sigmafinite measure in R d . A Poisson point process with intensity μ is a point process Γ such that, for any bounded Λ in R d , these properties both occur

- The random variable NΛ(Γ ) is distributed following a Poisson distribution with parameter μ(Λ) .
- Given the event { NΛ(Γ) = n } , the n points in ΓΛ are independent and distributed following the distribution μΛ/μ(Λ) .

The distribution of such a Poisson point process is denoted by π μ . When the intensity is μ = ζλ d , we say that the Poisson point process is stationary (or homogeneous) with intensity ζ &gt; 0, and denote its distribution π ζ . For any measurable set Λ ⊂ R d , we denote by π ζ Λ the distribution of a Poisson point process with intensity ζλ d Λ which is also the distribution of a stationary Poisson point process with intensity ζ restricted to Λ . For sake of brevity, π and πΛ denote the distribution of Poisson point processes with intensity ζ = 1.


<!-- p:194 -->


#### 5.2.2 Energy Functions

In this section, we present the energy functions with the standard assumptions which we assume in this mini-course. The choices of energy functions come from two main motivations. First, the GPP are natural models in statistical physics for modelling continuum interacting particles systems. In general, in this setting the energy function is a sum of the energy contribution of all pairs of points (see expression (5.1)). The GPP are also used in spatial statistics to fit as best as possible the real datasets. So, in a first step, the energy function is chosen by the user with respect to the characteristics of the dataset. Then the parameters are estimated in a second step.

Definition 5.1 An energy function is a measurable function

$$H \colon \mathcal { C } _ { f } \mapsto \mathbb { R } \cup \{ + \infty \}$$

such that the following assumptions hold

- H is non-degenerate :

$$H ( \emptyset ) < + \infty .$$

- H is hereditary : for any γ ∈ C f and x ∈ γ then

$$H ( \gamma ) < + \infty \Rightarrow H ( \gamma \langle \{ x \} ) < + \infty .$$

- H is stable : there exists a constant A such that for any γ ∈ C f

$$H ( \gamma ) \geq A N _ { \mathbb { R } ^ { d } } ( \gamma ) .$$

The stability implies that the energy is superlinear. If the energy function H is positive then the choice A = 0 works but in the interesting cases, the constant A is negative. The hereditary means that the set of allowed configurations (configurations with finite energy) is stable when points are removed. The non-degeneracy is very natural. Without this assumption, the energy would be equal to infinity everywhere (by hereditary).

(1) Pairwise Interaction Let us start with the most popular energy function which is based on a function (called pair potential)

$$\varphi \colon \mathbb { R } ^ { + } \to \mathbb { R } \cup \{ + \infty \} .$$


<!-- p:195 -->


The pairwise energy function is defined for any γ ∈ C f by

$$H ( \gamma ) = \sum _ { \{ x , y \} \subset \gamma } \varphi ( | x - y | ) .$$

Note that such an energy function is trivially hereditary and non-degenerate. The stability is more delicate and we refer to general results in [47]. However if φ is positive the result is obvious.

A standard example coming from statistical physics is the so-called LennardJones pair potential where φ(r) = ar - 12 + br - 6 with a &gt; 0 and b ∈ R . In the interesting case b &lt; 0, the pair potential φ(r) is positive (repulsive) for small r and negative (attractive) for large r . The stability is not obvious and is proved in Proposition 3.2.8 in [47].

The Strauss interaction corresponds to the pair potential φ(r) = 1 [ 0 ,R ] (r) where R &gt; 0 is a support parameter. This interaction exhibits a constant repulsion between the particles at distance smaller than R . This simple model is very popular in spatial statistics.

The multi-Strauss interaction corresponds to the pair potential

$$\varphi ( r ) = \sum _ { i = 1 } ^ { k } a _ { i } 1 _ { | R _ { i - 1 } , R _ { i } | } ,$$

where (ai ) 1 ≤ i ≤ k is a sequence of real numbers and 0 = R 0 &lt; R 1 &lt; . . . &lt; Rk a sequence of increasing real numbers. Clearly, the pair potential exhibits a constant attraction or repulsion at different scales. The stability occurs provided that the parameter a 1 is large enough (see Section 3.2 in [47]).

(2) Energy Functions Coming from Geometrical Objects Several energy functions are based on local geometrical characteristics. The main motivation is to provide random configurations such that special geometrical features appear with higher probability under the Gibbs processes than the original Poisson point process. In this paragraph we give examples related to the Delaunay-Voronoi diagram. Obviously other geometrical graph structures could be considered.

Let us recall that for any x ∈ γ ∈ C f the Voronoi cell C(x,γ) is defined by

$$C ( x , \gamma ) = \left \{ w \in \mathbb { R } ^ { d } , \text { such that } \forall y \in \gamma \ | x - w | \leq | x - y | \right \} .$$

The Delaunay graph with vertices γ is defined by considering the edges

$$D ( \gamma ) = \left \{ \{ x , y \} \subset \gamma \text { such that } C ( x , \gamma ) \cap C ( y , \gamma ) \neq \emptyset \right \} .$$

See [40] for a general presentation on the Delauany-Voronoi tessellations.


<!-- p:196 -->


5

A first geometric energy function can be defined by

$$H ( \gamma ) = \sum _ { x \in \gamma } 1 _ { C ( x , \gamma ) } \text { is bounded } \varphi ( C ( x , \gamma ) ) ,$$

where φ is any function from the space of polytopes in R d to R . Examples of such functions φ are the Area, the (d - 1 ) -Hausdorff measure of the boundary, the number of faces, etc. Clearly these energy functions are non-degenerate and hereditary. The stability holds as soon as the function φ is bounded from below.

Another kind of geometric energy function can be constructed via a pairwise interaction along the edges of the Delaunay graph. Let us consider a finite pair potential φ : R + ↦→ R . Then the energy function is defined by

$$H ( \gamma ) = \sum _ { \{ x , y \} \subset D ( \gamma ) } \varphi ( | x - y | )$$

which is again clearly non-degenerate and hereditary. The stability occurs in dimension d = 2 thanks to Euler's formula. Indeed the number of edges in the Delaunay graph is linear with respect to the number of vertices. Therefore the energy function is stable as soon as the pair potential φ is bounded from below. In higher dimension d &gt; 2, the stability is more complicated and not really understood. Obviously, if φ is positive, the stability occurs.

Let us give a last example of geometric energy function which is not based on the Delaunay-Voronoi diagram but on a germ-grain structure. For any radius R &gt; 0 we define the germ-grain structure of γ ∈ C by

$$L _ { R } ( \gamma ) = \bigcup _ { x \in \gamma } B ( x , R ) ,$$

where B(x,R) is the closed ball centred at x with radius R . Several interesting energy functions are built from this germ-grain structure. First the WidomRowlinson interaction is simply defined by

$$H ( \gamma ) = \text {Area} ( L _ { R } ( \gamma ) ) ,$$

where the 'Area' is simply the Lebesgue measure λ d . This model is very popular since it is one of a few models for which the phase transition result is proved (see Sect. 5.3.8). This energy function is sometimes called Area-interaction [3, 52]. If the Area functional is replaced by any linear combination of the Minkowski functionals we obtain the Quermass interaction [12].

Another example is the random cluster interaction defined by

$$H ( \gamma ) = N c c ( L _ { R } ( \gamma ) ) ,$$


<!-- p:197 -->


where Ncc denotes the functional which counts the number of connected components. This energy function is introduced first in [7] for its relations with the Widom-Rowlinson model. See also [14] for a general study in the infinite volume regime.

#### 5.2.3 Finite Volume GPP

Let Λ ⊂ R d such that 0 &lt; λ d (Λ) &lt; +∞ . In this section we define the finite volume GPP on Λ and we give its first properties.

Definition 5.2 The finite volume Gibbs measure on Λ with activity z &gt; 0, inverse temperature β ≥ 0 and energy function H is the distribution

$$P _ { \Lambda } ^ { z , \beta } = \frac { 1 } { Z _ { \Lambda } ^ { z , \beta } } z ^ { N _ { \Lambda } } e ^ { - \beta H } \pi _ { \Lambda } ,$$

where Z z,β Λ , called partition function, is the normalization constant ∫ z NΛ e - βH dπΛ . A finite volume Gibbs point process (GPP) on Λ with activity z &gt; 0, inverse temperature β ≥ 0 and energy function H is a point process on Λ with distribution P z,β Λ .

Note that P z,β Λ is well-defined since the partition function Z z,β Λ is positive and finite. Indeed, thanks to the non degeneracy of H

$$Z _ { \Lambda } ^ { z , \beta } \geq \pi _ { \Lambda } ( \emptyset ) e ^ { - \beta H ( \{ \emptyset \} ) } = e ^ { - \lambda ^ { d } ( \Lambda ) } e ^ { - \beta H ( \{ \emptyset \} ) } > 0$$

and thanks to the stability of H

$$Z _ { \Lambda } ^ { z , \beta } \leq e ^ { - \lambda ^ { d } ( \Lambda ) } \sum _ { n = 0 } ^ { + \infty } \frac { ( z e ^ { - \beta A } \lambda ^ { d } ( \Lambda ) ) ^ { n } } { n ! } = e ^ { \lambda ^ { d } ( \Lambda ) ( z e ^ { - \beta \Lambda } - 1 ) } < + \infty .$$

In the case β = 0, we recover that P z,β Λ is the Poisson point process π z Λ . So the activity parameter z is the mean number of points per unit volume when the interaction is null. When the interaction is active ( β &gt; 0), P z,β Λ favours the configurations with low energy and penalizes the configurations with high energy. This distortion strengthens as β is large.

There are many motivations for the exponential form of the density in (5.6). Historically, it is due to the fact that the finite volume GPP solves the variational principle of statistical physics. Indeed, P z,β Λ is the unique probability measure which realizes the minimum of the free excess energy, equal to the mean energy plus the entropy. It expresses the common idea that the equilibrium states in statistical physics minimize the energy and maximize the 'disorder'. This result is presented


<!-- p:198 -->


5

in the following proposition. Recall first that the relative entropy of a probability measure P on C Λ with respect to the Poisson point process π ζ Λ is defined by

$$I ( P | \pi _ { \Lambda } ^ { \zeta } ) = \begin{cases} \int \log ( f ) d P \text { if } P \prec \pi _ { \Lambda } ^ { z } \text { with } f = \frac { d P } { d \pi _ { \Lambda } ^ { \zeta } } \\ + \infty \quad \text {otherwise} . \end{cases}$$

Proposition 5.1 (Variational Principle) Let H be an energy function, z &gt; 0 , β ≥ 0 . Then

$$\{ P _ { \Lambda } ^ { z , \beta } \} = a r g { \min } _ { P \in \mathcal { P } _ { \Lambda } } \beta E _ { P } ( H ) - \log ( z ) E _ { P } ( N _ { \Lambda } ) + I ( P | \pi _ { \Lambda } ) ,$$

where P Λ is the space of probability measures on C Λ with finite intensity and EP(H) is the expectation of H under P , which is always defined (maybe equal to infinity) since H is stable.

Proof First we note that

$$\beta E _ { P _ { \Lambda } ^ { z , \beta } } ( H ) - \log ( z ) E _ { P _ { \Lambda } ^ { z , \beta } } ( N _ { \Lambda } ) + I ( P _ { \Lambda } ^ { z , \beta } | \pi _ { \Lambda } ) \\ = \beta \int H d P _ { \Lambda } ^ { z , \beta } - \log ( z ) E _ { P _ { \Lambda } ^ { z , \beta } } ( N _ { \Lambda } ) + \int \log \left ( z ^ { N _ { \Lambda } } \frac { e ^ { - \beta H } } { Z _ { \Lambda } ^ { z , \beta } } \right ) d P _ { \Lambda } ^ { z , \beta } \\ = - \log ( Z _ { \Lambda } ^ { z , \beta } ) . \\ \intertext { s l e q u a l l y i m p l i e s t h a r r i m u m o w } \text {This equality implies that the minimum of } \beta E _ { P } ( H ) - \log ( z ) E _ { P } ( N _ { \Lambda } ) + I ( P _ { \Lambda } )$$

This equality implies that the minimum of βEP(H) - log (z)EP (NΛ) + I (P | πΛ) should be equal to - log (Z z,β Λ ) . So for any P ∈ P Λ such that EP(H) &lt; +∞ and I (P | πΛ) &lt; +∞ let us show that βEP(H) - log (z)EP (NΛ) + I (P | πΛ) ≥ - log (Z z,β Λ ) with equality if and only if P = P z,β Λ . Let f be the density of P with respect to πΛ .

$$e x t \pi _ { \Lambda } . \\ \log ( Z _ { A } ^ { z , \beta } ) & \geq \log \left ( \int _ { \{ f > 0 \} } z ^ { N _ { \Lambda } } e ^ { - \beta H } d \pi _ { \Lambda } \right ) \\ & = \log \left ( \int z ^ { N _ { \Lambda } } e ^ { - \beta H } \, f ^ { - 1 } d P \right ) \\ & \geq \int \log \left ( z ^ { N _ { \Lambda } } e ^ { - \beta H } \, f ^ { - 1 } \right ) d P \\ & = - \beta E _ { P } ( H ) - \log ( z ) E _ { P } ( N _ { \Lambda } ) - \log ( f ) d P . \\ \intertext { s e c o n d i n e q u a l i t y , d u t e p t h s c r e n s i n e q u a l i t y , i s an e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u a l i t y f i n d o n l l e s } \intertext { s e x t t h s c r e n s i n e q u$$

The second inequality, due to the Jensen's inequality, is an equality if and only if z NΛ e - βH f - 1 is P a.s. constant which is equivalent to P = P z,β Λ . The proposition is proved.


<!-- p:199 -->


The parameters z and β allow to fit the mean number of points and the mean value of the energy under the GPP. Indeed when z increases, the mean number of points increases as well and similarly when β increases, the mean energy decreases. This phenomenon is expressed in the following proposition. The proof is a simple computation of derivatives.

Let us note that it is not easy to tune both parameters simultaneously since the mean number of points changes when β is modified (and vice versa). The estimation of the parameters z and β is discussed in the last Sect. 5.4.

Proposition 5.2 The function z ↦→ E P z,β Λ (NΛ) is continuous and differentiable, with derivative z ↦→ Var P z,β Λ (NΛ)/z on ( 0 , +∞ ) . Similarly the function β ↦→ E P z,β Λ (H) is continuous and differentiable with derivative β ↦→ - Var P z,β Λ (H) on R + .

Let us finish this section by explaining succinctly how to simulate such finite volume GPP. There are essentially two algorithms. The first one is based on a MCMC procedure where GPP are viewed as equilibrium states of Markov chains. The simulation is obtained by letting run for a long enough time the Markov chain. The simulation is not exact and the error is essentially controlled via a monitoring approach (see [42]). The second one is a coupling from the past algorithm which provided exact simulations. However, the computation time is often very long and these algorithms are not really that used in practice (see [32]).

#### 5.2.4 DLR Equations

The DLR equations are due to Dobrushin, Lanford and Ruelle and give the local conditional distributions of GPP in any bounded window Δ given the configuration outside Δ . We need to define a family of local energy functions (HΔ) Δ ⊂ R d .

Definition 5.3 For any bounded set Δ and any finite configuration γ ∈ C f we define

$$H _ { \Delta } ( \gamma ) \colon = H ( \gamma ) - H ( \gamma _ { \Delta ^ { c } } ) ,$$

with the convention ∞-∞= 0.

The quantity HΔ(γ) gives the energetic contribution of points in γΔ towards the computation of the energy of γ . As an example, let us compute these quantities in the setting of pairwise interaction introduced in (5.1);

$$H _ { \Delta } ( \gamma ) = \sum _ { \{ x , y \} \subset \gamma } \varphi ( | x - y | ) - \sum _ { \{ x , y \} \subset \gamma _ { \Delta ^ { c } } } \varphi ( | x - y | ) = \sum _ { \{ x , y \} \subset \gamma } \quad \varphi ( | x - y | ) .$$


<!-- p:200 -->


Note that HΔ(γ) does not depend only on points in Δ . However, trivially we have H(γ) = HΔ(γ) + H(γΔ c ), which shows that the energy of γ is the sum of the energy HΔ(γ) plus something which does not depends on γΔ .

Proposition 5.3 (DLR Equations for Finite Volume GPP) Let Δ ⊂ Λ be two bounded sets in R d with λ d (Δ) &gt; 0 . Then for P z,β Λ -a.s. all γΔ c

$$P _ { \Lambda } ^ { z , \beta } ( d \gamma _ { \Delta } | \gamma _ { \Delta ^ { c } } ) = \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } z ^ { N _ { \Delta } ( \gamma ) } e ^ { - \beta H _ { \Delta } ( \gamma ) } \pi _ { \Delta } ( d \gamma _ { \Delta } ) ,$$

where Z z,β Δ (γΔ c ) is the normalizing constant ∫ z NΔ(γ) e - βHΔ(γ) πΔ(dγΔ) . In particular the right term in (5.9) does not depend on Λ .

Proof From the definition of HΔ and the stochastic properties of the Poisson point process we have

$$P _ { \Lambda } ^ { z , \beta } ( d \gamma ) & = \frac { 1 } { z _ { \Lambda } ^ { z , \beta } } z _ { \Lambda } ^ { N _ { \Lambda } ( \gamma ) } e ^ { - \beta H ( \gamma ) } \pi _ { \Lambda } ( d \gamma ) \\ & = \frac { 1 } { z _ { \Lambda } ^ { z , \beta } } z _ { \Lambda } ^ { N _ { \Lambda } ( \gamma ) } e ^ { - \beta H _ { \Delta } ( \gamma ) } z _ { \Lambda \Lambda \Delta } ^ { N _ { \Lambda \Lambda } ( \gamma ) } e ^ { - \beta H ( \gamma _ { \Lambda \Lambda } \Delta ) } \pi _ { \Delta } ( d \gamma _ { \Delta } ) \pi _ { \Lambda \Lambda \Delta } ( d \gamma _ { \Lambda \Lambda } ) .$$

This expression ensures that the unnormalized conditional density of P z,β Λ (dγΔ | γΔ c ) with respect to πΔ(dγΔ) is γΔ ↦→ z NΔ(γ) e - βHΔ(γ) . The normalization is necessary Z z,β Δ (γΔ c ) and the proposition is proved.

The DLR equations give the local conditional marginal distributions of GPP. They are the main tool to understand the local description of P z,β Λ , in particular when Λ is large. Note that the local marginal distributions (not conditional) are in general not accessible. It is a difficult point of the theory of GPP. This fact will be reinforced in the infinite volume regime, where the local distributions can be nonunique.

The DLR equations have a major issue due the intractable normalization constant Z z,β Δ (γΔ c ) . In the next section the problem is partially solved via the GNZ equations.

#### 5.2.5 GNZ Equations

The GNZ equations are due to Georgii, Nguyen and Zessin and have been introduced first in [43]. They generalize the Slivnyak-Mecke formulas for Poisson point processes. In this section we present and prove these equations. We need first to define the energy of a point inside a configuration.


<!-- p:201 -->


Definition 5.4 Let γ ∈ C f be a finite configuration and x ∈ R d . Then the local energy of x in γ is defined by

$$h ( x , \gamma ) = H ( \{ x \} \cup \gamma ) - H ( \gamma ) ,$$

with the convention +∞- ( +∞ ) = 0. Note that if x ∈ γ then h(x, γ ) = 0.

Proposition 5.4 (GNZ Equations) For any positive measurable function f from R d × C f to R ,

$$\int \sum _ { x \in \gamma } f ( x , \gamma \langle \{ x \} ) P _ { \Lambda } ^ { z , \beta } ( d \gamma ) = z \int \int _ { \Lambda } f ( x , \gamma ) e ^ { - \beta h ( x , \gamma ) } d x P _ { \Lambda } ^ { z , \beta } ( d \gamma ) .$$

Proof Let us decompose the left term in (5.10).

$$P o f \, \text { Let us decompose the left term in (5 . 1 0 ) } \\ \int \sum _ { x \in \gamma } f ( x , \gamma \langle x \rangle ) P _ { A } ^ { z , \beta } ( d \gamma ) \\ = \frac { 1 } { Z _ { A } ^ { z , \beta } } \int \sum _ { x \in \gamma } f ( x , \gamma \langle x \rangle ) z ^ { N _ { A } ( \gamma ) } e ^ { - \beta H ( \gamma ) } \pi _ { A } ( d \gamma ) \\ = \frac { e ^ { - \lambda ^ { d } ( \Lambda ) } } { Z _ { A } ^ { z , \beta } } \sum _ { n = 1 } ^ { + \infty } \frac { z ^ { n } } { n ! } \sum _ { k = 1 } ^ { n } \int _ { A ^ { k } } f ( x _ { k } , \{ x _ { 1 } , \dots , x _ { n } \} \langle x _ { k } \rangle ) e ^ { - \beta H ( \{ x _ { 1 } , \dots , x _ { n } \} ) } d x _ { 1 } \dots d x _ { n } \\ = \frac { e ^ { - \lambda ^ { d } ( \Lambda ) } } { Z _ { A } ^ { z , \beta } } \sum _ { n = 1 } ^ { + \infty } \frac { z ^ { n } } { ( n - 1 ) ! } \int _ { A ^ { k } } f ( x , \{ x _ { 1 } , \dots , x _ { n - 1 } \} ) e ^ { - \beta H ( \{ x _ { 1 } , \dots , x _ { n - 1 } \} ) } \\ e ^ { - \beta h ( x , \{ x _ { 1 } , \dots , x _ { n - 1 } \} ) } d x _ { 1 } \dots d x _ { n - 1 } d x \\ = \frac { z } { Z _ { A } ^ { z , \beta } } \int _ { A } f ( x , \gamma ) z ^ { N _ { A } ( \gamma ) } e ^ { - \beta H ( \gamma ) } e ^ { - \beta h ( x , \gamma ) } \pi _ { A } ( d \gamma ) d x \\ = z \int \int _ { A } f ( x , \gamma ) e ^ { - \beta h ( x , \gamma ) } d x P _ { A } ^ { z , \beta } ( d \gamma ) . \\ \text { As usual the function } f \text { in (5. 1 0) can be chosen without a constant sign. We just } \\ \text { need to check that both terms in (5. 1 0) are integrable. } \\ \text { In the following proposition we show that the equations GNZ (5. 1 0) characterize }$$

As usual the function f in (5.10) can be chosen without a constant sign. We just need to check that both terms in (5.10) are integrable.

In the following proposition we show that the equations GNZ (5.10) characterize the probability measure P z,β Λ .

Proposition 5.5 Let Λ ⊂ R d bounded such that λ d (Λ) &gt; 0 . Let P be a probability measure on C Λ such that for any positive measurable function f from R d × C f to R

$$\int \sum _ { x \in \gamma } f ( x , \gamma \langle \{ x \} ) P ( d \gamma ) = z \int \int _ { \Lambda } f ( x , \gamma ) e ^ { - \beta h ( x , \gamma ) } d x \, P ( d \gamma ) .$$


<!-- p:202 -->


Then it holds that P = P z,β Λ .

Proof Let us consider the measure Q = 1 { H&lt; +∞} z - NΛ e βH P . Then

$$\text {Proof Let us consider the measure } Q = 1 _ { \{ H < + \infty \} } z ^ { - N _ { A } } e ^ { \beta H } P . \text { Then} \\ \int _ { x \in \gamma } f ( x , \gamma \ \{ x \} ) Q ( d \gamma ) \\ = \int _ { x \in \gamma } f ( x , \gamma \ \{ x \} ) 1 _ { \{ H ( \gamma ) < + \infty \} } z ^ { - N _ { A } ( \gamma ) } e ^ { \beta H ( \gamma ) } P ( d \gamma ) \\ = z ^ { - 1 } \int _ { x \in \gamma } f ( x , \gamma \ \{ x \} ) 1 _ { \{ H ( \gamma \ \{ x \} ) < + \infty \} } 1 _ { \{ h ( x , \gamma \ \{ x \} ) < + \infty \} } \\ = \int _ { A } f ( x , \gamma ) 1 _ { \{ H ( \gamma ) < + \infty \} } 1 _ { \{ h ( x , \gamma ) < + \infty \} } e ^ { - \beta h ( x , \gamma ) } \\ = \int _ { A } f ( x , \gamma ) 1 _ { \{ h ( x , \gamma ) < + \infty \} } d x P ( d \gamma ) \\ = \int _ { A } f ( x , \gamma ) 1 _ { \{ h ( x , \gamma ) < + \infty \} } d x Q ( d \gamma ) . \\ \text {We deduce that } Q \text { satisfies the Slivnyan-Mecke formula on } \{ \gamma \in \mathcal { C } _ { A } , H ( \gamma ) < \infty \} . \\ \text {Proof Let us well-known (see [36] for instance) that it implies that the measure Q}$$

We deduce that Q satisfies the Slivnyak-Mecke formula on { γ ∈ C Λ,H(γ) &lt; +∞} . It is well-known (see [36] for instance) that it implies that the measure Q (after normalization) is the Poisson point process πΛ restricted to { γ ∈ C Λ, H(γ) &lt; +∞} . The proposition is proved.

These last two propositions show that the GNZ equations contain completely the informations on P z,β Λ . Note again that the normalization constant Z z,β Λ is not present in the equations.

#### 5.2.6 Ruelle Estimates

In this section we present Ruelle estimates in the context of superstable and lower regular energy functions. These estimates are technical and we refer to the original paper [48] for the proofs.

Definition 5.5 An energy function H is said superstable if H = H 1 + H 2 where H 1 is an energy function (see Definition 5.1) and H 2 is a pairwise energy function defined in (5.1) with a non-negative continuous pair potential φ such that φ( 0 ) &gt; 0. The energy function H is said lower regular if there exists a summable decreasing sequence of positive reals (ψk)k ≥ 0 (i.e. ∑ +∞ k = 0 ψk &lt; +∞ ) such that for any finite configurations γ 1 and γ 2


<!-- p:203 -->


$$H ( \gamma ^ { 1 } \cup \gamma ^ { 2 } ) - H ( \gamma ^ { 1 } ) - H ( \gamma ^ { 2 } ) \\ \geq - \sum _ { k , k ^ { \prime } \in \mathbb { Z } ^ { d } } \psi _ { \| k - k ^ { \prime } \| } \left ( N _ { [ k + [ 0 , 1 ] ^ { d } ] } ^ { 2 } ( \gamma ^ { 1 } ) + N _ { [ k ^ { \prime } + [ 0 , 1 ] ^ { d } ] } ^ { 2 } ( \gamma ^ { 2 } ) \right ) . \\$$

Let us give the main example of superstable and lower regular energy function.

Proposition 5.6 (Proposition 1.3 [48]) Let H be a pairwise energy function with a pair potential φ = φ 1 + φ 2 where φ 1 is stable and φ 2 is non-negative continuous with φ 2 ( 0 ) &gt; 0 . Moreover, we assume that there exists a positive decreasing function ψ from R + to R such that

$$\int _ { 0 } ^ { + \infty } r ^ { d - 1 } \psi ( r ) d r < + \infty$$

and such that for any x ∈ R , φ(x) ≥ - ψ( ‖ x ‖ ) . Then the energy function H is superstable and lower regular.

In particular, the Lennard-Jones pair potential or the Strauss pair potential defined in Sect. 5.2.2 are superstable and lower regular. Note also that all geometric energy functions presented in Sect. 5.2.2 are not superstable.

Proposition 5.7 (Corollary 2.9 [48]) Let H be a superstable and lower regular energy function. Let z &gt; 0 and β &gt; 0 be fixed. Then for any bounded subset Δ ⊂ R d with λ d (Δ) &gt; 0 there exist two positive constants c 1 , c 2 such that for any bounded set Λ and k ≥ 0

$$P _ { \Lambda } ^ { z , \beta } ( N _ { \Delta } \geq k ) \leq c _ { 1 } e ^ { - c _ { 2 } k ^ { 2 } } .$$

In particular, Ruelle estimates (5.12) ensure that the random variable NΔ admits exponential moments for all orders under P z,β Λ . Surprisingly, the variate N 2 Δ admits exponential moments for small orders. This last fact is not true under the Poisson point process π z Λ = P z, 0 Λ . The interaction between the points improves the integrability properties of the GPP with respect to the Poisson point process.

### 5.3 Infinite Volume Gibbs Point Processes

In this section we present the theory of infinite volume GPP corresponding to the case ' Λ = R d ' of the previous section. Obviously, a definition inspired by (5.6) does not work since the energy of an infinite configuration γ is meaningless. A natural construction would be to consider a sequence of finite volume GPP (P z,β Λn )n ≥ 1 on bounded windows Λn = [- n, n ] d and let n tend to infinity. It is more or less what we do in the following Sects. 5.3.1 and 5.3.2, except that the convergence occurs only for a subsequence and that the field is stationarized (see Eq. (5.14)). As far as we know, there does not exist a general proof of the convergence of the sequence (P z,β Λn )n ≥ 1 without extracted a subsequence. The stationarization is a convenient setting here in order to use the tightness entropy tools. In Sects. 5.3.3 and 5.3.4 we prove that the accumulation points P z,β satisfy the DLR equations which is the standard definition of infinite volume GPP (see Definition 5.8). We make precise that the main new assumption in this section is the finite range property (see Definition 5.7). It means that the points interact with each other only if their distance is smaller than a fixed constant R &gt; 0. The GNZ equations in the infinite volume regime are discussed in Sect. 5.3.5. The variational characterisation of GPP, in the spirit of Proposition 5.1, is presented in Sect. 5.3.6. Uniqueness and non-uniqueness results of infinite volume GPP are treated in Sects. 5.3.7 and 5.3.8. These results, whose proofs are completely self contained here, ensure the existence of a phase transition for the Area energy function presented in (5.4). It means that the associated infinite volume Gibbs measures are unique for some parameters (z, β) and non-unique for other parameters.


<!-- p:204 -->


#### 5.3.1 The Local Convergence Setting

In this section we define the topology of local convergence which is the setting we use to prove the existence of an accumulation point for the sequence of finite volume Gibbs measures.

First, we say that a function from C to R is local if there exists a bounded set Δ ⊂ R d such that for all γ ∈ C , f(γ) = f(γΔ) .

Definition 5.6 The local convergence topology on the space of probability measures on C is the smallest topology such that for any local bounded function f from C to R the function P ↦→ ∫ fdP is continuous. We denote by τ L this topology.

Our tightness tool is based on the specific entropy which is defined for any stationary probability P on C by

Let us note that the continuity of functions f in the previous definition is not required. For instance the function γ ↦→ f(γ) = 1 NΔ(γ) ≥ k , where Δ is a bounded set in R d and k any integer, is a bounded local function. For any vector u ∈ R d we denote by τu the translation by the vector u acting on R d or C . A probability P on C is said stationary (or shift invariant) if for any vector u ∈ R d P = P ◦ τ - 1 u .

$$I _ { \zeta } ( P ) = \lim _ { n \to + \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } I ( P _ { \Lambda _ { n } } | \pi _ { \Lambda _ { n } } ^ { \zeta } ) ,$$

where I (PΛn | π ζ Λn ) is the relative entropy of PΛn , the projection of P on Λn , with respect to π ζ Λn (see Definition 5.7). Note that the specific entropy Iζ (P ) always exists (i.e. the limit in (5.13) exists); see chapter 15 in [22]. The tightness tool presented in Lemma 5.1 below is a consequence of the following proposition.


<!-- p:205 -->


Proposition 5.8 (Proposition 15.14 [22]) For any ζ &gt; 0 and any value K ≥ 0 , the set

$$\{ P \in \mathcal { P } \ s u c h \ t h a t \ I _ { \zeta } ( P ) \leq K \}$$

is sequentially compact for the topology τ L , where P is the space of stationary probability measures on C with finite intensity.

#### 5.3.2 An Accumulation Point P z,β

In this section we prove the existence of an accumulation point for a sequence of stationarized finite volume GPP. To the end we consider the Gibbs measures (P z,β Λn )n ≥ 1 on Λn := [- n, n ] d , where (P z,β Λ ) is defined in (5.6) for any z &gt; 0, β ≥ 0 and energy function H . We assume that H is stationary , which means that for any vector u ∈ R d and any finite configuration γ ∈ C f

$$H ( \tau _ { u } ( \gamma ) ) = H ( \gamma ) .$$

For any n ≥ 1, the empirical field  ̄ P z,β Λn is defined by the probability measure on C such that for any test function f

$$\int f ( \gamma ) \bar { P } _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) = \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } \int f ( \tau _ { u } ( \gamma ) ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) d u .$$

The probability measure  ̄ P z,β Λn can be interpreted as the Gibbs measure P z,β Λn where the origin of the space R d (i.e. the point { 0 } ) is replaced by a random point chosen uniformly inside Λn . It is a kind of stationarization of P z,β Λn and any accumulation point of the sequence (  ̄ P z,β Λn )n ≥ 1 is necessary stationary.

Proposition 5.9 The sequence (  ̄ P z,β Λn )n ≥ 1 is tight for the τ L topology. We denote by P z,β any of its accumulation points.

Proof Our tightness tool is the following lemma whose the proof is a consequence of Proposition 5.8 (See also Proposition 15.52 in [22]).

Lemma 5.1 The sequence (  ̄ P z,β Λn )n ≥ 1 is tight for the τ L topology if there exits ζ &gt; 0 such that

$$\sup _ { n \geq 1 } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } I ( P _ { \Lambda _ { n } } ^ { z , \beta } | \pi _ { \Lambda _ { n } } ^ { \zeta } ) < + \infty .$$


<!-- p:206 -->


So, let us compute I (P z,β Λn | π ζ Λn ) and check that we can find ζ &gt; 0 such that (5.15) holds.

$$( 5 . 1 5 ) \, \text {holds.} \\ \\ I ( P _ { A _ { n } } ^ { z , \beta } | \pi _ { \Lambda _ { n } } ^ { \zeta } ) & = \int \log \left ( \frac { d P _ { A _ { n } } ^ { z , \beta } } { d \pi _ { A _ { n } } ^ { \zeta } } \right ) d P _ { A _ { n } } ^ { z , \beta } \\ & = \int \left [ \log \left ( \frac { d P _ { A _ { n } } ^ { z , \beta } } { d \pi _ { A _ { n } } } \right ) + \log \left ( \frac { d \pi _ { A _ { n } } } { d \pi _ { A _ { n } } ^ { \zeta } } \right ) \right ] d P _ { A _ { n } } ^ { z , \beta } \\ & = \int \left [ \log \left ( z ^ { N _ { A _ { n } } } \, \frac { e ^ { - \beta H } } { Z _ { A _ { n } } ^ { z , \beta } } \right ) + \log \left ( e ^ { ( \zeta - 1 ) \lambda ^ { d } ( A _ { n } ) } \left ( \frac { 1 } { \zeta } \right ) ^ { N _ { A _ { n } } } \right ) \right ] d P _ { A _ { n } } ^ { z , \beta } \\ & = \int \left [ - \beta H + \log \left ( \frac { z } { \zeta } \right ) N _ { A _ { n } } \right ] d P _ { A _ { n } } ^ { z , \beta } + ( \xi - 1 ) \lambda ^ { d } ( A _ { n } ) - \log ( Z _ { A _ { n } } ^ { z , \beta } ) . \\ \text {Thanks to the non degeneracy and the stability of $H$ we find that}$$

Thanks to the non degeneracy and the stability of H we find that

$$I ( P _ { \Lambda _ { n } } ^ { z , \beta } | \pi _ { \Lambda _ { n } } ^ { \zeta } ) & \leq \int \left ( - A \beta + \log \left ( \frac { z } { \zeta } \right ) \right ) N _ { \Lambda _ { n } } d P _ { \Lambda _ { n } } ^ { z , \beta } \\ & + \lambda ^ { d } ( \Lambda _ { n } ) \left ( ( \zeta - 1 ) + 1 + \beta H ( \{ \vartheta \} ) \right ) .$$

Choosing ζ &gt; 0 such that - Aβ + log (z/ζ) ≤ 0 we obtain

$$I ( P _ { \Lambda _ { n } } ^ { z , \beta } | \pi _ { \Lambda _ { n } } ^ { \zeta } ) \leq \lambda ^ { d } ( \Lambda _ { n } ) ( \zeta + \beta H ( \{ \emptyset \} )$$

and (5.15) holds. Proposition 5.9 is proved.

In the following, for sake of simplicity, we say that  ̄ P z,β Λn converges to P z,β although it occurs only for a subsequence.

Note that the existence of an accumulation points holds under very weak assumptions on the energy function H . Indeed the two major assumptions are the stability and the stationarity. The superstability or the lower regularity presented in Definition 5.5 are not required here. However, if the energy function H is superstable and lower regular, then the accumulation points P z,β inherits Ruelle estimates (5.12). This fact is obvious since the function γ ↦→ 1 { NΔ(γ) ≥ k } is locally bounded.

Corollary 5.1 Let H be a superstable and lower regular energy function (see Definition 5.5). Let z &gt; 0 and β &gt; 0 be fixed. Then for any bounded subset Δ ⊂ R d with λ d (Δ) &gt; 0 , there exists c 1 and c 2 two positive constants such that for any k ≥ 0

$$P ^ { z , \beta } ( N _ { \Delta } \geq k ) \leq c _ { 1 } e ^ { - c _ { 2 } k ^ { 2 } } .$$


<!-- p:207 -->


The important point now is to prove that P z,β satisfies good stochastic properties as for instance the DLR or GNZ equations. At this stage, without extra assumptions, these equations are not necessarily satisfied. Indeed it is possible to build energy functions H such that the accumulation point P z,β is degenerated and charges only the empty configuration. In this mini-course our extra assumption is the finite range property presented in the following section. More general settings have been investigated for instance in [16] or [47].

#### 5.3.3 The Finite Range Property

The finite range property expresses that further a certain distance R &gt; 0 the points do not interact each other. Let us recall the Minkoswki ⊕ operator acting on sets in R d . For any two sets A,B ⊂ R d , the set A ⊕ B is defined by { x + y, x ∈ A and y ∈ B } .

Definition 5.7 The energy function H has a finite range R &gt; 0 if for every bounded Δ , the local energy HΔ (see Definition 5.3) is a local function on Δ ⊕ B( 0 , R) . It means that for any finite configuration γ ∈ C f

$$H _ { \Delta } ( \gamma ) \coloneqq H ( \gamma ) - H ( \gamma _ { \Delta ^ { c } } ) = H ( \gamma _ { \Delta \oplus B ( 0 , R ) } ) - H ( \gamma _ { \Delta \oplus B ( 0 , R ) \ \Delta ^ { c } } ) .$$

Let us illustrate the finite range property in the setting of pairwise interaction defined in (5.1). Assume that the interaction potential φ : R + → R ∪ {+∞} has a support included in [ 0 , R ] . Then the associated energy function has a finite R ;

$$d i e d i n [ 0 , R ] . \text { Then the associated energy function has a } & \infty \\ H _ { \Delta } ( \gamma ) = \sum _ { \{ x , y \} \subset \gamma } \varphi ( | x - y | ) \\ & \{ x , y \} \cap \Delta \neq \emptyset \\ | x - y | \leq R \\ = \sum _ { \{ x , y \} \subset \gamma \Delta \in B ( 0 , R ) } \varphi ( | x - y | ) . \\ \intertext { a r e a n g r y } \text {area function (5.4) inherits the finite range proper}$$

Also the area energy function (5.4) inherits the finite range property. A simple computation gives

$$H _ { \Delta } ( \gamma ) = \text {Area} \left ( \bigcup _ { x \in \gamma _ { \Delta } } B ( x , R ) \bigcup _ { x \in \gamma _ { \Delta \oplus B ( 0 , 2 R ) \wedge } } B ( x , R ) \right )$$

which provides a range of interaction equals to 2 R .


<!-- p:208 -->


Let us note that the energy functions defined in (5.2),(5.3) and (5.5) do not have the finite range property. Similarly the pairwise energy function (5.1) with the Lennard-Jones potential is not finite range since the support of the pair potential is not bounded. A truncated version of such potential is sometimes considered.

Let us finish this section by noting that the finite range property allows to extend the domain of definition of HΔ from the space C f to the set C . Indeed, since HΔ(γ) = HΔ(γΔ ⊕ B( 0 ,R)) , this equality provides a definition of HΔ(γ) when γ is in C . This point is crucial in order to correctly define the DLR equations in the infinite volume regime.

#### 5.3.4 DLR Equations

In Sect. 5.2 on the finite volume GPP, the DLR equations are presented as properties for P z,β Λ (see Sect. 5.2.4). In the setting of infinite volume GPP, the DLR equations are the main points of the definition of GPP.

Definition 5.8 (Infinite Volume GPP) Let H be a stationary and finite range energy function. A stationary probability P on C is an infinite volume Gibbs measure with activity z &gt; 0, inverse temperature β ≥ 0 and energy function H if for any bounded Δ ⊂ R d such that λ d (Δ) &gt; 0 then for P -a.s. all γΔ c

$$P ( d \gamma _ { \Delta } | \gamma _ { \Delta ^ { c } } ) = \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } z ^ { N _ { \Delta } ( \gamma ) } e ^ { - \beta H _ { \Delta } ( \gamma ) } \pi _ { \Delta } ( d \gamma _ { \Delta } ) ,$$

where Z z,β Δ (γΔ c ) is the normalizing constant ∫ z NΔ(γ) e - βHΔ(γ) πΔ(dγΔ) . As usual, an infinite volume GPP is a point process whose distribution is an infinite volume Gibbs measure.

Note that the DLR equations (5.18) make sense since HΔ(γ) is well defined for any configuration γ ∈ C (see the end of Sect. 5.3.3). Note also that the DLR equations (5.18) can be reformulated in an integral form. Indeed P satisfies (5.18) if and only if for any local bounded function f from C to R

$$\int f d P = \int f ( \gamma _ { \Delta } ^ { \prime } \cup \gamma _ { \Delta ^ { c } } ) \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } z ^ { N _ { \Delta } ( \gamma _ { \Delta } ^ { \prime } ) } e ^ { - \beta H _ { \Delta } ( \gamma _ { \Delta } ^ { \prime } \cup _ { \gamma _ { \Delta } } c ) } \pi _ { \Delta } ( d \gamma _ { \Delta } ^ { \prime } ) P ( d \gamma ) .$$

The term 'equation' is now highlighted by the formulation (5.19) since the unknown variate P appears in both left and right sides. The existence, uniqueness and non-uniqueness of solutions of such DLR equations are non trivial questions. In the next theorem, we show that the accumulation point P z,β obtained in Sect. 5.3.2 is such a solution. Infinite volume Gibbs measure exist and the question of existence is solved. The uniqueness and non-uniqueness are discussed in Sects. 5.3.7 and 5.3.8.


<!-- p:209 -->


Theorem 5.1 Let H be a stationary and finite range energy function. Then for any z &gt; 0 and β ≥ 0 the probability measure P z,β defined in Proposition 5.9 is an infinite volume Gibbs measure.

Proof We have just to check that P z,β satisfies, for any bounded Δ and any positive local bounded function f , the Eq. (5.19). Let us define the function fΔ by

$$f _ { \Delta } \colon \gamma \mapsto \int f ( \gamma _ { \Delta } ^ { \prime } \cup \gamma _ { \Delta ^ { c } } ) \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta } c ) } z ^ { N _ { \Delta } ( \gamma _ { \Delta } ^ { \prime } ) } e ^ { - \beta H _ { \Delta } ( \gamma _ { \Delta } ^ { \prime } \cup \gamma _ { \Delta } c ) } \pi _ { \Delta } ( d \gamma _ { \Delta } ^ { \prime } ) .$$

Since f is local and bounded and since H is finite range, the function fΔ is bounded and local as well. From the convergence of the sequence (  ̄ P z,β Λn )n ≥ 1 to P z,β with respect to the τ L topology, we have

$$and \text { local as well. From the convergence of the sequence } ( \bar { P } _ { \Lambda _ { n } } ^ { z , \beta } ) _ { n \geq 1 } & \text { to } P ^ { z , \beta } \text { with} \\ \int f _ { \Delta } d P ^ { z , \beta } \\ & = \lim _ { n \to \infty } \int f _ { \Delta } d \bar { P } _ { \Lambda _ { n } } ^ { z , \beta } \\ & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } \int f _ { \Delta } ( \tau _ { u } ( \gamma ) ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) d u . \\ & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } \int f ( \gamma ^ { \prime } _ { \Delta } \cup \tau _ { u } ( \gamma ) _ { \Delta ^ { c } } ) \frac { z ^ { N _ { \Lambda } ( \gamma ^ { \prime } _ { \Delta } ) } } { Z _ { \Delta } ^ { z , \beta } ( \tau _ { u } ( \gamma ) _ { \Delta ^ { c } } ) } e ^ { - \beta H _ { \Lambda } ( \gamma ^ { \prime } _ { \Delta } \cup \tau _ { u } ( \gamma ) _ { \Delta ^ { c } } ) } \\ & = \lim _ { n \to \infty } \frac { \pi _ { \Delta } ( d \gamma ^ { \prime } _ { \Delta } ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) d u } { \pi _ { \Lambda } ( z ^ { \beta } _ { \Delta } ) } \\ & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } \int f \left ( \tau _ { u } ( \gamma ^ { \prime } _ { \tau _ { u } ( \Lambda ) } ) \cup \gamma _ { \tau _ { u } ( \Lambda ) ^ { c } } \right ) \frac { Z ^ { - i ( N _ { n } ( \gamma ^ { \prime } _ { \tau _ { u } ( \Lambda ) ^ { c } } ) } } { Z _ { \tau _ { u } ( \Lambda ) } ^ { z , \beta } ( \gamma _ { \tau _ { u } ( \Lambda ) ^ { c } } ) } \\ & \quad - \beta H _ { \tau _ { u } ( \Lambda ) } ( \gamma ^ { \prime } _ { \tau _ { u } ( \Lambda ) ^ { c } } ) \cup \gamma _ { \tau _ { u } ( \Lambda ) } ( \tau _ { u } ^ { \prime } ( \Lambda ) ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) d u . \\ & \text { Denoting by } A _ { n } ^ { * } \text { the set of } u \in A _ { n } \text { such that } \tau _ { u } ( \Lambda ) \subset A _ { n } , \text { by Proposition } 5 . 3 , \\ P _ { \Lambda ^ { z , \beta } } ^ { z , \beta } \text { satisfies the DLR equation on } \tau _ { u } ( \Lambda ) \text { as soon as } \tau _ { u } ( \Lambda ) \subset A _ { n } \text { (i.e. } u \in A _ { n } ^ { * } ) . \\$$

Denoting by Λ ∗ n the set of u ∈ Λn such that τ - u(Δ) ⊂ Λn , by Proposition 5.3, P z,β Λn satisfies the DLR equation on τ - u(Δ) as soon as τ - u(Δ) ⊂ Λn (i.e. u ∈ Λ ∗ n ). It follows that for any u ∈ Λ ∗ n

$$& \int f ( \tau _ { u } \gamma ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) \\ & = \int \int f \left ( \tau _ { u } ( \gamma _ { \tau _ { u } ( \Delta ) } \cup \gamma _ { \tau _ { u } ( \Delta ) } ) \right ) \frac { z ^ { N } \tau _ { u } ( \Delta ) ( \gamma _ { \tau _ { u } ( \Delta ) } ^ { \prime } ) } { Z _ { \tau _ { u } ( \Delta ) } ^ { z , \beta } ( \gamma _ { \tau _ { u } ( \Delta ) } ) } e ^ { - \beta H _ { \tau _ { u } ( \Delta ) } ( \gamma _ { \tau _ { u } ( \Delta ) } ^ { \prime } ) \cup \gamma _ { \tau _ { u } ( \Delta ) } c ) } \\ & \quad \pi _ { \tau _ { u } ( \Delta ) } ( d \gamma _ { \tau _ { u } ( \Delta ) } ^ { \prime } ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) .$$


<!-- p:210 -->


By noting that λ d (Λ ∗ n ) is equivalent to λ d (Λn) when n goes to infinity, we obtain in compiling (5.20) and (5.21)

$$\int f _ { \Delta } d P ^ { z , \beta } & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } ^ { * } } \int \int f ( \tau _ { u } \gamma ) P _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) d u \\ & = \lim _ { n \to \infty } \int f ( \gamma ) F _ { \Lambda _ { n } } ^ { z , \beta } ( d \gamma ) \\ & = \int f d P ^ { z , \beta } \\$$

which gives the expected integral DLR equation on Δ with test function f .

#### 5.3.5 GNZ Equations

In this section we deal with the GNZ equations in the infinite volume regime. As in the finite volume case, the main advantage of such equations is that the intractable normalization factor Z z,β Λ is not present.

Note first that, in the setting of finite range interaction R &gt; 0, the local energy h(x, γ ) defined in Definition 5.4 is well-defined for any configuration γ ∈ C even if γ is infinite. Indeed, we clearly have h(x, γ ) = h(x, γB(x,R)) .

Theorem 5.2 Let P be a probability measure on C . Let H be a finite range energy function and z &gt; 0 , β ≥ 0 be two parameters. Then P is an infinite volume Gibbs measure with energy function H , activity z &gt; 0 and inverse temperature β if and only if for any positive measurable function f from R d × C to R

$$\int \sum _ { x \in \gamma } f ( x , \gamma \langle \{ x \} ) P ( d \gamma ) = z \int \int _ { \mathbb { R } ^ { d } } f ( x , \gamma ) e ^ { - \beta h ( x , \gamma ) } d x \, P ( d \gamma ) .$$

Proof Let us start with the proof of the 'only if' part. Let P be an infinite volume Gibbs measure. By standard monotonicity arguments it is sufficient to prove (5.22) for any local positive measurable function f . So let Δ ⊂ R d be a bounded set such that f(x,γ) = 1 Δ(x)f(x, γΔ) . Applying now the DLR equation (5.19) on the set Δ we find

$$& \int \sum _ { x \in \gamma } f ( x , \gamma \langle \{ x \} ) P ( d \gamma ) \\ & = \int \int \sum _ { x \in \gamma ^ { \prime } } f ( x , \gamma ^ { \prime } _ { \Delta } \langle \{ x \} ) \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } z ^ { N _ { \Delta } ( \gamma ^ { \prime } _ { \Delta } ) } e ^ { - \beta H _ { \Delta } ( \gamma ^ { \prime } _ { \Delta } \cup _ { A } c ) } \pi _ { \Delta } ( d \gamma ^ { \prime } _ { \Delta } ) P ( d \gamma ) .$$


<!-- p:211 -->


By computations similar to those developed in the proof of Proposition 5.4, we obtain

$$\int \sum _ { x \in \gamma } f ( x , \gamma \langle \{ x \} ) P ( d \gamma ) & = z \int \int _ { \Delta } \int f ( x , \gamma ^ { \prime } _ { \Delta } ) \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } e ^ { - \beta h ( x , \gamma ^ { \prime } _ { \Delta } \cup \gamma _ { \Delta ^ { c } } ) } \\ & = z \int \int _ { \mathbb { R } ^ { d } } f ( x , \gamma ) e ^ { - \beta h ( x , \gamma ) } d x P ( d \gamma ) \\$$

Let us now turn to the 'if part'. Applying Eq. (5.22) to the function  ̃ f(x,γ) = ψ(γΔ c )f (x, γ ) where f is a local positive function with support Δ and ψ a positive test function we find

$$\int \psi ( \gamma _ { \Delta ^ { c } } ) \sum _ { x \in \gamma _ { \Delta } } f ( x , \gamma \langle \{ x \} ) P ( d \gamma ) = z \int \psi ( \gamma _ { \Delta ^ { c } } ) \int _ { \mathbb { R } ^ { d } } f ( x , \gamma ) e ^ { - \beta h ( x , \gamma ) } d x P ( d \gamma ) .$$

This implies that for P almost all γΔ c the conditional probability measure P(dγΔ | γΔ c ) solves the GNZ equations on Δ with local energy function γΔ ↦→ h(x, γΔ ∪ γΔ c ) . Following an adaptation of the proof of Proposition 5.5, we get that

$$P ( d \gamma _ { \Delta } | \gamma _ { \Delta ^ { c } } ) = \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } z ^ { N _ { \Delta } ( \gamma ) } e ^ { - \beta H _ { \Delta } ( \gamma ) } \pi _ { \Delta } ( d \gamma _ { \Delta } ) ,$$

which is exactly the DLR equation (5.18) on Δ . The theorem is proved.

Let us finish this section with an application of the GNZ equations which highlights that some properties of infinite volume GPP can be extracted from the implicit GNZ equations.

Proposition 5.10 Let Γ be a infinite volume GPP for the hardcore pairwise interaction φ(r) = +∞ 1 [ 0 ,R ] (r) (see Definition 5.1) and the activity z &gt; 0 . Then

$$\frac { z } { 1 + z v _ { d } R ^ { d } } \leq E \left ( N _ { [ 0 , 1 ] ^ { d } } ( \Gamma ) \right ) \leq z ,$$

where vd is the volume of the unit ball in R d .

Note that the inverse temperature β does not play any role here and that EP ( N [ 0 , 1 ] d (Γ ) ) is simply the intensity of Γ .

Proof The local energy of such harcore pairwise interaction is given by

$$h ( x , \gamma ) = \sum _ { y \in \gamma _ { B ( x , R ) } } \varphi ( | x - y | ) = + \infty 1 _ { \gamma _ { B ( x , R ) } \neq \emptyset } .$$


<!-- p:212 -->


So the GNZ equation (5.22) with the function f(x, γ ) = 1 [ 0 , 1 ] d(x) gives

$$E \left ( N _ { [ 0 , 1 ] ^ { d } } ( \Gamma ) \right ) = z \int _ { [ 0 , 1 ] ^ { d } } P ( \Gamma _ { B ( x , R ) } = \emptyset ) d x = z \ P ( \Gamma _ { B ( 0 , R ) } = \emptyset ) ,$$

which provides a relation between the intensity and the spherical contact distribution of Γ . The upper bound in (5.23) follows. For the lower bound we have

$$E _ { P } \left ( N _ { [ 0 , 1 ] ^ { d } } ( \Gamma ) \right ) & = z \, P ( \Gamma _ { B ( 0 , R ) } = \emptyset ) \\ & \geq z \left ( 1 - E _ { P } \left ( N _ { B ( 0 , R ) } ( \Gamma ) \right ) \right ) \\ & = z \left ( 1 - v _ { d } R ^ { r } \, E _ { P } \left ( N _ { [ 0 , 1 ] ^ { d } } ( \Gamma ) \right ) \right ) . \\ \intertext { a l o s t h a r } \intertext { a l o s t h a r } \alpha \, \text { also that a } \text { not u r o l } \text { upper bound for } F _ { \Gamma } \left ( N _ { \Gamma _ { \ } a } \right ) \text { is o t i o ned via the }$$

Note also that a natural upper bound for EP ( N [ 0 , 1 ] d ) is obtained via the closed packing configuration. For instance, in dimension d = 2, it gives the upper bound π/( 2 √ 3 R 2 ) .

#### 5.3.6 Variational Principle

In this section, we extend the variational principle for finite volume GPP presented in Proposition 5.1 to the setting of infinite volume GPP. For brevity we present only the result without the proof which can be found in [13].

The variational principle claims that the Gibbs measures are the minimizers of the free excess energy defined by the sum of the mean energy and the specific entropy. Moreover, the minimum is equal to minus the pressure. Let us first define all these macroscopic quantities.

Let us start by introducing the pressure with free boundary condition. It is defined as the following limit

$$p ^ { z , \beta } \coloneqq \lim _ { n \to + \infty } \frac { 1 } { | \Lambda _ { n } | } \ln ( Z _ { \Lambda _ { n } } ^ { z , \beta } ) ,$$

The existence of such limit is proved for instance in Lemma 1 in [13].

The second macroscopic quantity involves the mean energy of a stationary probability measure P . It is also defined by a limit but, in opposition to the pressure, we have to assume that it exists. The proof of such existence is generally based on stationary arguments and nice representations of the energy contribution per unit volume. It depends strongly on the expression of the energy function H . Examples are given below. So for any stationary probability measure P on C we assume that the following limit exists in R ∪ {+∞} ,


<!-- p:213 -->


$$H ( P ) \coloneqq \lim _ { n \to \infty } \frac { 1 } { | \Lambda _ { n } | } \int H ( \gamma _ { \Lambda _ { n } } ) d P ( \gamma ) ,$$

and we call the limit mean energy of P .

We need to introduce a technical assumption on the boundary effects of H . We assume that for any infinite volume Gibbs measure P

$$\lim _ { n \to \infty } \frac { 1 } { | \Lambda _ { n } | } \int \partial H _ { \Lambda _ { n } } ( \gamma ) d P ( \gamma ) = 0 ,$$

where ∂HΛn (γ ) = HΛn (γ ) - H(γΛn ) .

Theorem 5.3 (Variational Principle, Theorem 1, [13]) We assume that H is stationary and finite range. Moreover, we assume that the mean energy exists for any stationary probability measure P (i.e. the limit (5.25) exists) and that the boundary effects assumption (5.26) holds. Let z &gt; 0 and β ≥ 0 two parameters. Then for any stationary probability measure P on C with finite intensity

$$I _ { 1 } ( P ) + \beta H ( P ) - \log ( z ) E _ { P } ( N _ { [ 0 , 1 ] ^ { d } } ) \geq - p ^ { z , \beta } ,$$

with equality if and only if P is a Gibbs measure with activity z &gt; 0 , inverse temperature β and energy function H .

Let us finish this section by presenting the two fundamental examples of energy functions satisfying the assumptions of Theorem 5.3.

Proposition 5.11 Let H be the Area energy function defined in (5.4) . Then both limits (5.25) and (5.26) exist. In particular, the assumptions of Theorem 5.3 are satisfied and the variational principle holds.

Proof Let us prove only that the limit (5.25) exists. The existence of limit (5.26) can be shown in the same way. By definition of H and the stationarity of P ,

$$\text { can be shown in the same way. By decrement of $R$ and the same $a$-th $a$-th $a$-th $a$-th $a$-th $a$-th $a$-th $a$-th $a$-th $a$-th $a$-th} \\ \int H ( \gamma _ { \Lambda _ { n } } ) P ( d \gamma ) & = \int \text {Area} ( L _ { R } ( \gamma _ { \Lambda _ { n } } ) ) P ( d \gamma ) \\ & = \lambda ^ { d } ( \Lambda _ { n } ) \int \text {Area} ( L _ { R } ( \gamma ) \cap [ 0 , 1 ] ^ { d } ) P ( d \gamma ) \\ & \quad + \int \left ( \text {Area} ( L _ { R } ( \gamma _ { \Lambda _ { n } } ) ) - \text {Area} ( L _ { R } ( \gamma ) \cap [ - n , n ] ^ { d } ) \right ) P ( d \gamma ) . \\$$

By geometric arguments, we get that

$$\left | \text {Area} ( L _ { R } ( \gamma _ { \Lambda _ { n } } ) ) - \text {Area} ( L _ { R } ( \gamma ) \cap [ - n , n ] ^ { d } ) \right | \leq C n ^ { d - 1 } ,$$


<!-- p:214 -->


5

for some constant C &gt; 0. We deduce that the limit (5.25) exists with

$$H ( P ) = \int A r e a ( L _ { R } ( \gamma ) \cap [ 0 , 1 ] ^ { d } ) P ( d \gamma ) .$$

Proposition 5.12 Let H be the pairwise energy function defined in (5.1) with a superstable, lower regular pair potential with compact support. Then the both limits (5.25) and (5.26) exist. In particular the assumptions of Theorem 5.3 are satisfied and the variational principle holds.

Proof Since the potential φ is stable with compact support, we deduce that φ ≥ 2 A and H is finite range and lower regular. In this setting, the existence of the limit (5.25) is proved in [21], Theorem 1 with

$$H ( P ) = \begin{cases} \frac { 1 } { 2 } \int \sum _ { 0 \ne x \in \gamma } \varphi ( x ) P ^ { 0 } ( d \gamma ) & \text {if } E _ { P } ( N _ { [ 0 , 1 ] ^ { d } } ^ { 2 } ) < \infty \\ + \infty & \text {otherwise} \end{cases}$$

where P 0 is the Palm measure of P . Recall that P 0 can be viewed as the natural version of the conditional probability P(. | 0 ∈ γ) (see [36] for more details). It remains to prove the existence of the limit (5.26) for any Gibbs measure P on C . A simple computation gives that, for any γ ∈ C ,

$$\partial H _ { \Lambda _ { n } } ( \gamma ) = \sum _ { x \in \gamma _ { \Lambda _ { n } ^ { \oplus } \Lambda _ { n } } \ y \in \gamma _ { \Lambda _ { n } \Lambda _ { n } ^ { \ominus } } } \varphi ( x - y ) ,$$

where Λ ⊕ n = Λn + R 0 and Λ ⊖ n = Λn - R 0 with R 0 an integer larger than the range of the interaction R .

Therefore thanks to the stationarity of P and the GNZ equations (5.22), we obtain

$$\text {Herefor thanks to the stationary of } & P \text { and the GN2 equations (3.22), we obtain } \\ & \left | \int \partial H _ { \Lambda _ { n } } ( \gamma ) d P ( \gamma ) \right | \leq \int \sum _ { x \in \gamma _ { \Lambda _ { n } ^ { \oplus } , \Lambda _ { n } } } \sum _ { y \in \gamma \ \{ x \} } | \varphi ( x - y ) | d P ( \gamma ) \\ & = z \int \int _ { \Lambda _ { n } ^ { \oplus } \Lambda _ { n } } e ^ { - \beta \sum _ { y \in \gamma } \varphi ( x - y ) } \sum _ { y \in \gamma _ { B ( 0 , R _ { 0 } ) } } | \phi ( x - y ) | d x d P ( \gamma ) \\ & = z | \Lambda _ { n } ^ { \oplus } \Lambda _ { n } | \int e ^ { - \beta \sum _ { y \in \gamma _ { B ( 0 , R _ { 0 } ) } } \varphi ( y ) } \sum _ { y \in \gamma _ { B ( 0 , R _ { 0 } ) } } | \varphi ( y ) | d P ( \gamma ) . \\ & \text {Since } \varpi \geq 2 A \text { denoting by } C \coloneqq \sup _ { x \in \Omega } | C | e ^ { - \beta c } \leq \infty \text { we find that }$$

Since φ ≥ 2 A , denoting by C := sup c ∈[ 2 A ;+∞ ) | c | e - βc &lt; ∞ we find that

$$\left | \int \partial H _ { \Lambda _ { n } } ( \gamma ) d P ( \gamma ) \right | \leq z C | \Lambda _ { n } ^ { \oplus } \rangle \Lambda _ { n } | \int N _ { B ( 0 , R _ { 0 } ) } ( \gamma ) e ^ { - 2 \beta A N _ { B ( 0 , R _ { 0 } ) } ( \gamma ) } d P ( d \gamma ) .$$


<!-- p:215 -->


Using Ruelle estimates (5.16), the integral in the right term of (5.30) is finite. The boundary assumption (5.26) follows.

#### 5.3.7 A Uniqueness Result

In this section we investigate the uniqueness of infinite volume Gibbs measures. The common belief claims that the Gibbs measures are unique when the activity z or (and) the inverse temperature β are small enough (low activity, high temperature regime). The non-uniqueness phenomenon (discussed in the next section) are in general related to some issues with the energy part in the variational principle (see Theorem 5.3). Indeed, either the mean energy has several minimizers or there is a conflict between the energy and the entropy. Therefore it is natural to expect the Gibbs measures are unique when β is small enough. When z is small, the mean number of points per unit volume is low and so the energy is in general low as well.

As far as we know, there do not exist general results which prove the uniqueness for small β or small z . In the case of pairwise energy functions (5.1), the uniqueness for any β &gt; 0 and z &gt; 0 small enough is proved via the Kirkwood-Salsburg equations (see Theorem 5.7 [48]). An extension of the Dobrushin uniqueness criterium in the continuum is developed as well [18]. The uniqueness of GPP can also be obtained via the cluster expansion machinery which provides a power series expansion of the partition function when z and β are small enough. This approach has been introduced first by Mayer and Montroll [37] and we refer to [45] for a general presentation.

In this section we give a simple and self-contained proof of the uniqueness of GPP for all β ≥ 0 and any z &gt; 0 small enough. We just assume that the energy function H has a local energy h uniformly bounded from below. This setting covers for instance the case of pairwise energy function (5.1) with non-negative pair potential or the Area energy function (5.4).

Let us start by recalling the existence of a percolation threshold for the Poisson Boolean model. For any configuration γ ∈ C the percolation of LR(γ) = ∪ x ∈ γ B(x, R) means the existence of an unbounded connected component in LR(γ) .

Proposition 5.13 (Theorem 1 [28]) For any d ≥ 2 , there exists 0 &lt; zd &lt; +∞ such that for z &lt; zd , π z (L 1 / 2 percolates ) = 0 and for z &gt; zd , π z (L 1 / 2 percolates ) = 1 .

The value zd is called the percolation threshold of the Poisson Boolean model with radius 1 / 2. By scale invariance, the percolation threshold for any other radius R is simply zd /( 2 R) d . The exact value of zd is unknown but numerical studies provide for instance the approximation z 2 ≃ 1 . 4 in dimension d = 2.

Theorem 5.4 Let H be an energy function with finite range R &gt; 0 such that the local energy h is uniformly bounded from below by a constant C . Then for any β ≥ 0


<!-- p:216 -->


5

and z &lt; zde Cβ /R d , there exists an unique Gibbs measure with energy function H , activity z &gt; 0 and inverse temperature β .

Proof The proof is based on two main ingredients. The first one is the stochastic domination of Gibbs measures, with uniformly bounded from below local energy function h , by Poisson processes. This result is given in the following lemma, whose proof can be found in [23]. The second ingredient is a disagreement percolation result presented in Lemma 5.3 below.

Lemma 5.2 Let H be an energy function such that the local energy h is uniformly bounded from below by a constant C . Then for any bounded set Δ and any outside configuration γΔ c the Gibbs distribution inside Δ given by

$$P ^ { z , \beta } ( d \gamma _ { \Delta } | \gamma _ { \Delta ^ { c } } ) = \frac { 1 } { Z _ { \Delta } ^ { z , \beta } ( \gamma _ { \Delta ^ { c } } ) } z ^ { N _ { \Delta } ( \gamma ) } e ^ { - \beta H _ { \Delta } ( \gamma ) } \pi _ { \Delta } ( d \gamma _ { \Delta } )$$

is stochastically dominated by the Poisson point distribution π ze - Cβ Δ (dγΔ) .

Thanks to Strassen's Theorem, this stochastic domination can be interpreted via the following coupling (which could be the definition of the stochastic domination): There exist two point processes Γ and Γ ′ on Δ such that Γ ⊂ Γ ′ , Γ ∼ P z,β (dγΔ | γΔ c ) and Γ ′ ∼ π ze - Cβ Δ (dγΔ) .

Lemma 5.3 Let γ 1 Δ c and γ 2 Δ c be two configurations on Δ c . For any R ′ &gt; R , there exist three point processes Γ 1 , Γ 2 and Γ ′ on Δ such that Γ 1 ⊂ Γ ′ , Γ 2 ⊂ Γ ′ , Γ 1 ∼ P z,β (dγΔ | γ 1 Δ c) , Γ 2 ∼ P z,β (dγΔ | γ 2 Δ c) and Γ ′ ∼ π ze - Cβ Δ (dγΔ) . Moreover, denoting by L Δ R ′ / 2 (Γ ′ ) the connected components of LR ′ / 2 (Γ ′ ) which are inside Δ ⊖ B( 0 , R ′ / 2 ) , then Γ 1 = Γ 2 on the set L Δ R ′ / 2 (Γ ′ ) .

Now the rest of the proof of Theorem 5.4 consists in showing that the Gibbs measure is unique as soon as π ze - Cβ (LR/ 2percolates ) = 0. Roughly speaking, if the dominating process does not percolate, the information coming from the boundary condition does not propagate in the heart of the model and the Gibbs measure is unique. To prove rigorously this phenomenon, we need a disagreement percolation argument introduced first in [50]. For any sets A,B ∈ R d , we denote by A ⊖ B the set (A c ⊕ B) c .

Proof Let us note first that, by Lemma 5.2, there exist three point processes Γ 1 , Γ 2 and Γ ′ on Δ such that Γ 1 ⊂ Γ ′ , Γ 2 ⊂ Γ ′ , Γ 1 ∼ P z,β (dγΔ | γ 1 Δ c) , Γ 2 ∼ P z,β (dγΔ | γ 2 Δ c) and Γ ′ ∼ π ze - Cβ Δ (dγΔ) . The main difficulty is now to show that we can build Γ 1 and Γ 2 such that Γ 1 = Γ 2 on the set L Δ R ′ / 2 (Γ ′ ) .

Let us decompose Δ via a grid of small cubes where each cube has a diameter smaller than ε = (R ′ - R)/ 2. We define an arbitrary numeration of these cubes (Ci) 1 ≤ i ≤ m and we construct progressively the processes Γ 1 , Γ 2 and Γ ′ on each cube Ci . Assume that they are already constructed on CI := ∪ i ∈ I Ci with all the expected properties: Γ 1 CI ⊂ Γ ′ CI , Γ 2 CI ⊂ Γ ′ CI , Γ 1 CI ∼ P z,β (dγCI | γ 1 Δ c) , Γ 2 CI ∼


<!-- p:217 -->


P z,β (dγCI | γ 2 Δ c) , Γ ′ CI ∼ π ze - Cβ CI (dγCI ) and Γ 1 CI = Γ 2 CI on the set L Δ R ′ / 2 (Γ ′ CI ) . Let us consider the smaller index j ∈ { 1 , . . . m }\ I such that either the distances d(Cj , γ 1 Δ c ) or d(Cj , γ 2 Δ c) or d(Cj , Γ ′ CI ) is smaller than R ′ - ε .

- If such an index j does not exist, by the finite range property the following Gibbs distributions coincide on Δ I = Δ \ CI ;

$$P ^ { z , \beta } ( d \gamma _ { \Delta ^ { I } } | \gamma _ { \Delta ^ { c } } ^ { 1 } \cup \Gamma _ { C _ { I } } ^ { 1 } ) = P ^ { z , \beta } ( d \gamma _ { \Delta ^ { I } } | \gamma _ { \Delta ^ { c } } ^ { 2 } \cup \Gamma _ { C _ { I } } ^ { 2 } ) .$$

Therefore we define Γ 1 , Γ 2 and Γ ′ on Δ I by considering Γ 1 Δ I and Γ ′ Δ I as in Lemma 5.2 and by putting Γ 2 Δ I = Γ 1 Δ I . We can easily check that all expected properties hold and the full construction of Γ 1 , Γ 2 and Γ ′ is over.

- If such an index j does exist, we consider the double coupling construction of Γ 1 , Γ 2 and Γ ′ on Δ I . It means that Γ 1 Δ I ⊂ Γ ′ Δ I , Γ 2 Δ I ⊂ Γ ′ Δ I , Γ 1 Δ I ∼ P z,β (dγ Δ I | γ 1 Δ c ∪ Γ 1 CI ) , Γ 2 Δ I ∼ P z,β (dγ Δ I | γ 2 Δ c ∪ Γ 2 CI ) and Γ ′ Δ I ∼ π ze Cβ Δ I (dγΔ) . Now we keep these processes Γ 1 Δ I , Γ 2 Δ I and Γ ′ Δ I only on the window Cj . The construction of the processes Γ 1 , Γ 2 and Γ ′ is now over CI ∪ Cj and we can check again that all expected properties hold. We go on to the construction of the processes on a new cube in (Ci)i ∈{ 1 ,...n }\{ I,j } and so on.

Let us now finish the proof of Theorem 5.4 by considering two infinite volume GPP  ̃ Γ 1 and  ̃ Γ 2 with distribution P 1 and P 2 . We have to show that for any local event A P 1 (A) = P 2 (A) . We denote by Δ 0 the support of such an event A . Let us consider a bounded subset Δ ⊃ Δ 0 and three new processes Γ 1 Δ , Γ 2 Δ and Γ ′ Δ on Δ constructed as in Lemma 5.3. Precisely, for any i = 1 , 2 Γ i Δ ⊂ Γ ′ Δ , Γ ′ ∼ π ze - Cβ Δ , the conditional distribution of Γ i Δ given  ̃ Γ i Δ c is P z,β ( |  ̃ Γ i Δ c) and Γ 1 Δ = Γ 2 Δ on the set L Δ R ′ / 2 (Γ ′ Δ ) . The parameter R ′ &gt; R is chosen such that

$$z e ^ { - C \beta } R ^ { \prime d } < z _ { d }$$

which is possible by assumption on z .

Thanks to the DLR equations (5.18), for any i = 1 , 2 the processes Γ i Δ and  ̃ Γ i Δ have the same distributions and therefore P i (A) = P(Γ i Δ ∈ A) . Denoting by { Δ ↔ Δ 0 } the event that there exists a connected component in LR ′ / 2 (Γ ′ ) which intersects (Δ ⊖ B( 0 , R ′ / 2 )) c and Δ 0, we obtain that

$$| P ^ { 1 } ( A ) - P ^ { 2 } ( A ) | & = | P ( \Gamma _ { \Delta } ^ { 1 } \in A ) - P ( \Gamma _ { \Delta } ^ { 2 } \in A ) | \\ & \leq E \left ( 1 _ { \{ \Delta \leftrightarrow \Delta _ { 0 } \} } \left | 1 _ { \Gamma _ { \Delta } ^ { 1 } \in A } - 1 _ { \Gamma _ { \Delta } ^ { 2 } \in A } \right | \right ) \\ & + E \left ( 1 _ { \{ \Delta \leftrightarrow \Delta _ { 0 } \} ^ { c } } \left | 1 _ { \Gamma _ { \Delta } ^ { 1 } \in A } - 1 _ { \Gamma _ { \Delta } ^ { 2 } \in A } \right | \right )$$


<!-- p:218 -->


$$& \leq P ( \{ \Delta \leftrightarrow \Delta _ { 0 } \} ) + E \left ( 1 _ { \{ \Delta \leftrightarrow \Delta _ { 0 } \} } \Big | 1 _ { \Gamma _ { \Delta } ^ { l } \in A } - 1 _ { \Gamma _ { \Delta } ^ { l } \in A } \Big | \right ) \\ & = P ( \{ \Delta \leftrightarrow \Delta _ { 0 } \} ) .$$

By the choice of R ′ in inequality (5.31) and Proposition 5.13, it follows that

$$\pi ^ { z e ^ { - C \beta } } \left ( L _ { R ^ { \prime } / 2 } \text {percolates} \right ) & = 0 \\ \\ \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot$$

and we deduce, by a monotonicity argument, the probability P( { Δ ↔ Δ 0 } ) tends to 0 when Δ tends to R d (see [38] for details on equivalent characterizations of continuum percolation). The left term in (5.32) does not depend on Δ and therefore it is null. Theorem 5.4 is proved.

#### 5.3.8 A Non-uniqueness Result

In this section we discuss the non-uniqueness phenomenon of infinite volume Gibbs measures. It is believed to occur for almost all models provided that the activity z or the inverse temperature β is large enough. However, in the present continuous setting without spin, it is only proved for few models and several old conjectures are still valid. For instance, for the pairwise Lennard-Jones interaction defined in (5.1), it is conjectured that for β large (but not too large) there exists an unique z such that the Gibbs measures are not unique. It would correspond to a liquidvapour phase transition. Similarly for β very large, it is conjectured that the nonuniqueness occurs as soon as z is larger than a threshold zβ . It would correspond to a crystallization phenomenon for which a symmetry breaking may occur. Indeed, it is expected, but not proved at all, that some continuum Gibbs measures would be not invariant under symmetries like translations, rotations, etc. This conjecture is probably one of the most important and difficult challenges in statistical physics. In all cases, the non-uniqueness appear when the local distribution of infinite volume Gibbs measures depend on the boundary conditions 'at infinity'.

In this section we give a complete proof of such non-uniqueness result for the Area energy interaction presented in (5.4). This result has been first proved in [52] but our proof is inspired by the one given in [7]. Roughly speaking, we build two different Gibbs measures which depend, via a percolation phenomenon, on the boundary conditions 'at infinity'. In one case, the boundary condition 'at infinity' is empty and in the other case the boundary condition is full of particles. We show that the intensity of both infinite volume Gibbs measures are different.

Let us cite another famous non-uniqueness result for attractive pair and repulsive four-body potentials [34]. As far as we know, this result and the one presented below on the Area interaction, are the only rigorous proofs of non-uniqueness results for continuum particles systems without spin.


<!-- p:219 -->


Theorem 5.5 For z = β large enough, the infinite volume Gibbs measures for the Area energy function H presented in (5.4) , the activity z and the inverse temperature β are not unique.

Proof In all the proof we fix z = β . Let us consider following finite volume Gibbs measures on Λn = [- n, n ] d with different boundary conditions:

$$d P _ { \Lambda _ { n } } ( \gamma ) = \frac { 1 } { Z _ { \Lambda _ { n } } } 1 _ { \{ \gamma _ { \Lambda _ { n } \wedge \Lambda _ { n } ^ { \ominus } } \} } z ^ { N _ { \Lambda _ { n } } ( \gamma ) } e ^ { - z \text {Area} \left ( \Lambda _ { n } \cap L _ { R } ( \gamma ) \right ) } d \pi _ { \Lambda _ { n } } ( \gamma ) ,$$

and

$$d Q _ { \Lambda _ { n } } ( \gamma ) = \frac { 1 } { Z _ { \Lambda _ { n } } ^ { \prime } } z ^ { N _ { \Lambda _ { n } } ( \gamma ) } e ^ { - z \text {Area} \left ( \Lambda _ { n } ^ { \ominus } \cap L _ { R } ( \gamma ) \right ) } d \pi _ { \Lambda _ { n } } ( \gamma ) ,$$

where Λ ⊖ n = Λn ⊖ B( 0 , R/ 2 ) . Recall that R is the radius of balls in LR(γ) = ∪ x ∈ γ B(x, R) and that the range of the interaction is 2 R . As in Sect. 5.3.2 we consider the associated empirical fields  ̄ PΛn and  ̄ QΛn defined by

$$\int f ( \gamma ) d \bar { P } _ { \Lambda _ { n } } ( \gamma ) = \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } f ( \tau _ { u } ( \gamma ) ) d P _ { \Lambda _ { n } } ( \gamma ) d u$$

and

$$\int f ( \gamma ) d \bar { Q } _ { \Lambda _ { n } } ( \gamma ) = \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } f ( \tau _ { u } ( \gamma ) ) d Q _ { \Lambda _ { n } } ( \gamma ) d u ,$$

where f is any measurable bounded test function. Following the proof of Proposition 5.9 we get the existence of an accumulation point  ̄ P (respectively  ̄ Q ) for (  ̄ PΛn ) (respectively (  ̄ QΛn ) ). As in Theorem 5.1, we show that  ̄ P and  ̄ Q satisfy the DLR equations and therefore they are both infinite volume Gibbs measures for the Area energy function, the activity z and the inverse temperature β = z . Now it remains to prove that  ̄ P and  ̄ Q are different when z is large enough. Note that the difference between  ̄ P and  ̄ Q comes only from their boundary conditions 'at infinity' (i.e. the boundary conditions of PΛn and QΛn when n goes to infinity).

Let us start with a representation of PΛn and QΛn via the two type WidomRowlinson model on Λn . Consider the following event of allowed configurations on C 2 Λn

$$\mathcal { A } = \left \{ ( \gamma ^ { 1 } , \gamma ^ { 2 } ) \in \mathcal { C } _ { \Lambda _ { n } } ^ { 2 } , \, \text {s.t.} \, \begin{smallmatrix} a ) \, L _ { R / 2 } ( \gamma ^ { 1 } ) \cap L _ { R / 2 } ( \gamma ^ { 2 } ) = \emptyset \\ b ) \, L _ { R / 2 } ( \gamma ^ { 1 } ) \cap \Lambda _ { n } ^ { c } = \emptyset \end{smallmatrix} \right \}$$

which assumes first that the balls with radii R/ 2 centred at γ 1 and γ 2 do not overlap and secondly that the balls centred at γ 1 are completely inside Λn .


<!-- p:220 -->


5

The two type Widom-Rowlinson model on Λn with boundary condition b) is the probability measure  ̃ PΛn on C 2 Λn which is absolutely continuous with respect to the product (π z Λn ) ⊗ 2 with density

$$\frac { 1 } { \tilde { Z } _ { n } } 1 _ { \mathcal { A } } ( \gamma ^ { 1 } , \gamma ^ { 2 } ) z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) } z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 2 } ) } d \pi _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) d \pi _ { \Lambda _ { n } } ( \gamma ^ { 2 } ) ,$$

where  ̃ ZΛn is a normalization factor.

Lemma 5.4 The first marginal (respectively the second marginal) distribution of  ̃ PΛn is PΛn (respectively QΛn ).

Proof By definition of  ̃ PΛn , its first marginal admits the following unnormalized density with respect to πΛn (dγ 1 )

$$f ( \gamma ^ { 1 } ) & = \int 1 _ { \mathcal { Z } } ( \gamma ^ { 1 } , \gamma ^ { 2 } ) z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) } z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 2 } ) } d \pi _ { \Lambda _ { n } } ( \gamma ^ { 2 } ) \\ & = e ^ { ( z - 1 ) \lambda ^ { d } ( \Lambda _ { n } ) } z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) } \int 1 _ { \mathcal { W } } ( \gamma ^ { 1 } , \gamma ^ { 2 } ) d \pi _ { \Lambda _ { n } } ^ { z } ( \gamma ^ { 2 } ) \\ & = e ^ { ( z - 1 ) \lambda ^ { d } ( \Lambda _ { n } ) } z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) } \left \{ \gamma _ { \Lambda _ { n } \wedge A _ { n } ^ { \circledast } } ^ { 1 } \right \} e ^ { - z \Area ( \Lambda _ { n } \cap L _ { R } ( \gamma ^ { 1 } ) ) } \\ \intertext { w i c h i s prop $ o r p o r t i o n a l $ t o t the density of P _ { \Lambda _ { n } } \colon A $ i s i m i l a r $ computation $ g r e s t h e $ a n d $ t h e $ m a $ s e $ }$$

which is proportional to the density of PΛn . A similar computation gives the same result for QΛn .

Now let us give a representation of the two type Widom-Rowlinson model via the random cluster model. The random cluster process RΛn is a point process on Λn distributed by

$$\frac { 1 } { \hat { z } _ { n } } z ^ { N _ { \Lambda _ { n } } ( \gamma ) } 2 ^ { N _ { c c } ^ { \Lambda _ { n } } ( \gamma ) } d \pi _ { \Lambda _ { n } } ( \gamma ) ,$$

where N Λn cc (γ ) is the number of connected components of LR/ 2 (γ ) which are completely included in Λn . Then we build two new point processes ˆ Γ 1 Λn and ˆ Γ 2 Λn by splitting randomly and uniformly the connected component of RΛn . Each connected component inside Λn is given to ˆ Γ 1 Λn or ˆ Γ 2 Λn with probability an half each. The connected components hitting Λ c n are given to ˆ Γ 2 Λn . Rigorously this construction is done by the following way. Let us consider (Ci(γ )) 1 ≤ i ≤ N Λn cc (γ ) the collection of connected components of LR/ 2 (γ ) inside Λn . Let (εi )i ≥ 1 be a sequence of independent Bernoulli random variables with parameter 1 / 2. The processes ˆ Γ 1 Λn and ˆ Γ 2 Λn are defined by

$$\hat { \Gamma } _ { \Lambda _ { n } } ^ { 1 } = \bigcup _ { 1 \leq i \leq N _ { c c } ^ { \Lambda _ { n } } ( R _ { \Lambda _ { n } } ) , \, \epsilon _ { i } = 1 } R _ { \Lambda _ { n } } \cap C _ { i } ( R _ { \Lambda _ { n } } ) \quad \text {and} \quad \hat { \Gamma } _ { \Lambda _ { n } } ^ { 2 } = R _ { \Lambda _ { n } } \langle \hat { \Gamma } _ { \Lambda _ { n } } ^ { 1 } .$$


<!-- p:221 -->


Lemma 5.5 The distribution of ( ˆ Γ 1 Λn , ˆ Γ 2 Λn ) is the two-type Widom-Rowlinson model with boundary condition b). In particular, ˆ Γ 1 Λn ∼ PΛn and ˆ Γ 2 Λn ∼ QΛn .

Proof For any bounded measurable test function f we have

$$\text {Lemma 5.5} \ \text {The distribution of } & \ \{ \hat { I } _ { \mathbf A _ { n } } ^ { 2 } , \hat { I } _ { \mathbf A _ { n } } ^ { 2 } \} \ \text {is the two-type Widdom-Rowlinson} \\ \text {model with boundary condition} \, b \colon & \, \text {in particular} \, \hat { I } _ { \mathbf A _ { n } } ^ { 1 } \sim P _ { \mathbf A _ { n } } \text { and } \hat { I } _ { \mathbf A _ { n } } \sim Q _ { \mathbf A _ { n } } . \\ \text {Proof for any bounded measurable test function } & \ f { \text {we have} } \\ & \ E ( f ( \hat { I } _ { \mathbf A _ { n } } ^ { 1 } , \hat { I } _ { \mathbf A _ { n } } ^ { 2 } ) ) \\ & = E \left [ \ f { \left ( \underbrace { \bigcup _ { 1 \leq i \leq N ^ { A _ { n } } _ { c c } ( R _ { A _ { n } } ) } , \epsilon _ { i } = 1 } _ { 1 \leq i \leq N ^ { A _ { n } } _ { c c } ( R _ { A _ { n } } ) } } \right ] \\ & = Q _ { \mathbf A _ { n } } \bigcap \left ( \underbrace { \bigcup _ { 1 \leq i \leq N ^ { A _ { n } } _ { c c } ( R _ { A _ { n } } ) } , \epsilon _ { i } = 1 } _ { 1 \leq i \leq N ^ { A _ { n } } _ { c c } ( R _ { A _ { n } } ) } } C _ { i } ( R _ { A _ { n } } ) ^ { c } \right ) \right ] \\ & = \frac { 1 } { \hat { Z } _ { n } } \int _ { \Omega _ { n } } \sum _ { \substack { \overline { Z } _ { n } ^ { A _ { n } } ( \mathbf Y ) = \overline { 2 N ^ { A _ { n } } _ { c c } ( \mathbf Y ) } } } \frac { 1 } { \frac { 1 } { 2 N ^ { A _ { n } } _ { c c } ( \mathbf Y ) } } \\ & = \frac { 1 } { \hat { Z } _ { n } } \int _ { ( \epsilon _ { i } ) \in \{ 0 , 1 \} ^ { \gamma } } ( \underbrace { \bigcup _ { x \in \mathbf Y , \, \epsilon _ { i } = 1 } } _ { x \in \mathbf Y , \, \epsilon _ { i } = 1 } ) z ^ { N _ { A _ { n } } ( \mathbf Y ) } d \pi _ { A _ { n } } ( \gamma ) \\ & = \frac { 1 } { \hat { Z } _ { n } } \int ( 1 _ { \mathcal { A } } / f ) \left ( \underbrace { \bigcup _ { ( x , \epsilon _ { i } ) \in \tilde { \gamma } , \, \epsilon _ { i } = 1 } } _ { ( ( x , \epsilon _ { i } ) \in \tilde { \gamma } , \, \epsilon _ { i } = 0 } } ( 2 z ) ^ { N _ { A _ { n } } ( \mathbf Y ) } d \tilde { \pi } _ { A _ { n } } ( \tilde { \gamma } ) \\ \text {where } & \tilde { \pi } _ { A _ { n } } , \, \text {is a marked Poisson point process on } A _ { n } \times \{ 0 , 1 \} . \, \text {It means that the points} \\ \text {are distributed by } & \pi _ { A _ { n } } , \, \text {and that each point } x \, \text {is marked independently by a Bernoulli} \\ \text {variable } & \epsilon _ { i } , \, \text {with parameter } 1 / 2 . \, \text {We obtain}$$

where  ̃ πΛn is a marked Poisson point process on Λn ×{ 0 , 1 } . It means that the points are distributed by πΛn and that each point x is marked independently by a Bernoulli variable εx with parameter 1 / 2. We obtain

$$\text {variable $\epsilon_{x}$ with parameter $1/2$. We obtain} \\ E ( f ( \hat { \Gamma } _ { \Lambda _ { n } } ^ { 1 } , \hat { \hat { \Gamma } } _ { \Lambda _ { n } } ^ { 2 } ) ) \\ = \frac { e ^ { | \Lambda _ { n } | } } { \hat { Z } _ { n } } \int ( \mathbf 1 _ { \mathcal { A } } f ) \left ( \bigcup _ { ( x , \epsilon _ { x } ) \in \bar { \gamma } , \, \epsilon _ { x } = 1 } \{ x \} , \quad \bigcup _ { ( x , \epsilon _ { x } ) \in \bar { \gamma } , \, \epsilon _ { x } = 0 } \{ x \} \right ) z ^ { N _ { \Lambda _ { n } } ( \gamma ) } d \tilde { \pi } _ { \Lambda _ { n } } ^ { 2 } ( \tilde { \gamma } ) \\ = \frac { e ^ { | \Lambda _ { n } | } } { \hat { Z } _ { n } } \int \int ( \mathbf 1 _ { \mathcal { A } } f ) \left ( \gamma ^ { 1 } , \gamma ^ { 2 } \right ) z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) } z ^ { N _ { \Lambda _ { n } } ( \gamma ^ { 2 } ) } d \pi _ { \Lambda _ { n } } ( \gamma ^ { 1 } ) d \pi _ { \Lambda _ { n } } ( \gamma ^ { 2 } ) , \\ \text {which proves the lemma.}$$

which proves the lemma.


<!-- p:222 -->


Note that the random cluster process RΛn is a finite volume GPP with energy function ˆ H = - N Λn cc , activity z and inverse temperature log ( 2 ) . Its local energy ˆ h is defined by

$$\hat { h } ( x , \gamma ) = N _ { c c } ^ { \Lambda _ { n } } ( \gamma ) - N _ { c c } ^ { \Lambda _ { n } } ( \gamma \cup \{ x \} ) .$$

Thanks to a geometrical argument, it is not difficult to note that ˆ h is uniformly bounded from above by a constant cd (depending only on the dimension d ). For instance, in the case d = 2, a ball with radius R/ 2 can overlap at most five disjoints balls with radius R/ 2 and therefore c 2 = 5 - 1 = 4 is suitable.

By Lemma 5.2, we deduce that the distribution of RΛn dominates the Poisson point distribution π 2 ze - c d Λn . So we choose

$$z > \frac { z _ { d } e ^ { c _ { d } } } { 2 R ^ { d } }$$

which implies that the Boolean model with intensity 2 ze - cd and radii R/ 2 percolates with probability one (see Proposition 5.13). For any γ ∈ C , we denote by C ∞ (γ ) the unbounded connected components in LR/ 2 (γ ) (if it exists) and we define by α the intensity of points in C ∞ (γ ) under the distribution π 2 ze - c d ;

$$\alpha \coloneqq \int N _ { [ 0 , 1 ] ^ { d } } \left ( \gamma \cap C _ { \infty } ( \gamma ) \right ) d \pi ^ { 2 z e ^ { - c _ { d } } } ( \gamma ) > 0 .$$

We are now in position to finish the proof of Theorem 5.5 by proving that the difference in intensities between  ̄ Q and  ̄ P is larger than α .

The local convergence topology τ L ensures that, for any local bounded function f , the evaluation P ↦→ ∫ fdP is continuous. Actually, the continuity of such evaluation holds for the larger class of functions f satisfying: (1) f is local on some bounded set Δ , (2) there exists A &gt; 0 such that | f(γ) | ≤ A( 1 + # (γ )) . In particular, the application P ↦→ i(P) := ∫ N [ 0 , 1 ] d (γ )P (dγ ) is continuous (see [25] for details). We deduce that

$$for details(). We deduce that \\ i ( \bar { Q } ) - i ( \bar { P } ) & = \int N _ { [ 0 , 1 ] ^ { d } } ( \gamma ) d \bar { Q } ( \gamma ) - \int N _ { [ 0 , 1 ] ^ { d } } ( \gamma ) d \bar { P } ( \gamma ) \\ & = \lim _ { n \to \infty } \left ( \int N _ { [ 0 , 1 ] ^ { d } } ( \gamma ) d \bar { Q } _ { \Lambda _ { n } } ( \gamma ) - \int N _ { [ 0 , 1 ] ^ { d } } ( \gamma ) d \bar { P } _ { \Lambda _ { n } } ( \gamma ) \right ) \\ & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } \left ( \int N _ { [ 0 , 1 ] ^ { d } } ( \tau _ { u } \gamma ) d Q _ { \Lambda _ { n } } ( \gamma ) \\ & - \int N _ { [ 0 , 1 ] ^ { d } } ( \tau _ { u } \gamma ) d P _ { \Lambda _ { n } } ( \gamma ) \right ) d u .$$


<!-- p:223 -->


By the representation of PΛn and Qλn given in Lemma 5.5, we find

$$i ( \bar { Q } ) - i ( \bar { P } ) & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } E \left ( N _ { [ 0 , 1 ] ^ { d } } ( \tau _ { u } \hat { \Gamma } _ { \Lambda _ { n } } ^ { 2 } ) - N _ { [ 0 , 1 ] ^ { d } } ( \tau _ { u } \hat { \Gamma } _ { \Lambda _ { n } } ^ { 1 } ) \right ) d u \\ & = \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } E \left ( N _ { \tau _ { u } [ 0 , 1 ] ^ { d } } ( R _ { \Lambda _ { n } } \cap C _ { b } ( R _ { \Lambda _ { n } } ) ) \right ) d u ,$$

where Cb(γ) are the connected components of LR/ 2 (γ ) hitting Λ c n . Since the distribution of RΛn dominates π 2 ze - c d Λn ,

$$i ( \bar { Q } ) - i ( \bar { P } ) & \geq \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { [ - n , n - 1 ] ^ { d } } \int N _ { \tau _ { u } [ 0 , 1 ] ^ { d } } \left ( \gamma \cap C ( \gamma ) _ { \infty } \right ) d \pi ^ { 2 z e ^ { - c ^ { d } } } _ { \Lambda _ { n } } ( \gamma ) d u , \\ & \geq \lim _ { n \to \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { [ - n , n - 1 ] ^ { d } } \alpha d u = \alpha > 0 . \\ \intertext { t h e o r m i s p r o w }$$

The theorem is proved.

### 5.4 Estimation of Parameters

In this section we investigate the parametric estimation of the activity z ∗ and the inverse temperature β ∗ of an infinite volume Gibbs point process Γ . As usual the star specifies that the parameters z ∗ , β ∗ are unknown whereas the variable z and β are used for the optimization procedures. Here the dataset is the observation of Γ trough the bounded window Λn = [- n, n ] d (i.e. the process ΓΛn ). The asymptotic means that the window Λn increases to the whole space R d (i.e. n goes to infinity) without changing the realization of Γ .

For sake of simplicity, we decide to treat only the case of two parameters (z, β) but it would be possible to consider energy functions depending on an extra parameter θ ∈ R p . The case where H depends linearly on θ can be treated exactly as z and β . For the non linear case the setting is much more complicated and each procedure has to be adapted. References are given in each section.

In all the section, we assume that the energy function H is stationary and has a finite range R &gt; 0. The existence of Γ is therefore guaranteed by Theorem 5.1. The procedures presented below are not affected by the uniqueness or non-uniqueness of the distribution of such GPP.

In Sect. 5.4.1, we start by presenting the natural maximum likelihood estimator. Afterwards, in Sect. 5.4.2, we introduce the general Takacs-Fiksel estimator which is a mean-square procedure based on the GNZ equations. The standard maximum pseudo-likelihood estimator is a particular case of such estimator and is presented in Sect. 5.4.3. An application to an unobservable issue is treated in Sect. 5.4.4. The last Sect. 5.4.5 is devoted to a new estimator based on a variational GNZ equation.


<!-- p:224 -->


5

#### 5.4.1 Maximum Likelihood Estimator

The natural method to estimate the parameters is the likelihood inference. However a practical issue is that the likelihood depends on the intractable partition function. In the case of sparse data, approximations were first proposed in [44], before simulation-based methods have been developed [26]. Here, we treat only the theoretical aspects of the MLE and these practical issues are not investigated.

Definition 5.9 The maximum likelihood estimator of (z ∗ , β ∗ ) is given for any n ≥ 1 by

$$( \hat { z } _ { n } , \hat { \beta } _ { n } ) = \arg \max _ { z > 0 , \beta \geq 0 } \frac { 1 } { Z _ { \Lambda _ { n } } ^ { z , \beta } } z ^ { N _ { \Lambda _ { n } } ( \Gamma ) } e ^ { - \beta H ( \Gamma _ { \Lambda _ { n } } ) } .$$

Note that the argmax is not necessarily unique and that the boundary effects are not considered in this version of MLE. Other choices could be considered.

In this section we show the consistency of such estimators. The next natural question concerns the asymptotic distribution of the MLE but this problem is more arduous and is still partially unsolved today. Indeed, Mase [35] and Jensen [29] proved that the MLE is asymptotically normal when the parameters z and β are small enough. Without these conditions, phase transition may occur and some longrange dependence phenomenon can appear. The MLE might then exhibit a non standard asymptotic behavior, in the sense that the rate of convergence might differ from the standard square root of the size of the window and the limiting law might be non-Gaussian.

The next theorem is based on a preprint by S. Mase (Asymptotic properties of MLEsofGibbs models on Rd, 2002, unpublished preprint). See also [15] for general results on consistency.

Theorem 5.6 We assume that the energy function H is stationary, finite range and not almost surely constant (i.e. there exists a subset Λ ⊂ R d such that H(γΛ) is not πΛ(dγΛ) almost surely constant). We assume also that the mean energy exists for any stationary probability measure P (i.e. the limit (5.25) exists) and that the boundary effects assumption (5.26) holds. Moreover we assume that for any ergodic Gibbs measure P , the following limit holds for P -almost every γ

$$\lim _ { n \mapsto \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } H ( \gamma _ { \Lambda _ { n } } ) = H ( P ) .$$

Then, almost surely the parameters ( ˆ zn, ˆ βn) converge to (z ∗ , β ∗ ) when n goes to infinity.

Proof Let us assume that the Gibbs distribution P of Γ is ergodic. Otherwise P can be represented as a mixture of ergodic stationary Gibbs measures (see [46, Theorem 2.2 and 4.1]). Therefore the proof of the consistency of the MLE reduces to the case when P is ergodic, which is assumed henceforth.


<!-- p:225 -->


Let us consider the log-likelihood contrast function

$$K _ { n } ( \theta , \beta ) = - \log ( Z _ { \Lambda _ { n } } ^ { e ^ { - \theta } , \beta } ) - \theta N _ { \Lambda _ { n } } ( \Gamma ) - \beta H ( \Gamma _ { \Lambda _ { n } } )$$

related to the parametrization θ = - log (z) . It is clear that ( ˆ zn, ˆ βn) = (e -  ̃ θn ,  ̃ βn) where (  ̃ θn,  ̃ βn) is the argmax of (θ, β) ↦→ Kn(θ,β) . So it is sufficient to show that (  ̃ θn,  ̃ βn) converges almost surely to ( - log (z ∗ ), β ∗ ) . The limit (5.24), the ergodic Theorem and the assumption (5.36) imply the existence of the following limit contrast function

$$K ( \theta , \beta ) \colon = - p ^ { e ^ { - \theta } , \beta } - \theta E _ { P } ( N _ { [ 0 , 1 ] ^ { d } } ( \Gamma ) ) - \beta H ( P ) = \lim _ { n \to \infty } \frac { K _ { n } ( \theta , \beta ) } { \lambda ^ { d } ( \Lambda _ { n } ) } .$$

The variational principle (Theorem 5.3) ensures that (θ, β) ↦→ K(θ,β) is lower than I 1 (P) with equality if and only if P is a Gibbs measure with energy function H , activity z and inverse temperature β . Since H is not almost surely constant, it is easy to see that two Gibbs measures with different parameters z, β are different (this fact can be viewed used the DLR equations in a very large box Λ ). Therefore K(θ,β) is maximal, equal to I 1 (P) , if and only if (θ, β) = (θ ∗ , β ∗ ) .

Therefore it remains to prove that the maximizers of (θ, β) ↦→ Kn(θ,β) converge to the unique maximizer of (θ, β) ↦→ K(θ,β) . First note that the functions Kn are concave. Indeed, the Hessian of Kn is negative since

$$\frac { \partial ^ { 2 } K _ { n } ( \theta , \beta ) } { \partial ^ { 2 } \theta } = - \text {Var} _ { P _ { \Lambda _ { n } } ^ { e ^ { - \theta } , \beta } } ( N _ { \Lambda _ { n } } ) , \quad \frac { \partial ^ { 2 } K _ { n } ( \theta , \beta ) } { \partial ^ { 2 } \beta } = - \text {Var} _ { P _ { \Lambda _ { n } } ^ { e ^ { - \theta } , \beta } } ( H )$$

and

$$\frac { \partial ^ { 2 } K _ { n } ( \theta , \beta ) } { \partial \theta \partial \beta } = - C o v _ { P _ { \Lambda _ { n } } ^ { e ^ { - \theta } , \beta } } ( N _ { \Lambda _ { n } } , H ) .$$

The convergence result for the argmax follows since the function (θ, β) ↦→ K(θ,β) is necessarily strictly concave at (θ ∗ , β ∗ ) because K(θ,β) is maximal uniquely at (θ ∗ , β ∗ ) .

Let us finish this section with a discussion on the extra assumption (5.36) which claims that the empirical mean energy converges to the expected value energy. This assumption is in general proved via the ergodic theorem or a law of large numbers. In the case of the Area energy function H defined in (5.4), it is a direct consequence of a decomposition as in (5.28) and the ergodic Theorem. In the case of pairwise interaction, the verification follows essentially the proof of Proposition 5.12.


<!-- p:226 -->


5

#### 5.4.2 Takacs-Fiksel Estimator

In this section we present an estimator introduced in the eighties by Takacs and Fiksel [19, 49]. It is based on the GNZ equations presented in Sect. 5.3.5. Let us start by explaining briefly the procedure. Let f be a test function from R d × C to R . We define the following quantity for any z &gt; 0, β &gt; 0 and γ ∈ C

$$C _ { \Lambda _ { n } } ^ { z , \beta } ( f , \gamma ) = \sum _ { x \in \gamma A _ { n } } f ( x , \gamma \langle \{ x \} ) - z \int _ { \Lambda _ { n } } e ^ { - \beta h ( x , \gamma ) } f ( x , \gamma ) d x .$$

By the GNZ equation (5.22) we obtain

$$E \left ( C _ { \Lambda _ { n } } ^ { z ^ { * } , \beta ^ { * } } ( f , \Gamma ) \right ) = 0$$

where Γ is a GPP with parameter z ∗ and β ∗ . Thanks to the ergodic Theorem it follows that for n large enough

$$\frac { C _ { \Lambda _ { n } } ^ { z ^ { * } , \beta ^ { * } } ( f , \Gamma ) } { \lambda ^ { d } ( \Lambda _ { n } ) } \approx 0 .$$

Then the Takacs-Fiksel estimator is defined as a mean-square method based on functions C z ∗ ,β ∗ Λn (fk, Γ ) for a collection of test functions (fk) 1 ≤ k ≤ K .

Definition 5.10 Let K ≥ 2 be an integer and (fk) 1 ≤ k ≤ K a family of K functions from R d × C to R . The Takacs-Fiksel estimator ( ˆ zn, ˆ βn) of (z ∗ , β ∗ ) is defined by

$$( \hat { z } _ { n } , \hat { \beta } _ { n } ) = \arg \min _ { ( z , \beta ) \in \mathcal { D } } \sum _ { k = 1 } ^ { K } \left ( C _ { \Lambda _ { n } } ^ { z , \beta } ( f _ { k } , \Gamma ) \right ) ^ { 2 } ,$$

where D ⊂ ( 0 , +∞ ) ×[ 0 , +∞ ) is a bounded domain containing (z ∗ , β ∗ ) .

In opposition to the MLE procedure, the contrast function does not depend on the partition function. This estimator is explicit except for the computation of integrals and the optimization procedure. In [9] the Takacs-Fiksel procedure is presented in a more general setting including the case where the functions fk depend on parameters z and β . This generalization may lead to a simpler procedure in choosing fk such that the integral term in (5.37) is explicitly computable.

In the rest of the section, we prove the consistency of the estimator. General results on consistency and asymptotic normality are developed in [9].

Theorem 5.7 (Consistency) We make the following integrability assumption: for any 1 ≤ k ≤ K

$$E \left ( | f _ { k } ( 0 , \Gamma ) | ( 1 + | h ( 0 , \Gamma ) | ) \sup _ { ( z , \beta ) \in \mathcal { D } } e ^ { - \beta h ( 0 , \Gamma ) } \right ) < + \infty .$$


<!-- p:227 -->


We assume also the following identifiability condition: the equality

$$\sum _ { k = 1 } ^ { K } E \left ( f _ { k } ( 0 , \Gamma ) \left ( z e ^ { - \beta h ( 0 , \Gamma ) } - z ^ { * } e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) \right ) ^ { 2 } = 0$$

holds if and only (z, β) = (z ∗ , β ∗ ) . Then the Takacs-Fiksel estimator ( ˆ zn, ˆ βn) presented in Definition 5.10 converges almost surely to (z ∗ , β ∗ ) .

Proof As in the proof of Theorem 5.6, without loss of generality, we assume that the Gibbs distribution of Γ is ergodic. Therefore, thanks to the ergodic Theorem, almost surely for any 1 ≤ k ≤ K

$$\lim _ { n \mapsto \infty } \frac { C _ { \Lambda _ { n } } ^ { z , \beta } ( f _ { k } , \Gamma ) } { \lambda ^ { d } ( \Lambda _ { n } ) } & = E \left [ \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } f _ { k } ( x , \Gamma \wedge x ) \right ] \\ & - z E \left [ \int _ { [ 0 , 1 ] ^ { d } } e ^ { - \beta h ( x , \Gamma ) } f _ { k } ( x , \Gamma ) d x \right ] . \\ \intertext { B y t h e G N Z e q uation ( 5 . 2 2 ) }$$

By the GNZ equation (5.22)

$$E \left [ \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } f _ { k } ( x , \Gamma \langle x \rangle ) \right ] = z ^ { * } E \left [ \int _ { [ 0 , 1 ] ^ { d } } e ^ { - \beta ^ { * } h ( x , \Gamma ) } f _ { k } ( x , \Gamma ) d x \right ] .$$

Using the stationarity and compiling (5.40) and (5.41), we obtain that the contrast function

$$K _ { n } ( z , \beta ) = \sum _ { k = 1 } ^ { K } \left ( \frac { C _ { \Lambda _ { n } } ^ { z , \beta } ( f _ { k } , \Gamma ) } { \lambda ^ { d } ( \Lambda _ { n } ) } \right ) ^ { 2 } \\$$

admits almost surely the limit

$$\lim _ { n \mapsto \infty } K _ { n } ( z , \beta ) = K ( z , \beta ) \colon = \sum _ { k = 1 } ^ { K } E \left ( f _ { k } ( 0 , \Gamma ) \left ( z e ^ { - \beta h ( 0 , \Gamma ) } - z ^ { * } e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) \right ) ^ { 2 } ,$$

which is null if and only if (z, β) = (z ∗ , β ∗ ) . Therefore it remains to prove that the minimizers of the contrast function converge to the minimizer of the limit contrast function. In the previous section we solved a similar issue for the MLE procedure using the convexity of contrast functions. This argument does not work here and we need more sophisticated tools.


<!-- p:228 -->


We define by Wn(.) the modulus of continuity of the contrast function Kn ; let η be a positive real

$$W _ { n } ( \eta ) = \sup \left \{ | K _ { n } ( z , \beta ) - K _ { n } ( z ^ { \prime } , \beta ^ { \prime } ) | , \\ & \quad \text {with } ( z , \beta ) , ( z ^ { \prime } , \beta ^ { \prime } ) \in \mathcal { D } , \ \| ( z - z ^ { \prime } , \beta - \beta ^ { \prime } ) \| \leq \eta \right \} .$$

Lemma 5.6 (Theorem 3.4.3 [27]) Assuming that there exists a sequence (εl ) l ≥ 1 , which goes to zero when l goes to infinity, such that for any l ≥ 1

$$P \left ( \lim s u p \left \{ W _ { n } \left ( \frac { 1 } { l } \right ) \geq \epsilon _ { l } \right \} \right ) = 0$$

then almost surely the minimizers of (z, β) ↦→ Kn(z, β) converges to the minimizer of (z, β) ↦→ K(z,β) .

Let us show that the assertion (5.42) holds. Thanks to equalities (5.40), (5.41) and assumption (5.38), there exists a constant C 1 such that for n large enough, any 1 ≤ k ≤ K and any (z, β) ∈ D

$$\frac { | C _ { \Lambda _ { n } } ^ { z , \beta } ( f _ { k } , \Gamma ) | } { \lambda ^ { d } ( \Lambda _ { n } ) } \leq C _ { 1 } .$$

We deduce that for n large enough

$$We deduce that for n \, large enough \\ | K _ { n } ( z , \beta ) - K _ { n } ( z ^ { \prime } , \beta ^ { \prime } ) | \\ \leq \frac { C _ { 1 } } { \lambda ^ { d } ( \Lambda _ { n } ) } \sum _ { k = 1 } ^ { K } \int _ { \Lambda _ { n } } | f _ { k } ( x , \Gamma ) | \left | z e ^ { - \beta h ( x , \Gamma ) } - z ^ { \prime } e ^ { - \beta ^ { \prime } h ( x , \Gamma ) } \right | d x \\ \leq \frac { C _ { 1 } | \beta - \beta ^ { \prime } | } { \lambda ^ { d } ( \Lambda _ { n } ) } \max _ { 1 \leq k \leq K } \int _ { \Lambda _ { n } } | f _ { k } ( x , \Gamma ) h ( x , \Gamma ) | \sup _ { ( z , \beta ^ { \prime \prime } ) \in \mathcal { D } } z e ^ { - \beta ^ { \prime \prime } h ( x , \Gamma ) } d x \\ + \frac { C _ { 1 } | z - z ^ { \prime } | } { \lambda ^ { d } ( \Lambda _ { n } ) } \max _ { 1 \leq k \leq K } \int _ { \Lambda _ { n } } | f _ { k } ( x , \Gamma ) | \sup _ { ( z , \beta ^ { \prime \prime } ) \in \mathcal { D } } e ^ { - \beta ^ { \prime \prime } h ( x , \Gamma ) } d x . \\ \\ \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h s c r { D } } \quad \intertext { B r y h$$

By the ergodic Theorem, the following convergences hold almost surely

$$& \lim _ { n \mapsto + \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } | f _ { k } ( x , \Gamma ) h ( x , \Gamma ) | \sup _ { ( z , \beta ^ { \prime \prime } ) \in \mathcal { D } } z e ^ { - \beta ^ { \prime \prime } h ( x , \Gamma ) } d x \\ & = E \left ( | f _ { k } ( 0 , \Gamma ) h ( 0 , \Gamma ) | \sup _ { ( z , \beta ^ { \prime \prime } ) \in \mathcal { D } } z e ^ { - \beta ^ { \prime \prime } h ( 0 , \Gamma ) } \right ) < + \infty ,$$


<!-- p:229 -->


and

$$& \lim _ { n \mapsto + \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \int _ { \Lambda _ { n } } | f _ { k } ( x , \Gamma ) | \sup _ { ( z , \beta ^ { \prime \prime } ) \in \mathcal { D } } e ^ { - \beta ^ { \prime \prime } h ( x , \Gamma ) } d x \\ & = E \left ( | f _ { k } ( 0 , \Gamma ) | \sup _ { ( z , \beta ^ { \prime \prime } ) \in \mathcal { D } } e ^ { - \beta ^ { \prime \prime } h ( 0 , \Gamma ) } \right ) < + \infty . \\$$

This implies the existence of a constant C 2 &gt; 0 such that for n large enough, any 1 ≤ k ≤ K and any (z, β) ∈ D

$$| K _ { n } ( z , \beta ) - K _ { n } ( z ^ { \prime } , \beta ^ { \prime } ) | < C _ { 2 } \| ( z - z ^ { \prime } , \beta - \beta ^ { \prime } ) \| .$$

The assumption (5.42) occurs with the sequence εl = C 2 /l and Theorem 5.7 is proved.

Remark 5.1 (On the Integrability Assumption) The integrability assumption (5.38) is sometimes difficult to check, especially when the local energy h( 0 , γ ) is not bounded from below. For instance in the setting of pairwise energy function H defined in (5.1) with a pair potential φ having negative values, Ruelle estimates (5.16) are very useful. Indeed, by stability of the energy function, the potential φ is necessary bounded from below by 2 A and therefore

$$E \left ( e ^ { - \beta h ( 0 , \Gamma ) } \right ) < E \left ( e ^ { - 2 A \beta N _ { B ( 0 , R ) } ( \Gamma ) } \right ) < + \infty ,$$

where R is the range of the interaction.

Remark 5.2 (On the Identifiability Assumption) In the identifiability assumption (5.39), the sum is null if and only if each term is null. Assuming that the functions are regular enough, each term is null as soon as (z, β) belongs to a 1-dimensional manifold embedded in R 2 containing (z ∗ , β ∗ ) . Therefore, assumption (5.39) claims that (z ∗ , β ∗ ) is the unique element of these K manifolds. If K ≤ 2, there is no special geometric argument to ensure that K 1-dimensional manifolds in R 2 have an unique intersection point. For this reason, it is recommended to choose K ≥ 3. See Section 5 in [9] for more details and complements on this identifiability assumption.

#### 5.4.3 Maximum Pseudo-Likelihood Estimator

In this section we present the maximum pseudo-likelihood estimator, which is a particular case of the Takacs-Fiksel estimator. This procedure has been first introduced by Besag in [5] and popularized by Jensen and Moller in [31] and Baddeley and Turner in [2].


<!-- p:230 -->


5

Definition 5.11 The maximum pseudo-likelihood estimator ( ˆ zn, ˆ βn) is defined as a Takacs-Fiksel estimator (see Definition 5.10) with K = 2, f 1 (x, γ ) = 1 and f 2 (x, γ ) = h(x, γ ) .

This particular choice of functions f 1, f 2 simplifies the identifiability assumption (5.39). The following theorem is an adaptation of Theorem 5.7 in the present setting of MPLE. The asymptotic normality is investigated first in [30] (see also [6] for more general results).

####### Theorem 5.8 (Consistency) Assuming

$$E \left ( ( 1 + h ( 0 , \Gamma ) ^ { 2 } ) \sup _ { ( z , \beta ) \in \mathcal { D } } e ^ { - \beta h ( 0 , \Gamma ) } \right ) < + \infty$$

$$P \left ( h ( 0 , T ) = h ( 0 , \emptyset ) \right ) < 1 ,$$

then the maximum pseudo-likelihood estimator ( ˆ zn, ˆ βn) converges almost surely to (z ∗ , β ∗ ) .

Proof Let us check the assumptions of Theorem 5.7. Clearly, the integrability assumption (5.44) ensures the integrability assumptions (5.38) with f 1 = 1 and f 2 = h . So it remains to show that assumption (5.45) implies the identifiability assumption (5.39). Consider the parametrization z = e - θ and ψ the function

$$\psi ( \theta , \beta ) = E \left ( e ^ { - \theta ^ { * } - \beta ^ { * } h ( 0 , \Gamma ) } ( e ^ { U } - U - 1 ) \right ) ,$$

$$U = \beta ^ { * } h ( 0 , \Gamma ) + \theta ^ { * } - \beta h ( 0 , \Gamma ) - \theta .$$

The function ψ is convex, non negative and equal to zero if and only if U is almost surely equal to zero. By assumption (5.45) this fact occurs when (z, β) = (z ∗ , β ∗ ) . Therefore the gradient ∇ ψ = 0 if and only (z, β) = (z ∗ , β ∗ ) . Noting that

$$\frac { \partial \psi ( \theta , \beta ) } { \partial \theta } = E \left ( z ^ { * } e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } - z e ^ { - \beta h ( 0 , \Gamma ) } \right )$$

and

with

and

$$\frac { \partial \psi ( \theta , \beta ) } { \partial \beta } = E \left ( h ( 0 , \Gamma ) \left ( z ^ { * } e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } - z e ^ { - \beta h ( 0 , \Gamma ) } \right ) \right ) ,$$

the identification assumption (5.39) holds. The theorem is proved.


<!-- p:231 -->


#### 5.4.4 Solving an Unobservable Issue

In this section we give an application of the Takacs-Fiksel procedure in a setting of partially observable dataset. Let us consider a Gibbs point process Γ for which we observe only LR(Γ ) in place of Γ . This setting appears when Gibbs point processes are used for producing random surfaces via germ-grain structures (see [41] for instance). Applications for modelling micro-structure in materials or microemulsion in statistical physics are developed in [8].

The goal is to furnish an estimator of z ∗ and β ∗ in spite of this unobservable issue. Note that the number of points (or balls) is not observable from LR(Γ ) and therefore the MLE procedure is not achievable, since the likelihood is not computable. When β is known and fixed to zero, it corresponds to the estimation of the intensity of the Boolean model from its germ-grain structure (see [39] for instance).

In the following we assume that Γ a Gibbs point process for the Area energy function defined in (5.4), the activity z ∗ and the inverse temperature β ∗ . This choice is natural since the energy function depends on the observations LR(Γ ) . The more general setting of Quermass interaction is presented in [17] but for sake of simplicity, we treat only here the simpler case of Area interaction.

We opt for a Takacs-Fiksel estimator but the main problem is that the function

$$C _ { \Lambda _ { n } } ^ { z , \beta } ( f , \gamma ) = \sum _ { x \in \gamma \Lambda _ { n } } f ( x , \gamma \langle \{ x \} ) - z \int _ { \Lambda _ { n } } e ^ { - \beta h ( x , \gamma ) } f ( x , \gamma ) d x ,$$

which appears in the procedure, is not computable since the positions of points are not observable. The main idea is to choose the function f properly such that the sum is observable although each term of the sum is not. To this end, we define

$$f _ { 1 } ( x , \gamma ) = \text {Surface} \left ( \partial B ( x , R ) \cap L _ { R } ^ { c } ( \gamma ) \right )$$

$$f _ { 2 } ( x , \gamma ) = 1 _ { \{ B ( x , R ) \cap L _ { R } ( \gamma ) = \emptyset \} } ,$$

where ∂B(x,R) is the boundary of the ball B(x,R) (i.e. the sphere S(x, R) ) and the 'Surface' means the (d - 1 ) -dimensional Hausdorff measure in R d . Clearly the function f 1 gives the surface of the portion of the sphere S(x, R) outside the germ-grain structure LR(γ) . The function f 2 indicates if the ball B(x,R) hits the germ-grain structure LR(γ) . Therefore we obtain that

$$\sum _ { x \in \gamma _ { \Lambda _ { n } } } f _ { 1 } ( x , \gamma \langle \{ x \} ) = S u r f a c e \left ( \partial L _ { R } ( \gamma _ { \Lambda _ { n } } ) \right )$$

and


<!-- p:232 -->


5

and

$$\sum _ { x \in \gamma _ { \Lambda _ { n } } } f _ { 2 } ( x , \gamma \langle \{ x \} ) = N _ { i s o } \left ( L _ { R } ( \gamma _ { \Lambda _ { n } } ) \right ) ,$$

where N iso (LR(γΛn )) is the number of isolated balls in the germ-grain structure LR(γΛn ) . Let us note that these quantities are not exactly observable since, in practice, we observe LR(γ) ∩ Λn rather than LR(γΛn ) . However, if we omit this boundary effect, the values C z,β Λn (f 1 , Γ ) and C z,β Λn (f 2 , Γ ) are observable and the Takacs-Fiksel procedure is achievable. The consistency of the estimator is guaranteed by Theorem 5.7. The integrability assumption (5.38) is trivially satisfied since the functions f 1, f 2 and h are uniformly bounded. The verification of the identifiability assumption (5.39) is more delicate and we refer to [9], example 2 for a proof. Numerical estimations on simulated and real datasets can be found in [17].

#### 5.4.5 A Variational Estimator

In this last section, we present a new estimator based on a variational GNZ equation which is a mix between the standard GNZ equation and an integration by parts formula. This equation has been first introduced in [11] for statistical mechanics issues and used recently in [1] for spatial statistic considerations. In the following, we present first this variational equation and afterwards we introduce its associated estimator of β ∗ . The estimation of z ∗ is not considered here.

Theorem 5.9 Let Γ be a GPP for the energy function H , the activity z and the inverse temperature β . We assume that, for any γ ∈ C , the function x ↦→ h(x, γ ) is differentiable on R d \ γ . Let f be a function from R d × C to R which is differentiable and with compact support with respect to the first variable. Moreover we assume the integrability of both terms below. Then

$$E \left ( \sum _ { x \in \Gamma } \nabla _ { x } f ( x , \Gamma \langle x \rangle ) \right ) = \beta E \left ( \sum _ { x \in \Gamma } f ( x , \Gamma \langle x \rangle ) \nabla _ { x } h ( x , \Gamma \langle x \rangle ) \right ) .$$

Proof By the standard GNZ equation (5.22) applied to the function ∇ x f , we obtain

$$E \left ( \sum _ { x \in \Gamma } \nabla _ { x } f ( x , \Gamma \langle x \rangle ) \right ) & = z E \left ( \int _ { \mathbb { R } ^ { d } } e ^ { - \beta h ( x , \Gamma ) } \nabla _ { x } f ( x , \Gamma ) d x \right ) . \\$$

By a standard integration by part formula with respect to the first variable x , we find that

$$E \left ( \sum _ { x \in \Gamma } \nabla _ { x } f ( x , \Gamma \langle \{ x \} ) \right ) = z \beta E \left ( \int _ { \mathbb { R } ^ { d } } \nabla _ { x } h ( x , \Gamma ) e ^ { - \beta h ( x , \Gamma ) } f ( x , \Gamma ) d x \right ) .$$


<!-- p:233 -->


Using again the GNZ equation we finally obtain (5.46).

Note that Eq. (5.46) is a vectorial equation. For convenience it is possible to obtain a real equation by summing each coordinate of the vectorial equation. The gradient operator is simply replaced by the divergence operator.

Remark 5.3 (On the Activity Parameter z ) The parameter z does not appear in the variational GNZ equation (5.46). Therefore these equations do not characterize the Gibbs measures as in Proposition 5.5. Actually these variational GNZ equations characterize the mixing of Gibbs measures with random activity (See [11] for details).

Let us now explain how to estimate β ∗ from these variational equations. When the observation window Λn is large enough we identify the expectations of sums in (5.46) by the sums. Then the estimator of β ∗ is simply defined by

$$\hat { \beta } _ { n } = \frac { \sum _ { x \in \Gamma _ { \Lambda _ { n } } } \text {div} _ { \Lambda _ { n } } f ( x , \Gamma \langle \{ x \} ) } { \sum _ { x \in \Gamma _ { \Lambda _ { n } } } f ( x , \Gamma \langle \{ x \} ) \text {div} _ { x } h ( x , \Gamma \langle \{ x \} ) } .$$

Note that this estimator is very simple and quick to compute in comparison to the MLE, MPLE or the general Takacs-Fiksel estimators. Indeed, in (5.47), there are only elementary operations (no optimization procedure, no integral to compute).

Let us now finish this section with a consistency result. More general results for consistency, asymptotic normality and practical estimations are available in [1].

Theorem 5.10 Let Γ be a GPP for a stationary and finite range energy function H , activity z ∗ and inverse temperature β ∗ . We assume that, for any γ ∈ C , the function x ↦→ h(x, γ ) is differentiable on R d \ γ . Let f be a stationary function from R d × C to R , differentiable with respect to the first variable and such that

$$E \left ( ( | f ( 0 , \Gamma | + | \nabla _ { x } f ( 0 , \Gamma ) | + | f ( 0 , \Gamma ) \nabla _ { x } h ( 0 , \Gamma ) | ) e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) < + \infty$$

and

$$E \left ( f ( 0 , \Gamma ) d i v _ { x } h ( 0 , \Gamma ) e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) \neq 0 .$$

Then the estimator ˆ βn converges almost surely to β ∗ .

Proof As usual, without loss of generality, we assume that the Gibbs distribution of Γ is ergodic. Then by the ergodic theorem the following limits both hold almost surely

$$\lim _ { n \mapsto + \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \sum _ { x \in \Gamma _ { \Lambda _ { n } } } \, d i v _ { x } f ( x , \Gamma \langle \{ x \} ) = E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] } ^ { d } } d i v _ { x } f ( x , \Gamma \langle \{ x \} ) \right ) _ { \substack { ( 5 . 5 0 ) } }$$


<!-- p:234 -->


and

$$& \lim _ { n \mapsto + \infty } \frac { 1 } { \lambda ^ { d } ( \Lambda _ { n } ) } \sum _ { x \in \Gamma _ { \Lambda _ { n } } } f ( x , \Gamma \langle x \rangle ) d i v _ { x } h ( x , \Gamma \langle x \rangle ) \\ & = E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } f ( x , \Gamma \langle x \rangle ) d i v _ { x } h ( x , \Gamma \langle x \rangle ) \right ) . \\ \intertext { t h o b e t h e x p a t i o n s i n g } \intertext { t h o b e t h e x p a t i o n s i n g }$$

Note that both expectations in (5.50) and (5.51) are finite since by the GNZ equations, the stationarity and assumption (5.48)

$$E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] } ^ { d } } | d i v f ( x , \Gamma \langle \{ x \} ) | \right ) = E \left ( | d i v f ( 0 , \Gamma ) | e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) < + \infty$$

and

$$E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } | f ( x , \Gamma \langle \{ x \} ) \text {div} h ( x , \Gamma \langle \{ x \} ) | \right ) & = E \left ( | f ( 0 , \Gamma ) \text {div} h ( 0 , \Gamma ) | e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) \\ & < + \infty .$$

We deduce that almost surely

$$\lim _ { n \to + \infty } \hat { \beta } _ { n } = \frac { E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } \text {div} f ( x , \Gamma \{ \{ x \} ) \right ) } { E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } f ( x , \Gamma \{ \{ x \} ) \text {div} h ( x , \Gamma \{ \{ x \} ) \right ) } , \\ \intertext { h o r o t h o n i m p e r i o n $ i $ o n t u l p h o n k s t o o s u m p e r i o n }$$

where the denominator is not null thanks to assumption (5.49). Therefore it remains to prove the following variational GNZ equation

$$E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } \nabla _ { x } f ( x , \Gamma \langle \{ x \} ) \right ) = \beta ^ { * } E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } f ( x , \Gamma \langle \{ x \} ) \nabla _ { x } h ( x , \Gamma \langle \{ x \} ) \right ) .$$

Note that this equation is not a direct consequence of the variational GNZ equation (5.46) since the function x ↦→ f(x, γ ) does not have a compact support. We need the following cut-off approximation. Let us consider (ψn)n ≥ 1 any sequence of functions from R d to R such that ψn is differentiable, equal to 1 on Λn , 0 on Λ c n + 1 and such that |∇ ψn | and | ψn | are uniformly bounded by a constant C (which does not depend on n ). It is not difficult to build such a sequence of functions. Let us now apply the variational GNZ equation (5.46) to the function (x, γ ) ↦→ ψn(x)f(x,γ) , we obtain


<!-- p:235 -->


$$E \left ( \sum _ { x \in \Gamma } \psi _ { n } ( x ) \nabla _ { x } f ( x , \Gamma \langle \{ x \} ) \right ) & + E \left ( \sum _ { x \in \Gamma } \nabla _ { x } \psi _ { n } ( x ) f ( x , \Gamma \langle \{ x \} ) \right ) \\ & = \beta ^ { * } E \left ( \sum _ { x \in \Gamma } \psi _ { n } ( x ) f ( x , \Gamma \langle \{ x \} ) \nabla _ { x } h ( x , \Gamma \langle \{ x \} ) \right ) . \\ \intertext { T h a n k s to the G i N Z equation and the stationary we get }$$

Thanks to the GNZ equation and the stationarity we get

$$\left | E \left ( \sum _ { x \in \Gamma } \psi _ { n } ( x ) \nabla _ { x } f ( x , \Gamma \langle \{ x \} ) \right ) - \lambda ^ { d } ( \Lambda _ { n } ) E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } \nabla _ { x } f ( x , \Gamma \langle \{ x \} ) \right ) \right | \\ \leq C z ^ { * } \lambda ^ { d } ( \Lambda _ { n + 1 } \lambda ) E \left ( | \nabla _ { x } f ( 0 , \Gamma ) | e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) , \\$$

and

$$\text {end} \\ \left | E \left ( \sum _ { x \in \Gamma } \psi _ { n } ( x ) f ( x , \Gamma \langle \{ x \} ) \nabla _ { x } h ( x , \Gamma \langle \{ x \} ) \right ) \right | \\ - \lambda ^ { d } ( \Lambda _ { n } ) E \left ( \sum _ { x \in \Gamma _ { [ 0 , 1 ] ^ { d } } } f ( x , \Gamma \langle \{ x \} ) \nabla _ { x } h ( x , \Gamma \langle \{ x \} ) \right ) \right | \\ \leq C z ^ { * } \lambda ^ { d } ( \Lambda _ { n + 1 } \langle \Lambda _ { n } ) E \left ( | f ( 0 , \Gamma ) \nabla _ { x } h ( 0 , \Gamma ) | e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) , \\ \text {end}$$

and finally

$$\left | E \left ( \sum _ { x \in \Gamma } \nabla _ { x } \psi _ { n } ( x ) f ( x , \Gamma \langle \{ x \} ) \right ) \right | & \leq C z ^ { * } \lambda ^ { d } ( \Lambda _ { n + 1 } \Lambda _ { n } ) E \left ( | f ( 0 , \Gamma ) | e ^ { - \beta ^ { * } h ( 0 , \Gamma ) } \right ) . \\ \text {There, dividing Eq. (5.53) by \lambda^{d} ( \Lambda_{n}), using the previous approximations and}$$

Therefore, dividing Eq. (5.53) by λ d (Λn) , using the previous approximations and letting n go to infinity, we find exactly the variational equation (5.52). The theorem is proved.

Acknowledgements The author thanks P. Houdebert, A. Zass and the anonymous referees for the careful reading and the interesting comments. This work was supported in part by the Labex CEMPI(ANR-11-LABX-0007-01), the CNRS GdR 3477 GeoSto and the ANR project PPP (ANR16-CE40-0016).


<!-- p:236 -->


### References

1. A. Baddeley, D. Dereudre, Variational estimators for the parameters of Gibbs point process models. Bernoulli 19 (3), 905-930 (2013)
2. A. Baddeley, R. Turner, Practical maximum pseudolikelihood for spatial point patterns (with discussion). Aust. N. Z. J. Stat. 42 (3), 283-322 (2000)
3. A.J. Baddeley, M.N.M. van Lieshout, Area-interaction point processes. Ann. Inst. Stat. Math. 47 (4), 601-619 (1995)
4. A. Baddeley, P. Gregori, J. Mateu, R. Stoica, D. Stoyan, Case Studies in Spatial Point Process Models . Lecture Notes in Statistics, vol. 185 (Springer, New York, 2005)
5. J. Besag, Spatial interaction and the statistical analysis of lattice systems. J. R. Stat. Soc. Ser. B 36 , 192-236 (1974). With discussion by D. R. Cox, A. G. Hawkes, P. Clifford, P. Whittle, K. Ord, R. Mead, J. M. Hammersley, and M. S. Bartlett and with a reply by the author
6. J.-M. Billiot, J.-F. Coeurjolly, R. Drouilhet, Maximum pseudolikelihood estimator for exponential family models of marked Gibbs point processes. Electron. J. Stat. 2 , 234-264 (2008)
7. J.T. Chayes, L. Chayes, R. Kotecký, The analysis of the Widom-Rowlinson model by stochastic geometric methods. Commun. Math. Phys. 172 (3), 551-569 (1995)
8. S.N. Chiu, D. Stoyan, W.S. Kendall, J. Mecke, Stochastic Geometry and Its Applications , 3rd edn. (Wiley, Chichester, 2013)
9. J.-F. Coeurjolly, D. Dereudre, R. Drouilhet, F. Lavancier, Takacs-Fiksel method for stationary marked Gibbs point processes. Scand. J. Stat. 39 (3), 416-443 (2012)
10. D.J. Daley, D. Vere-Jones, An Introduction to the Theory of Point Processes. Vol. I. Elementary Theory and Methods . Probability and Its Applications (New York), 2nd edn. (Springer, New York, 2003).
11. D. Dereudre, Diffusion infini-dimensionnelles et champs de Gibbs sur l'espace des trajectoires continues . PhD, Ecole polytechnique Palaiseau (2002)
12. D. Dereudre, The existence of quermass-interaction processes for nonlocally stable interaction and nonbounded convex grains. Adv. Appl. Probab. 41 (3), 664-681 (2009)
13. D. Dereudre, Variational principle for Gibbs point processes with finite range interaction. Electron. Commun. Probab. 21 , Paper No. 10, 11 (2016)
14. D. Dereudre, P. Houdebert, Infinite volume continuum random cluster model. Electron. J. Probab. 20 (125), 24 (2015)
15. D. Dereudre, F. Lavancier, Consistency of likelihood estimation for Gibbs point processes. Ann. Stat. 45 (2), 744-770 (2017)
16. D. Dereudre, R. Drouilhet, H.-O. Georgii, Existence of Gibbsian point processes with geometry-dependent interactions. Probab. Theory Relat. Fields 153 (3-4), 643-670 (2012)
17. D. Dereudre, F. Lavancier, K. Staˇ nková Helisová, Estimation of the intensity parameter of the germ-grain quermass-interaction model when the number of germs is not observed. Scand. J. Stat. 41 (3), 809-829 (2014)
18. R.L. Dobrushin, E.A. Pecherski, A criterion of the uniqueness of Gibbsian fields in the noncompact case, in Probability Theory and Mathematical Statistics (Tbilisi, 1982) . Lecture Notes in Mathematics, vol. 1021 (Springer, Berlin, 1983), pp. 97-110
19. T. Fiksel, Estimation of parametrized pair potentials of marked and nonmarked Gibbsian point processes. Elektron. Informationsverarb. Kybernet. 20 (5-6), 270-278 (1984)
20. H.-O. Georgii, Canonical Gibbs Measures . Lecture Notes in Mathematics, vol. 760 (Springer, Berlin, 1979). Some extensions of de Finetti's representation theorem for interacting particle systems
21. H.-O. Georgii, Large deviations and the equivalence of ensembles for Gibbsian particle systems with superstable interaction. Probab. Theory Relat. Fields 99 (2), 171-195 (1994)
22. H.-O. Georgii, Gibbs Measures and Phase Transitions . de Gruyter Studies in Mathematics, vol. 9, 2nd edn. (Walter de Gruyter, Berlin, 2011)
23. H.-O. Georgii, T. Küneth, Stochastic comparison of point random fields. J. Appl. Probab. 34 (4), 868-881 (1997)


<!-- p:237 -->


24. H.-O. Georgii, H.J. Yoo, Conditional intensity and Gibbsianness of determinantal point processes. J. Stat. Phys. 118 (1-2), 55-84 (2005)
25. H.-O. Georgii, H. Zessin, Large deviations and the maximum entropy principle for marked point random fields. Probab. Theory Relat. Fields 96 (2), 177-204 (1993)
26. C.J. Geyer, J. Møller, Simulation procedures and likelihood inference for spatial point processes. Scand. J. Stat. 21 (4), 359-373 (1994)
27. X. Guyon, Random Fields on a Network . Probability and Its Applications (New York) (Springer, New York, 1995). Modeling, statistics, and applications, Translated from the 1992 French original by Carenne Ludeña
28. P. Hall, On continuum percolation. Ann. Probab. 13 (4), 1250-1266 (1985)
29. J.L. Jensen, Asymptotic normality of estimates in spatial point processes. Scand. J. Stat. 20 (2), 97-109 (1993)
30. J.L. Jensen, H.R. Künsch, On asymptotic normality of pseudo likelihood estimates for pairwise interaction processes. Ann. Inst. Stat. Math. 46 (3), 475-486 (1994)
31. J.L. Jensen, J. Møller, Pseudolikelihood for exponential family models of spatial point processes. Ann. Appl. Probab. 1 (3), 445-461 (1991)
32. W.S. Kendall, J. Møller, Perfect simulation using dominating processes on ordered spaces, with application to locally stable point processes. Adv. Appl. Probab. 32 (3), 844-865 (2000)
33. O.K. Kozlov, Description of a point random field by means of the Gibbs potential. Uspehi Mat. Nauk 30 (6(186)), 175-176 (1975)
34. J.L. Lebowitz, A. Mazel, E. Presutti, Liquid-vapor phase transitions for systems with finiterange interactions. J. Stat. Phys. 94 (5-6), 955-1025 (1999)
35. S. Mase, Uniform LAN condition of planar Gibbsian point processes and optimality of maximum likelihood estimators of soft-core potential functions. Probab. Theory Relat. Fields 92 (1), 51-67 (1992)
36. K. Matthes, J. Kerstan, J. Mecke, Infinitely Divisible Point Processes (Wiley, Chichester, 1978). Translated from the German by B. Simon, Wiley Series in Probability and Mathematical Statistics
37. J. Mayer, E. Montroll, Molecular distributions. J. Chem. Phys. 9 , 2-16 (1941)
38. R. Meester, R. Roy, Continuum Percolation . Cambridge Tracts in Mathematics, vol. 119 (Cambridge University Press, Cambridge, 1996)
39. I.S. Molchanov, Consistent estimation of the parameters of Boolean models of random closed sets. Teor. Veroyatnost. i Primenen. 36 (3), 580-587 (1991)
40. J. Møller, Lectures on random Vorono ̆ ı tessellations . Lecture Notes in Statistics, vol. 87 (Springer, New York, 1994)
41. J. Møller, K. Helisová, Likelihood inference for unions of interacting discs. Scand. J. Stat. 37 (3), 365-381 (2010)
42. J. Møller, R.P. Waagepetersen, Statistical Inference and Simulation for Spatial Point Processes . Monographs on Statistics and Applied Probability, vol. 100 (Chapman &amp; Hall/CRC, Boca Raton, 2004)
43. X. Nguyen, H. Zessin, Integral and differential characterizations Gibbs processes. Mathematische Nachrichten, 88 (1), 105-115 (1979)
44. Y. Ogata, M. Tanemura, Likelihood analysis of spatial point patterns. J. R. Stat. Soc. Ser. B 46 (3), 496-518 (1984)
45. S. Poghosyan, D. Ueltschi, Abstract cluster expansion with applications to statistical mechanical systems. J. Math. Phys. 50 (5), 053509, 17 (2009)
46. C. Preston, Random fields . Lecture Notes in Mathematics, vol. 534 (Springer, Berlin, 1976)
47. D. Ruelle, Statistical Mechanics: Rigorous Results (W. A. Benjamin, Inc., New York, 1969)
48. D. Ruelle, Superstable interactions in classical statistical mechanics. Commun. Math. Phys. 18 , 127-159 (1970)
49. R. Takacs, Estimator for the pair-potential of a Gibbsian point process. Statistics, 17 (3), 429433 (1986)
50. J. van den Berg, C. Maes, Disagreement percolation in the study of Markov fields. Ann. Probab. 22 (2), 749-763 (1994)


<!-- p:238 -->


51. M.N.M. van Lieshout, Markov Point Processes and Their Applications (Imperial College Press, London, 2000)
52. B. Widom, J.S. Rowlinson, New model for the study of liquid-vapor phase transitions. J. Chem. Phys. 52 , 1670-1684 (1970)


<!-- p:239 -->


####### LECTURE NOTES IN MATHEMATICS

Editors in Chief: J.-M. Morel, B. Teissier;

####### Editorial Policy

1. Lecture Notes aim to report new developments in all areas of mathematics and their applications - quickly, informally and at a high level. Mathematical texts analysing new developments in modelling and numerical simulation are welcome.

Manuscripts should be reasonably self-contained and rounded off. Thus they may, and often will, present not only results of the author but also related work by other people. They may be based on specialised lecture courses. Furthermore, the manuscripts should provide sufficient motivation, examples and applications. This clearly distinguishes Lecture Notes from journal articles or technical reports which normally are very concise. Articles intended for a journal but too long to be accepted by most journals, usually do not have this 'lecture notes' character. For similar reasons it is unusual for doctoral theses to be accepted for the Lecture Notes series, though habilitation theses may be appropriate.

2. Besides monographs, multi-author manuscripts resulting from SUMMER SCHOOLS or similar INTENSIVE COURSES are welcome, provided their objective was held to present an active mathematical topic to an audience at the beginning or intermediate graduate level (a list of participants should be provided).

The resulting manuscript should not be just a collection of course notes, but should require advance planning and coordination among the main lecturers. The subject matter should dictate the structure of the book. This structure should be motivated and explained in a scientific introduction, and the notation, references, index and formulation of results should be, if possible, unified by the editors. Each contribution should have an abstract and an introduction referring to the other contributions. In other words, more preparatory work must go into a multi-authored volume than simply assembling a disparate collection of papers, communicated at the event.

3. Manuscripts should be submitted either online at www.editorialmanager.com/lnm to Springer's mathematics editorial in Heidelberg, or electronically to one of the series editors. Authors should be aware that incomplete or insufficiently close-to-final manuscripts almost always result in longer refereeing times and nevertheless unclear referees' recommendations, making further refereeing of a final draft necessary. The strict minimum amount of material that will be considered should include a detailed outline describing the planned contents of each chapter, a bibliography and several sample chapters. Parallel submission of a manuscript to another publisher while under consideration for LNM is not acceptable and can lead to rejection.
4. In general, monographs will be sent out to at least 2 external referees for evaluation.

A final decision to publish can be made only on the basis of the complete manuscript, however a refereeing process leading to a preliminary decision can be based on a pre-final or incomplete manuscript.

Volume Editors of multi-author works are expected to arrange for the refereeing, to the usual scientific standards, of the individual contributions. If the resulting reports can be forwarded to the LNM Editorial Board, this is very helpful. If no reports are forwarded or if other questions remain unclear in respect of homogeneity etc, the series editors may wish to consult external referees for an overall evaluation of the volume.

<!-- p:240 -->


5. Manuscripts should in general be submitted in English. Final manuscripts should contain at least 100 pages of mathematical text and should always include
- a table of contents;
- an informative introduction, with adequate motivation and perhaps some historical remarks: it should be accessible to a reader not intimately familiar with the topic treated;
- a subject index: as a rule this is genuinely helpful for the reader.
- For evaluation purposes, manuscripts should be submitted as pdf files.
6. Careful preparation of the manuscripts will help keep production time short besides ensuring satisfactory appearance of the finished book in print and online. After acceptance of the manuscript authors will be asked to prepare the final LaTeX source files (see LaTeX templates online: https://www.springer.com/gb/authors-editors/book-authorseditors/manuscriptpreparation/5636) plus the corresponding pdf- or zipped ps-file. The LaTeX source files are essential for producing the full-text online version of the book, see http://link.springer.com/bookseries/304 for the existing online volumes of LNM). The technical production of a Lecture Notes volume takes approximately 12 weeks. Additional instructions, if necessary, are available on request from lnm@springer.com.
7. Authors receive a total of 30 free copies of their volume and free access to their book on SpringerLink, but no royalties. They are entitled to a discount of 33.3 % on the price of Springer books purchased for their personal use, if ordering directly from Springer.
8. Commitment to publish is made by a Publishing Agreement ; contributing authors of multiauthor books are requested to sign a Consent to Publish form . Springer-Verlag registers the copyright for each volume. Authors are free to reuse material contained in their LNM volumes in later publications: a brief written (or e-mail) request for formal permission is sufficient.

####### Addresses:

Professor Jean-Michel Morel, CMLA, École Normale Supérieure de Cachan, France E-mail: moreljeanmichel@gmail.com

Professor Bernard Teissier, Equipe Géométrie et Dynamique,

Institut de Mathématiques de Jussieu - Paris Rive Gauche, Paris, France

[E-mail: bernard.teissier@imj-prg.fr](mailto:bernard.teissier@imj-prg.fr)

Springer: Ute McCrory, Mathematics, Heidelberg, Germany,

[E-mail: lnm@springer.com](mailto:lnm@springer.com)
