---
id: "Dumenil_2022_Delaunay-Random-Points-Surface"
source_pdf: "../pdf/Dumenil_2022_Delaunay-Random-Points-Surface.pdf"
source_filename: "Dumenil_2022_Delaunay-Random-Points-Surface.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 96.0
visual_assets: "disabled"
references_file: "../references/Dumenil_2022_Delaunay-Random-Points-Surface.references.md"
---

<!-- p:1 -->

HAL

open science

####### Expected Size of the 3-Dimensional Delaunay Triangulation of Random Points on a Surface

Charles Duménil

####### V To cite this version:

Charles Duménil. Expected Size of the 3-Dimensional Delaunay Triangulation of Random Points on a Surface. Computational Geometry [cs.CG]. Université de Lorraine, 2022. English. &lt;NNT: 2022LORR0050&gt;. 〈tel03695908&gt;

HAL Id: tel-03695908

https://theses.hal.science/tel-03695908v1

Submitted on 15 Jun 2022

HAL is a multi-disciplinary open access archive L'archive ouverte pluridisciplinaire HAL, est desfor the deposit and dissemination of scientific re- tinée au dépôt et à la diffusion de documents sciensearch documents, whether they are published or not. tifiques de niveau recherche, publiés ou non, émanant The documents may come from teaching and research des établissements d'enseignement et de recherche institutions in France or abroad, or from public or pri- français ou étrangers, des laboratoires publics ou vate research centers. privés.

Autorisation

HAL


<!-- p:2 -->

L

UNIVERSITÉ

DE LORRAINE

##### Expected Size of the 3-Dimensional Delaunay Triangulation of Random Points on a Surface

#### THÈSE

présentée et soutenue publiquement le 09 Mai 2022

pour l'obtention du

####### Doctorat de l'Université de Lorraine

(Mention Informatique)

par

####### Charles Duménil

| Philippe Chassaing   | (Pr ́ esident du jury)   |
|----------------------|-------------------------|
| Dominique Attali     | (Rapportrice)           |
| Nicolas Bonichon     | (Rapporteur)            |
| Andr ́ e Lieutier     | (Examinateur)           |
| R ́ egine Marchand    | (Examinatrice)          |
| Olivier Devillers    | (Directeur de th` ese)  |

####### Composition du jury


<!-- p:3 -->


##### Résumé en francais

Nous résumons ici, en francais, le contenu de la présente thèse. Ce résumé est une traduction de l'introduction, ainsi que des préambules de chacune des quatre parties qui constituent cette thèse. Cette thèse a pour but d'évaluer la taille de la triangulation de Delaunay de points aléatoirement distribués sur une surface. Dans cette introduction, nous donnons une explication des concepts en jeu dans ce problème, et présentons comment cette thèse est organisée pour le résoudre. La triangulation de Delaunay, et son dual, le diagramme de Voronoï, sont des objets géométriques qui sont apparus de manière récurrente dans l'histoire des sciences [LP12]. En dimension 2, le diagramme de Voronoï d'un ensemble de points X est une partition du plan en polygones convexes, aussi appelés cellules, une pour chaque point de X, tel que la cellule de p ∈ X est l'ensemble des points plus proches de p que de tout autre point de X. D'autre part, la triangulation de Delaunay est l'ensemble des triangles Pon e  drt  e oe oe e  nt o ds i  e cs or et la triangulation de Delaunay partagent une propriété de dualité : les centres des cercles cireconscrits aux triangles de Delaunay sont les sommets des cellules des diagrammes de Voronoï. Ces définitions sont généralisables dans des dimensions supérieures. La première apparition de la triangulation de Delaunay semble être due à Johannes Kepler en 1611 dans son article "On the Six-Cornered Snowflake", dans lequel Kepler étudiait le célèbre problème de l'emballage des sphères. Plus tard, ils réapparaissent en astronomie avec René Descartes, et en épidémiologie au 19me siècle lorsque John Snow utilise un diagramme de Voronoï pour identifier les sources géographiques d'une épidémie de choléra. C'est au cours du 20me siècle que le mathématicien russe Georges Voronoï a formalisé le diagramme dit de Voronoï en dimension quelconque [Vor08]. Son élève, Boris Delaunay, a ensuite formalisé la triangulation de Delaunay dans son article "Sur la sphère vide" [Del34]. Entre-temps, la triangulation de Delaunay et le diagramme de Voronoï ont été impliqués dans des disciplines aussi diverses que la cristallographie, la métallurgie, la météorologie [OBS92], ou plus récemment, la gravité quantique [BCW09]. Aujourd'hui, la triangulation de Delaunay est l'une des structures les plus étudiées en géométrie algorithmique. En raison de ses propriétés, la triangulation de Delaunay peut être utilisée pour créer un maillage efficace pour la résolution d'équations différentielles. En algorithmique, elle peut être utilisée pour obtenir, par exemple, l'arbre couvrant minimal d'un ensemble de points. Un domaine dans lequel les résultats de cette thèse peuvent être significatifs, est la modélisation géométrique [FP09, BDTY00]. En effet, pour le problème de reconstruction de surface [ACK01, AB99], la triangulation de Delaunay peut jouer un rôle intermédiaire mais nécessaire. Le problème est le suivant : calculer une approximation linéaire par morceaux d'une surface à partir d'un ensemble de points échantillons. Puisque certains algorithmes utilisent la triangulation de Delaunay tridimensionnelle comme étape pour la reconstruction de la surface, il est important de connaître la complexité combinatoire (plus simplement appelée taille) de la triangulation de Delaunay de ces points. Cette taille peut avoir un impact sur les complexités en temps et en mémoire de l'algorithme de reconstruction. Pour le cas en 2 dimensions, comme il sera expliqué dans la partie I, nous savons que la taille de la triangulation de Delaunay reste linéaire avec le nombre de points. En 3 dimensions, ce n'est plus le cas. La taille de la triangulation de Delaunay en 3D peut varier de linéaire à quadratique. Cette taille dépend de la façon dont les points sont distribués dans R3. En ce qui concerne le problème de reconstruction de surface, les points sont supposés être distribués sur la surface que l'on veut reconstruire. Ainsi, la taille de la triangulation de Delaunay dépendra à la fois de la surface sur laquelle les points sont répartis, et de la façon dont ils sont répartis sur cette surface. Pour modéliser mathématiquement les points, nous devons choisir un type d'échantillon. Il peut être déterministe, avec de bonnes propriétés comme "tout disque d'un rayon donné contient au moins un point de l'échantillon". Nous appellerons un tel échantillon déterministe un bon échantillon. Mais l'échantillon peut aussi être aléatoire, comme un échantillon uniforme ou un processus ponctuel de Poisson. Dans les deux cas, nous considérons que le nombre de points tend vers l'infini, et calculons une approximation asymptotique de la taille de la triangulation de Delaunay. Comme nous l'expliquerons dans la partie I, Chapitre 4, Erickson a trouvé un bon échantillon de n points distribués sur un cylindre de révolution pour lequel la triangulation de Delaunay est O(n√n) [Eri05]. La construction d'un tel échantillon est très spent  unt ne t  ns nt oos   nh r   nue pour la triangulation de Delaunay. A l'inverse, lorsqu'un bon échantillon est distribué sur une surface générique, Erickson [Eri01b] et parallèlement, Attali et al. [ABL03] ont prouvé que la triangulation de Delaunay est O(n log n), où la constante cachée dans le grand O dépend des caractéristiques de la surface, comme son diamètre, sa courbure maximale, etc... La définition d'une surface générique sera donnée plus tard, pour l'instant, on gardera à l'esprit qu'une surface générique est une surface qui a des propriétés "typiques", par exemple elle ne présente aucune symétrie particulière. Plus tard, Devillers et al. [DEG08] ont montré que lorsqu'un échantillon aléatoire uniforme est distribué sur un cylindre, la triangulation de Delaunay a une taille moyenne Θ(n log n), prouvant au passage que certaines constructions déterministes sont assez pathologiques.


<!-- p:4 -->


Ces travaux ouvrent une porte à une question naturelle :

Quelle est la taille moyenne de la triangulation 3D-Delaunay d'un échantillon aléatoirement distribué sur une surface ?

C'est le problème que nous essayons de résoudre dans cette thèse. Notons que le résultat peut dépendre de la surface, en particulier nous nous intéressons au cas des surfaces génériques, pour lesquelles les résultats expérimentaux semblent montrer une limite linéaire. Pour modéliser les points, nous choisissons d'utiliser un processus ponctuel de Poisson car il vérifie des propriétés d'homogénéité et d'indépendance qui sont pratiques pour les calculs. Nous désignons le processus ponctuel de Poisson par X. Un tel processus s'accompagne d'un paramètre appelé intensité, dénoté par λ, qui correspond au nombre moyen de points que nous pouvons trouver dans une région ae   s oi  o  e ot o  oe s is  oits sont distribués a une aire de 1, de sorte que le nombre moyen de points distribués sur la surface est λ. Dans la partie I, Chapitre 5, nous présentons une première solution du problème en appliquant directement le résultat d'Attali et al. décrit ci-dessus pour un bon échantillon déterministe, au processus ponctuel de Poisson. Néanmoins, la limite résultante pour le processus de Poisson ne peut pas être meilleure que la limite originale pour un bon échantillon, et nous montrons seulement que la triangulation de Delaunay a une taille moyenne de O(λ log2 λ). L'un des principaux problèmes de cette méthode est qu'elle n'utilise pas du tout le fait que l'échantillon de pints est un processus de Poisson, mais simplement le fait qu'il s'agit d'un bon échantillon avec forte probabilité, et donc nous n'excluons pas les cas pathologiques. Pour utiliser efficacement les propriétés d'un processus de Poisson, nous devons adopter une approche différente. Afin de prouver la borne moyenne de O(n log n) pour l'échantillon uniforme sur un cylindre, Devillers et al. ont remarqué que l'intersection du cylindre avec une sphère passant par deux points p et q sur le cylindre contient toujours un triangle spécifique dessiné sur le cylindre. Cela les conduit à étudier un graphe à 2 dimensions dans lequel deux points sont voisins s'il existe un tel triangle qui ne contient pas d'autres points. Un tel graphe a une taille moyenne Θ(n log n), et c'est ainsi qu'ils obtiennent la limite O(n log n). Ce graphe de "triangle vide" est un cas particulier des graphes de régions vides. Dans la partie II, nous définissons un type de graphes de régions vides, nous formalisons une méthode pour calculer des bornes inférieures et supérieures sur leur taille moyenne, et nous donnons des résultats fins pour de tels graphes. Comme Attali et al. l'a souligné, l'intersection d'une sphère avec une surface générique a approximativement une forme elliptique, alignée avec les directions de courbure de la surface. Ceci nous amène à

étudier un graphe particulier de régions vides pour lequel les régions sont des ellipses alignées sur l'axe.


<!-- p:5 -->


Nous prouvons, dans la partie II, Chapitre 8, que si les ellipses concernées ont un rapport d'aspect copris entre β et 1, avec 0 &lt; β &lt; 1, alors le nombre moyen de voisins de tout point du graphe est Θ β

Afin d'illustrer la méthode développée dans la partie II, nous calculons, dans la partie III, des bornes asymptotiques fines sur la taille moyenne de la triangulation 3D-Delaunay dans deux cas spécifiques. Dans la partie III, Chapitre 12, nous considérons un cylindre de révolution, comme dans [DEG08], et prouvons la borne Θ(λln λ) mais pour un processus ponctuel de Poisson. Compte tenu de la similarité entre l'échantillon uniforme et l'échantillon de Poisson, le but de ce chapitre est principalement de présenter concrètement la méthode dans un cas simple en 3 dimensions. Ensuite, dans le Chapitre 13, nous calculons la taille de la triangulation 3D-Delaunay d'un processus de Poisson distribué sur une sphère aplatie. Cette surface possède suffisamment de propriétés génériques pour que la triangulation de Delaunay se comporte bien. En particulier, à l'inverse du cylindre, son axe médian est bi-dimensionnel. En utilisant des ellipses vides alignées aux axe, et avec un rapport d'aspect borné, nous montrons que la taille moyenne de la triangulation est Θ(λ). Ceci fournit une surface lisse sur laquelle un processus ponctuel de Poisson a une triangulation 3D-Delaunay de taille linéaire. Dans le chapitre 14, nous simulons un processus de Poisson sur une sphère aplatie et une sphère allongée pour montrer que nos résultats sont expérimentalement corrects.

Enfin, dans la partie IV, nous traitons le cas des surfaces génériques. Même si une sphère aplatie est une surface spécifique, nous pourrons réutiliser certains calculs de cette partie moyennant quelques adaptations. En effet, la sphère aplatie est la surface d'un objet convexe, ce qui n'est généralement pas le cas. Il possède beaucoup de symétries, ce qui n'est pas non plus le cas en général. Dans cette partie, nous nous concentrons plus sur la façon de gérer ces adaptations que sur les calculs qui étaient déjà assez fastidieux dans le cas du sphéroïde.

La suite du résumé décrit plus précisément chaque partie de la thèse.

Dans cette thèse, nous fournissons une méthode pour calculer la taille moyenne de certains graphes de régions vides, et en particulier, de la triangulation de Delaunay de points sur une surface, pour un ensemble de points qui est un processus ponctuel de Poisson. La compréhension du sujet nécessite des connaissances dans au moins trois grands domaines des mathématiques et de l'informatique : La géométrie, la combinatoire et les probabilités. Nous les décrivons dans la partie I.

Pour être bref, un processus ponctuel de Poisson est un ensemble aléatoire de points, pour lequel les calculs sont pratiques. Un graphe de régions vides est un type spécifique de graphe géométrique dont Ira dd  n nn  o l n  en  n dan nombre de ses arêtes. Comme les sommets des graphes étudiés sont tirés d'un processus ponctuel de Poisson, le nombre d'arêtes des graphes est une valeur aléatoire. Nous calculons l'espérance de cette valeur, qui correspond, en quelque sorte, à une valeur moyenne probabiliste.

Pour expliquer en détail ces notions, nous décomposons cette partie en trois chapitres. Le chapitre 1 sera consacré à la géométrie. Nous l'utiliserons pour rappeler quelques notions mathématiques de base, et présenterons certaines notations que nous utiliserons. Puis nous consacrerons une section à la géométrie des courbes planes, en particulier pour décrire la notion de courbure. Enfin, dans la dernière section du chapitre, nous expliquons le concept de surface générique, et présentons les caractéristiques spécifiques que possèdent les surfaces génériques.

Le chapitre 2 est consacré à la combinatoire. Nous présentons la notion de graphe, et quelques outils comme la formule d'Euler que nous utilisons pour calculer leur taille. Nous définissons ensuite ce qu'est la triangulation de Delaunay d'un ensemble de points, et expliquons comment sa taille varie en dimension 2 et 3.

Dans le chapitre 3, nous présentons les outils probabilistes que nous utiliserons. Nous commençons par expliquer ce qu'est un processus ponctuel de Poisson, et quelles sont ses propriétés. Ensuite, nous présentons l'une des formules les plus utilisées dans cette thèse : la formule de Slivnyak-Mecke, qui sert à calculer une espérance. Nous illustrons l'utilisation de cette formule à travers l'exemple de la triangulation 2D de Delaunay.

Dans le chapitre 4, nous présentons l'état de l'art du problème de la détermination de la taille de la triangulation 3D de Delaunay de points sur une surface. Nous présentons l'évolution de ce calcul en fonction du sous-ensemble de R3 où sont distribués les points, et de la manière dont ils sont distribués. En effet, nous commençons par présenter le cas de points distribués aléatoirement dans le cube unitaire, qui a une taille linéaire en espérance. Ensuite, nous considérons que les points sont distribués sur une surface de R3. Dans ce cas, nous présentons d'abord le cas d'une surface polyédrique. Pour un échantillon déterministe ou aléatoire, il a été montré que la triangulation est linéaire. Ensuite, nous présentons un résultat basé sur un paramètre de la distribution des points appelé la dispersion. Enfin, nous considérons que les points sont distribués sur une surface lisse. Quel que soit le type d'échantillon, nous présentons que si les points sont distribués sur un cylindre, la triangulation n'est plus linéaire. Nous présentons ensuite les études qui ont été faites sur des surfaces génériques, qui excluent le cylindre. Les surfaces génériques n'avaient été étudiées qu'avec un échantillon déterministe.


<!-- p:6 -->


Enfin, dans le chapitre 5, nous introduisons la première contribution de cette thèse, le calcul de la taille de la triangulation 3D-Delaunay de points aléatoires distribués sur une surface générique, en montrant qu'un échantillon aléatoire vérifie les propriétés d'une bonne déterministe avec une forte probabilité

Dans la partie II, nous introduisons la notion de graphe de régions vides. Étant donné un ensemble de points X, un graphe de régions vides est un graphe dans lequel deux points p et q de X sont voisins si une région définie pour (p, q) ne contient aucun autre point de X. Cette notion unifie la triangulation classique de Delaunay [Del34], le graphe de Gabriel [GS69], le squelette β [KR85, ABE98], le graphe des ellipses vides [DEG08], le graphe des plus proches voisins, les graphes Θ, et les graphes de Yao [Yao82].

o oe e n o  et  e el e e e  e ar ne supérieure et une borne inférieure sur le degré d'un point dans un graphe de régions vides donné, lorsque l'échantillon de points X est un processus ponctuel de Poisson. La partie II se compose de cinq chapitres.

Dans le chapitre 6, à titre d'exemple pédagogique, nous montrons comment nous pouvons trouver des bornes asymptotiquement fines sur le calcul du degré moyen d'un point dans la triangulation de Delaunay à 2 dimension en utilisant la méthode décrite par Devroye, Lemaire et Moreau [DLM04].

Dans le chapitre 7, nous formalisons la méthode citée ci-dessus, afin de la généraliser. Nous donnons une définition formelle des graphes à région vide, et fournissons deux lemmes : Les lemmes de combinaison et de partition qui seront réutilisés tout au long de la thèse. Enfin, nous illustrons la formalisation sur l'exemple de Delaunay.

Dans le chapitre 8, nous considérons un graphe de région vide spécifique : le graphe des ellipses vides alignés aux axes. Nous faisons une distinction entre le cas où nous considérons toutes les ellipses alignées aux axes et le cas où les ellipses ont un rapport d'aspect borné. Nous montrons que dans le premier cas, le degré moyen d'un point est Θ (ln λ) dans un processus ponctuel de Poisson avec une intensité λ, et et 1, pour 0 &lt; β &lt; 1. Ce chapitre a un intérêt particulier pour la thèse. En effet, dans les parties III et IV, nous calculons la triangulation de Delaunay de points sur une surface, et nous montrerons que les intersections des sphères de Delaunay avec la surface approchent des ellipses alignées aux axes de courbure. Nous pourrons donc réutiliser les résultats de ce chapitre.

Dans le chapitre 9, nous estimons la probabilité qu'un point ait des voisins plus éloignés qu'un certain seuil, dans la triangulation de Delaunay et dans le graphe d'ellipses vides alignées aux axes avec un rapport d'aspect borné. Nous montrons que dans les deux cas, cette probabilité décroît exponentiellement avec la distance.

Enfin, dans les chapitres 10 et 11, nous présentons quelques graphes de régions vides supplémentaires : le graphe d'ellipses vides avec un rapport d'aspect borné, qui diffère par le fait que les ellipses ne sont plus alignées aux axes, un graphe de régions vides où les régions sont définies par des équations du quatrième ordre, et quelques caractéristiques sur les graphes de type plus proche voisin.

Dans la partie III, nous illustrons notre méthode de calcul pour le cas de la triangulation 3D de Delaunay de points distribués sur deux surfaces spécifiques.

Nous rappelons brièvement ce qu'est une triangulation de Delaunay tridimensionnelle. Considérons un ensemble X de points dans R3 dans une position générique. La triangulation de Delaunay tridimensionnelle de X est la triangulation 3D dans laquelle aucun point de X n'est à l'intérieur d'une sphère circonscrite un tétraèdre de la triangulation 3D. Nous utiliserons souvent le mot "triangulation" seul (sans "3D") même si elle est en fait constituée de tétraèdres. Pour simplifier notre étude, nous ne prenons en compte que la propriété selon laquelle une arête (p, q) est dans la triangulation s'il existe une sphère vide passant par p et q.

Cette propriété suggère une approche du graphe des régions vides de la triangulation de Delaunay où


<!-- p:7 -->


les régions sont des sphères. Dans le cas où les points sont distribués sur une surface de R3, l'étude des sphères de Delaunay n'a d'intérêt que sur une partie négligeable de la sphère, à savoir son intersection avec la surface. Nous pouvons alors proposer une définition légèrement différente qui s'adapte aux surfaces.

Pour chaque paire (p, q) de l'échantillon de points X, nous considérons l'ensemble R(p, q) des intersections de la surface avec les sphères passant par p et q. On dit alors qu'une arête (p, q) est une arête de Delaunay, s'il existe une région dans R(p, q) qui ne contient pas d'autres points de X.

Cette définition permet d'éclairer le comportement de la triangulation de Delaunay de points sur une surface. En effet, tout d'abord, elle ramène le problème à un graphe de régions vides bidimensionnel qui permet une comparaison avec la triangulation de Delaunay classique bidimensionnelle et les graphes de régions vides étudiés dans la partie précédente. Deuxièmement, la comparaison rend plus compréhensible la complexité de la triangulation. Comme nous allons le voir, de telles régions peuvent être approchées par des ellipses alignées aux axes. Selon les propriétés du point de la surface sur laquelle le graphe est étudié, le comportement ressemblera plus ou moins à un graphe d'ellipses alignées aux axes avec un rapport d'aspect borné.

Nous divisons cette partie en trois chapitres. Le chapitre 12 est dédié au cas du cylindre, qui avait déjà été étudié dans la littérature. Ici, il est surtout utilisé comme exemple pédagogique et pour montrer l'efficacité de notre méthode. Le chapitre 13 est consacré à une surface spécifique, suffisamment générale pour représenter efficacement le cas des surfaces génériques. Cette surface est un ellipsoide aplati de révolution. Ce chapitre donne un premier exemple de surface sur laquelle une triangulation 3D-Delaunay de points aléatoires est linéaire en moyenne. Il permet également d'introduire la méthode et quelques lemmes qui seront réutilisés dans la dernière partie de la thèse. Enfin, dans le chapitre 14, nous illustrons nos résultats sur deux ellipsoïdes de révolution. Un qui est aplati, comme dans le chapitre 13, et un qui est allongé, pour lequel la triangulation de Delaunay est supposée avoir un comportement similaire à celui que l'on retrouve sur un cylindre.

Comme nous il sera vu dans la partie III, lorsqu'un processus ponctuel de Poisson d'intensité λ est distribué sur une surface, sa triangulation de Delaunay a une taille moyenne qui peut varier, au moins de linéaire à quasi-linéaire.

Dans la partie IV, nous considérons une surface générique S. Sa généricité lui fait partager des propriétés avec la sphère aplatie, qui sont significatives pour la triangulation de Delaunay. Nous décrivons ces propriétés dans le chapitre 15, conjointement avec les différences que nous observons. Cela donne lieu à un schéma de preuve que nous expliquons à la fin du chapitre. De manière générale, nous adaptons le schéma de preuve utilisé pour le sphéroïde. Une des propriétés génériques importantes est que l'ensemble Z de S, des points p tels que r*(p) = 1 sphère aplatie, nous avons montré que le degré d'un point dépend fortement fortement de sa distance à Z. Nous désignons alors par hp la distance de p à Z.

Chaque chapitre suivant décrit une analyse partielle du degré attendu d'un point p dansS dans la triangulation de Delaunay en fonction de la position de p sur S et de son éventuel voisin q. Dans le ps o o s n n ous  one o   o o s  ont n oos comptons sont géodésiquement proches de p. Nous désignons par Loc(p) le voisinage local de p. Dans le voisinage local de p, nous pouvons approcher S par une quadrique, et ainsi nous pourrons réutiliser ou adapter la plupart des calculs déjà effectués dans le chapitre 13. Dans le voisinage local, nous pouvons annr  d  r  r or en  o   d-n   snt Nous montrerons que Loc(p) est un voisinage local circulaire de rayon Θ(1) lorsque p est loin de Z, ou de rayon Θ(h3) lorsque p est proche de Z. Nous distinguons dans ce chapitre, le calcul pour les points qui se trouvent sur, ou près de la partie convexe de la surface, où les deux courbures principales sont de même signe, et les points qui sont loin de la partie convexe, où le rayon médian est fini.

Dans le chapitre 17, nous calculons le degré distant d'un point, c'est-à-dire le nombre moyen de voisins qui sont proches des points symétriques de p. Nous désignerons par Rem(p) ce voisinage. Ici encore, nous devons différencier le comptage en fonction de la position de p. En effet, si p est proche de S', le l'ensemble des points ayant deux points symétriques, alors p peut avoir des voisins distants en plusieurs endroits de S. Dans ce chapitre, nous introduisons la notion de points symétriques supplémentaires, afin de compter les voisins distants d'un point p dont la sphère médiane est proche d'une sphère médiale avec plusieurs points de contact.


<!-- p:8 -->


Enfin, dans le chapitre 18, nous comptons les arêtes restantes. Pour les arêtes (p, q) telles que p est loin de Z, un argument de recouvrement montrera que leur nombre est o(λ). A l'inverse, si p est proche de Z, son voisinage local et distant sont trop petits pour utiliser l'argument de recouvrement. Nous allons donc considérer un plus grand voisinage local, appelé voisinage de moyenne distance comme dans la partie III. Nous prouvons que p a O(log λ) tels voisins mais avec une probabilité exponentiellement décroissante avec la distance à Z. Comme pour le cas du sphéroïde, cela nous permet d'intégrer le degré moyen autour de Z, afin d'obtenir un nombre linéaire moyen d'arêtes dont l'extrémité est proche de Z.

L'ensemble de ces calculs fournit la borne linéaire recherchée.

La thèse se conclut par une conjecture qui permettrait de faire abstraction de la notion de généricité.


<!-- p:9 -->


####### Remerciements

"A delayed game is eventually good, but a rushed game is forever bad."

- Shigeru Miyamoto

Loin de moi l'idée de justifier le temps que j'ai pris pour achever cette thèse. Néanmoins, je vois dans cette citation un soupçon de raison valable. Car il m'en a fallu, du temps, pour en arriver à bout. Un peu plus de cinq années, de recherche, de reflexion, d'enseignements, d'écriture... et de café! Si ce temps ne fut pas vain, c'est essentiellement grâce à l'accompagnement de toutes les personnes qui m'ont entouré pendant ma thèse. Je les remercie dans les lignes qui suivent. La première personne que je souhaite remercier est évidemment Olivier, mon encadrant. Déjà pour la confiance qu'il a su m'accorder pour traiter ce sujet, mais aussi pour sa gentillesse, sa bienveillance, ainsi que pour la patience et la compréhension dont il a fait preuve. Ses qualités humaines furent une aide constante et une nécessité pour moi. Je tiens aussi à le remercier pour son professionnalisme et sa sagacité qui font le chercheur qu'il est, et dont j'ai eu l'immense fierté d'être un doctorant. Merci Olivier. Je tiens aussi à remercier les personnes sans lesquelles je n'aurais pu m'approcher de ce doctorat. À savoir Anne, qui m'a permis de reprendre le Master de mathématiques qui m'a conduit à cette thèse. Ainsi que Steve qui, à l'issue du Master, m'a accueilli en stage dans son équipe, et m'a donc non seulement fait entrer au Loria mais m'a aussi fait découvrir le milieu de la recherche. Plus formellement, je remercie les membres du jury, pour avoir accepté de lire ma thèse, pour en avoir apporté des corrections et pour avoir écouté ma soutenance. Malgré le temps qu'a pris ma thèse, aller au Loria quotidiennement fut toujours un plaisir. Ceci, je le dois à mes collègues. Parmi eux, se trouvent les membres de Gamble, l'équipe de Géo-Algo au sein de laquelle j'ai fait mon doctorat. Cette équipe est peuplée de chercheurs tous plus sympathiques les uns que les autres. Des permanents pour leur bienveillance, aux stagiaires pour leur humour, en passant par les doctorants et les post-doc pour leurs interminables conversations, je tiens à les remercier. Parmi mes collègues, je tiens aussi à citer les doctorants des autres équipes, que j'ai plus ou moins cotoyés, dont certains furent des amis proches. Le soutien mutuel qui s'opère naturellement entre doctorants est une nécessité bienvenue, et pour ça, je remercie tous ceux que j'ai croisés. Parce qu'il m'a souvent fallu décompresser, je me dois de remercier tous ceux qui m'ont accompagné en dehors du labo. En première ligne sont les grimpeurs. En effet, l'escalade fut ma principale activité extra-professionnelle. En plus de me servir de défouloir, elle fut source de nombreuses rencontres, et de beaucoup de satisfaction. Pour la joie que j'ai partagée avec eux, je remercie tous les grimpeurs, occasionnels ou réguliers, que j'ai rencontré au cours de ma thèse. Parmi ces rencontres figure celle de ma compagne, qui m'a apporté son soutien alors que je préparais ma soutenance, je l'en remercie tendrement. Et quand le sport ne suffisait plus, ils étaient toujours présents pour partager un verre, ceux avec qui je suis lié depuis plus de vingt ans, mes amis de toujours, merci à vous aussi. Finalement, parce que je leur serai éternellement reconnaissant pour tout ce qu'ils ont toujours fait pour moi et pour l'amour qu'ils m'ont transmit, je remercie mes parents.

- vii
- ix


<!-- p:10 -->


Je dédie cette thèse à mes parents Dominique et Georges.


<!-- p:11 -->


Cette thèse a reçu le soutien de l'ANR-17-CE40-0017 (ASPAG).

- xi


<!-- p:12 -->


##### Contents

| Introduction   | Introduction                    | Introduction                                                                      | Introduction                                                               | 1                                    |
|----------------|---------------------------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|--------------------------------------|
| I              | Presentation of general notions | Presentation of general notions                                                   | Presentation of general notions                                            | 5                                    |
|                | Geometry                        | Geometry                                                                          | Geometry                                                                   | 9                                    |
| 1              | 1.1                             | Geometry of plane curves . .                                                      | . . . . . . . . . . . . . . .                                              | . . . . . . . . . . . . . . . . . 9  |
|                |                                 | 1.1.1                                                                             | The notion of curvature . . . . . . . . . . . . .                          | . . . . . . . . . . . . . . . . . 9  |
|                |                                 | 1.1.2                                                                             | The medial axis of a curve . . . . . . . . . . . .                         | . . . . . . . . . . . . . . . . . 11 |
|                | 1.2                             | Geometry of surfaces .                                                            | . . . . . . . . . . . . . . . . . .                                        | . . . . . . . . . . . . . . . . . 13 |
|                |                                 | 1.2.1                                                                             | Basic notions on surfaces . . . . . . . . . . . . .                        | . . . . . . . . . . . . . . . . . 13 |
|                |                                 | 1.2.2                                                                             | Analytic description of a surface . . . . . . . . .                        | . . . . . . . . . . . . . . . . . 15 |
|                | 1.3                             | Generic surface .                                                                 | . . . . . . . . . . . . . . . . . . . . .                                  | . . . . . . . . . . . . . . . . . 16 |
|                |                                 | 1.3.1                                                                             | Maxima of curvature . . . . . . . . . . . . . . .                          | . . . . . . . . . . . . . . . . . 16 |
|                |                                 | 1.3.2                                                                             | Medial axis and contact types . . . . . . . . . .                          | . . . . . . . . . . . . . . . . . 17 |
|                |                                 | 1.3.3                                                                             | Summary of the cases . . . . . . . . . . . . . . .                         | . . . . . . . . . . . . . . . . . 20 |
| 2              | Combinatorics                   | Combinatorics                                                                     | Combinatorics                                                              | 23                                   |
|                | 2.1                             | Graph theory . .                                                                  | . . . . . . . . . . . . . . . . . . . . .                                  | . . . . . . . . . . . . . . . . . 23 |
|                |                                 | 2.1.1                                                                             | Generalities on graphs . . . . . . . . . . . . . .                         | . . . . . . . . . . . . . . . . . 23 |
|                |                                 | 2.1.2                                                                             | Counting the edges of a planar graph . . . . . .                           | . . . . . . . . . . . . . . . . . 24 |
|                | 2.2                             | The Delaunay triangulation .                                                      | . . . . . . . . . . . . . .                                                | . . . . . . . . . . . . . . . . . 25 |
|                |                                 | 2.2.1                                                                             | The 2D-Delaunay triangulation . . . . . . . . .                            | . . . . . . . . . . . . . . . . . 25 |
|                |                                 | 2.2.2                                                                             | In three dimensions (and higher) . . . . . . . .                           | . . . . . . . . . . . . . . . . . 26 |
| 3              | Probabilities                   | Probabilities                                                                     | Probabilities                                                              | 29                                   |
|                | 3.1                             | Poisson point process . .                                                         | . . . . . . . . . . . . . . . . .                                          | . . . . . . . . . . . . . . . . . 29 |
|                | 3.2                             | Slivnyak-Mecke's theorem .                                                        | . . . . . . . . . . . . . . .                                              | . . . . . . . . . . . . . . . . . 30 |
| 4              | State of the art                | State of the art                                                                  | State of the art                                                           | 33                                   |
|                | 4.1                             | Expected size of the d D-Delaunay triangulation of a uniform set of points        | Expected size of the d D-Delaunay triangulation of a uniform set of points | . . . . . . 33                       |
|                | 4.2                             | Analysis of the 3D-Delaunay triangulation of points on a polyhedral surface 4.2.1 | Probabilistic analysis . . . . . . . .                                     | . . . . . 35 35                      |


<!-- p:13 -->


|    |                                                      | 4.2.2                                                                                                                                                                      | Deterministic analysis . . . . . . . . . . . . . . . .                                                                                                                     | . . . . . . . . . . . . . . . . 36   |
|----|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
|    |                                                      | 4.2.3                                                                                                                                                                      | On polyhedral surfaces of any dimension . . . . .                                                                                                                          | . . . . . . . . . . . . . . . . 37   |
|    | 4.3                                                  | Evaluating the size of the Delaunay triangulation with respect to the spread of points . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | Evaluating the size of the Delaunay triangulation with respect to the spread of points . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | the . . . 37                         |
|    | 4.4                                                  | Another probabilistic approach .                                                                                                                                           | . . . . . . . . . . . . . .                                                                                                                                                | . . . . . . . . . . . . . . . . 37   |
|    | 4.5                                                  | Deterministic nice sample on generic surfaces                                                                                                                              | . . . . . . .                                                                                                                                                              | . . . . . . . . . . . . . . . . 39   |
| 5  | A Poisson sample on a surface is a good sample       | A Poisson sample on a surface is a good sample                                                                                                                             | A Poisson sample on a surface is a good sample                                                                                                                             | 41                                   |
|    | 5.1                                                  | Notation, definitions, previous results . .                                                                                                                                | . . . . . . . . .                                                                                                                                                          | . . . . . . . . . . . . . . . . 41   |
|    | 5.2                                                  | Is a Poisson sample a good sample? .                                                                                                                                       | . . . . . . . . . . .                                                                                                                                                      | . . . . . . . . . . . . . . . . 42   |
| II | Stochastic analysis of empty region graphs           | Stochastic analysis of empty region graphs                                                                                                                                 | Stochastic analysis of empty region graphs                                                                                                                                 | 47                                   |
| 6  | A                                                    | sub-graph and a super-graph of the 2D-Delaunay triangulation                                                                                                               | sub-graph and a super-graph of the 2D-Delaunay triangulation                                                                                                               | 51                                   |
|    | 6.1                                                  | The Gabriel and half-moon graphs . . . .                                                                                                                                   | . . . . . . . . .                                                                                                                                                          | . . . . . . . . . . . . . . . . 51   |
| 7  |                                                      | General method                                                                                                                                                             | General method                                                                                                                                                             | 55                                   |
|    | 7.1                                                  | Empty region graphs . . . . . .                                                                                                                                            | . . . . . . . . . . . . . .                                                                                                                                                | . . . . . . . . . . . . . . . . 55   |
|    | 7.2                                                  | Combination and Partition lemmas . . . .                                                                                                                                   | . . . . . . . .                                                                                                                                                            | . . . . . . . . . . . . . . . . 56   |
|    | 7.3                                                  | Alternative proof of the linear complexity of the Delaunay triangulation                                                                                                   | Alternative proof of the linear complexity of the Delaunay triangulation                                                                                                   | . . . . . . . 57                     |
|    | 7.4                                                  | Formalized method . . .                                                                                                                                                    | . . . . . . . . . . . . . . . . . .                                                                                                                                        | . . . . . . . . . . . . . . . . 57   |
|    | 7.5                                                  | Expected degree in some empty singleton-region graphs . . . .                                                                                                              | Expected degree in some empty singleton-region graphs . . . .                                                                                                              | . . . . . . . . . . . . . 58         |
| 8  | Empty axis-aligned ellipse graphs                    | Empty axis-aligned ellipse graphs                                                                                                                                          | Empty axis-aligned ellipse graphs                                                                                                                                          | 61                                   |
|    | 8.1                                                  | Some features with axis-aligned ellipses                                                                                                                                   | . . . . . . . . . .                                                                                                                                                        | . . . . . . . . . . . . . . . . 61   |
|    | 8.2                                                  | Empty axis-aligned ellipse graph . . .                                                                                                                                     | . . . . . . . . . . .                                                                                                                                                      | . . . . . . . . . . . . . . . . 62   |
|    |                                                      | 8.2.1                                                                                                                                                                      | Upper bound on the expected degree . . . . . . .                                                                                                                           | . . . . . . . . . . . . . . . . 62   |
|    |                                                      | 8.2.2 Lower bound on the expected degree                                                                                                                                   | . . . . . . .                                                                                                                                                              | . . . . . . . . . . . . . . . . 64   |
|    | 8.3                                                  |                                                                                                                                                                            | Ellipses with bounded aspect ratio, the rhombus graph .                                                                                                                    | . . . . . . . . . . . . . . . . 66   |
|    |                                                      | 8.3.1                                                                                                                                                                      | An upper bound on the expected degree . . . . .                                                                                                                            | . . . . . . . . . . . . . . . . 67   |
|    |                                                      | 8.3.2 A lower bound on the expected degree                                                                                                                                 | . . . . . .                                                                                                                                                                | . . . . . . . . . . . . . . . . 69   |
|    | 8.4                                                  | On empty axis-aligned ellipse graphs with a single aspect ratio . . .                                                                                                      | On empty axis-aligned ellipse graphs with a single aspect ratio . . .                                                                                                      | . . . . . . . . . . 70               |
| 9  | On the probability of the existence of far neighbors | On the probability of the existence of far neighbors                                                                                                                       | On the probability of the existence of far neighbors                                                                                                                       | 73                                   |
|    | 9.1                                                  | In the Delaunay triangulation                                                                                                                                              | . . . . . . . . . . . . . . .                                                                                                                                              | . . . . . . . . . . . . . . . . 73   |
|    | 9.2                                                  | In the empty axis-aligned graph with bounded aspect ratio. . . .                                                                                                           | In the empty axis-aligned graph with bounded aspect ratio. . . .                                                                                                           | . . . . . . . . . . . 73             |
| 10 | Analysis of two additional empty region graphs       | Analysis of two additional empty region graphs                                                                                                                             | Analysis of two additional empty region graphs                                                                                                                             | 79                                   |
|    | 10.1 Empty ellipse graph with bounded aspect         | 10.1 Empty ellipse graph with bounded aspect                                                                                                                               | ratio . . . . . .                                                                                                                                                          | . . . . . . . . . . . . . . . . 79   |
|    | 10.2 Empty 4/2-ball graph                            | 10.2 Empty 4/2-ball graph                                                                                                                                                  | . . . . . . . . . . . . . . . . . . . .                                                                                                                                    | . . . . . . . . . . . . . . . . 81   |


<!-- p:14 -->


85

| 11 On nearest-neighbor-like graphs, a way to compute some integrals                                                                                 | 85                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| 11.1 The nearest-neighbor graph . . . .                                                                                                             | . . . . . . . . . . . . . . . . . . . . . . . . . . . . 85                                             |
| 11.2 Formalization                                                                                                                                  | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 86                     |
| 11.3 Application of nearest-neighbor-like graphs                                                                                                    | . . . . . . . . . . . . . . . . . . . . . . . . 87                                                     |
| III 3D-Delaunay triangulation for two                                                                                                               |                                                                                                        |
| specific surfaces                                                                                                                                   | 89                                                                                                     |
| 12.1 The right circular cylinder                                                                                                                    | 93 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 93                                |
| 12.2 Description of the fundamental regions on the cylinder                                                                                         | . . . . . . . . . . . . . . . . . 94                                                                   |
| 12.3 Proof of the graph inclusion .                                                                                                                 | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 95                                       |
| 12.4 Computation of an upper bound on E [ ♯ Del( X )] .                                                                                             | . . . . . . . . . . . . . . . . . . . . 96                                                             |
| 12.5 A lower bound on E [ ♯ Del( X )] . . .                                                                                                         | . . . . . . . . . . . . . . . . . . . . . . . . . . . . 99                                             |
| 12.6 Conjecture on two classes of surface . . . . .                                                                                                 | . . . . . . . . . . . . . . . . . . . . . . . 103                                                      |
|                                                                                                                                                     | 13 105                                                                                                 |
| Delaunay triangulation of a Poisson process on an oblate spheroid                                                                                   | 13.1 The oblate spheroid . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 105 |
| 13.1.1 Some generalities on the oblate spheroid . . .                                                                                               | . . . . . . . . . . . . . . . . . . 105                                                                |
| 13.2 Overview of the proof . . . . . . . . . . . . . . . . . . . . . .                                                                              | . . . . . . . . . . . . . . 107                                                                        |
| 13.3 On the probability of existence of neighbors far from the medial sphere. . . .                                                                 | . . . . . 111                                                                                          |
| 13.4 Expected number of close neighbors ( Proof of Lemma 13.1 ) . . . . . . . .                                                                     | . . . . . . 116                                                                                        |
| 13.4.1 General scheme . .                                                                                                                           | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 117                                        |
| . . .                                                                                                                                               | . . . . . . . . 117                                                                                    |
| 13.4.2 Description of the regions of F 1 on the spheroid . . . . . . . . . 13.4.3 Choice of specific spheres for q on the side of p with respect to |                                                                                                        |
| P Med 13.4.4 Proof of the graph inclusion . . . . . . . . . . . . . . . . . . . . . .                                                               | . . . . . 119                                                                                          |
| 13.4.5 When q is on the side of p with respect to P . . . . . . . . . . .                                                                           | . . . . . . 131                                                                                        |
| Computation of an upper bound on the                                                                                                                | Med . . . . . . 133                                                                                    |
| 13.4.6 expected number of close neighbors.                                                                                                          | . 134                                                                                                  |
| 13.4.7 On some geometric quantities close to Z . . . . . . . . . . . . .                                                                            | . . . . . . . . . 138                                                                                  |
| 13.4.8 On the probability of existence Delaunay neighbors outside CN( p ).                                                                          | . . . . . . 141                                                                                        |
| Expected degree of a point close to Z Proof of Lemma 13.3 .                                                                                         | 13.5 ( ) . . . . . . . . . . . . . 142                                                                 |
| 13.5.1 Description of fundamental regions on the spheroid .                                                                                         | . . . . . . . . . . . . . . 143                                                                        |
| 13.5.2 Choice of specific spheres .                                                                                                                 | . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 143                                          |
|                                                                                                                                                     | 13.5.3 Proof of the graphs inclusion . . . . . . . . . . . . . . . . . . . . . . . . . . . . 148       |
| 13.5.4 Computation of an upper                                                                                                                      | bound on the expected degree . . . . . . . . . . . . 149                                               |
|                                                                                                                                                     | 13.5.5 On the probability of existence Delaunay neighbors outside MRN ( p ) . . . . . . 152            |
| 14.1 Simulation . . . .                                                                                                                             | 155 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 156                        |
| . .                                                                                                                                                 |                                                                                                        |
|                                                                                                                                                     | 14.2 Experimental results . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 158  |


<!-- p:15 -->


## IV Expected size of the 3D-Delaunay triangulation of a Poisson point process distributed on a generic surface 161

| process distributed on a generic surface   | process distributed on a generic surface                                  | process distributed on a generic surface                                                                                                        | 161                             |
|--------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| 15 Generic surfaces                        | 15 Generic surfaces                                                       | 15 Generic surfaces                                                                                                                             | 165                             |
|                                            | 15.1 What                                                                 | is generic or not in an oblate spheroid . . . . . . . . . . . . . . . . .                                                                       | . . . . . . 165                 |
|                                            | 15.1.1                                                                    | Common points between an oblate spheroid and a generic surface .                                                                                | . . . . . . 165                 |
|                                            | 15.1.2                                                                    | Differences between an oblate spheroid and a generic surface . . . .                                                                            | . . . . . . 166                 |
|                                            | 15.2 Sketch . . . . .                                                     | of proof . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                              | . . . . . . 166                 |
|                                            | 15.2.1                                                                    | Decomposition of the generic surface . . . . . . . . . . . . . . . . .                                                                          | . . . . . . 167                 |
|                                            | 15.2.2                                                                    | Approach of the proof . . . . . . . . . . . . . . . . . . . . . . . . .                                                                         | . . . . . . 167                 |
| 16 Expected local degree of a point        | 16 Expected local degree of a point                                       | 16 Expected local degree of a point                                                                                                             | 169                             |
|                                            | 16.1 Local degree of a point on the convex hull and a little beyond . . . | . . . .                                                                                                                                         | . . . . . . 169                 |
|                                            | 16.1.1                                                                    | Choice of the specific spheres . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . 170                 |
|                                            | 16.1.2                                                                    | Proof of the graph inclusion . . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . 171                 |
|                                            | 16.1.3                                                                    | Computation of the expected local degree . . . . . . . . . . . . . .                                                                            | . . . . . . 171                 |
|                                            | 16.2 Local                                                                | degree of a point far from the convex hull and from Z . . . . . . . .                                                                           | . . . . . . 172                 |
|                                            | 16.2.1                                                                    | Choice of the specific spheres . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . 172                 |
|                                            | 16.2.2                                                                    | Proof of the graph inclusion . . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . 179                 |
|                                            | 16.2.3                                                                    | Computation of the expected degree . . . . . . . . . . . . . . . . .                                                                            | . . . . . . 181                 |
|                                            | 16.3 Local                                                                | degree of a point close to Z or Y . . . . . . . . . . . . . . . . . . . .                                                                       | . . . . . . 182                 |
|                                            | 16.3.1                                                                    | On the position of p and the value 1 - κ 1 ( p ) r ∗ ( p ) . . . . . . . . . .                                                                  | . . . . . . 182                 |
|                                            | 16.3.2                                                                    | Local degree of a point at distance h p from Z . . . . . . . . . . . .                                                                          | . . . . . . 184                 |
|                                            | 16.3.3                                                                    | Local degree of a point close to Y . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . 185                 |
| 17 Expected remote degree of a point       | 17 Expected remote degree of a point                                      | 17 Expected remote degree of a point                                                                                                            | 187                             |
|                                            | 17.1 Far from the convex hull and with one symmetrical point . . . . . .  | . . . .                                                                                                                                         | . . . . . . 187                 |
|                                            | 17.2 Close                                                                | to points with multiple symmetrical points . . . . . . . . . . . . . . .                                                                        | . . . . . . 189                 |
|                                            | 17.2.1                                                                    | Supplementary symmetrical points . . . . . . . . . . . . . . . . . . 17.2.2 Counting of the remote Delaunay neighbors . . . . . . . . . . . . . | . . . . . . 190 . . . . . . 191 |
|                                            |                                                                           | . . . . . . . . . . . . . . . . . . .                                                                                                           | . . . . . . 192                 |
|                                            | 17.3 Close 17.3.1 Points close to the                                     | to the boundary of the convex hull boundary of the convex hull, and inside S . . . .                                                            | . . . . . . 192                 |
|                                            | 17.3.2                                                                    | Points close to the convex hull, inside H . . . . . . . . . . . . . . .                                                                         | . . . . . . 192                 |
|                                            |                                                                           | ′ .                                                                                                                                             |                                 |
|                                            | 17.4 Remote                                                               | neighbors of points close to Z or to Y . . . . . . . . . . . . . . .                                                                            | . . . . . . 193                 |
| 18 Remaining neighbors                     | 18 Remaining neighbors                                                    | 18 Remaining neighbors                                                                                                                          | 195                             |
|                                            | 18.1 On the probability that p                                            | has a Delaunay neighbor outside Loc( p ) ∪ Rem( p )                                                                                             | . . . . . 195                   |
|                                            | 18.2                                                                      | Middle-range neighbors of a point in Z + . . . . . . . . . . . . . . . . . . .                                                                  | . . . . . . 197                 |
|                                            | 18.2.1                                                                    | Choice of the specific spheres when q is on the side of p . . . . . . .                                                                         | . . . . . . 197                 |
|                                            | 18.2.2 18.2.3 Computation of                                              | If q is on the side of p with respect to P Bis ( p, p ) . . . . . . . . . . . the expected degree . . . . . . . . . . . . . . . . .             | . . . . . . 202 . . . . . . 203 |
|                                            | 18.2.4                                                                    | Unlikely neighbors . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                        | . . . . . . 205                 |


<!-- p:16 -->


| 18.2.5 Expected size of the Delaunay triangulation . . . . . . .           | . . . . . . . . . . . . 205   |
|----------------------------------------------------------------------------|-------------------------------|
| Conclusion                                                                 | 207                           |
| Appendices                                                                 | 209                           |
| A.1 Jacobian of the Blaschke-Petkantschin variables substitution . .       | . . . . . . . . . . . . 209   |
| A.2 Some integrals . . . . . . . . . . . . . . . . . . . . . . . . . . . . | . . . . . . . . . . . . 210   |
| A.3 The set of 4/2-balls passing through two points is a good pencil       | . . . . . . . . . . . . 212   |
| Bibliography                                                               | 218                           |


<!-- p:17 -->


##### List of Figures

|   1.1 | A regular parametric curve . . . . . . . . . . . . . . . . . . . . . . . . . . . . .            | . . . . . . 10   |
|-------|-------------------------------------------------------------------------------------------------|------------------|
|   1.2 | An osculating circle . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .          | . . . . . . 10   |
|   1.3 | The evolute of an ellipse . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .         | . . . . . . 12   |
|   1.4 | Three different contact types . . . . . . . . . . . . . . . . . . . . . . . . . . . .           | . . . . . . 12   |
|   1.5 | The medial axis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .         | . . . . . . 13   |
|   1.6 | The principal curvatures . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .          | . . . . . . 14   |
|   1.7 | Two tangent spheres with maximal curvature on both sides of surface . . . . .                   | . . . . . . 15   |
|   1.8 | The sets Z and Y . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .          | . . . . . . 17   |
|   1.9 | Generic medial axis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .         | . . . . . . 19   |
|  1.10 | Convex part and simple points . . . . . . . . . . . . . . . . . . . . . . . . . . .             | . . . . . . 20   |
|  1.11 | The sets Z , Z ′ , S ′ and Y ′ . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .      | . . . . . . 21   |
|   2.1 | A representation of a graph . . . . . . . . . . . . . . . . . . . . . . . . . . . . .           | . . . . . . 23   |
|   2.2 | A plane graph with a vertex with high degree . . . . . . . . . . . . . . . . . . .              | . . . . . . 24   |
|   2.3 | An instance of Delaunay triangulation . . . . . . . . . . . . . . . . . . . . . . .             | . . . . . . 26   |
|   2.4 | A quadratic case for the 3D-Delaunay triangulation . . . . . . . . . . . . . . . .              | . . . . . . 27   |
|   3.1 | Blaschke-Petkantchin variables substitution . . . . . . . . . . . . . . . . . . . .             | . . . . . . 31   |
|   4.1 | The Voronoi diagram . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .           | . . . . . . 34   |
|   4.2 | A super-linear triangulation of points on a surface . . . . . . . . . . . . . . . .             | . . . . . . 38   |
|   4.3 | The half-moons of two points . . . . . . . . . . . . . . . . . . . . . . . . . . . .            | . . . . . . 38   |
|   4.4 | Right triangle included in ellipse . . . . . . . . . . . . . . . . . . . . . . . . . .          | . . . . . . 39   |
|   5.1 | Illustration of the proof of Lemma 5.3 for the 2D case. . . . . . . . . . . . . . .             | . . . . . . 42   |
|   5.2 | A maximal packing . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .           | . . . . . . 44   |
|   6.1 | Gabriel, Delaunay and half-moon graphs . . . . . . . . . . . . . . . . . . . . . .              | . . . . . . 52   |
|   7.1 | Any disk contains a half-moon . . . . . . . . . . . . . . . . . . . . . . . . . . .             | . . . . . . 58   |
|   8.1 | Axis-aligned ellipses partition and fundamental regions, unbounded aspect ratio                 | . . . . . . 63   |
|   8.2 | xy -Ell ellipses and a realization of G ∅ { xy -Ell } . . . . . . . . . . . . . . . . . . . . . | . . . . . . 65   |
|   8.3 | Axis-aligned ellipses partition and fundamental regions, bounded aspect ratio .                 | . . . . . . 67   |
|   8.4 | β -Ell ellipses and a realization of G ∅ { β -Ell } . . . . . . . . . . . . . . . . . . . . . . | . . . . . . 69   |
|   9.1 | Far neighbors in 2D-Delaunay . . . . . . . . . . . . . . . . . . . . . . . . . . . .            | . . . . . . 74   |
|   9.2 | Far neighbors in the empty ellipse graph . . . . . . . . . . . . . . . . . . . . . .            | . . . . . . 75   |
|  10.1 | Triangle included in ellipse . . . . . . . . . . . . . . . . . . . . . . . . . . . . .          | . . . . . . 79   |
|  10.2 | The family of regions B 4/2 ( p, q ) . . . . . . . . . . . . . . . . . . . . . . . . . . .      | . . . . . . 81   |
|  11.1 | A monotonic pencil of lemniscates . . . . . . . . . . . . . . . . . . . . . . . . .             | . . . . . . 88   |


<!-- p:18 -->


93

|   12.1 | A right circular circular cylinder . . . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 93   |
|--------|------------------------------------------------------------------------------------------------|--------------------------------------|
|   12.2 | Fundamental regions on the cylinder . . . . . . . . . . . . . .                                | . . . . . . . . . . . . . . . . 95   |
|   12.3 | Partition of the bisector plane for the cylinder . . . . . . . . .                             | . . . . . . . . . . . . . . . . 97   |
|   13.1 | The oblate spheroid . . . . . . . . . . . . . . . . . . . . . . .                              | . . . . . . . . . . . . . . . . 106  |
|   13.2 | The center of a shrunken sphere from p lies on a spheroid . .                                  | . . . . . . . . . . . . . . . . 112  |
|   13.3 | The family F γ 0 of triangles . . . . . . . . . . . . . . . . . . . .                          | . . . . . . . . . . . . . . . . 115  |
|   13.4 | Partition of the bisector plane for V 1 . . . . . . . . . . . . . .                            | . . . . . . . . . . . . . . . . 133  |
|   13.5 | Sphere passing through two opposite points of a quadrilateral                                  | . . . . . . . . . . . . . . . . 134  |
|   13.6 | A disk sector . . . . . . . . . . . . . . . . . . . . . . . . . . .                            | . . . . . . . . . . . . . . . . 135  |
|   13.7 | Fundamental family F 2 of regions . . . . . . . . . . . . . . . .                              | . . . . . . . . . . . . . . . . 144  |
|   13.8 | The bisector plane partitioned for F 2 . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 148  |
|   13.9 | The family of regions F ∗ 2 ( p, q ) . . . . . . . . . . . . . . . . . .                       | . . . . . . . . . . . . . . . . 150  |
|   14.1 | Two spheroids . . . . . . . . . . . . . . . . . . . . . . . . . . .                            | . . . . . . . . . . . . . . . . 155  |
|   14.2 | Different coordinate systems . . . . . . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 156  |
|   14.3 | Differential surface element on a spheroid . . . . . . . . . . .                               | . . . . . . . . . . . . . . . . 157  |
|   14.4 | Simulations on a generic surface . . . . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 159  |
|   14.5 | Simulations on a non generic surface . . . . . . . . . . . . . .                               | . . . . . . . . . . . . . . . . 159  |
|   15.1 | Choice of orientation on self-including surface . . . . . . . . .                              | . . . . . . . . . . . . . . . . 167  |
|   15.2 | Decomposition of the surface . . . . . . . . . . . . . . . . . .                               | . . . . . . . . . . . . . . . . 168  |
|   16.1 | Definition of ω p ( q ) . . . . . . . . . . . . . . . . . . . . . . . .                        | . . . . . . . . . . . . . . . . 176  |
|   16.2 | Distance &#124; pω p ( q ) &#124; with respect to &#124; pq &#124; . . . . . . . . . . . . . . | . . . . . . . . . . . . . . . . 177  |
|   16.3 | The intersection locally included in a strip . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 178  |
|   16.4 | The partition of the bisector plane . . . . . . . . . . . . . . .                              | . . . . . . . . . . . . . . . . 180  |
|   17.1 | ω p ( q ) in the generic case . . . . . . . . . . . . . . . . . . . . .                        | . . . . . . . . . . . . . . . . 188  |
|   17.2 | A point p can have Delaunay neighbors far from { p, p } . . . .                                | . . . . . . . . . . . . . . . . 190  |
|   17.3 | Supplementary symmetrical point . . . . . . . . . . . . . . . .                                | . . . . . . . . . . . . . . . . 191  |
|   17.4 | The curves S ′ , Z and W in Z ′ + . . . . . . . . . . . . . . . . .                            | . . . . . . . . . . . . . . . . 193  |
|   18.1 | Intersection of σ Low with S . . . . . . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 198  |
|   18.2 | Intersection of σ Osc with S . . . . . . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 200  |
|   18.3 | Intersection of σ 0 Sym with S . . . . . . . . . . . . . . . . . . .                           | . . . . . . . . . . . . . . . . 201  |
|   18.4 | Intersection of σ Norm with S . . . . . . . . . . . . . . . . . . .                            | . . . . . . . . . . . . . . . . 201  |
|   18.5 | Intersection of σ ∞ Sym with S . . . . . . . . . . . . . . . . . . .                           | . . . . . . . . . . . . . . . . 202  |
|   18.6 | Intersection of σ 2 and σ 1 with S . . . . . . . . . . . . . . . .                             | . . . . . . . . . . . . . . . . 202  |
|   18.7 | The partition of P Bis ( p, q ) for p and q close to Z . . . . . . .                           | . . . . . . . . . . . . . . . . 203  |
|   18.8 | And the corresponding regions . . . . . . . . . . . . . . . . .                                | . . . . . . . . . . . . . . . . 203  |
|   18.9 | The triangles when q is on the side of p . . . . . . . . . . . .                               | . . . . . . . . . . . . . . . . 204  |


<!-- p:19 -->


## Introduction

This thesis aims at evaluating the size of the Delaunay triangulation of points drawn on a surface with a random distribution. In this introduction, we give an explanation of the concepts involved in this problem, and present how this thesis is organized to solve it. The Delaunay triangulation, and its dual, the Voronoi diagram, are geometrical objects that appeared recurrently in the scientific history [LP12]. In dimension 2, the Voronoi diagram of a set of points X is a decomposition of the plane into convex polygons (also called cells), one for each point of X, such that the cell of p ∈ X is the set of points closer to p than to any other point of X. On the other hand, the Delaunay triangulation is the set of triangles for which the circumscribing circle does not contain other points of X [Del34]. The Voronoi diagram and the Delaunay triangulation share a duality property: the circumcenters of the Delaunay triangles are the vertices of the cells of the Voronoi diagrams. These definitions are generalizable in higher dimensions. The first appearance of the Delaunay triangulation seems to be due to Johannes Kepler in 1611 in his paper "On the Six-Cornered Snowflake", in which Kepler studied the famous problem of sphere packing. Later, they reappeared in astronomy with René Descartes, and in epidemiology in the 19th century when John Snow used a Voronoi diagram to identify geographic sources of a cholera epidemic. It is during the 20th century that the Russian mathematician Georges Voronoi formalized the now-called Voronoi diagram in any dimension [Vor08]. Its student, Boris Delaunay, then formalized the Delaunay triangulation in his paper "Sur la sphère vide" [Del34]. In the meantime, the Delaunay triangulation and Voronoi diagram were involved in disciplines as various as crystallography, metallurgy, meteorology [OBS92], or more recently, quantum gravity [BCW09]. Today, the Delaunay triangulation is one the most studied structures in computational geometry. Because of its properties, the Delaunay triangulation can be used to create efficient meshing for solving differential equations. In algorithmics, it can be used to obtain, for instance, the minimal covering tree of a set of points. A field in which the results of this thesis may be significant, is geometric modeling [FP09, BDTY00]. Indeed, for the problem of surface reconstruction [ACK01, AB99], the Delaunay triangulation can play an intermediate but necessary role. The problem is the following: compute a piecewise linear approximation of a surface from a set of sample points. Since some algorithms use the 3-dimensional Delaunay triangulation as a step for the surface reconstruction, we can be interested in knowing the combinatorial complexity (more simply called size) of the Delaunay triangulation of such points. This size may impact both the time and memory complexities of the reconstruction algorithm. For the 2 dimensional case, as it will be explained in Part I, we know that the size of the Delaunay triangulation remains linear with the number of points. In 3 dimension, it is not anymore the case. The size of the 3D-Delaunay triangulation can range from linear to quadratic. This size depends on how the points are distributed in R3. Concerning the surface reconstruction problem, the points are supposed to be distributed on the surface we want to reconstruct. Thus the size of the Delaunay triangulation will depend both on the surface on which the points are distributed, and on how they are distributed on this surface. To mathematically model the points, we need to choose a sample type. It can be a deterministic sample, with good properties like "any disk of a given radius contains at least one sample point". We will call such a deterministic sample a good sample. But the sample also can be random, like a uniform sample or a Poisson point process. In both cases, we consider that the number of points goes to infinity, and compute an asymptotic approximation of the size of the Delaunay triangulation. As we will explain

in Part I, Chapter 4, Erickson found a good sample of n points distributed on a cylinder of revolution for


<!-- p:20 -->


2

which the Delaunay triangulation is O(n√n) [Eri05]. The construction of such a sample is very specific, and the fact that the cylinder is a surface of revolution, induces a pathological behavior for the Delaunay triangulation. Conversely, when a good sample is distributed on a generic surface, Erickson [Eri01b] and conjointly, Attali et al. [ABL03] proved that the Delaunay triangulation is O(n log n), where the hidden constant in the big O depends on characteristics of the surface, like its diameter, its maximal curvature, etc... The definition of a generic surface will be given later, for now, keep in mind that a generic surface is a surface that has "typical" properties, like no particular symmetries. Later Devillers et al. [DEG08] showed that when a uniform random sample is distributed on a cylinder, the Delaunay triangulation has an expected size Θ(n log n), proving by the way that some deterministic constructions are quite pathological.

These works open a door to a natural question:

What is the expected size of the 3D-Delaunay triangulation of a random sample distributed on a surface?

It is the problem we try to solve in this thesis. Note that the result may depend on the surface, in particular we are interested in the case of generic surfaces, for which experimental results seem to show a linear bound.

To model points, we choose to use a Poisson point process since it verifies properties of homogeneity and independence that are convenient for the computations. We denoted the Poisson point process by X. Such a process goes along with a parameter called intensity, denoted by λ, that corresponds to the expected number of points we may find in a region of area 1. Thus without loss of generality we may consider that the surface on which the points are distributed has area 1, so that the expected number of points distributed on the surface is λ.

In Part I, Chapter 5, we present a first solution of the problem by applying directly the result of Attali et al. described above for good deterministic sample to Poisson point process. Nevertheless, the resulting bound for Poisson process cannot be better than the original one for good sample, and we only show that the Delaunay triangulation has expected size O(λ log2 λ). One the main issue of this method, is that it does not use at all the fact that the data sample is a Poisson process but just that it is a good sample with high probability, and thus we actually don't exclude pathological cases.

To efficiently use the properties of a Poisson process, we have to take a different approach. In order to prove the expected O(n log n) bound for the uniform sample distributed on a cylinder, Devillers et al. remarked that the intersection of the cylinder with a sphere passing though two points p and q on -  s  t s t     et d  s s  e dimensional graph in which two points are neighbors if there exists such a triangle that does not contain other data points. Such a graph has expected size Θ(n log n), and this is how they obtain the O(n log n) bound. This "empty triangle" graph is a particular case of empty region graphs. In Part II, we define a kind of empty region graphs, we formalize a method to compute lower and upper bounds on their expected size, and give tight results for such graphs.

As Attali et al. pointed out, the intersection of a sphere with a generic surface has almost an elliptic shape, aligned with the curvature directions of the surface. This leads us to study a particular empty region graph for which the regions are axis-aligned ellipses. We prove, in Part II, Chapter 8, that if the involved ellipses have an aspect ratio ranging from β to 1, with 0 &lt; β &lt; 1, then the expected number of neighbors of any point in the graph is Θ (ln

In order to illustrate the method developed in Part II, we compute, in Part III, tight asymptotic bounds e   r t ss t  i -   s e  o consider a cylinder of revolution, as in [DEG08], and reprove the Θ (λln λ) bound but for a Poisson point process. Considering the similarity between uniform and Poisson sample, the goal of this chapter is mainly to present concretely the method in a 3-dimensional simple case. Then, in Chapter 13, we compute the size of the 3D-Delaunay triangulation of a Poisson process distributed on an oblate spheroid (a flattened sphere). This surface has enough generic properties for the Delaunay triangulation to behave well. In particular, conversely to the cylinder, its medial axis is bi-dimensional. Using empty axis-aligned ie  s       tt   e le  e se provides a smooth surface on which a Poisson point process has a 3D-Delaunay triangulation that is


<!-- p:21 -->


3

linear. In Chapter 14, we simulate a Poisson process on both an oblate and a prolate spheroid to show that our results are experimentally correct. Finally in Part IV, we treat the case of generic surfaces. Even if an oblate spheroid is a specific surface, we will be able to reuse some computations in this part up to some adaptations. Indeed the oblate spheroid is the surface of a convex body, that is not generally the case. It has a lot of symmetries, that is not generally the case either. In this part, we focus more on how to deal with these adaptations than on the computations that were already quite tedious in the spheroid case.


<!-- p:22 -->


Part I

##### Presentation of general notions, state of the art, and a first approach


<!-- p:23 -->


####### Preamble of Part I

In this thesis, we provide a method to compute the expected size of some empty region graphs, and in particular, of the Delaunay triangulation of points on a surface, for a set of points that is a Poisson point process. The understanding of the subject requires knowledge in at least three main fields of mathematics and computer sciences: Geometry, Combinatorics and Probabilities. To be brief, a Poisson point process is a random set of points, quite practical for computations. An empty region graph is a specific kind of geometric graph of which the Delaunay triangulation is an example. The size of a graph corresponds roughly to the number of its edges. Since the vertices of the graphs studied are drawn from a Poisson point process, the number of edges of the graphs is a random value. We compute the expectation of this value, that corresponds, in some sense, to a probabilistic average value. To explain in detail such notions, we decompose this part into three chapters. Chapter 1 will be dedicated to geometry. We will use it to recall some basic mathematical notions, and present some notations we will use. Then we dedicate a section to the geometry of plane curves, in particular to describe the notion of curvature. Finally, in the last section of the chapter, we explain the concept of generic surface, and present specific features that generic surfaces have. Chapter 2 is dedicated to combinatorics. We present the notion of graphs, and some tools like Euler's formula that we use to compute their size. Then we define what is the Delaunay triangulation of a set of points, and explain how its size vary in dimension 2 and 3. In Chapter 3, we present the probabilistic tools that we will use. We start by explaining what is Poisson point process, and what are its properties. Then we present one of the most used formula of the thesis: the Slivnyak-Mecke formula, that serves in computing some expected value. We illustrate the use of this formula through the example of the 2D-Delaunay triangulation. In Chapter 4, we present the state of the art of the problem of determining the size of the 3D-Delaunay triangulation of points on a surface. We present how evolved this computation depending on the subset of R3 where the points are distributed, and how they are distributed. Indeed we start by presenting the case of points randomly distributed in the unit cube, which has linear size in expectation. Then we consider that the points are distributed on a surface of R3. In that case, we first present the case of a polyhedral surface. For both a deterministic or a random sample, it has been shown that the triangulation is linear. Then we present a result based on a parameter of the distribution of point called the spread. Finally we consider that points are distributed on a smooth surface. Whatever is the kind of sample, we present that if points are distributed on a cylinder, the triangulation is not anymore linear. Then we present the study that have been made on generic surfaces, that exclude the cylinder. Generic surfaces had only been studied with deterministic sample. Finally, in Chapter 5, we introduce the first contribution of this thesis, computing the size of the 3D-Delaunay triangulation of random points distributed on a generic surface, by showing that a random sample verifies the properties of a good deterministic with high probability.


<!-- p:24 -->


## Chapter 1

### Geometry

In this first chapter, we present the basics on geometry that we will use all along the thesis. Geometry is omnipresent in this thesis since we study the combinatorial complexity of Delaunay triangulation (that is a geometric graph), of a Poisson point process (whose formulas involve the geometric size of region), distributed on surfaces.

The fact that the points are distributed on surfaces, commits us to study the notion of curvature. We introduce this notion on curves in Section 1.1, in which we also present what is the medial axis of a curve.

In Section 1.2, we extend those notions to surfaces, and show how we can parameterize a surface at any point.

Finally in Section 1.3, we present the notion of genericity and what it induces on surfaces.

#### 1.1 Geometry of plane curves

Before talking about surfaces, we recall some classical notions about the geometry of plane curves. These notions will be extended to the case of surfaces.

##### 1.1.1 The notion of curvature

We consider the definition of a smooth planar curve from Porteus [Por01]:

Definition 1.1. A smooth parametric curve in R2 is a smooth map

$$\gamma \colon \mathbb { R } & \to \mathbb { R } ^ { 2 } \\ t & \mapsto \gamma ( t ) ,$$

with domain an open connected subset of R. It is said regular at t if its first derivative γ'(t) is non-zero.

(x(t) When it is necessary, we will write γ(t) = At a regular point t, we can define the tangent of (y(t)) a curve γ. Its expression is given by:

$$\mathcal { T } _ { \gamma } ( t ) \, \colon \, u \mapsto \gamma ( t ) + u \gamma ^ { \prime } ( t ) ,$$

whn sod (  l ao  Aou     o  s (e, uh y'(t) γ(t) is called the normal of γ at t. It is directed by the vector nγ(t) := When there are no −x′(t) ambiguity on the curve, we will usually say "the tangent of γ(t)" instead of the tangent of γ at t.

In a sense, the tangent corresponds to the "closest" line to the curve. The one that approximates the curve at the first order derivative. This notion of closeness can be extended, not only to lines, but also to circles. We search, at any point t, a notion of closest circle to the curve at t. Consider a circle centered on c and passing through p, and let γc be a parameterization of this circle. For any t, γc(t) verifies:


<!-- p:25 -->


Figure 1.1: The regular curve t → (t, t3)

y

x

t

γ(t) =

t3

$$\| c - \gamma _ { \mathcal { C } } ( t ) \| ^ { 2 } = \| c - p \| ^ { 2 } \, .$$

We can derivate successively this equation to obtain new equations that involve the derivatives of γc. Note that∥c − p|2 is constant.

$$( c - \gamma _ { \mathcal { C } } ( t ) ) \cdot \gamma _ { \mathcal { C } } ^ { \prime } ( t ) & = 0 , \\ ( c - \gamma _ { \mathcal { C } } ( t ) ) \cdot \gamma _ { \mathcal { C } } ^ { \prime \prime } ( t ) - \| \gamma _ { \mathcal { C } } ^ { \prime } ( t ) \| ^ { 2 } & = 0 ,$$

and so on, but it is not necessary to go further. For a given γc(t), the equations above define the center c. The circle we search is the one centered on c that is defined by those equations in which we have substituted γc and its derivatives, by γ and its derivatives,

Definition 1.2. The osculating circle of γ at a regular point t is the circle passing through γ(t) and centered on c(t) where c(t) verifies:

$$\begin{array} { c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c$$

The radius of curvature of γ at t is then the radius of the osculating circle at t, and the curvature κ(t) of γ at t is the inverse of the radius of curvature.

Figure 1.2: The circle osculating γ at t.

c(t)

Q

Tγ(t)

1

κ(t)

γ(t)


<!-- p:26 -->


We can obtain a parametric expression of the curvature κ(t) of γ at any regular point t by isolating the vector c(t) − γ(t) in Equation 1.1, as it is done in [GAS17]. Indeed the radius of curvature of γ at t is defined by the radius of the osculating circle, that is ∥c(t) − γ(t)|. So we rewrite (c(t) − γ(t)) · γ"(t). Since c(t) − γ(t) and nγ(t) are in the same direction, we have:

$$( c ( t ) - \gamma ( t ) ) \cdot \gamma ^ { \prime \prime } ( t ) & = \| \gamma ^ { \prime } ( t ) \| ^ { 2 } \\ & = \frac { \| \gamma ^ { \prime } ( t ) \| ^ { 2 } } { n _ { \gamma } ( t ) \cdot \gamma ^ { \prime \prime } ( t ) } n _ { \gamma } ( t ) \cdot \gamma ^ { \prime \prime } ( t ) ,$$

$$( c ( t ) - \gamma ( t ) ) = \frac { \| \gamma ^ { \prime } ( t ) \| ^ { 2 } } { n _ { \gamma } ( t ) \cdot \gamma ^ { \prime \prime } ( t ) } n _ { \gamma } ( t ) .$$

y'(t) Since nγ(t) = we have∥nγ(t)| =∥|γ′(t)||, it follows that: −x′(t)

$$| | c ( t ) - \gamma ( t ) | | & = \frac { | | \gamma ^ { \prime } ( t ) | | ^ { 3 } } { | y ^ { \prime } ( t ) x ^ { \prime \prime } ( t ) - x ^ { \prime } ( t ) y ^ { \prime \prime } ( t ) | } , \text { and} \\ \kappa ( t ) & = \frac { | y ^ { \prime } ( t ) x ^ { \prime \prime } ( t ) - x ^ { \prime } ( t ) y ^ { \prime \prime } ( t ) | } { | \gamma ^ { \prime } ( t ) | | ^ { 3 } } . \\$$

This non-signed curvature is called the geometric curvature. Its oriented version, also called algebraic curvature, is given by:

$$\frac { n _ { \gamma } ( t ) \cdot \gamma ^ { \prime \prime } ( t ) } { \| \gamma ^ { \prime } ( t ) \| ^ { 3 } } . \\ \cdots .$$

Roughly, it is positive when the curve "turns" in the direction of the normal.

We state this result in the case of curves parameterized as graphs of functions:

Proposition 1.3. Let f : R → R be a smooth function. The geometric curvature of the curve y = f(x) is given at x by:

$$\kappa ( x ) = \frac { | f ^ { \prime \prime } ( x ) | } { \left ( 1 + ( f ^ { \prime } ( x ) ) ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } .$$

At some point in the thesis, we have to consider the points of maximum of curvature of a surface. We present here a theorem that states that such points exists even on quite simple cases. The theorem can be found in [Por01].

Theorem 1 (Four-Vertex theorem). Let γ be a closed connected regular smooth plane curve with no self intersection. Then γ has at least two local minima and two local maxima of curvature.

The theorem is not that easy to extend on surfaces, but it gives a good intuition that such maxima also exist.

The set of centers of curvature of a curve γ is called the evolute of γ. Except if γ is a circle, the evolute of γ is a curve that has cusps (non regular point) at the local minima and maxima of curvature of γ. We illustrate the Four-vertex theorem in Figure 1.3 where the evolute has indeed four cusps.

##### 1.1.2 The medial axis of a curve

In this paragraph, rather than the parameterization of curve γ, we focus our interest on its image in R2. More precisely, we consider that:

$$\gamma \colon = \{ \gamma ( t ) , \ t \in \mathbb { R } \} .$$

We study the notion of contact of a curve with a tangent circle at a given point (See [Rut18, BGG85, Eri01b]). Consider a point p, and a circle tangent to the curve at p. If the circle is not the osculating

and then, circle at p, then we say that it has an A1 contact with the curve. In other words, the circle is tangent to the curve, and so shares the first derivative of the curve at p, but it does not share the second order derivative. Conversely the osculating circle may have an A2 contact with the surface, since it shares with the surface the first and second order derivative. But it is possible that an osculating circle shares its third order derivative with the curve at p. Since a circle can be seen as the graph of a even function, the third order derivative at p must be 0. For the third order derivative of the curve to be also 0 at p, p must be generically an extrema of curvature. In this case, we say that the contact is an A3 contact. We assume that for almost all curves, there are no higher possible contact type (this will be discussed in Section 1.3 for surfaces). The A3 contacts correspond to cusps on the evolute (see Figure 1.4).


<!-- p:27 -->


Figure 1.3: The evolute (in yellow) of an ellipse γ (in blue).

c(t)

γ(t)

Figure 1.4: Three different contact types. Left: an A1 contact type, only tangent. Middle: an A2 contact type, osculating. Right: an A3 contact type, osculating at a maximum of curvature.

In the latter paragraph, we assumed that there was only one contact between the curve and the circle. But there can be more. Consider that, from a point p that is not an extrema of curvature, we make grow a tangent circle until it touches another point of the curve at p. We call such a circle a medial circle of γ at p, or a medial circle of p if there is no ambiguity on γ. The other contact point of the circle is called a symmetrical point of p. At p, the contact was an A1 contact since the circle is tangent to the curve. At the symmetrical point, generically, it is also an A1 contact. Since such a circle shares two A1 contacts, we say that the contact is A2. The set of medial centers forms a one-dimensional curve, that we call the medial axis [Lee82]. The extremities of the medial axis corresponds to cusps of the evolute, at maxima of curvature. This happens when two symmetrical points converge. At some points, the medial axis may be divided into three branches, where the medial circle has 3 contacts points. We write such contact A3 (see Figure 1.5).


<!-- p:28 -->


Figure 1.5: The inner medial axis (in red) of the black curve. Its extremities are centers of A3 contact circles (in green). It has some intersection points at the center of A3 circles, (in blue).

#### 1.2 Geometry of surfaces

In this section, we extend the notions developed for the curves, to surfaces.

##### 1.2.1 Basic notions on surfaces

In this thesis, we study the behavior of the Delaunay triangulation of point distributed on a surface. We formalize the notion of surfaces that we consider. We define what is a regular surface, using the definition from Do Carmo [DC16].

Definition 1.4. A subset S ⊂ R3 is a regular surface if, for each p ∈ S there exists a neighborhood V in R3 and a map f : U → V ∩ S of an open set U ⊂ R2 onto V ∩S ⊂ R3 such that:

1. f is smooth (f is infinitely differentiable),
2. f is a homeomorphism (f has a continuous inverse f−1 : V ∩ S → U),
3. f is an immersion (for each u ∈ U, the differential d fu is injective).

The first condition is necessary since we expect to do some differential calculus on S. The second condition implies that the surface has no self-intersection, for the bijective part of the homeomorphism, while the continuity of the inverse guarantees us to be able to consider differentiable functions from S to R. Finally the third condition, also called regular condition, implies that at any p ∈ S, S admits a tangent plane.

Rather than parametric regular surfaces, we consider their image in R3, i.e. the set of points they define, and the properties of the surface that are independent of the parameterization. Thus we will consider a smooth surface S as the image of a parametric regular surface, knowing that, at any p ∈ S we can find a parameterization.

Later, the surface will be considered not only smooth but also analyic.

The Monge form of surfaces As we said, a smooth surface S admits a tangent plane at any point. ot oo t   ( nnt t t     or ot s ta normal vector. Only two directions are possible. A surface is said orientable if we can choose, for any point, a normal vector n(p), that varies continuously on S. A choice of orientation makes the surface an oriented surface.

Assume that S is an oriented smooth surface, and consider p ∈ S and its tangent plane Ts(p). Then consider a plane P passing through p and orthogonal to Ts(p). Locally, P ∩ S is a planar curve. We can then consider the algebraic curvature of this curve. By rotating P around the normal, the curvature obtained varies continuously in R. We denote by κ1(p) the maximal curvature, obtained in the plane P1, and by κ2(p) the minimal curvature obtained in P2. They are called the principal curvatures of S


<!-- p:29 -->


Figure 1.6: The principal curvatures of S at p are the curvatures of the red curves at p.

P\_2

n

P1

S

p

at p, and their associated directions in Ts(p) are called principal directions (see Figure 1.6). Note that changing the orientation inverts κ1 and κ2.

Let kθ(p) be the curvature of the curve S ∩ Pθ where Pθ makes an angle θ with P1. In the 18th century, Euler [Eul67] stated a theorem that asserts that:

$$k _ { \theta } ( p ) = \kappa _ { 1 } ( p ) \cos ^ { 2 } \theta + \kappa _ { 2 } ( p ) \sin ^ { 2 } \theta ,$$

which implies, by the same time, that the principal directions are orthogonal. If the principal curvatures l   i d  s   t.

This orthogonality induces a natural choice of coordinate system for not umbilical point. Consider the x-axis in the maximal principal direction, the z-axis in the normal direction η(p), and the y-axis in the minimal principal direction such that (x, y, z) is direct. It remains then to make an arbitrary choice for x-axis orientation. Such a coordinates system at p is called a Monge coordinates system [HGY+99]. In such a coordinate system, at p, S is locally parameterized by z = fp(x, y) where:

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } ( p ) x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } ( p ) y ^ { 2 } + O ( | x | ^ { 3 } + | y | ^ { 3 } ) .$$

We call such an expression of S the Monge form of S at p.

We extend the notion of osculating circle. At p, the curvatures vary from κ2(p) to κ1(p) depending on the direction of cutting plane. We could consider as many osculating sphere, but we will only consider the extreme ones. Thus for a given orientation, we call first osculating sphere, the sphere passing through p and centered at (0, 0, 1) in the Monge coordinate system. Similarly we call second osculating sphere κ1 1). the sphere passing through p and centered at (0, 0,

Highly related with principal direction is the notion of line of curvature. A line of curvature is a curve on S whose tangent at every point is aligned with a principal direction. Since at not umbilical point, the principal directions are orthogonal, they generically form an orthogonal net on the surface.

####### Closed surface

A surface S is said closed if it is compact without boundary. The closeness of a surface implies two important properties:

- by compactness, any continuous function admits a maximum. For instance, if the surface is C2, we can consider the maximal absolute curvature, denoted κsup, on the surface. It is defined by

$$\kappa _ { \sup } \coloneqq \max _ { p \in \mathcal { S } } \left ( | \kappa _ { 1 } ( p ) | , | \kappa _ { 2 } ( p ) | \right ) .$$


<!-- p:30 -->


Such a value is a constant depending on the particular surface considered. At a later stage, we will give other constants that we can define on a closed surface.

- we can distinguish inner and outer orientations, where the inner orientation points inward S, and the outer orientation points outward.

##### 1.2.2 Analytic description of a surface

We enumerate here the different approximations we will use in the thesis, depending on the order of precision we need. We consider a closed surface S. We assume that S is at least C2 so that we can consider its tangent plane and its Monge form z = fp(x, y) at any point, as in Equation 1.2 .

Around p, the surface can be locally caught between two spheres tangent to S, with radius 1 κsup' and centered on both sides of S. Thus S can also be caught between two parabolas of revolution with curvature 2κsup at their summit (see Figure 1.7). That provides lower and upper bounds for fp and we can claim that, if √x2 + y2 ≤ √2 then: 2κsup

$$| f _ { p } ( x , y ) | \leq \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) .$$

The neighborhood √x2 + y2 ≤ √2 around p is then chosen to be the usual neighborhood, i.e. the 2κsup neighborhood in which we can consider the Monge form of S.

If S is Cn with n ≥ 2, we can extend its Monge form this way:

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \sum _ { k = 3 } ^ { k = n } \frac { 1 } { k ! } \sum _ { i + j = k } \binom { k } { i } m _ { i , j } x ^ { i } y ^ { j } + O ( | x | ^ { n + 1 } + | y | ^ { n + 1 } ) .$$

Note that, to lighten the notations, we deleted the "(p)" behind each coefficient, since it is clear from the context.

Figure 1.7: A 2D view of two tangent spheres (in red) with maximal curvature on both sides of the surface S, and two parabolas (in green).

S

p

We won't go further the fourth order, where the Monge form is then:

$$f _ { p } ( x , y ) & = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \frac { 1 } { 6 } \left ( m _ { 3 , 0 } x ^ { 3 } + 3 m _ { 2 , 1 } x ^ { 2 } y + 3 m _ { 1 , 2 } x y ^ { 2 } + m _ { 0 , 3 } y ^ { 3 } \right ) \\ & + \frac { 1 } { 2 } \left ( m _ { 4 , 0 } x ^ { 4 } + 4 m _ { 3 , 1 } x ^ { 3 } y + 6 m _ { 2 , 2 } x ^ { 2 } y ^ { 2 } + 4 m _ { 1 , 3 } x y ^ { 3 } + m _ { 0 , 4 } y ^ { 4 } \right ) + O ( | x | ^ { 5 } + | y | ^ { 5 } ) .$$

If S is three-times differentiable at p, we can have a bound on the remaining term using the Taylor's formula with Lagrange's remainder [Col12]:

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + R _ { 3 } ( x , y ) ,$$


<!-- p:31 -->


with R3(x, y) = Σ Rij(x, y)xiyj, where each remaining term verifies: i+j=3

$$| R _ { i j } ( x , y ) | \leq \frac { 1 } { i ! j ! } \sup _ { 0 \leq t \leq 1 } \left | \frac { \partial ^ { 3 } f _ { p } ( t x , t y ) } { \partial x ^ { i } y ^ { j } } \right | .$$

If S is C3, there exists M3 &gt; 0 depending on p such that all the terms supo≤t≤1 ∂3 fp(tx,ty) are ∂xiyj bounded in √x2 + y2 ≤ √2 by M3 from above, it follows that: 2κsup

$$| R _ { 3 } ( x , y ) | \leq M _ { 3 } \sum _ { i + j = 3 } \frac { 1 } { i ! j ! } ( x , y ) | x | ^ { i } | y | ^ { j } = \frac { 1 } { 6 } M _ { 3 } ( | x | + | y | ) ^ { 3 } \leq \frac { \sqrt { 2 } } { 3 } M _ { 3 } \sqrt { x ^ { 2 } + y ^ { 2 } } ^ { 3 } .$$

For most parts of the surface, this approximation will be enough. However, some points of the surface have their third order derivative with respect to x that is 0, more formally:

$$\frac { \partial ^ { 3 } f _ { p } ( 0 , 0 ) } { \partial x ^ { 3 } } = 0 .$$

This happens at extrema of curvature as explained in Section 1.1. At such points, we will need a more precise approximation, since the bound M3 over the four derivatives of order 3 might be a bit rough.

For this case, we will assume that S is C4 and consider the remaining term R3+, denoted with a + in index to express that we extend partially the order 3. Then we can say that there exists M4 &gt; 0 that is a bound over all fourth order derivatives for √x2 + y2 ≤ 2ksup √2 , and then we have:

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \frac { 1 } { 6 } m _ { 3 , 0 } x ^ { 3 } + R _ { 3 + } ( x , y ) ,$$

$$R _ { 3 + } ( x , y ) = O \left ( x ^ { 4 } + x ^ { 2 } | y | + | x | y ^ { 2 } + | y | ^ { 3 } \right ) ,$$

with

or more precisely, for √x2 + y2 ≤ √2 we have: 2κsup

$$| R _ { 3 + } ( x , y ) | & \leq M _ { 3 } \left ( \frac { 1 } { 2 } x ^ { 2 } | y | + \frac { 1 } { 2 } | x | y ^ { 2 } + \frac { 1 } { 6 } | y | ^ { 3 } \right ) + \frac { 1 } { 2 4 } M _ { 4 } x ^ { 4 } \\ & = M _ { 3 } | y | \left ( \frac { 1 } { 2 } x ^ { 2 } + \frac { 1 } { 2 } | x y | + \frac { 1 } { 6 } y ^ { 2 } \right ) + \frac { 1 } { 2 4 } M _ { 4 } x ^ { 4 } \\ & \leq M _ { 3 } | y | \left ( x ^ { 2 } + y ^ { 2 } \right ) + \frac { 1 } { 2 4 } M _ { 4 } ( x ^ { 4 } + x ^ { 2 } y ^ { 2 } ) \\ & = \left ( x ^ { 2 } + y ^ { 2 } \right ) \left ( M _ { 3 } | y | + \frac { 1 } { 2 4 } M _ { 4 } x ^ { 2 } \right ) .$$

#### 1.3 Generic surface

The main result of the thesis concerns orientable closed analytic generic surfaces. In a common definition, generic means that we consider "almost all" the orientable closed regular surfaces. More precisely, the set of surfaces in R3 we consider must be a dense set in the set of orientable closed regular surfaces. On a generic object, we can quantify the dimension of a subset of points defined by a so called transversality constraint. Basically, each (independent) transversality constraint on the points makes the dimension of t os e s  t  s  t       es that are shared by generic surfaces. Those properties are important in the context of the Delaunay triangulation. In particular, those properties are related with the contact types that the surface has with a tangent sphere.

##### 1.3.1 Maxima of curvature

By the Four-Vertex theorem, we saw that a planar regular closed curve admits maxima of curvature. This property can be extended on an oriented regular surface S. Consider a line of curvature on S, p on this curve and the principal curvature κ1(p). On this curve the function κ1 may admit a maximum.


<!-- p:32 -->


Figure 1.8: The sets Z and Y in red. At an extremity Z′ of Z, the other contact point with the first osculating sphere (in grey) is a point of Y.

As maximum of curvature along the maximal principal direction, they are solutions of the equation m3,o(p) = 0. Thus by transversality, such points form one-dimensional curves on S with finite total length.

Among such points p maxima of curvature, for a given orientation, we consider the first osculating sphere, and have a look on its intersection with S. Since p is a maximum of curvature, the intersection locally contains only p. The question is on what happens far from p. Two cases can arise depending on the position of p:

- Either the intersection contains only p,
- or the intersection contains p and another subset of the surface.

The set of points p verifying the first case is denoted by Z, as in [ABL03]. As we will see, a point close to Z is subject to have an expected logarithmic degree in the Delaunay triangulation of random points on S. As a subset of the maxima of curvature, Z is also a finite reunion of finite curves on S. Such curves are either topological circles on S or topological segment. In that second case, we need to clarify what happens at the extremities of Z that we denote by Z'. This case arises when the intersection of the first osculating sphere with surface has exactly two points. One of this points is p, the other one generically does not belong to Z. The set of such other points is a finite set of isolated points denoted Y, also as denoted in [ABL03]. In other words, a point of Z' has only one symmetrical point and it is a point of Y, and conversely (see Figure 1.8).

As pointed out by Porteus in [Por01], the umbilical points on a generic smooth surface are isolated points. Moreover they don't lie on Z generically [ABL03].

##### 1.3.2 Medial axis and contact types

In this paragraph, we extend the notion of contact points and medial axis, aforementioned for planar curves. We assume that S is a generic smooth surface and show the properties that the genericity induces on the medial axis of S. By smooth we actually mean that S is not only C∞ but also analytic, otherwise the surface could have a very complex medial axis [CCM97].

####### Medial sphere and symmetrical points

We call a medial sphere of S at p, or medial sphere of p, the boundary of a maximal open ball B with p on its boundary such that B ∩ S = Ø. We recall that for a point p on a planar curve, a symmetrical point p of p is a point of the curve such that there exists a medial circle passing through p and p. This notion can be extended to surfaces. We say that two different points are symmetrical on S if their exists a medial sphere passing through those two points.


<!-- p:33 -->


For a given orientation, we can talk about the medial sphere σ*(p) of a point p, that is the one centered in the direction n(p) . We denote by c*(p) its center, and by r*(p) its radius, respectively called medial center and medial radius of p. When it is clear that they depend on p, we will simple write σ*, c* or r*. We say that p ∈ S is a symmetrical point of p only if the medial sphere of p passes also through p. In other words, the symmetrical points of p depends on the chosen orientation.

Taking into account the notion of medial radius, we can give another definition of Z: Z is the set of points p such that κ1(p) = r*(p). Indeed, when two symmetrical points approach each other, their medial sphere tends to be osculating. If the surface is closed, then we can consider the minimal medial radius, also called reach in [BLW19], and denoted rch:

$$\text {rch} \colon = \min _ { p \in \mathcal { S } } \left ( r ^ { * } ( p ) \right )$$

(d)  () 1 for any p, we have rch ≤ 1. A ball centered on p and with radius rch has an κ1(p) κsup intersection with the surface that is a topological disk, so it provides a relevant upper bound for the size of some neighborhood.

In order to remain homogeneous in the counting of symmetrical points, we make some precision for two kinds of points:

- If, for a given orientation, the medial sphere of p degenerates into a plane, we consider that p has a symmetrical point at infinity.
- If p belongs to Z ∪ Z', we say that p is its own symmetrical point.

Thus we claim the following generic properties:

Proposition 1.5. Let S be an orientable generic smooth surface. For each orientation of S, we have:

1. Any point of S has, at least, one symmetrical point.
2. The set of points of S that have at least two symmetrical points is a finite reunion of finite curves on S.
3. The set of points of S that have at least three symmetrical points is a finite reunion of isolated points on S.
4. No point of S has four symmetrical points.

We explain this property using the dimension of the medial axis (see Figure 1.9). Let p be a point on S, and choose an orientation of S. By definition of a medial sphere, p has at least a symmetrical point, possibly at infinity. We explain separately the case, for a given orientation, where p has an infinite symmetrical point, from the case where all of its symmetrical points are finite. At the same time we will name the different parts of S according to their medial sphere.

####### If all symmetrical points of p are finite

Suppose first that p has exactly one symmetrical point that is finite and different from p, we denoted it by p, and consider the medial center c*(p) of p. By moving a little bit p in any direction on S, the condition of having a single symmetrical point remain true, and we might assume that c*(p) forms a bi-dimensional sheet, close to the bisector plane of p and p. Now consider the set of centers of such points. It is exactly the center of A2 contact sphere, where an A2 contact sphere, is a sphere that shares wm  ts  sts tt   t   st tt t t as  tch contact points, i.e. of an A2 medial sphere, is denoted by S (for "simple" and because it corresponds to the most representative part of the surface S).

At the boundary of the medial centers of S points (the points of S), two things can happen:


<!-- p:34 -->


Figure 1.9: The five possible contact centers on the medial axis of a generic surface, as they are presented in [Eri01b]. From left to right: A2, A3, A3, A4, and A1A3. On the green edges lie centers of medial sphere at Z.

- Either two sheets of medial centers meet each other. In that case their intersection is made of centers of A3 contact spheres. As intersection of two bi-dimensional objects, such an intersection is generically one-dimensional object. The set of points of S whose medial sphere has an A3 contact with the surface is denoted S'. The points of S' form curves on the surface.
- Or a sheet of medial center meets an end. In other words, when c*(p) moves toward such an end, p and p are actually converging toward a limit that we will call pz. Moreover, their first osculating sphere also converges, toward the first osculating sphere of pz. In other word, the first osculating spe prs a  s rs r  pa tns o os a  re ors pz, and we can say that pz belongs to Z. Thus, the external boundary of the medial centers corresponds to medial center of points of Z. As extrema of curvature, such contact points are not only osculating but shares also the third derivative, so that they are A3 contact. It is important to keep in mind that each of the subsets described refers to a given orientation. So, the Z curve of a given orientation can cross the Z curve of the other orientation, but it is not possible that the Z curve of a given orientation intersects itself.

As we said, the sets of A3 and A3 medial centers are one-dimensional objects. Generically they can meet another A2 sheet of medial centers. This happens on a finite reunion of isolated points. We can again distinguish two cases:

- Either a line of A3 medial centers meets an A2 sheet into an A4 medial center. The set of points on S whose medial sphere has an A4 contact with the surface is denoted by S". A point S' is a point of concurrency of three S' curves that symmetrical each other.
- Or a line of A3 medial centers meets an A2 sheet into an A3A1 medial center. The A3 contact lies at an extremity of Z, it is called a Z' point. The A1 contact is called a Y point. Since a A3 medial center is the limit of a A1 medial center, an A3A1 contact is also the limit an A2 medial curve. Thus a point of Y is an extremity of the set S', and two others S' curves are converge to a Z' point.

Roughly speaking, two S' curves meet into an S" point, while a Z curve meets an S' into a Z′ point.

####### If p has an infinite symmetrical point

Similarly, we can consider the points of S that have a symmetrical point at infinity: those whose medial sphere degenerates into a plane. Those points constitute what we call the convex part of S. Among them are the points with no finite symmetrical points, i.e. with only the infinite symmetrical point. The set of such points is denoted H (as in hull). The set H constitutes the interior of the convex part.

The set of points of the convex part with exactly one finite symmetrical point forms the set denoted H', made of curves on the boundary of H. The extremities of H' is a finite set of isolated points. We denote it by H". The points of H" have exactly 2 finite symmetrical points and one at infinity. In other words, their medial sphere is a plane that touches the surface at three points. Note that H" points lie at two extremities of H' curves and an extremity of an S' curve. In some sense H' is like a frontier between H and S points where the medial centers go to infinity.

We could ask ourselves if a point in the interior of the convex part could be its own symmetrical point, in other words if a point p of Z can be in H ∪ H' ∪ H". Since the medial sphere of a point of H is a plane, this would imply that κ1(p) = 0. To respect the convex properties, the first (maximal) principal curvature must be non positive. But genericity implies that a maximum of non positive function cannot be 0. So on the convex hull of a generic surface, κ1 &lt; 0, and there is no Z point, neither Y points.


<!-- p:35 -->


If the surface is closed, the sets H, H' and H" exist only for the outer orientation.

##### 1.3.3 Summary of the cases

We summarize the different possible types of points on a generic closed orientable surface, and recall some notations.

Consider an orientation of S and a point p ∈ S. In the given orientation, the point p has a single medial sphere σ*(p), which is the one centered in the direction of the normal. The ball for which σ*(p) is the boundary is denoted by B (σ*(p)). If σ*(p) degenerates into the tangent plane of p, B (σ*(p)) corresponds to half-space directed by the normal. The set of points p for which σ*(p) degenerates into the tangent plane of p is called the convex part of the surface.

Figure 1.10: An illustration of the decomposition with H and S sets. Here S is the reunion of four disjoint spheres centered on the vertices of a regular tetrahedron. H' delineates the convex part. The S' curves meet at an S" point on each sphere.

H

S


H

S


H

We list now the different kinds of points of the convex part. Those points have no medial axis, and distinct elements of E.

- H = {p ∈ S, r*(p) = +∞, B (σ*(p)) ∩ S = {p}} is the set of points whose tangent plane has a single contact with the surface. H is inside the convex part. It forms an open subset of S.
- H′ = {p ∈ S, r*(p) = +∞, ∃p ∈ S\ {p}, B (σ*(p)) ∩S = {p, p}} is the set of points whose tangent plane has two contacts with the surface. H' lies on the boundary of H. It forms a curve.
- H" = {p ∈ S, r*(p) = +∞, ∃(p0, p1) ∈ (S \ {p})2 , B (σ*(p)) ∩S = {p, P0, p1}} is the set of points whose tangent plane has three contacts with the surface. H" lies on the boundary of H' (and H). It is made of isolated points.

Note that a closed surface has H, H' and H" sets only for the outer orientation. See Figure 1.10 for an illustration of H, H' and H" sets.


<!-- p:36 -->


Figure 1.10 also illustrates S, S' and S" sets, that we summarize now. If a point p is not on the convex part H ∪ H' ∪ H", its medial sphere is an actual sphere (not a plane), and p has a finite medial radius. Among those points, we have to differentiate the points p such that κ1(p)r*(p) = 1 from the others. All points such that κ1(p)r*(p) &lt; 1 have at least one symmetrical point. When it is single, we denote it by p. We must also differentiate the cases when κ1(p)r*(p) = 1. The points p that are not on the convex part, that verify κ1(p)r*(p) &lt; 1 and whose symmetrical points p verify κ1(p)r*(p) &lt; 1, are called simple points.

- S = {p ∈ S, r*(p) &lt; ∞, κ1(p)r*(p) &lt; 1, ∃p ∈ S \ {p}, B (σ*(p)) ∩ S = {p, p} ∧ κ1(p)r*(p) &lt; 1} is the set of simple points with one symmetrical points. S forms an open subset of S. Even if, in some sense, the S points are the most common points of S, the reader may pay attention not to confuse the notations S and S.
- S′ = {p ∈ S, r*(p) &lt; ∞, κ1(p)r*(p) &lt; 1, ∃( ̄0, P1) ∈ (S\ {p})2, B (σ*(p)) ∩S = {p, P0, P1} is the set of simple points with two symmetrical points. S' forms a curve at the boundary of S. Some S' curves meet an end at H" points.
- S" = {p ∈ S, r*(p) &lt; ∞, κ1(p)r*(p) &lt; 1, ∃(p0, p1, P2) ∈ (S\ {p})3, B (σ*(p)) ∩S = {p, P0, p1, p2}} is the set of simple points with three symmetrical points. S" lies where three S' curves meet. It is made of isolated points.

Figure 1.11: A point of Z′ is a concurrency point of two S' curves and one Z curve. The points of Y′ are endpoints of S' curves.

YJ

S

Z

Finally it remains to consider the points such κ1(p)r*(p) = 1 and with a single symmetrical point p such that κ1(p)r*(p) = 1.

- Z = {p ∈ S, r*(p) &lt; ∞, κ1(p)r*(p) = 1, B (σ*(p)) ∩ S = {p}}. Z is a subset of the maximum of curvature. It forms curves on S also called ridges.
- Z′ = {p ∈ S, r*(p) &lt; ∞, κ1(p)r*(p) = 1, ∃p ∈ (S \ {p}) , B (σ*(p)) ∩ S = {p, p}}. Z′ lies at extremities of Z curves and is a set of isolated points.
- Y = {p ∈ S, r*(p) &lt; ∞, κ1(p)r*(p) &lt; 1, ∃p ∈ (S \ {p}) , B (σ*(p)) ∩S = {p, p} ∧ κ1(p)r*(p) = 1}. Y lies at extremities of S' curves. The points of Y are symmetrical with some points of Z'.

See Figure 1.11 for an illustration of Z, Z′ and Y points. Generically there exists no other kind of contact points.


<!-- p:37 -->


## Chapter 2

### Combinatorics

In this chapter, we present basic notions of combinatorics. The first section is dedicated to fundamental notions in graph theory while the second section focuses on the Delaunay triangulation. In particular, we introduce the notion of size of a graph, and present some bounds on the size of the Delaunay triangulation.

#### 2.1 Graph theory

In mathematics and computer science, graphs are widely studied structures. We present in this section some fundamental notions that we will use through this thesis.

##### 2.1.1Generalities on graphs

Usually [Eri99], a graph G is defined as an ordered pair (V, E) where V is a non-empty set, and E is a set of pairs of V. An element of V is called a vertex, an element of E is called an edge. If the edges of E are unordered pairs, we say that the graph is undirected, otherwise we say that it is directed. A directed graph will be denoted with an arrow: G. In an undirected graph, two vertices that share an edge are called neighbors. In a directed graph, the neighborness relation is not anymore symmetrical and we say that a vertex q is a successor of a vertex p, if the set of directed edges V contains (p, q).

Figure 2.1: Two representations of the graph G = (V, E) with V = {a, b, c, d, e}, and E = {(a, b), (a, c), (b, c), (b, d), (b, e), (c, d), (d, e)}. The right representation shows that G is planar, this representation is a plane graph.

8

d

e

C


b

aó

ad

It can be helpful to visualize graphs. They can be represented in the plane, by considering the vertices as usual points and the edges as curves that link the points. With such a representation, we must pay attention to the fact that an intersection between edges is not necessary a vertex. If a graph can be represented in the plane in such a way that its edges intersect only at the vertices, we say that the graph ts t  n nn ( lt  d   e ot t te e  sn can always find a plane graph with straight lines, so will consider that its always the case. In a plane graph, we call face a region bounded by edges, and outerface the unbounded external face. We denote by F the set of faces of a plane graph, including the outerface.


<!-- p:38 -->


Figure 2.2: A plane graph in which the vertex p has degree #V – 1. Nevertheless the average degree remains smaller than 6 since the graph is planar.

●


A planar graph is said maximal if no edge can be added without losing the planar property. The faces of a maximal planar graph are triangles, i.e. have 3 edges on their boundary.

Consider now two graphs G = (V, E) and G′ = (V, E') whose set of vertices is the same. If E′ ⊆ V we say that G′ is a sub-graph of G, and conversely that G is a super-graph of G'.

##### 2.1.2 Counting the edges of a planar graph

The main purpose of the thesis is to compute the number of edges of a given graph according to its number of vertices. For a set A, we will denote by #A the number of elements in A. For a graph G = (V, E), #G is also called size, or combinatorial complexity, of the graph. #G corresponds to #E + #V, so we are interested in computing #E with respect to #V. The Euler's formula [Eul58] gives a relation between the numbers #V, #E, and #F in a connected plane graph:

Theorem 2.1 (Euler's formula). Let V, E, and F be respectively the set of vertices, edges and faces of a connected plane graph, then:

$$\mathfrak { V } - \mathfrak { H } E + \mathfrak { H } F = 2 .$$

If a plane graph is maximal, then all of its faces are triangles, and even the outer face has 3 edges. Thus we can claim that each edge is the boundary of two distinct faces, and that each face is bounded by exactly 3 edges. Knowing that, we can proceed to the counting of incidences (e, f) where e is an edge of the face f. Since for each edge, there are 2 faces, the number of such incidences is 2E. On the other hand, since all faces are triangles we can say that the number of incidences is 3F. Thus in a maximal planar graph, we have the following relation:

$$2 \ddot { \P } E = 3 \ddot { \P } F .$$

We can use those two formulas to obtain:

$$\ddot { \S } E - \ddot { \S } F & = \ddot { \S } V - 2 \text { then substitute } \ddot { F } \text { by } \frac { 2 } { 3 } \ddot { \S } E , \\ \frac { 1 } { 3 } \ddot { \S } E & = \ddot { \S } V - 2 , \text { to finally obtain} \\ \ddot { \S } E & = 3 \ddot { \S } V - 6 , \text { and } \\ \ddot { \S } F & = 2 \ddot { \S } V - 4 ,$$

proving that any maximal planar graph, and by extension any connected planar graph, has asymptotically a linear number of edges with respect to its number of vertices.

A data that will have a strong importance all along the thesis is, for a given vertex p, the number of neighbors of p. We call it the degree of p and denote it by deg(p) or deg(p, G) if we need to precise that we count the edges of G. If the graph is directed, we can be interested the number of successors of p, we call this number the outer degree of p and denote it by deg(p). Even in a planar graph, a vertex can be neighbor of all other vertices of E, thus we cannot generally find a better bound than V – 1 on the degree of a vertex (see Figure 2.2). Nevertheless we can bound the average degree of a vertex in a planar graph. Indeed, if the graph is undirected, each edge has two endpoints and the sum of degrees corresponds to 2#E, thus:


<!-- p:39 -->


$$\sum _ { p \in V } \deg ( p ) & = 2 \ddot { \not V } \\ & \leq 6 \ddot { \not V } - 1 2 \text { and then} , \\ \frac { 1 } { \ddot { \not V } } \sum _ { p \in V } \deg ( p ) & \leq 6 - \frac { 1 2 } { \ddot { V } } .$$

Conversely, having an information on the degree of each vertex of a graph is a great help to bound the number of edges.

#### 2.2 The Delaunay triangulation

The Delaunay triangulation is the central object of this thesis. We describe it in this section, and give some properties on its size depending on the dimension considered.

##### 2.2.1The 2D-Delaunay triangulation

If the vertices are actually geometric points in Rd, for any d ≥ 1, we can consider graphs that depend on the relative position of the points. One example of such graphs in R2 is the graph induced by the Delaunay triangulation [Del34].

Formally, a Delaunay triangulation of a set of points is a simplicial complex, i.e. a set of vertices, edges, triangles, and simplices of higher dimension if necessary, such that any sub-simplex of a simplex (any edge of a triangle for instance) is in the simplicial complex, and the non-empty intersection of two simplices is a sub-simplex of both.

In dimension 2, for a set of vertices V in general position (no three vertices aligned, no four vertices cocyclic), the Delaunay triangulation, denoted Del(V), of V is the unique simplicial complex (V, E, F) in which (p, q, r) is a triangle of F if and only if the circle C circumscribing p, q and r has no points of V in its interior. In that case, we say that C is empty. It is equivalent to say that (p, q) is an edge of E if and only if there exists an empty circle C passing through p and q. Note that one of the definitions involves three points and one circle, while the other involves two points and a whole pencil of circles. This will make an important difference later.

The Delaunay triangulation of V induces the graph (V, E) that is a plane graph whose all faces are triangles except for the outer face (see Figure 2.3). We will often refers to the Delaunay triangulation or to its induced graph without distinction.

To have a complete information on the Delaunay triangulation, it requires then to know not only the set of points and edges, but also the set of faces. Thus the combinatorial complexity of a 2D-triangulation is then given by the sum #V + #E + F. We denote it by  Del(V), and call it more simply the size of the triangulation.

In 2D, since the Delaunay triangulation is planar, the Euler formula is enough to evaluate  Del(V) for any set of points V, indeed we have:

$$\ddot { \S D e l } ( V ) = \Theta ( \ddot { \S V } ) .$$

When we consider the Delaunay simplicial complex in 3 dimensions, this linear relation does not hold anymore.


<!-- p:40 -->


So that we can deduce:

Figure 2.3: The Delaunay triangulation of 35 points in the plane. We can remark that most of the triangles are not so flat.

##### 2.2.2 In three dimensions (and higher)

The Delaunay triangulation can be generalized to any dimension d. We recall that a d-simplex is the generalization of triangle in higher dimension, i.e. the simplest polytope in dimension d. Consider a set of vertices V in Rd, a d-simplex is an element of Del(V) if the d-sphere passing through its d + 1 vertices is empty.

In dimension 3, the Delaunay triangulation of a set of points V is the simplicial complex in which a tetrahedron belongs to Del(V) if and only if the sphere circumscribing its four vertices is empty. Even if the simplex with highest dimension is now a tetrahedron, we still say that it is a triangulation, specifying that it is a 3D-Delaunay triangulation. We denote by C the set of cells of the triangulation, including the outercell.

Euler's formula on 3D-triangulations is:

$$\ddot { \mathfrak { V } } - \ddot { \mathfrak { H } } E + \ddot { \mathfrak { H } } F - \ddot { \mathfrak { C } } = 0 .$$

However, it is not anymore sufficient to compute precisely the size of such a triangulation in terms of its number of vertices. Indeed, an edge can be in as many triangles as possible and we cannot use the same counting as before. We can construct explicit examples with a quadratic number of edges.

For instance, consider two lines l and l' not parallel neither intersecting. Consider a set V of points, and distribute the points such that half of them are on each line. Let p be a point of V ∩l, and q a point of V ∩l'. Since we can find a sphere tangent to l at p and to l′ at q, (p, q) is an edge of Del(V). Therefore, ×  = θ(#V2) each point on l shares an edge with all points of l'. In other words, there are at least HV X 2 2 edges in Del(V). We can even find a set of points where all pairs of points are neighbors in the Delaunay triangulation. For instance by distributing V on the moment curve t → (t, t2, t3).

Nevertheless, we can apply the counting of incidences "face-cells". This quantity is equal to 2#F and greater than 4#C (since the outercell is not a tetrahedra), and so we have #F ≥ 2#C. We could have considered a notion equivalent to maximal planar graph for triangulation but we will be satisfied with an inequality. By substituting this in Euler's formula, we obtain:

$$\ddot { \mathbb { V } } - \ddot { \mathbb { Z } } E + \mathfrak { f } F - \frac { 1 } { 2 } \ddot { \mathbb { H } } F \leq 0 .$$

#F = 2#E − 2#V and so,

#F ≤ 2#E and,

#C ≤#E.


<!-- p:41 -->


Figure 2.4: A quadratic case for the 3D-Delaunay triangulation: two lines are not coplanar, and half of the point set is on each line.

C


e

Since a triangulation contains a covering tree in which the number of edges is the number of vertices minus one, we can state the following property:

Proposition 2.2. The size of the 3D-Delaunay triangulation Del(V) of a set of points V verifies:

$$\ddot { \mathfrak { g } } D e l ( V ) = \Theta ( \mathfrak { g } E ) ,$$

where E is the set of edges of Del(V).

Finally, we make the remark that both of Euler's formulas and the counting of incidences are particular cases of the Dehn-Sommerville equations in higher dimensions. Those equations provide also an upper bound on size of the Delaunay triangulation in dimension d:

$$\ddot { \L } D e l ( V ) = O ( \ddot { \L } V ^ { \lceil \frac { d } { 2 } \rceil } ) ,$$

and this bound is reached for points on the moment curve t → (t, t2, . . . , td).


<!-- p:42 -->


Chapter 2. Combinatorics


<!-- p:43 -->


## Chapter 3

### Probabilities

In this chapter, we present the random point process we use to model data points, namely the Poisson point process. We define it and present some of its properties, including the Slivnyak-Mecke formula, which will often be used.

For an event A, we denote by 1[A] and P [A], respectively the indicator function and the probability of A, for a random value V, we denote by E [V] its expected value, and for a region R we denote by |R| its length, area, volume, etc..., depending on its dimension.

#### 3.1 Poisson point process

In order to model the data points, we use a Poisson point process. A Poisson point process is a set of points randomly distributed in a chosen space. We use such a sample because it has convenient mathematical properties. There exist homogeneous and nonhomogeneous processes, but in the whole thesis, we will only use homogeneous processes, without mentioning it. A (homogeneous) Poisson process is associated with a parameter, usually denoted by λ, and called intensity of the Poisson process. As

When it is distributed on S ⊂ Rd, a Poisson point process X with intensity λ is characterized by the two following properties [CSKM13]:

- For any region R ⊂ S, P [# (X ∩ R) = m] = (λ|R|)m −e−λ|R|, for m ∈ N. m!
- The number of points of k disjoint regions form k independent random variables.

Note that to be completely accurate, we might consider that the regions are Borel sets. In the whole thesis, the only regions we consider are intersections of balls of dimension d with subsets of Rd for d = 2 or d = 3, so it is clear that they are Borel sets.

The first property indicates that, in a given region, the number of points of a Poisson process behave like a Poisson distribution. The second property gives an independence property between two disjoint regions. It is an important property that does not have, for instance, a uniform process. Indeed, in a uniform process of n points, knowing that k points are in given region implies that n − k points are in its complementary.

The counting property implies two formulas:

- P [# (X ∩ R) = 0] = e−λ|R|, and
- E [# (X ∩ R)] = λ|R|.

We will make a heavy use of the first formula. Indeed it reflects the fact that a region is empty of data points, that is what characterizes that an edge belongs to the Delaunay triangulation. The second property allows to see λ as an expected number of points in a region of measure 1. Thus the combinatorial complexity of graphs will be expressed as a function of λ.


<!-- p:44 -->


#### 3.2Slivnyak-Mecke's theorem

In stochastic geometry, we can be interested in counting the expected value of some quantities. For instance, the expected length of a path in a given graph [CD16, BM11, BDCD19], or the expected size of the Delaunay triangulation in a given manifold [CCE21]. In our case, we will mainly count the expected size of empty region graphs.

Ad  e ee pe  e oe oe  e soe oe e ee  snt in the 2D-Delaunay triangulation of a Poisson point process X. As mentioned in Chapter 2, the average degree in a triangulation of n points, and therefore in the Delaunay triangulation, is 6 - 12. We prove n here a well known [Møl94] and quite close result for Poisson process:

Theorem 3.1. Let X be a Poisson point process in R2 and p a point of R2. The expected degree E [deg(p, Del)] of p in the Delaunay triangulation Del (X ∪ {p}) is 6.

The result differs in the fact that the average value 6 – 12 is for all points while the expected value 6 n is for all Poisson point processes.

We distribute the Poisson process X in R2 and without loss of generality, assume that p is the origin. Let D(p, q, r) denote the open disk with p, q, and r on its boundary. The number of neighbors of p in Del(X ∪ {p}) is the number of distinct pairs (q, r) in X2 with q ≠ r such that D(p, q, r) is empty. It is given by the random value:

$$\deg ( p , D e l ) = \frac { 1 } { 2 } \sum _ { q \in X } \sum _ { r \in X \ \{ q \} } \mathbb { 1 } _ { [ \mathcal { D } ( p , q , r ) \cap X = \emptyset ] } ,$$

where the factor  corrects the double counting of each set {q, r} in the sum. Note that, to lighten the notations, we write only deg (p, Del) where we should write deg (p, Del(X ∪ {p}). What we are interested in is the expectation of this value:

$$\mathbb { E } \left [ \deg \left ( p , D e l \right ) \right ] & = \mathbb { E } \left [ \frac { 1 } { 2 } \sum _ { q \in X } \sum _ { r \in X \ \{ q \} } \mathbb { 1 } _ { \left [ \mathcal { D } ( p , q , r ) \cap X = \emptyset \right ] } \right ] \\ & = \frac { 1 } { 2 } \mathbb { E } \left [ \sum _ { q \in X } \sum _ { r \in X \ \{ q \} } \mathbb { 1 } _ { \left [ \mathcal { D } ( p , q , r ) \cap X = \emptyset \right ] } \right ] \, . \\ \intertext { a s u m o a P o i sson p o r s e t o a n i n t e r a l } \mathbb { E } \left [ \sum _ { q \in X } \sum _ { r \in X \ \{ q \} } \mathbb { 1 } _ { \left [ \mathcal { D } ( p , q , r ) \cap X = \emptyset \right ] } \right ] \, . \\ \intertext { a s u m o a P o i sson p o r s e t o a n i n t e r a l }$$

To switch from a sum on a Poisson process to an integral R2, we introduce the Slyvniak-Mecke formula [SW08, p 68, Corollary 3.2.3], adapted to our notations and context:

Theorem 3.2 (Slivnyak-Mecke formula). Let X be a Poisson process distributed on E with intensity λ, let m ∈ N, and let f : 2E × Em → R be a nonnegative measurable function. Then

$$\mathbb { E } \left [ \sum _ { ( x _ { 1 } , \dots , x _ { m } ) \in X _ { \neq } ^ { m } } f ( X , x _ { 1 } , \dots , x _ { m } ) \right ] = \lambda ^ { m } \int _ { E } \dots \int _ { E } \mathbb { E } \left [ f ( X \cup \{ x _ { 1 } , \dots , x _ { m } \} , x _ { 1 } , \dots , x _ { m } ] \, d x _ { m } \dots d x _ { 1 } ,$$

where Xm denotes the set of tuples of Xm with distinct elements, and 2E denotes the power set of E (including any set of points of E).

We apply Slivnyak-Mecke formula on E [deg (p, Del)] for E = R2, m = 2, (x1, x2) = (q, r), and f(X, q, r) = 1[D(p,q,r)∩(X∪{q,r})=0] to obtain:

$$\mathbb { E } \left [ \deg ( p , D e l ) \right ] = \frac { 1 } { 2 } \lambda ^ { 2 } \int _ { \mathbb { R } ^ { 2 } } \int _ { \mathbb { R } ^ { 2 } } \mathbb { E } \left [ 1 _ { \mathcal { D } ( p , q , r ) \cap ( X \cup \{ q , r \} ) = \emptyset ] } \right ] d r d q ,$$

but since q and r lie on the boundary of D(p, q, r), we can write:

$$\mathbb { E } \left [ \deg ( p , \text {Del} ) \right ] & = \frac { 1 } { 2 } \lambda ^ { 2 } \int _ { \mathbb { R } ^ { 2 } } \int _ { \mathbb { R } ^ { 2 } } \mathbb { E } \left [ \mathbb { 1 } _ { [ \mathcal { D } ( p , q , r ) \cap X = \emptyset ] } \right ] \text {d} r d q \\ & = \frac { 1 } { 2 } \lambda ^ { 2 } \int _ { \mathbb { R } ^ { 2 } } \int _ { \mathbb { R } ^ { 2 } } \mathbb { P } \left [ \mathcal { D } ( p , q , r ) \cap X = \emptyset \right ] \text { d} r d q ,$$


<!-- p:45 -->


Figure 3.1: The Blaschke-Petkantchin variables substitution converts the Cartesian coordinates of q and r into polar coordinates related to the circle circumscribing p, q and r.

y

r

yr

θr

C

θ

q

ρ

yq

q

4

p

xr xq

x

and by definition of a Poisson process,

$$= \frac { 1 } { 2 } \lambda ^ { 2 } \int _ { \mathbb { R } ^ { 2 } } \int _ { \mathbb { R } ^ { 2 } } e ^ { - \lambda | \mathcal { D } ( p , q , r ) | } d r d q .$$

In order to express in a simpler way the area of D(p, q, r), we use a Blaschke-Petkantschin like variables substitution [SW08, Theorem 7.2.7] from R4 to R × [0, 2π)3 that expresses the parameterization of p and q into (ρ, φ, θp, θq) where (ρ, φ) denotes the polar coordinates of the center c of the circle circumscribing p, q, and r, and θq and θr. denote the angles from c of the points q and r to the horizontal line (see Figure 3.1).

The coordinates are then rewritten:

$$x _ { q } & = \rho ( \cos \varphi + \cos \theta _ { q } ) , \ y _ { q } = \rho ( \sin \varphi + \sin \theta _ { q } ) , \\ x _ { r } & = \rho ( \cos \varphi + \cos \theta _ { r } ) , \ y _ { \rho } = r ( \sin \varphi + \sin \theta _ { r } ) .$$

And the Jacobian matrix J of the Blaschke-Petkantschin variables substitution is:

$$J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) = \begin{pmatrix} \cos \varphi + \cos \theta _ { q } & - \rho \sin \varphi & - \rho \sin \theta _ { q } & 0 \\ \sin \varphi + \sin \theta _ { q } & \rho \cos \varphi & \rho \cos \theta _ { q } & 0 \\ \cos \varphi + \cos \theta _ { r } & - \rho \sin \varphi & 0 & - \rho \sin \theta _ { r } \\ \sin \varphi + \sin \theta _ { r } & \rho \cos \varphi & 0 & \rho \cos \theta _ { r } \end{pmatrix} \, .$$

In Appendix A.1, we show that

$$\det \left ( J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) \right ) = 4 \rho ^ { 3 } \sin \left ( \frac { \pi - ( \theta _ { q } - \theta _ { r } ) } { 2 } \right ) \sin \left ( \frac { \theta _ { q } - \varphi } { 2 } \right ) \sin \left ( \frac { \varphi - \theta _ { r } } { 2 } \right ) .$$

So that we get:

$$& \quad \mathbb { E } \left [ \deg \left ( p , D \right ) \right ] = \frac { 1 } { 2 } \lambda ^ { 2 } \int _ { R ^ { + } } \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { 2 \pi } e ^ { - \lambda \pi \rho ^ { 2 } } | \det \left ( J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) \right ) | \, d \theta _ { r } d \theta _ { q } d \varphi d \rho \\ & = \lambda ^ { 2 } \int _ { \mathbb { R } ^ { + } } 2 \rho ^ { 3 } e ^ { - \lambda \pi \rho ^ { 2 } } d \rho \times \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { 2 \pi } \left ( \sin \left ( \frac { \pi - ( \varrho _ { q } - \theta _ { r } ) } { 2 } \right ) \sin \left ( \frac { \theta _ { q } - \varphi } { 2 } \right ) \sin \left ( \frac { \theta - \theta _ { r } } { 2 } \right ) \right | d \theta _ { r } d \theta _ { q } d \varphi .$$

Since a primitive of ρ → 2ρ3e−λπρ2 is ρ → λπρ2+1 (λπ)2 we have + 2ρ3e−λπρ2 (λπ)2 , SO: 1

$$\mathbb { E } \left [ \deg \left ( p , \text {Del} \right ) \right ] = \frac { 1 } { \pi ^ { 2 } } \times \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { 2 \pi } \left | \sin \left ( \frac { - ( \theta _ { q } - \theta _ { r } ) } { 2 } \right ) \sin \left ( \frac { \theta _ { q } - \varphi } { 2 } \right ) \sin \left ( \frac { \varphi - \theta _ { r } } { 2 } \right ) \right | d \theta _ { r } d \theta _ { q } d \varphi ,$$


<!-- p:46 -->


simplified by the translation (θq, θr) → (θq − π − φ, θr − π − φ) applied in the (2π, 2π)-periodic function (θq, θr) → sin π−(θq −θr) sin θq-4 sin 4-θr 2 2 2

$$\mathbb { E } \left [ \deg ( p , \text {Del} ) \right ] & = \frac { 1 } { \pi ^ { 2 } } \times \int _ { 0 } ^ { 2 \pi } d \varphi \times \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { 2 \pi } \left | \sin \left ( \frac { \theta _ { q } - \theta _ { r } } { 2 } \right ) \right | \sin \frac { \theta _ { q } } { 2 } \sin \frac { \theta _ { r } } { 2 } d \theta _ { r } d \theta _ { q } \\ & = \frac { 2 } { \pi } \int _ { 0 } ^ { \pi } \int _ { 0 } ^ { \pi } 4 \left | \sin \left ( \theta _ { q } - \theta _ { r } \right ) \right | \sin \theta _ { q } \sin \theta _ { r } d \theta _ { r } d \theta _ { q } ,$$

and after linearisation of the sinus:

$$= \frac { 2 } { \pi } \times 3 \pi \\ = 6 .$$

As expected the result is a constant. As we will explain it in Part II, this is due to the fact that a disk with p on its boundary has an area quadratic with the distance of its center from p. To get an intuition on that, consider two Poisson processes on R, X1 with intensity 1, and X2 with intensity 2. Then "zoom" on X2 by a factor 2, until it appears as spread as X1. Since disks remain unchanged by zooming we cannot make anymore any difference between the two cases, and understand why the intensity is not involved in the degree of a point.

We might accept that, even if this computation is feasible and provides an exact value, it remains a bit tedious, and we may suppose that, with more complex regions than disks, a simplification would help. A large part of the thesis is dedicated in finding a simpler way to approximate such computations.

Finally, if we distribute a Poisson process X on a compact body S in Rd, the number of edges E of the dD-Delaunay triangulation of X can be expressed as E = 1 Σp∈x deg(p, Del), and its expected value is:

$$\mathbb { E } \left [ E \right ] = \frac { 1 } { 2 } \int _ { p \in \mathcal { S } } \mathbb { E } \left [ \deg ( p , D e l ) \right ] d p ,$$

by Slivnyak-Mecke formula. It is the quantity E [deg(p, Del)] that we will try to evaluate in almost all cases.


<!-- p:47 -->


## Chapter 4

### State of the art

In this chapter, we present the state of the art in the problem of approximating the combinatorial complexity of the 3D-Delaunay triangulation depending on where and how the sample points are distributed.

In dimension 2, the complexity of the Delaunay triangulation of n points is Θ(n), as we explained in Chapter 2. To be more precise, the number of triangles is between n and 2n triangles, depending on the size of the convex hull. In dimension 3, the gap between the lower and upper bound ranges from linear to quadratic. In that case, the size of the Delaunay triangulation depends both of the subset of R3 in which the points are distributed and on the way they are distributed on this subset. We present, through the following sections, how different authors studied the size of the Delaunay triangulation depending on the distribution they chose.

#### 4.1 Expected size of the dD-Delaunay triangulation of a uniform set of points

In his paper "Higher-dimensional Voronoi diagrams in linear expected time" [Dwy91], Dwyer proved, in 1991, that when n points are uniformly distributed in a unit d-ball in Rd, the expected size of the Delaunay triangulation is Θ(n):

Theorem 4.1 (Dwyer, 1991). Let X be a set of n sites drawn independently from the uniform distribution on the interior of the unit d-ball. Then the expected number of simplices of the dual of the Voronoi diagram of X, is Θ(n) for fixed d as n → ∞.

Actually, the result in the paper is more precise since the hidden constant in the Θ(n) is given.

Even if we did not mention it in the background, the Voronoi diagram is a fundamental object of computational geometry. It is the dual of the Delaunay triangulation, defined for a set X of points, as the set of convex regions {x ∈ Rd, dist(x, p) ≤ dist(x, q) ∀q ∈ X \ {p}} for all p ∈ X. Thus, the number of edges issue from p in the Delaunay triangulation is the number of faces of the region of p in the Voronoi diagram (see Figure 4.1).

In the first section of the paper, Dwyer establishes a general formula that expresses the probability Pn that a d-simplex is in the triangulation. Thus, if Sn expresses the number of simplices of Del(X), then

$$\mathbb { E } \left [ S _ { n } \right ] = \binom { n } { d + 1 } P _ { n } ,$$

since there are (d+1) possible d-simplices.

The expression of Pn is of the kind of the one we used in Chapter 3, and to simplify it, Dwyer uses a Blaschke-Petkantschin like variables substitution also. Computing the integral in the expression of Pn where:


<!-- p:48 -->


$$P _ { n } = d ! \kappa _ { d } \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } I ( q , r ) d r d q , \, \text {and} \\ \mathbb { E } \left [ S _ { n } \right ] \sim \frac { \kappa _ { d } n ^ { d + 1 } } { d + 1 } \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } I ( q , r ) d r d q ,$$

ho s  t (   ) ir ( sxe (,  e (( p) =  or radius r at distance q from (0, 0) is empty.

Then, in the second section of his paper, Dwyer applies his method on n points distributed uniformly on the unit disk. He decomposes fo∞ f I(q, r)drdq in various cases depending on r and q, for which the only dominating case, with respect to n, is q ≤ 1 and 0 ≤ r ≤ 1 − q. It corresponds to the case where the possible empty sphere is inside the unit ball, and where:

$$\int _ { 0 } ^ { 1 } \, \int _ { 0 } ^ { 1 - q } I ( q , r ) d r d q \sim d ^ { d - 2 } d ! v _ { d } n ^ { - d } ,$$

$$v _ { d } = \frac { \Gamma \left ( ( d ^ { 2 } + 1 ) / 2 \right ) \Gamma \left ( d / 2 \right ) ^ { d + 1 } } { \sqrt { \pi } d ! \Gamma \left ( d ^ { 2 } / 2 \right ) \Gamma \left ( ( d + 1 ) / 2 \right ) ^ { d } } ,$$

denotes the expected volume of a d-simplex with random vertices on the unit d-sphere.

$$\mathbb { E } \left [ S _ { n } \right ] \sim \kappa _ { d } v _ { d } \frac { d ! d ^ { d - 2 } } { d + 1 } n .$$

| E [ S n ] ∼ 2 n         | for d = 2   |
|-------------------------|-------------|
| E [ S n ] ∼ 24 π 2 35 n | for d = 3   |
| E [ S n ] ∼ 286 n       | for d = 4   |

This gives:

This provides:

Figure 4.1: The Voronoi diagram (in red) and the Delaunay triangulation of 10 points uniformly distributed in the unit disk.

A

reduces the expression to:


<!-- p:49 -->


This work has been completed by Calka in his "Habilitation à diriger des recherches" [Cal09], in which he studied the distribution of various features (number of faces, circumradius, global shape, etc..) of a cell of the Voronoi diagram of a Poisson process.

In a more recent paper, Bienkowski et al. [BDadHS05] also proved the average linearity of the Delaunay triangulation of points uniformly distributed in the unit cube. Actually it is conjectured that this holds for any convex body.

#### 4.2 Analysis of the 3D-Delaunay triangulation of points on a polyhedral surface

In [Dwy91], the points were distributed randomly. The choice of using a random distribution has various reasons, such as being easier to simulate. Indeed, it corresponds to a sample naturally homogeneous (the expected number of points in a region depends directly on the volume of the region), the expressions used for computation are derived from probabilistic theories, we can obtain exact values and not only results up to a constant. But we could have consider other samples, not necessarily random.

For practical problems, like surface reconstruction, we can be interested in distributing the points on a subset of the ambient space with a smaller dimension. The next papers that we present deal with the case where points are distributed on surfaces.

There are various way to distribute such points. As in [Dwy91], we can use a random sample, either uniform or Poisson. Among the advantages of random process, we can note that they almost surely exclude pathological position of points. We can also use a deterministic sample. In this case, we have to specify conditions so the sample is sufficiently good. To study the size of the Delaunay triangulation, we want the number of points distributed in a region to be directly related with the area of such a region. A natural idea for a deterministic sample can be to distribute the points on a grid, but this is not a very good idea with the Delaunay triangulation since some points may be co-spherical. Another condition can be: any ball of a given radius contains at least one point of the sample, for instance. There can be different kinds of such deterministic samples. We all gather them under the name nice samples.

##### 4.2.1 Probabilistic analysis

In 2001, Golin and Na wondered about how the size of the Delaunay triangulation behave when the sample points are distributed on a polyhedral surface.

When the surface is a convex polytope, they proved, in "On the average complexity of 3D-Voronoi diagrams of random points on convex polytopes" [GN03], that the expected size of the 3D-Delaunay triangulation was linear:

Theorem 4.2 (Golin and Na, 2001). Let P be the boundary of a convex polytope in R3. Let X be a set of points drawn from the standard 2-dimensional Poisson distribution on P with rate λ. Then E [# Del(X)] = Θ(λ).

The global idea of the paper is to count the number of what they call Voronoi combinatorial spheres. For two points p and q of R3, the combinatorial sphere of (p, q) corresponds to the set of spheres passing through p and q. If p and q belong to the sample point, they say that σ(p, q) is a Voronoi combinatorial sphere if there exists an empty sphere passing through p and q.

Then they proceed to two decomposition among the spheres. First they introduce the notion of good and bad spheres. A bad sphere is a sphere whose interior has an intersection with P that has an area greater than log2 λ of Type-I, whose interior has an intersection with P that is a complete disk; spheres of Type-II, whose interior has an intersection with P that is a section of disk that contains their center; and spheres of Type-III for the remaining spheres. They show that:


<!-- p:50 -->


```
# [# (Bad Voronoi spheres)] = o(1),
    # [# (Type-I Voronoi spheres)] = O(lambda),
    # [# (Type-II Voronoi spheres)] = O(lambda),
    # [# (C) 1. T_II  Voronoi spheres)] = O(lambda),
```

- E [# (Good Type-III spheres)] = o(λ),

proving their linear bound.

In 2002, in "The probabilistic complexity of the Voronoi diagram of points on a polyhedron" [GN02], Golin and Na weakened their hypothesis on the subset of R3 where the Poisson sample is distributed, to consider a set of triangles, and showed that with high probability, the size of the Delaunay triangulation was O(λ ln6 λ):

Theorem 4.3 (Golin and Na, 2002). Let F be a collection of k triangles in R3. Let X be a set of points drawn from 2-dimensional Poisson distribution on F with rate λ. Then P [ Del(X) = O(λln6 λ)] = 1 − λ−Ω(log n).

In this paper, Golin and Na reduced their analysis to the case with two triangles. They decompose the set of possible spheres depending on the closest point on each triangle from the center of the sphere. This creates six categories of spheres "face/face", "face/edge", "face/vertex", etc.. and for all of them, they proved that the total number of pairs (p, q), with p on a triangle and q on the other, is smaller than O (λ ln6 λ) with high probability.

##### 4.2.2Deterministic analysis

At almost the same time, Attali and Boissonnat prefered to use a deterministic approach, to compute the size of the Delaunay triangulation of points on a polyhedral surface.

They consider a so-called e-sample that is sample of points such that, any ball centered on the surface and with radius € contains at least one point of sample. This sample condition bring the guarantee that there is no too large region on the surface that does not contain any point.

l] ,ss o o d o ot ee o o o,, :der   r they obtained the bound O(n9/5) for any polyhedral surface, and O(n√n) when the surface is the boundary of a convex polytpe.

A few years later, in 2004, Attali and Boissonnat improved their bound by considering an (€, κ)- sample that is an e-sample for which any disk on the surface contains at most κ points. Thus, in a given region of the surface, we can have an upper bound on the number of points depending on the area of the region. This sampling is considered almost uniform. In their paper: "A linear bound on the complexity of the Delaunay triangulation of points on polyhedral surfaces" [AB04], they showed we can reach a linear bound, for which the hidden constant contains a factor κ2, and properties of the surface like its number of faces, its area, etc...

The idea is the following, as it was done in [AB03], the polyhedral surface is decomposed into a regular part that corresponds to the faces reduced from their boundary by strip of width €, and a singular part, that is the complementary of the regular part, that corresponds to the parts of the faces at a distance smaller that € from their edges.

Using packing arguments, like the fact that a region R of the surface contains O ( |R+ε/2 sample E2 points, they proved that the number of edges with:

- both endpoints in the regular part is O(κn),
- both endpoints in the singular part is O(κ2n),
- an endpoint in each part is O(κ2n) also.

Since κ is used as a constant, they proved:


<!-- p:51 -->


Theorem 4.4 (Attali and Boissonnat, 2004). let S be a polyhedral surface and P be an (e, κ)-sample of S of size #P = n. The number of edges in the Delaunay triangulation of P is O(n).

Thus, for a polyhedral surface, this shows that probabilistic and deterministic approaches yield similar results.

##### 4.2.3 On polyhedral surfaces of any dimension

In 2008, in their paper: "A tight bound for the Delaunay triangulation of points on a surface" [AAD12], mnnn- e e s n   oe s    n o   nna polyhedron in Rd. They proved that the complexity of the triangulation is then O (n p d−k+1 for k = [d+1]. p+1 1. Nevertheless, the sampling has to be distributed on each face of any dimension, from all vertices to all faces of dimension p. The hypotheses are stronger than those of Theorem 4.4 for which it is not necessary to sample the edges of the polyhedral surface.

Note that the bound obtained is tight. Indeed, for each d and p, they can find a p-dimensional polyhedron P such that, if a nice sample is distributed on each face of P then its Delaunay triangulation is Ω (n−p+ d−k+1

#### 4.3 Evaluating the size of the Delaunay triangulation with respect to the spread of the points

The spread, denoted ∆, of a set of points is defined by Erickson as the ratio between the longest and shortest pairwise distances.

In his paper "Nice point sets can have nasty Delaunay triangulation" [Eri01a], Erickson makes the remark that, in R3, the spread is minimized when n points are distributed on a lattice. In that case we have ∆ = Θ (n1/3) and the 3D-Delaunay triangulation is linear. On the other hand, when the points are regularly distributed on two skew lines, as we explained in Chapter 2, the spread is Ω (n), and the triangulation is quadratic.

For some nice samples, like e-nets [BDDG20], of n points distributed on a surface, the spread is O(√n). Erickson shows a construction in which a nice set of points with spread √n has a Θ(n√n) Delaunay triangulation. Consider a right circular cylinder, and draw an helix around the cylinder such that the helix makes √n turns around the cylinder. Then distributed uniformly √n points on each turn of the helix. Erickson showed that any point p is neighbor with all other points of the same turn of p, giving √n neighbors to p (see Figure 4.2). Since such points are almost uniform, this illustrates that going from polyhedral surfaces to smooth surfaces is not that trivial.

In the latter paper: "Dense point set have sparse Delaunay triangulation" [Eri05], Erickson proved the following theorem:

Theorem 4.5 (Erickson 2005). The Delaunay triangulation of any finite set of points in R3 with spread ∆ has complexity O(∆3).

This implies that n points uniformly distributed on a surface have an O(n√n) Delaunay triangulation.

#### 4.4 Another probabilistic approach

In 2004, Devroye et al. used, in their paper "Expected time analysis for Delaunay point location" [DLM04], a method to analyze efficiently the Delaunay triangulation of random points in the plane. Roughly speaking, the method consists in taking strictly smaller regions than the Delaunay disks to obtain various upper bounds.

First they notice the following property (see Figure 4.3):

Lemma 4.6 (Devroye et al., 2004). Let x1, . . . , xn be points in the plane. If (xi, xj) is a Delaunay edge, then one of two half-circles with diameter [xixj] cannot contain any other data point.


<!-- p:52 -->


38 Chapter 4. State of the art

●

Figure 4.2: n points are distributed on an helix on the cylinder, each point, for instance the red one, is neighbor with √n other points.

They then considered the half-moon graph, in which two points p and q are neighbors if at least one the two half-circles for which [pq] is a diameter (also called half-moons of (p, q)) does not contain other points of data sample.

q

p

Figure 4.3: If (p, q) is a Delaunay edge, then there exists an empty disk with p and q on its boundary (say the grey one). This disk contains one of the two half-moons of (p, q).

Bal s so l o   do s   do -o   o an be seen as the starting point of the method we develop in Part II, and that we use all along the thesis. Indeed the half-moon graph is far easier to study than the Delaunay triangulation since instead of all the circles passing through two points, we just consider two half-circles. This induces some loose in the precision of the result, but we can show that, when we count the number of edges, we lose only a constant factor. Devroye et al. also used this method to bound the length of the edges emanating from a given point with high probability. We make the remark that in their paper, they considered a uniform point process distributed in a unit square, forcing them to study what happens close to its boundary. In this thesis, we use Poisson point processes, and we can distribute such a process, in the whole plane, avoiding boundary problems. In 2007, Devillers et al. studied the 3D-Delaunay triangulation of random points distributed on the cylinder. In their paper: "Empty-ellipse graphs" [DEG08], they show that when n points are randomly uniformly distributed on a cylinder, their Delaunay triangulation is actually Θ(n log n) in expectation. This shows, at the same time, that the configuration in helix of complexity Θ (n√n) proposed by Erickson is pathological.


<!-- p:53 -->


To obtain this bound, they considered the so called empty axis-aligned ellipse graphs, that is the plane graph in which two points p and q are neighbors if there exists an empty axis-aligned ellipse with p and q on its boundary. The "axis-aligned" condition means that, given a frame with two orthogonal axis, the great and small axis of the ellipses are parallel to the axis of frame. They figured out that any ellipse passing through p and q contains an axis-aligned right triangle with [pq] as hypotenuse (see Figure 4.4).

Figure 4.4: Any axis-aligned ellipse passing through p and q contains one of the two axis-aligned right triangle with [pq] as hypotenuse.

q

p

V

This provides a super-graph of the empty axis-aligned ellipse graph, namely the empty axis-aligned right triangle graph, in the same manner that the half-moon graph was a super graph of the Delaunay triangulation. And then they showed that the empty axis-aligned right triangle graph has size Θ(n log n).

Then they consider n random points on a cylinder, and a sphere passing through p and q. Then they unroll the cylinder into a plane and show that the intersection of the sphere with the cylinder contains, once unrolled, an axis aligned right triangle. In some sense, we could say that the empty right triangle graph is a super-graph of the 3D-Delaunay triangulation of points on the cylinder.

This proves, up to the lower bound that can be obtained similarly, the following theorem:

Theorem 4.7 (Devillers et al., 2007). The Delaunay triangulation of n points chosen independently and uniformly at random from a right circular cylinder has expected complexity Θ(n log n).

This is roughly the method we will use to compute the expected size of the 3D-Delaunay triangulation of points distributed on a surface. Showing that, in some sense, it corresponds to a plane graph that we can study.

#### 4.5 Deterministic nice sample on generic surfaces

Devillers et al. showed that the worst case Θ(n√n) cylinder case was quite pathological because of the way the points were distributed. Experimental results seem to show that for more general surfaces, like "generic" surfaces, the size of the Delaunay triangulation seems to be far better than O(n√n), rather close to O(n ln n) or even O(n), and we might think that the geometry of the cylinder itself is pathological for the Delaunay triangulation.

Indeed, consider two points p and q on the cylinder such that they belong to the perpendicular (to the cylinder axis) section C of the cylinder. Then p and q are necessarily neighbors in the 3D-Delaunay triangulation since the sphere whose C is a great circle is obviously empty. The problem is that on the cylinder, for any point p, the medial radius r*(p) and the osculating radius are equal. κ1(p)

Thus in 2004, Attali et al. in their paper "Complexity of the Delaunay triangulation of points on surfaces: the smooth case" [ABL03], and Erickson [Eri01b] paralelly in a another paper, showed that the Delaunay triangulation of a nice sample distributed on a generic smooth surface has complexity O(n log n), that is better than the Θ(n√n) bound obtained on the cylinder with the same sample, i.e. an (€, κ)-sample, that we prefer to rename here an (€, η)-sample because the letter κ is commonly used to denote the curvatures on surfaces. As it was the case for polyhedral surfaces, any region R of a smooth surface contains O (κ1 |R+ε/21 sample points. ε2

By generic surface, as we explained in Chapter 1, they roughly mean that the set of points of the κ1 can mimic, in a first step, the approach in the paper [AB04] on polyhedral surfaces, where Z plays the role of the edges. Thus they consider a strip of width δ around Z, and start to count the number of edges whose both endpoints are not in the strip. They show that this number is linear with the number of points. To prove this, they show that a Delaunay sphere passing through two points p and q has an intersection with the surface, that is contained in one or two bounded regions on the surface. One region is in a neighborhood of p, the other is possibly around the symmetrical point of p, denoted by p. We briefly recall that p is the other contact point on the surface of the medial sphere of p. Those regions have respectively a diameter Θ (√1−κ1(p)r+(p) 1−κ2(p)r*(p) Θ pue /1−κ1(p)r* (p) 1−κ2(p)r*(p) ). Thus they contain a finite number of points (depending on η). As long as p is far from Z, both 1 − κ1(p)r*(p) and 1 − κ1(p)r*(p) are strictly positive, and the result holds. When p approaches Z, they need to refine their analysis, since Z is also defined as the set of points where 1 − κ1(p)r*(p) = 0.


<!-- p:54 -->


Thus they divide the strip around Z into points very close to Z, at distance smaller than √€ and points at distance between √€ and δ from Z, i.e. between the very close points to Z and the boundary of the strip. If p is among the very close points, they showed that a Delaunay sphere passing though p has an intersection with the surface contained in a rectangle with sides Θ(√€) × Θ (€) axis aligned with principal directions and centered on the closest point on Z from p. Such a point p has a number of neighbors that is O (ηε−ν ). Since there are at most O(ηε−γ) sample points very close to Z, the total

number of edges with an endpoint very close to Z is O (ηε−ž × ηε−1 ) = O (η2ε−2) = O(n).

In the other case, they showed that the intersection of a Delaunay sphere with the surface is comprised inside two rectangles centered on p and p, axis-aligned with the principal directions, and with sides Θ hp 1 € × Θ (€), where hp denotes the distance from p to Z.

By integrating the degree for hp from √ε and δ, they obtain the total number of edges with an endpoint at distance between √ε to δ from Z. Since δ is a constant,

$$\int _ { \sqrt { \varepsilon } } ^ { \delta } \frac { 1 } { h _ { p } } d h _ { p } = O \left ( \log \frac { 1 } { \varepsilon } \right ) ,$$

and then there are O (κ2ε−2 log 1) = O(k2n log n) such edges. This last bound is the worst one. This is not that surprising, since around Z, the intersection surface/sphere approaches an intersection cylinder/sphere. They deduced the following theorem:

Theorem 4.8. Let S be a C5 surface satisfying genericity properties, and let X be an (ε, η)-sample of S of size n. The combinatorial complexity of the Delaunay triangulation is O(n log n).

Since using a random sample, instead of a nice sample, on the cylinder, improved the bound of the Delaunay triangulation, we have good chance to think that the bound on the degree of a point close to Z might also be improved. Indeed we will show in Part IV that, when a Poisson process is distributed on a surface, the expected degree of point p at distance hp &gt; 0 from Z is O (ln 1 , and since this is  ̄hp integrable around 0, the total number of edges remains linear.


<!-- p:55 -->


## Chapter 5

### A first approach of the problem: A Poisson sample on a surface is a good sample

As we said in Chapter 2, the complexity of the 3D-Delaunay triangulation of n points distributed in R3 ranges from linear to quadratic. When the points are a deterministic good sample of a smooth compact generic surface, Attali, Boissonnat and Lieutier[ABL03], and Erickson[Eri01b] proved that the size of the Delaunay triangulation is O(n ln n).

When the points are a Poisson process with parameter λ distributed on a surface, experimental results seem to show that the bound is linear or quasi-linear. An approach to obtain a bound on the 3D-Delaunay triangulation of a Poisson process is to show that a Poisson process is likely to be a good sample, and then to apply the result of Attali et al..

In this chapter, we prove that a Poisson point process with intensity λ on a closed smooth surface is an (ε, η)-sample for ε = 3√ ln λ and η = 1000 ln λ with high probability. This yields that the complexity of λ the Delaunay triangulation of a Poisson sample of an oriented closed smooth generic surface is O(λ ln2 λ) losing an extra logarithmic factor with respect to the case of good sampling (see Section 5.2).

This chapter is the first of the contributions.

#### 5.1 Notation, definitions, previous results

We consider an oriented closed smooth generic surface S embedded in R3, as Attali, Boissonnat and w     o   t tt st o      e  ot consider a Poisson point process X with parameter λ &gt; 0 distributed on S. By definition of a Poisson process, E [#X] = λ. Then we consider the 3D-Delaunay triangulation of X. Since it is a 3-dimensional triangulation, # Del(X) is the sum of the number of tetrahedrons, triangles, edges and vertices that belong to the Delaunay triangulation. By Proposition 2.2,  Del(X) = O(#E), so it is enough to count only the edges.

For a point p ∈ S and positive number R, we denote by Ds(p, R) the intersection of S with a ball centered on p and with radius R. Since for R small enough, it is a topological disk, we call Ds(p, R) a disk. Then we define what is a good-sampling of a surface and precise the result by Attali, Boissonnat and Lieutier.

Definition 5.1 (Good sample). A point-set on a surface is an (ε, η)-sample if any ball of radius ε centered on the surface contains at least one and at most η points of the sample.

A good sample is usually called an "epsilon-kappa" sample, but the notation κ was already used for the curvature so we preferred to use the denomination good sample, with a parameter η.


<!-- p:56 -->


Figure 5.1: Illustration of the proof of Lemma 5.3 for the 2D case.

1

Ksup

C

●

A

√3

V

p

2ksup

Theorem 5.2 ([ABL03], Prop 19). The 3D-Delaunay triangulation of an (ε, η)-sample of a closed oriented smooth generic surface has complexity O ln ey2 ε

While the result of Attali et al. provides a bound O(n ln n) on the complexity of the Delaunay triangulation of an (ε, η)-sample of n points when η is a constant, by looking more carefully at the result [ABL03, Eq.(14)], we notice that the actual complexity can be expressed by C()2 ln(ε−1) for C being a constant of the surface.

#### 5.2 Is a Poisson sample a good sample?

In a Poisson sample with intensity λ on the surface, a disk of radius ε = is expected to contain π points, but with constant probability it can be empty or contains more than any constant number of points. Thus with high probability there will be such disks even if their number is limited, and such a sample is likely not to be a good sample with ε2 = 1 and η constant. Nevertheless, it is possible to not consider η as a constant, namely, we take η = Θ(ln(λ)). In a first Lemma, we bound the area of Ds(p, R), for any p ∈ S and R &gt; 0 sufficiently small.

Lemma 5.3. Let S be a C2 closed surface with curvature bounded by κsup, and consider p ∈ S and R &gt; 0 smaller than . The area of Ds(p, R) is greater than 314 πR2. Ksup

Proof. The bound is obtained by considering the fact that the surface must stay in between the two tangent spheres of curvature κsup tangent to the surface at p. In the tangent plane Ts(p) at p, the disk √3 R is included in the projection of Ds(p, R) on the tangent plane. Its centered on p and with radius 2 area is πR2. We deduce that Ds(p, R) has an area greater than □

Lemma 5.4. Let S be a C3 surface of curvature bounded by κsup. For R small enough, the area of Ds(p, R) is smaller than 514 πR2.

Proof. We consider the Monge form of S at p:

$$z = f ( x , y ) \text { where } f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + O ( x , y ) ^ { 3 } .$$


<!-- p:57 -->


We denote by da an element of surface, and by πp the orthogonal projection on Ts(p). Since on Ds(p, R), the slope of the normal to S is bounded, we have:

$$| D _ { S } ( p , R ) | & = \int _ { D _ { S } ( p , R ) } d a = \int \int _ { \pi _ { p } ( D _ { S } ( p , R ) ) } \sqrt { 1 + \left ( \frac { \partial f _ { p } } { \partial x } ( x , y ) \right ) ^ { 2 } + \left ( \frac { \partial f _ { p } } { \partial y } ( x , y ) \right ) ^ { 2 } } d x d y \\ & \leq \int \int _ { x ^ { 2 } + y ^ { 2 } \leq R ^ { 2 } } \sqrt { 1 + \left ( \frac { \partial f _ { p } } { \partial x } ( x , y ) \right ) ^ { 2 } + \left ( \frac { \partial f _ { p } } { \partial y } ( x , y ) \right ) ^ { 2 } } \, d x d y .$$

Since fp is C3 and ∂fp(x,y) 2(x, y) ∼ κ1x, we can say that there exists a neighborhood around p on ∂x which ∂f | ≤ √2|κ1||x| ≤ √2κsup|x|, and then ∂f 2 ≤ 2(κsupx)2. Applying the same for y, and turning ∂x ∂x to polar coordinates, we get:

$$| D _ { S } ( p , R ) | \leq \int _ { \theta = 0 } ^ { 2 \pi } \int _ { r = 0 } ^ { R } r \sqrt { 1 + 2 ( r \kappa _ { \sup } ) ^ { 2 } } d r d \theta = \frac { \pi } { 3 } \frac { ( 2 ( R \kappa _ { \sup } ) ^ { 2 } + 1 ) ^ { \frac { 3 } { 2 } } - 1 } { \kappa _ { \sup } ^ { 2 } }$$

Noticing that, for 0 ≤ u ≤ 1, (u + 1) 2 − 1 = u3 u+√u+1+2 V 15 u , we can conclude that for any R √u+1+1 8 small enough,

$$| D _ { S } ( p , R ) | \leq \frac { \pi } { 3 } \frac { \frac { 1 5 } { 4 } ( R \kappa _ { \sup } ) ^ { 2 } } { \kappa _ { \sup } ^ { 2 } } = \frac { 5 } { 4 } \pi R ^ { 2 } . \\$$

Lemma 5.5. Let S be a C3 closed surface with area 1. Let MR be a maximal set of kR disjoint disks Ds(pi, R) on S. If R is small enough then kR ≤ 4 3πR2

Proof. By Lemma 5.3, for R small enough, we have Ds(p, R) ≥ 314 πR2. Thus:

$$k _ { R } \frac { 3 } { 4 } \pi R ^ { 2 } \leq \sum _ { i = 1 } ^ { i = k _ { R } } | D _ { \mathcal { S } } ( p _ { i } , R ) | \leq | \mathcal { S } | = 1 ,$$

and we can deduce the following bound: kR ≤ 4 3πR2

□

Lemma 5.6. Let X be a Poisson point process of parameter λ distributed on a C3 smooth closed surface S of area 1. If λ is large enough, the probability that there exists p ∈ S such that Ds (p, 3√ ln λ does λ not contain any point of X is O(λ−1).

Proof. We prove that a Poisson sample has no empty disk of radius 3 ln λ with probability O(λ−1). λ In a first part we use a packing argument. On the one hand, for any ε &gt; 0 small enough, given a maximal set Mε/3 and any point p ∈ S, the disk Ds(p, ε) contains entirely one of the disks Ds(pi, j) that belong to Mε/3, say its center is c, and so Ds(c, 3) ⊂ Ds(p, ε). Indeed, by maximality of Mε/3, the disk Ds(p, ε/3) intersects a disk of Mε/3 whose diameter is 2% so Ds(p, ε) contains it entirely. On the other hand, remember from Lemma 5.3 that if ε is small enough then |Ds(p, ε)| ≥ 3 πε2. Then we can 4 bound the probability of existence of an empty disk for ε small enough:

$$\mathbb { P } \left [ \exists p \in \mathcal { S } , \ X \cap D _ { \mathcal { S } } ( p , \varepsilon ) = \emptyset \right ] & \leq \mathbb { P } \left [ \exists i < k _ { \varepsilon / 3 } , \ X \cap D _ { \mathcal { S } } ( p , \varepsilon / 3 ) = \emptyset \right ] \\ & \leq k _ { \varepsilon / 3 } \mathbb { P } \left [ X \cap D ( c , \varepsilon / 3 ) = \emptyset \right ] \\ & \leq \frac { 4 } { 3 \pi ( \varepsilon / 3 ) ^ { 2 } } e ^ { - \lambda \frac { \pi } { 4 } \pi ( \xi ) ^ { 2 } } \\ & = \frac { 1 2 } { \pi ^ { 2 } } e ^ { - \lambda \frac { \pi ^ { 2 } } { 1 2 } } .$$


<!-- p:58 -->


Figure 5.2: A disk of radius ε always contains a disk of a maximal set of disks of radius

•c

ω|3

pi

E

By taking ε = 3V ln λ we get: λ

$$\mathbb { P } \left [ \exists p \in \mathcal { S } , \ X \cap D _ { \mathcal { S } } ( p , 3 \sqrt { \frac { \ln \lambda } { \lambda } } ) = \emptyset \right ] \leq \frac { 4 \lambda } { 3 \pi \ln \lambda } e ^ { - \frac { 3 \pi \ln \lambda } { 4 } } = O ( \lambda ^ { - 1 } ) .$$

□

We have proved that when a Poisson sample is distributed on a surface, the points sufficiently cover the surface, i.e., there is no large empty disk on the surface with high probability. Now we have to verify the other property of a good sample, namely, a Poisson sample does not create any concentration of points in a small area.

Lemma 5.7. Let X be a Poisson point process of parameter λ distributed on a C3 closed surface of area 1. If λ is large enough, the probability that there exists p ∈ S such that Ds(p, 3V ln λ ) contains more than λ 1000 ln λ points of X is O(λ−2).

Proof. Consider an Mε maximal set, we can notice that for any p ∈ S, the disk Ds(p, ε) with p ∈ S is entirely contained in one disk Ds(pi, 3ε), say that pi = c. Indeed, by maximality of Mε, the disk Ds(p, ε) intersects a disk from Mε say Ds(c, ε) so Ds(c, 3ε) contains entirely Ds(p, ε).

Then we can bound the probability of existence of a disk containing more than η points:

$$\mathbb { P } \left [ \exists p \in \mathcal { S } , \, \mathbb { \dot { \ } } ( X \cap D _ { S } ( p , \varepsilon ) ) & > \eta \right ] & \leq \mathbb { P } \left [ \exists i < k _ { \varepsilon } , \, \mathbb { \dot { \ } } ( X \cap D _ { S } ( p _ { i } , 3 \varepsilon ) ) > \eta \right ] \\ & \leq k _ { \varepsilon } \, \mathbb { P } \left [ \mathbb { H } \left ( X \cap D _ { S } ( c , 3 \varepsilon ) \right ) > \eta \right ] \\ & \leq \frac { 4 } { 3 \pi \varepsilon ^ { 2 } } \, \mathbb { P } \left [ \mathbb { H } \left ( X \cap D _ { S } ( c , 3 \varepsilon ) \right ) > \eta \right ] .$$

We use a Chernoff inequality [MU05] to bound P [# (X ∩ D(c, 3ε)) &gt; η]: if V follows a Poisson law of mean v0, then ∀v &gt; v0,

$$P ( V > v ) \leq e ^ { v - v _ { 0 } } \left ( \frac { v _ { 0 } } { v } \right ) ^ { v } .$$

From Lemmas 5.3 and 5.4, we have that: 27 πε2 ≤ |Ds(c, 3ε)| ≤ 45 πε2 for ε small enough. Conse4 45 λπε2. 4

Then we apply the above Chernoff bound with v = 45 eπλε2 (chosen for the convenience of the 4 calculus)


<!-- p:59 -->


$$\mathbb { P } \left [ \mathfrak { H } ( X \cap D ( c , 3 \varepsilon ) ) > \frac { 4 5 } { 4 } e \pi \lambda \varepsilon ^ { 2 } \right ] & \leq e ^ { \frac { 4 5 } { 4 } e \pi \lambda e ^ { 2 } - v _ { 0 } } \left ( \frac { v _ { 0 } } { \frac { 4 } { 4 } e \pi \lambda e ^ { 2 } } \right ) ^ { 4 5 } \\ & \leq e ^ { \frac { 4 5 } { 4 } e \pi \lambda e ^ { 2 } - \frac { 2 } { 4 } \pi \lambda e ^ { 2 } } \left ( \frac { \frac { 4 } { 4 } \pi \lambda e ^ { 2 } } { \frac { 4 } { 4 } e \pi \lambda e ^ { 2 } } \right ) ^ { \frac { 4 5 } { 4 } } \\ & = e ^ { - \frac { 2 7 } { 4 } \pi \lambda e ^ { 2 } } .$$

So for ε = 3V lnλ and η = 45 eπλε2 = 405 eπλ, we have: λ 4 4

$$\mathbb { P } \left [ \exists p \in \mathcal { S } , \, \mathfrak { g } \left ( X \cap D \left ( p , 3 \sqrt { \frac { \ln \lambda } { \lambda } } \right ) \right ) > \frac { 4 0 5 } { 4 } e \pi \ln \lambda \right ] \leq \frac { 4 \lambda } { 2 7 \pi \ln \lambda } e ^ { - \frac { 2 4 3 } { 4 } \pi \ln \lambda } = O ( \lambda ^ { - 1 8 9 } ) .$$

Since 405 eπ &lt; 1000, it is sufficient for our purpose to say: 4

$$\mathbb { P } \left [ \exists p \in \mathcal { S } , \, \not \, \mathfrak { g } \left ( X \cap D \left ( p , 3 \sqrt { \frac { \ln \lambda } { \lambda } } \right ) \right ) > 1 0 0 0 \ln \lambda \right ] = O ( \lambda ^ { - 2 } )$$

□

Theorem 5.8. On a C3 closed surface, a Poisson sample of parameter λ large enough is a (3γ ln λ , 1000 ln λ)- λ sample with probability 1 − O(λ−1).

Proof. From Lemmas 5.6 and 5.7, we have that a Poisson sample is not a (3y ln λ , 1000 ln λ)-sample with λ probability O(λ−1). □

Theorem 5.9. For λ large enough, the Delaunay triangulation of a point set Poisson distributed with parameter λ on a closed smooth generic surface of area 1 has O(λln2 λ) expected size.

Proof. Given a Poisson sample X we distinguish two cases:

- If X is a good sample, i.e., an (ε, η)-sample with ε = 3V ln λ and η = 1000 ln λ, we apply the λ O ((n)2 ln(ε−1)) bound from the paper by Attali et al., that is O(λ ln2 λ).
- If X is not a good sample, which arises with small probability by Lemma 5.8, we bound the triangulation size by the quadratic bound:

$$\sum _ { k \in \mathbb { N } } k ^ { 2 } \, \mathbb { P } \left [ \mathfrak { h } X = k \right ] = \sum _ { k \in \mathbb { N } } k ^ { 2 } \frac { \lambda ^ { k } } { k ! } e ^ { - \lambda } = \lambda ( \lambda + 1 ) = O ( \lambda ^ { 2 } )$$

Combining the two results, we get

$$\mathbb { E } \left [ \mathbb { T } \text {Del} ( X ) \right ] & = \mathbb { E } \left [ \mathbb { T } \text {Del} ( X ) | X \text { is a good sample} \right ] \mathbb { P } \left [ X \text { is a good sample} \right ] \\ & + \mathbb { E } \left [ \mathbb { T } \text {Del} ( X ) | X \text { is not a good sample} \right ] \mathbb { P } \left [ X \text { is not a good sample} \right ] \\ & \leq O \left ( \lambda \ln ^ { 2 } \lambda \right ) \times 1 + O ( \lambda ^ { 2 } ) \times O \left ( \lambda ^ { - 1 } \right ) = O ( \lambda \ln ^ { 2 } \lambda ) .$$

□

This first approach gives a bound quasi-linear on the size of the 3D-Delaunay triangulation of points on a surface. Nevertheless, the experimental observations seem to show that we can reach a linear bound. Indeed with this computation, we did not us the properties of a Poisson point process, and since the bound found in [ABL03] gives a worst case bound that lies in a small part of the surface, we might expect that it should vanish in average with a Poisson point process.

In Parts III and IV, we compute the expected size of the 3D-Delaunay triangulation of a Poisson point process on surface, using a method based on empty-region graphs, and developed in Part II.


<!-- p:60 -->


46 Chapter 5. A Poisson sample on a surface is a good sample Part II


<!-- p:61 -->


## Stochastic analysis of empty region graphs


<!-- p:62 -->


####### Preamble of Part II

Given a set of points X, an empty region graph is a graph in which two points p and q of X are neighbors if some region defined for (p, q) does not contain any other point of X. This notion unifies the classical Delaunay triangulation [Del34], the Gabriel graph [GS69], the β-skeleton [KR85, ABE98], the empty d a t re dd-  do - t   ss

The main goal of this part is to present and illustrate a method that provides an upper and a lower bound on the degree of a point in a given empty region graph, when the data sample X is a Poisson point process. Part II consists of five chapters.

In Chapter 6, as a pedagogical example, we show how we can find asymptotically tight bounds on the computation of the expected degree of a point in the 2-dimensional Delaunay triangulation using the method described by Devroye, Lemaire and Moreau [DLM04].

In Chapter 7, we formalize the method cited above, in order to generalize it. We give a formal definition of empty region graphs, and provide two lemmas: Combination and Partition lemmas that will be reused all along the thesis. Finally we illustrate the formalization on the Delaunay example.

In Chapter 8, we consider a specific empty region graph: the empty axis-aligned ellipse graph. We make a distinction between the case where we consider all the axis-aligned ellipses and the case where the ellipses have a bounded aspect ratio. We show that in the first case, the expected degree of point is Θ (ln λ) in a Poisson point process with intensity λ, and in the second case, the expected degree is θ(ln 1) for ellipses with an aspect ratio bounded between β and 1, for 0 &lt; β &lt; 1. This chapter has a particular relevance for the thesis. Indeed in Parts III and IV, we compute the Delaunay triangulation of points on a surface, and we will show that the intersections of Delaunay spheres with the surface approaches axis-aligned ellipses. So we will be able to reuse the results of this chapter.

In Chapter 9, we estimate that probability that a point has neighbors farther than some threshold, in d    s       a show that in both cases, this probability decreases exponentially with the threshold.

Finally, in Chapters 10 and 11, we present some additional empty region graphs: The empty ellipse graph with bounded aspect ratio, which differs by the fact that the ellipses are not anymore axis-aligned, an empty region graph where regions are defined by fourth order equations, and some features on nearestneighbor-like graphs.


<!-- p:63 -->


## Chapter 6

### A sub-graph and a super-graph of the 2D-Delaunay triangulation

In Part I, Section 3.2, we have shown that the expected degree of a point in the 2D-Delaunay triangulation is 6 (Theorem 3.1). Even if this case was simple, some of the involved computations were quite tedious. In this chapter, we show that a lower or an upper bound can be obtained with far much less effort.

#### 6.1 The Gabriel and half-moon graphs

A way to obtain a lower and an upper bound on the expected degree of a point in the Delaunay triangulation, is to consider a sub-graph and a super-graph. In order to find such graphs, we prefer to consider a different definition of the Delaunay triangulation. Instead of considering the neighborliness in Delaunay defined by three points and their circumscribed circle, we could use the equivalent property that two points are neighbors if there exists a disk with those two points on its boundary that is empty. Derived from this definition of the Delaunay triangulation, we suggest a method that provides a sub-graph and a super-graph of the Delaunay graph and so, allows to calculate a lower and an upper bound on the expected degree within a constant factor.

To obtain a sub-graph, we can simply restrict the set of possible disks. More precisely, for any pair (p, q), we consider the disk for which the segment [p, q] is a diameter. It is called the Gabriel disk of p and q and denoted gab(p, q) [GS69]. Then we consider the Gabriel graph, denoted Gab in which to points p and q are neighbors if gab(p, q) is empty.

To obtain a super-graph, we consider the half-moon method [DLM04]. We define the half-moons hmr(p, q) and hme(p, q) of p and q as being the two halves of the Gabriel disk gab(p, q) separated by the int  t       t   ss    t    y b) dn we consider the, so called, half-moon graph HM, in which two points p and q are neighbors if hm(p, q) or hme(p, q) is empty.

We formalize through lemmas, that those graphs are super-graph and sub-graph. This is illustrated in Figure 6.1.

Lemma 6.1. The Delaunay graph is included in the half-moon graph.

Proof. Consider a set X of points in the plane and, p and q in X that are neighbors in Del(X). By definition of the Delaunay triangulation, there exists a disk with p and q on its boundary that is empty. The center of that disk lies on the bisector line of [p, q] and, depending if it is to the right or the left of pÀ, the disk will contain, respectively, either hmr(p, q) or hme(p, q), that will in turn be also empty, by inclusion. So that p and q are also neighbors in HM(X). □

Lemma 6.2. The Gabriel graph is included in the Delaunay graph.

Proof. This is clear by noticing that we reduce the set of possibly disks with two given points on its boundary. □


<!-- p:64 -->


Figure 6.1: The Gabriel graph, on the left, is included in the Delaunay triangulation, in the middle, itself included in the half-moon graph, on the right.

Then we compute the expected degree of a point in Gab(X) and HM(X) for a Poisson point process X.

Lemma 6.3. Let X be a Poisson point process with intensity λ in R2 and p a point of R2. The expected degree E [deg (p, Gab)] of the origin p in the Gabriel graph Gab(X ∪ {p}) is 4.

Proof.

$$\mathbb { E } \left [ \deg ( p , G a b ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { I } _ { [ g a b ( p , q ) \cap X = \emptyset ] } \right ] \\ & = \int _ { q \in \mathbb { R } ^ { 2 } } \lambda \, \mathbb { P } \left [ g a b ( p , q ) \cap X = \emptyset \right ] \, d q \\ & = \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { 2 \pi } \lambda e ^ { - \lambda \frac { \pi r ^ { 2 } } { 4 } } r d \theta d r \\ & = 4 .$$

Lemma 6.4. Let X be a Poisson point process with intensity λ in R2 and p a point of R2. The expected degree E [deg (p, HM)] of p in HM(X ∪ {p}) is 12.

Proof. We can express the counting of neighbors of a point p in HM by the following way: q is neighbor of p, if hmr(p, q) or hme(p, q) is empty, but it should not be counted twice if both are empty, i.e. if gab(p, q) is empty. Thus:

$$\deg \left ( p , H M \right ) & = \sum _ { q \in X } \left ( \mathbb { I } _ { \left [ h m _ { r } ( p , q ) \cap X = \emptyset \right ] } + \mathbb { 1 } _ { \left [ h m _ { \epsilon } ( p , q ) \cap X = 0 \right ] } - \mathbb { 1 } _ { \left [ g a b ( p , q ) \cap X = 0 \right ] } \right ) \text { and so,} \\ \mathbb { E } \left [ \deg \left ( p , H M \right ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X } \left ( \mathbb { I } _ { \left [ h m _ { r } ( p , q ) \cap X = 0 \right ] } + \mathbb { 1 } _ { \left [ h m _ { \epsilon } ( p , q ) \cap X = 0 \right ] } - \mathbb { 1 } _ { \left [ g a b ( p , q ) \cap X = 0 \right ] } \right ) \right ] ,$$

then we can apply Slivnyak-Mecke theorem and the result of the previous lemma:

$$\mathbb { E } \left [ \deg \left ( p , H M \right ) \right ] = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( \mathbb { P } \left [ h m _ { r } ( p , q ) \cap X = \emptyset \right ] + \mathbb { P } \left [ h m _ { \ell } ( p , q ) \cap X = \emptyset \right ] \right ) d q - 4 ,$$


<!-- p:65 -->


and since |hmr(p, q)| = |hme(p, q)|,

$$| \Psi ( p , H M ) | & = 2 \int _ { \mathbb { R } ^ { 2 } } \lambda \, \mathbb { P } \left [ h m _ { r } ( p , q ) \cap X = \emptyset \right ] d q - 4 \\ & = 2 \int _ { \mathbb { R } ^ { 2 } } \lambda e ^ { - \lambda | h m _ { r } ( p , q ) | } d q - 4 \\ & = 2 \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { 2 \pi } \lambda e ^ { - \lambda \frac { \pi r ^ { 2 } } { 8 } } r d \theta d r - 4 \\ & = 1 6 - 4 \\ & = 1 2 .$$

□

And we finally bound the expected degree of the point p in the Delaunay triangulation:

Corollary 6.5. Let X be a Poisson point process with intensity λ in R2 and p a point of R2. The expected degree E [deg (p, Del)] of p in Del(X ∪ {p}) is Θ(1) .

Proof. We apply the five lemmas above to obtain the inequality:

$$4 = \mathbb { E } \left [ \deg \left ( p , G a b \right ) \right ] \leq \mathbb { E } \left [ \deg \left ( p , D e l \right ) \right ] \leq \mathbb { E } \left [ \deg \left ( p , H M \right ) \right ] = 1 2 .$$

□

This result is weaker than the exact bound of Theorem 3.1 but the computations are much simpler. It also illustrates that, given similar regions, the degree remains equal in order of magnitude. In that case, for two points p and q, gab(p, q) and hmr(p, q) or hme(p, q) have both an area quadratic in the distance between p and q, and this induces a constant expected degree.


<!-- p:66 -->


54 Chapter 6. A sub-graph and a super-graph of the 2D-Delaunay triangulation


<!-- p:67 -->


## Chapter 7

### General method

We propose a general method that both formalizes and generalizes the half-moon method to link the ss   s -     s - a s o formalize the following facts: (i) the Delaunay disks can be parameterized by their center on the bisector line of [p, q], (ii) this bisector line can be partitioned in two half-lines from the middle of [p, q], and (iii) each half-moon is contained in all disks centered on one of the half-lines.

In a more general setting, the general idea is (i) to identify a parameter space in Rk defining the regions, (ii) to partition this space in convex domains, and (ii) have inclusion relations for regions at the vertices of the partition.

In this Chapter, we introduce the three main tools that will be use to formalize this method, namely the notion of empty region graph, the Combination lemma, and the Partition lemma. At the end of the chapter, we prove again Corollary 6.5 in this formalized context.

#### 7.1 Empty region graphs

We start by defining the notion of empty region graph [CCL09]:

Definition 7.1. For each pair (p, q) ∈ Rd × Rd, let R(p, q) be a family of regions. Consider a locally finite point set X ⊂ Rd. We denote by R(X) the directed graph on X in which q is a successor of p if there exists an empty region in R(p, q).

This notion unifies the classical Delaunay triangulation [Del34] where R(p, q) is the set of disks whose boundaries contains p and q, the Gabriel graph [GS69] where R(p, q) is reduced to the disk of diameter pq, the β-skeleton [ABE98, KR85] where R(p, q) is either the intersection or the reunion of two disks whose boundary contains p and q, the empty ellipse graph [DEG08], the nearest-neighbor graph where R(p, q) is reduced to the disk centered on p and passing through q, the Θ-graphs where R(p, q) is reduced to a truncated cone emanating from p, and passing though q, and the Yao graphs [Yao82] where R(p, q) is reduced to an angular sector emanating from p, and passing though q.

0

We chose to consider the directed version of empty region graph, because it fits better with the computations we do. Indeed, we might pay attention to the symmetry of R(p, q). If R(p, q) = R(q, p), the case for the Delaunay triangulation and the Gabriel graph, among others. In that case, we will write simply GR(X) without an arrow, its directness is not involved in the counting. Conversely, if R(X) that goes in a single direction. In such a graph, we {hme} ≠ {hmr,hme}' but if we would have considered undirected graphs, those three graphs would have been the same, since hmr(p, q) = hme(q, p).

In the previous section, we have computed the expected degree of a point in the half-moon graph and the Gabriel graph. The main reason why they have an easier computation than the Delaunay triangulation is because their family of empty regions is finite. That is something we will try to reproduce in the following. If an empty region graph is too difficult to study, we show that we can find a super-graph and a sub-graph whose families of regions are finite. If we can, we choose two bounding graphs whose expected degree have the same order of magnitude.


<!-- p:68 -->


7R, we can either restrict the set of regions or consider larger regions. We formalize this in the following lemma:

Lemma 7.2. For all pairs (p, q), let R(p, q) and R'(p, q) be two families of regions. If, for any r′ ∈ R·

If for all r' ∈ R'(p, q), there exists r ∈ R such that r ⊂ r', then it exists r1 ∈ R that is included in r0 and □

Thus, in order to find a super-graph of a given empty region graph Gk, it would be enough to find a family of regions R' such that for all r ∈ R(p, q), there exists r' ∈ R' such that r' ⊂ r. But this is not that easy, to help us in this objective, we introduce two lemmas in the next section.

#### 7.2 Combination and Partition lemmas

The following lemmas are instrumental for proving that if a set of regions depends on k parameters and if the k-tuple of parameters belongs to a convex polyhedron P of Rk then, if we want to prove that all regions parameterized by P contain a given region, it is enough to prove this inclusion for the regions parameterized by the vertices of P. If P is not bounded, we can extend the lemma to limit points at infinity: for a point c going to infinity along some ray of Rk the region rc has a limit. The result also holds using this limit regions. We will show below as a didactic example how this lemma can be applied on Delaunay disks.

Before introducing the lemmas, we need hypotheses on the possible family of regions. Thus we introduce the notion of good pencil of regions:

Definition 7.3. A family of regions R is called a k-dimensional good pencil in Rd, if

- for any r ∈ R, there exists c ∈ Rk and Ec : Rd → R such that r = {x ∈ Rd, Ec(x) &lt; 0}, and
- for any x ∈ Rd, either the sign of c → Ec(x) is constant, or there exists one hyper-plane of dimension k − 1 in Rk that cuts Rk into a part on which c → Ec(x) is negative and a part on which c → Ec(x) is positive.

In practice, for any c, we consider an equation Ec(x) &lt; 0. For a given c, it defines a region, that we denote rc, for which c is called the parameter. In some cases, we will not be interested in all regions defined by c ∈ Rk, but only on a restricted domain of Rk. This restricted domain will be called the space of parameters of the pencil.

An example of (d-1)-dimensional good pencil in Rd, is the set of d-balls whose boundary contains 2 given points. They define the regions used for the dD-Delaunay triangulation. In this case, Ec(x) is an equation quadratic in x and linear in c, the linearity in c ensures the good pencil property.

Lemma 7.4 (Combination Lemma). Let R be a k-dimensional good pencil of regions in Rd, and consider a region rc ∈ R parameterized by c. If c ∈ P ⊂ Rk, then rc contains ∩rv , where X(P) denotes v∈X(P)

the extreme points of the convex hull of P.

Proof. Consider a polytope P ⊂ Rk and two vertices a and b of P. Let x ∈ Rd be a point of ra ∩ rb, and t et (xt e x t     t  x t ] s t  td   l  e. And since R is a good pencil, c → Ec(x) is then negative on [a, b]. Thus rc contains x. The extension from a segment [a, b] to the convex hull of P in the case k &gt; 1 follows directly from its convexity. □


<!-- p:69 -->


where R is a good pencil of regions. For any polytope P, we can consider the region rρ(p, q) that is the intersection of is a super-graph of R. If {r0} c lies in a space that can be partitioned into such polytopes, then we can apply the Combination lemma on all the polytopes to ensure that the graph that is the reunion of the empty singleton-region graphs defined for each polytopes is a super-graph of 70 This is stated in the next lemma:

be an empty region graph with R(p, q) = {rc, c ∈ P ⊂ Rk} a set of regions parameterized by c. Let (Pi)1≤i≤n be a convex subdivision of P, the parameter space. Let R R* and

$$\overrightarrow { d e g } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { R } } ^ { 0 } \right ) \leq \sum _ { 1 \leq i \leq n } \overrightarrow { d e g } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { R } } ^ { 0 } \right )$$

Proof. Consider the pair (p, q) and the region rc(p, q). Using the convex subdivision, there is some i such that c ∈ Pi and ri(p, q) ⊂ rc(p, q) by the hypothesis in the lemma. Then is a sub-graph of R as a corollary of Lemma 7.2. □

Note that the lemma holds for undirected graphs that can be seen as directed graphs with the two orientations for each edge.

#### 7.3 Alternative proof of the linear complexity of the Delaunay triangulation

We show, as an example, that any Delaunay triangulation is a sub-graph of the half-moon graph using Combination and Partition Lemma:

Alternative proof of Lemma 6.1. Consider two points p and q in the plane. Let R(p, q) be the family of disk with p and q on their boundary. We show that any disk of R(p, q) contains either hmr(p, q) or hme(p, q).

2yq by xc. In that parameterization, xc → Ec(x, y) is an affine function and so R(p, q) is a good pencil

Consider a coordinate system in which p is the origin. We assume without loss of generality that yq &gt; 0. A disk of R(p, q) can be parameterized by the inequality Ec(x, y) : x2 − 2xxc + y2 − 2yyc &lt; 0 −2xqxc+yq where c verifies yc = i. Note that Ec(x, y) depends on p and q, but we hide it in the notations. 2yq −2xqxc+y2 Since yc = tee  xc =  se    toe  t   tt  et se the actual geometric centers of the disks. That provides a 1-dimensional family of disks parameterized

Then we can consider the center cgab = (xgab, ygab) of the Gabriel disk and the center cr at infinity on the bisector line to the right of pÈ, note that the x coordinate xr of cr is +∞ since yq &gt; 0; their associated regions are the Gabriel disk gab(p, q) and the half-plane HPr(p, q) to the right of p♀. Since the ray [xgab, xr) is convex, we can apply the Combination lemma with (k, d) = (1, 2) to ensure that any disk whose center belongs to [cgab, cr) contains hmr(p, q), indeed hmr(p, q) = gab(p, q) ∩ HPr(p, q) (see Figure 7.1). We apply the same reasoning for hme(p, q), and disk centered on [cgab, ce). Finally, since [xgab, xr) and [xgab, xe) partition the whole set R of parameters, we can apply the Partition lemma to conclude that any disk with p and q on its boundary, contains either hm,(p, q) or hme(p, q) depending on the position of its center on the bisector line, and that proves that for any data sample X, that Del(X) is a sub-graph of HM(X). □

#### 7.4 Formalized method

On the basis of this example, we describe the general idea of the method we will apply to compute an upper bound on the expected degree of a point in a given empty region graph applied on a Poisson point process.


<!-- p:70 -->


Figure 7.1: Any disk with p and q on its boundary contains either hmr(p, q) or hme(p, q).

gab

q

gab

p

HPr

Ic

We consider the origin p ∈ Rd and, for any q ∈ Rd, a good pencil R(p, q) of regions of Rd. We find a parameterization for each region of R(p, q) in the form of a family of inequalities Ec(x) &lt; 0. We say that c is the parameter of the region rc(p, q) = {x ∈ Rd, Ec(x) &lt; 0}. Remind that c depends also on q, but we hide it to lighten the notations.

Still for a given q ∈ Rd, we partition this space of parameters into disjoint convex polytopes that we call tiles. The tiles are choşen such that their vertices are parameter of specific regions that characterizes the degree of the graph R (e.g. in the same sense that the Gabriel disk characterizes the degree of the Delaunay triangulation). Then we apply Combination lemma to obtain a fundamental region as the intersection of the regions parameterized by the vertices of the tile. Of course, if a tile is not well chosen, the computed degree may not be tight.

The reunion of the fundamental regions constitute the finite family F(p, q), in bijection with a family of tiles that pave the space of parameters c by the following relation: for each region r(p, q) ∈ F(p, q), there exists a unique tile T(p, q) such that for all c ∈ T(p, q), rc(p, q) contains r(p, q) (e.g. for the halfmoons, F = {hmr, hme}). This family F(p, q) defines in turn the super graph x that is a super-graph by Partition lemma.

To obtain an upper bound on the expected degree of p in (X ∪ {p}), it remains to compute R the expected degree of p in κ(X ∪ {p}) (or an upper bound), that is supposed to be easier. The computations will involve Poisson formulas that are functions of the area of regions. For some regions, this can lead to quite complicated integrals. In order to simplify this computation we may use smaller regions with easier expressions. Here again, it is essential to preserve the order of magnitude of the area.

To complete the analysis, we get a lower bound by selecting, for each q, a single region ro(p, q) from to guarantee the tightness of both bounds.

For the sake of clarity, we usually get rid of some parts of the notations, like the pair (p, q).

#### 7.5 Expected degree in some empty singleton-region graphs

Cn  .(     (          o   l (X ∪ {p}) is given by: {r}

$$\mathbb { E } \left [ \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \{ r \} } ^ { \emptyset } \right ) \right ] = \lambda \int _ { q \in \mathbb { R } ^ { d } } e ^ { - \lambda | r ( p , q ) | } d q .$$


<!-- p:71 -->


If the volume of the regions r(p, q) varies homogeneously with the distance |pq|, i.e. if there exists a positive constant Vr such that |r(p, q)| = Vr|pq|d, then we can apply a spherical variables substitution to obtain the following lemma:

Lemma 7.6. For each pair (p, q) ∈ Rd × Rd, let r(p, q) be a region of Rd. Let X a Poisson process distributed in Rd. If there exists Vr such that |r(p, q)| = Vr|pq|d, then

$$\frac { V _ { d } } { V _ { x } } ,$$

where Vd denotes the volume of the unit d-ball.

Proof. We recall that:

$$\mathbb { E } \left [ \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \{ r \} } ^ { \emptyset } \right ) \right ] & = \lambda \int _ { q \in \mathbb { R } ^ { d } } e ^ { - \lambda | r ( p , q ) | } d q \\ & = \lambda \int _ { q \in \mathbb { R } ^ { d } } e ^ { - \lambda V _ { r } | p q | ^ { d } } d q .$$

since the regions are homogeneous. Applying a spherical variable substitution, we obtain:

$$\mathbb { E } \left [ \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \{ r \} } ^ { \emptyset } \right ) \right ] = \lambda \int _ { s \in S ^ { d } \ 1 } \int _ { 0 } ^ { + \infty } \rho ^ { d - 1 } \ e ^ { - \lambda V _ { r } \rho ^ { d } } d \rho d s ,$$

where Sd-1 denotes the unit sphere,

$$\mathbb { E } \left [ \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \{ r \} } ^ { \emptyset } \right ) \right ] & = \lambda \int _ { s \in S ^ { d } \ 1 } \, d s \left [ - \frac { 1 } { \lambda d V _ { r } } e ^ { - \lambda V _ { r } \rho ^ { d } } \right ] _ { 0 } ^ { + \infty } \\ & = \frac { | S ^ { d - 1 } | } { d V _ { r } } \\ & = \frac { V _ { d } } { V _ { r } } .$$

□

This case has actually already been studied by Devroye in [Dev88] in a more general configuration, but we presented here a far simpler proof for Poisson processes.

2 t     =  d d, d  t   p e p  ) the expected outer degree of any point of X in the Gabriel graph is π = 4, proving again Lemma 6.3.

We illustrate this lemma for some 2-dimensional empty region graphs that we already computed before. In 2D, the unit ball is the unit disk, and Vd = π. Consider the nearest neighbor graph. It is the for which r(p, q) = D(p, q), the disk centered on p passing through q. It is clear that |r(p, q)| = π|pq|2. Thus, by Lemma 7.6, if X denotes a Poisson process in R2, the expected outer degree of any point of X is π = 1. Actually, this is obvious since, in general position, a point has only one nearest neighbor.


<!-- p:72 -->


Chapter 7. General method


<!-- p:73 -->


## Chapter 8

### Empty axis-aligned ellipse graphs

In that section, we analyze empty region graphs where the regions are axis-aligned ellipses. By "axisaligned", we mean that their axes of symmetry are parallel to the x and y axes. We then call aspect ratio, the ratio of the lengths of the vertical axis to the horizontal axis of the ellipse.

#### 8.1 Some features with axis-aligned ellipses

te spne o e p  s e ope e oe s oos  bn used thereafter. In R2, we consider an axis-aligned ellipse with the origin p on its boundary. We denote the ellipse r since it is seen as a region. Such an ellipse has three degrees of freedom, that can be set by considering a positive number α and a point c = (xc, yc), so that r can be defined by the inequality:

$$r \colon \alpha ^ { 2 } x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } < 0 .$$

In that parameterization, c is the parameter of r, and α its aspect ratio. To ensure that the boundary of the ellipse passes through a second point q, we have to set one of the three parameters xc, yc or α, so that we add the equation:

$$\alpha ^ { 2 } x _ { q } ^ { 2 } - 2 x _ { q } x _ { c } + y _ { q } ^ { 2 } - 2 y _ { q } y _ { c } = 0 .$$

Expressing α in terms of c and q, we define

$$E _ { c } ( x , y ) = & \alpha ^ { 2 } x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } , \quad \text {with } \alpha ^ { 2 } = \frac { 2 x _ { q } x _ { c } - y _ { q } ^ { 2 } + 2 y _ { q } y _ { c } } { x _ { q } ^ { 2 } } ,$$

and name rc(p, q) the only axis-aligned ellipse passing through p and q with c for parameter. A parameterization of rc(p, q) is then:

$$r _ { c } ( p , q ) \colon E _ { c } ( x , y ) < 0 .$$

In most of the proofs, we bring the expression back to a more common one, namely 22 a2 十 b2 − 1 = 0, in which the ellipse has aspect ratio b and area πab. 0

Proposition 8.1. For a given q ∈ R2, the parameters c of the ellipses rc(p, q) with same aspect ratio lie on a line perpendicular to (pq).

Proof. Set α in the equation: α2x2 − 2xqxc + y2 − 2yqyc = 0. The set of points c = (xc, yc) that verify the equation defines a line parallel to L : xxq + yyq = 0, by omitting the constant terms α2x2 + y2. But the expression of L defines clearly a line perpendicular to (pq), and adding back the constant term don't affect the direction of the line. □

Proposition 8.2. For a given q ∈ R2 and for α ∈ R+, consider the ellipse rc(p, q) parameterized by 2, 2

The geometric center of rc(p, q) is the middle of [p, q], and its area is π一4 (αx2 .2 十 y2 0


<!-- p:74 -->


Proof. We note Ec(x, y) := α2x2 − 2xxc + y2 − 2yyc with α2 = 2xqxc−y2 +2yqyc If yc = 2yq, then x α2 − 2xqxc = 0, and so xc = 12 α2xq. We rewrite the expression of Ec(x, y) to obtain a canonical from:

2

$$\alpha ^ { 2 } x ^ { 2 } _ { q } - 2 x _ { q } x _ { c } & = 0 , \, \text {and} \, \ s o \ x _ { c } = \frac { 1 } { 2 } \alpha ^ { 2 } x _ { q } . \, \text {We rewrite the expression of } E _ { c } ( x , y ) \, \text {to obtain a canonical from:} \\ E _ { c } ( x , y ) & = \alpha ^ { 2 } x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } \\ & = \alpha ^ { 2 } x ^ { 2 } - \alpha ^ { 2 } x _ { q } + y ^ { 2 } - y y _ { q } \\ & = \alpha ^ { 2 } ( x ^ { 2 } - x x _ { q } ) + y ^ { 2 } - y y _ { q } \\ & = \alpha ^ { 2 } \left ( ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 2 } - ( \frac { 1 } { 2 } x _ { q } ) ^ { 2 } \right ) + ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } \\ & = \alpha ^ { 2 } ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 2 } + ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - \frac { 1 } { 4 } \alpha ^ { 2 } x _ { q } ^ { 2 } - \frac { 1 } { 4 } y _ { q } ^ { 2 } \\ & = \frac { 1 } { 4 } \left ( \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) \left ( 4 \frac { \alpha ^ { 2 } } { \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 2 } + 4 \frac { 1 } { \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - 1 \right ) . \\ \text {So that another equation of } r _ { c } ( p , q ) \text { is}$$

So that another equation of rc(p, q) is:

$$4 \frac { \alpha ^ { 2 } } { \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 2 } + 4 \frac { 1 } { \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - 1 < 0 .$$

We identify, with that expression, that re(p, q) is the translation, by the vector pÀ, of the ellipse defined by:

$$4 \frac { \alpha ^ { 2 } } { \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } x ^ { 2 } + 4 \frac { 1 } { \alpha ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } y ^ { 2 } - 1 < 0 ,$$

(αx2 y2 whose center is p, and area is π 十 五 α

□

Such an ellipse rc(p, q), with c = 1α2xq, yq), i.e. centered on the middle of [p, q] and with aspect ratio α, will be denoted Ellα (p, q). As an example, we have Ell1 = gab.

In Parts III and IV, ellipses may be parameterized by inequalities of the form:

$$\alpha _ { 1 } ^ { 2 } x ^ { 2 } - 2 x x _ { c } + \alpha _ { 2 } ^ { 2 } y ^ { 2 } - 2 y y _ { c } \leq 0 ,$$

that induces an aspect ratio α1 With that parameterization, the parameter that makes the ellipse centered on the middle of [p, q] is c = (−α1xq, α2 α2yq). 2

#### 8.2 Empty axis-aligned ellipse graph

In this section, we prove, using our framework, a logarithmic bound for the empty axis-aligned ellipse graph of a Poisson point process in a bounded domain. A similar result was proven for a uniform distribution instead of a Poisson distribution [DEG08].

For two points p and q in R2, we consider the family E(p, q) of all axis-aligned ellipses with p and q on their boundaries. Assuming that p is the origin, we show that the expected degree of p in the associated empty-region graph G%(X) is Θ(ln λ) when X is a Poisson process of intensity λ.

##### 8.2.1 Upper bound on the expected degree

In order to identify an upper bound, we consider the graph G∆ {∆r,∆e} where ∆r(p, q) (resp. ∆e(p, q)) dd  s (e  tt  oe   s  rt t -e t sp

Lemma 8.3. G% is a super-graph of G%. {∆r,∆e}

Proof. Consider two point p and q in R2. All regions involved depend on the pair (p, q), since it is clear, we omit to write it. For each region rc ∈ E, we consider the parameterization given by Equation 8.1.

The inequality Ec(x, y) &lt; 0 is an affine parameterization of the ellipse rc(p, q) by c = (xc, yc). Thus € is a good pencil. We may pay attention to the fact that c is not the usual geometric center of the ellipses. The space P ⊂ R2 where c lives is delimited by the inequality: 2xqxc − y2 + 2yqye &gt; 0 that is the half-plane whose boundary is the line perpendicular to (pq) passing through c0 = (0, y¿) and that does not contain p, otherwise the equation has no real solutions. We study briefly the behavior of the regions according to the position of their parameter: as seen in section 8.1, each line parallel to the boundary of the half-plane preserves the value of α, in that sense, we name Lα the line {(x, y), α2x2 = 2xqx−y2+2yqy} q of parameters of ellipses with aspect ratio α (Proposition 8.1).


<!-- p:75 -->


Figure 8.1: Left: The partition of space of parameters in R2 into {Pr, Pe}. Right: The corresponding family of ellipses. Any region whose parameter is in Pe, like rc, contains ∆r, and conversely for Pe.

4

cl

L0

Pl

b

c∞

LMid

co

●

p

Pr

Cr

Ell∞

rc

b

HP

Ell0

HP

r

On the boundary L0 of P, the ellipses degenerate into parabolas, more precisely, at the infinite parameters cr, on the right of pÀ and ce, on its left, the parabolas degenerate them-selves into, respectively, the half-planes HPr and HPe whose boundary is (pq). At c0, rc0 degenerates into the horizontal strip rc0 = {|y − yq 2 2

Then, we consider the horizontal ray LMid : y = y ∩ P, emanating from co, and named after the fact that any ellipse parameterized on LMid is centered on the middle of [p, q]. Let c∞ be the point at infinity on this ray, When the parameter c is equal to c∞, its region degenerates into the vertical strip: rc∞ = {|x − xq &lt; |xq|} }, seen as a vertical ellipse with infinite aspect ratio and so corresponding to Ell∞. 2 On LMid, ellipses warp continuously from the horizontal strip Ell0 to the vertical one Ell∞.

Finally we define Pr = (cr, c0, c∞) and Pe = (c∞, c0, ce), where (a, b, c) denotes the angular sector between [b, a) and [b, c).

By the Combination lemma, if c ∈ Pr then

$$\Delta _ { r } = E l l ^ { 0 } \cap H P _ { r } \cap E l l ^ { \infty } \subset r _ { c }$$

$$\Delta _ { \ell } = E \text {ll} ^ { 0 } \cap H P _ { \ell } \cap E \text {ll} ^ { \infty } \subset r _ { c } .$$

and if c ∈ Pe then

And since Pr and Pe partition the space of parameters P, by the Partition lemma, we have

$$\mathcal { G } _ { \mathfrak { E } } ^ { \emptyset } \subset \mathcal { G } _ { \{ \Delta _ { r } , \Delta _ { \ell } \} } ^ { \emptyset } = \mathcal { G } _ { \{ \Delta _ { r } \} } ^ { \emptyset } \cup \mathcal { G } _ { \{ \Delta _ { \ell } \} } ^ { \emptyset } .$$

Now, we bound from above the expected degree of p in G0 Gł∆r,∆e}(X ∪ {p}) when X is a Poisson point process with intensity λ. The area of both the triangles ∆r and ∆e is |xqyq| . Unfortunately, for 2 any positive λ, SR ∫R e−λ|xy|dydx does not converge. In that case, we assume that X is distributed in a rectangle R = [−L, L] × [−l, l] for positive L and l.

Lemma 8.4. Let X be a Poisson point process with intensity λ in R = [−L, L] × [−l, l]. The expected Proof. Before computing the expected degree, we introduce a utility lemma proven in Appendix A.2, that bounds the integral IL,t(t) = ∫0ν ∫0 1J T e−txydydx for a positive t:


<!-- p:76 -->


Lemma 8.5. Let L, l, and t be 3 positive numbers. If tLl &gt; 1 then:

$$\frac { \ln ( t L l ) } { t } < I _ { L , l } ( t ) \leq \frac { \ln ( t L l ) } { t } + \frac { 1 } { t } .$$

As in Section 6.1, we can express the counting of neighbors of a point p in GΔ G{∆r,∆e}(X ∪ {p}) by the following way: q is neighbor of p, if ∆r or ∆e is empty, but it should not be counted twice if both are empty, i.e. if ∆r ∪ ∆l is empty. Thus:

$$\deg \left ( p , \mathcal { G } _ { \{ \Delta _ { r } , \Delta _ { \ell } \} } ^ { 0 } \right ) = \ \sum _ { q \in X } \left ( \mathbb { I } _ { [ \Delta _ { r } \cap X = 0 ] } + \mathbb { I } _ { [ \Delta _ { \ell } ( p , q ) \cap X = \emptyset ] } - \mathbb { I } _ { [ ( \Delta _ { r } \cup \Delta _ { \ell } ) \cap X = \emptyset ] } \right ) ,$$

for which we compute the expected value:

$$for \text { which we compute the expected value: } \\ \\ \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \Delta , \Delta , \ell } ^ { \emptyset } \right ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { I } _ { \Delta , \cap X = 0 } + \mathbb { I } _ { \Delta , \cap X = 0 } \right ] - \mathbb { I } _ { ( \Delta , \cup \Delta _ { \ell } ) \cap X = 0 } \right ] \\ & = \int _ { R } \lambda ( \mathbb { P } \left [ \Delta _ { r } \cap X = \emptyset \right ] + \mathbb { P } \left [ \Delta _ { \ell } \cap X = \emptyset \right ] - \mathbb { P } \left [ ( \Delta _ { r } \cup \Delta _ { \ell } ) \cap X = \emptyset \right ] ) d q \\ & = \int _ { R } \lambda \left ( 2 e ^ { - \lambda | \Delta _ { r } | } - e ^ { - 2 \lambda | \Delta _ { r } | } \right ) d q \\ & = \int _ { - L - \ell } ^ { L } \int _ { \lambda } \lambda \left ( 2 e ^ { - \lambda | \frac { x y } { 2 } | } - e ^ { - \lambda | x y | } \right ) d y d x \\ & = 4 \lambda \left ( 2 \int _ { 0 } ^ { L } \int _ { 0 } ^ { \ell } e ^ { - \lambda x } \frac { y d x } { d y d x - \int _ { 0 } ^ { L } \int _ { 0 } ^ { \ell } e ^ { - \lambda x } d y d x } \right ) \\ & = 4 \lambda \left ( 2 I _ { L } ( \frac { \lambda } { 2 } ) - I _ { L } ( \lambda ) \right ) \\ & = 4 \lambda \left ( \frac { 4 } { \lambda } \left ( 1 + \ln ( \frac { \lambda L L } { 2 } ) \right ) - \frac { \ln ( \lambda L l ) } { \lambda } \right ) + O ( 1 ) \text { by Lemma 8.5} , \\ & = 4 \left ( 3 ( \ln ( \lambda ) + \ln ( L l ) ) + 4 ( 1 - \ln ( 2 ) ) \right ) + O ( 1 ) \\ & = 1 2 \ln ( \lambda L l ) + O ( 1 ) .$$

□

Remind that, for the Delaunay triangulation, the constant expected degree is derived from the fact that the Gabriel disk of two points has an area quadratic in their distance. For that new case, with ellipses, it is the "xy" area that provides a logarithmic degree.

-h  o  t  os -ee  ot   on re d t s tion, we might also be interested in a lower bound.

##### 8.2.2 Lower bound on the expected degree

We find one by considering an empty region graph where the set of regions is strictly included in the original one. Still using the example of the Delaunay triangulation we try to identify, for a point q, a special ellipse that plays the role of Gabriel disk. In order to get a tight bound, the area of the chosen ellipse must be Θ(xqyq).

To find such an ellipse, we use Proposition 8.2, in which it is stated that an ellipse rc parameterized by Equation 8.1, and centered on the middle of [p, q] has parameter c with yc = yq and area 2


<!-- p:77 -->


te p dse o o os e  o s  s se -xe e :t : te points lie on the hyperbola y = 1 the ellipses have the same area. Right: An instance of G0 x, {xy-Ell} restricted to the red point p. A far point keeps chance to be a neighbor of p as long as it is close to an axis.

s

p

:

π一4 (α(q)x2 十 We determine α(q) such that |rc| = π14 (α(q)x2 十 yq 2 by solving the equation q α(q)2 q α(q)2 A = π 4 (α(q)x2 2 q 十 α(q) 2 where α(q) is the unknown variable:

$$4 \left ( \mu ( q ) q ^ { q } \right ) ^ { 2 } \intertext { A = \frac { \pi } { 4 } \left ( \alpha ( q ) x _ { q } ^ { 2 } + \frac { y _ { q } ^ { 2 } } { \alpha ( q ) ^ { 2 } } \right ) } \Leftrightarrow \ 0 = \pi \frac { x _ { q } ^ { 2 } x _ { q } ^ { 2 } - A \alpha ( q ) + \frac { \pi } { 4 } y _ { q } ^ { 2 } } { 4 x _ { q } ^ { 2 } } \\ \Leftrightarrow \ 0 = \left ( \alpha ( q ) - 2 \frac { A - \sqrt { A ^ { 2 } - ( \frac { \pi } { 2 } x _ { q } y _ { q } ) ^ { 2 } } } { \pi x _ { q } ^ { 2 } } \right ) \left ( \alpha ( q ) - 2 \frac { A + \sqrt { A ^ { 2 } - ( \frac { \pi } { 2 } x _ { q } y _ { q } ) ^ { 2 } } } { \pi x _ { q } ^ { 2 } } \right ) \quad \text {if } A \geq \frac { \pi } { 2 } x _ { q } y _ { q } .$$

According to the equation, the wanted area must be greater than π/2 xqYq. This quantity appears to be a good candidate. We obtain α(q) = yq by substituting A by κ|2 xqYq in the previous equation. x2 xq That corresponds to the ellipse with equation:

$$r _ { c } ( p , q ) \colon \left ( \frac { y _ { q } } { x _ { q } } \right ) ^ { 2 } \left ( x - \frac { 1 } { 2 } x _ { q } \right ) ^ { 2 } + \left ( y - \frac { 1 } { 2 } y _ { q } \right ) ^ { 2 } \leq \frac { 1 } { 2 } y _ { q } ^ { 2 }$$

with the expression type we used in the beginning of the chapter, or

$$r _ { c } ( p , q ) \colon y _ { q } ^ { 2 } \left ( x - \frac { 1 } { 2 } x _ { q } \right ) ^ { 2 } + x _ { q } ^ { 2 } \left ( y - \frac { 1 } { 2 } y _ { q } \right ) ^ { 2 } \leq \frac { 1 } { 2 } x _ { q } ^ { 2 } y _ { q } ^ { 2 } ,$$

in a more symmetrical version.

y2 Thus, for any pair (p, q), we choose the ellipse rc(p, q) parameterized by c = yq and denoted 2xq 2 by xy-Ell(p, q) to fulfill the required conditions for a good sub-graph (see Figure 8.2).

Lemma 8.6. G%x is a sub-graph of G0. {xy-Ell}

$$P r o f { \sigma } { \text { Clearly because } } x y { \text {-Ell} } \in \mathfrak { E } . \quad \Box$$

Lemma 8.7. Let X be a Poisson point process with intensity λ in R = [−L, L] × [−l, l]. The expected degree E deg (p, G{xy-u)] of the origin p in G0x (X ∪ {p}) is Ω(ln λ + ln L + ln l). {xy-El}


<!-- p:78 -->


Proof. As said above, for any q ∈ R2, the area of xy-Ell(p, q) is πxqyq

Then we can express the expected degree:

$$\text {we can express the expected degree:} \\ \\ \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ x y - E l \} } ^ { 0 } \right ) \right ] = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { I } _ { x y - E l \cap X = 0 } \right ] \\ = \int _ { R } \lambda \mathbb { P } \left [ x y - E l l \cap X = 0 \right ] d p \\ = \int _ { R } \lambda e ^ { - \lambda | x y - E l | } d p \\ = \int _ { - L } ^ { L } \int _ { - l } ^ { l } \lambda e ^ { - \lambda | \pi ^ { \frac { x y } { 2 } } | } d y d x \\ = 4 \lambda \int _ { 0 } ^ { L } \int _ { 0 } ^ { l } e ^ { - \lambda \pi ^ { \frac { x y } { 2 } } } d y d x \\ = 4 \lambda I _ { L , l } ( \frac { \lambda \pi } { 2 } ) \\ = 4 \lambda \frac { 2 } { \lambda \pi } \ln ( \frac { \lambda \pi L l } { 2 } ) + \Omega ( 1 ) \text { by Lemma 8.5,} \\ = \frac { 8 } { \pi } ( \ln ( \lambda L l ) + \ln ( \frac { \pi } { 2 } ) ) + \Omega ( 1 ) \\ = \frac { 8 } { \pi } \ln ( \lambda L l ) + \Omega ( 1 ) .$$

So that we can finally conclude:

Theorem 8.8. Let X be a Poisson point process with intensity λ in R = [−L, L] × [−l, l]. The expected degree E [deg (p, Gk)] of the origin p in Gk(X ∪ {p}) is Θ(ln λ + ln L + ln l) .

Proof. We apply Lemmas 8.3 to 8.7:

$$\Omega ( \ln \lambda + \ln L + \ln l ) = \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ x y - \text {E} \} } ^ { \theta } \right ) \right ] \leq \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \mathfrak { e } } ^ { 0 } \right ) \right ] \leq \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ \Delta _ { r } , \Delta _ { l } \} } ^ { \theta } \right ) \right ] = O ( \ln \lambda + \ln L + \ln l ) .$$

□

#### 8.3 Ellipses with bounded aspect ratio, the rhombus graph

In the previous part, we proved that when the aspect ratio is not bounded, neither is the expected degree. One can wonder what happens when the aspect ratio ranges between two finite numbers. For two points p and q in R2 and a number β ∈ (0, 1), we consider the family ε[β,1](p, q) of horizontal elliptic regions with p and q on their boundary and whose aspect ratio ranges between β and 1. An important fact to be considered is that, when the aspect ratio is not bounded, a point q far from p could be a neighbor of p as long as it is close enough to the axis, since in that case, ellipses passing through p and q may have a small area, and that leads to a logarithmic bound. When the aspect ratio is bounded, all ellipses preserve an area Ω(x2 + y2), so that we expect a constant bound on the expected degree. We show that the expected degree of p in the empty region graph Gkts,1] (X ∪{p}) is Θ(ln 1) when X is a Poisson process of intensity λ.


<!-- p:79 -->


##### 8.3.1 An upper bound on the expected degree

In order to apply the same method as above, we search for simple geometrical regions that fit inside the whole family e[β,1](p, q). A good choice is the following: as before, we consider the intersection of ellipses that are centered on the midpoint of [p, q], and we cut the intersection along the line (pq). The remaining regions hm[β,1](p, q) and hm[β, [β,1] (p, q) look like two axis-aligned right triangles with rounded sides for almost all q (see side figure).

Ell1

q

hme

[β,1]

hm

[β,1]

p

$$\text {Lemma 8.9.} \ \mathcal { G } _ { \{ h m _ { r } ^ { [ \beta , 1 ] } , \ h m _ { \ell } ^ { [ \beta , 1 ] } \} } \ i s \ a \ s u p e r { - g r a p h } \ o f \mathcal { G } _ { \mathfrak { E } ^ { [ \beta , 1 ] } } ^ { 0 } .$$

Proof. The proof is very similar to the one of Lemma 8.3 so we just spell the important points out. For each rc(p, q) ∈ e[β,1](p, q), we consider the parameterization by Equation 8.1 where:

$$E _ { c } ( x , y ) = \alpha ^ { 2 } x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } , \, \text {with } \alpha ^ { 2 } = \frac { 2 x _ { q } x _ { c } - y _ { q } ^ { 2 } + 2 y _ { q } y _ { c } } { x _ { q } ^ { 2 } } \\ \text {and } \beta \leq \alpha \leq 1 .$$

2xqxc−y2+2yqyc The space P ⊂ R2 where c lives is delimited by the inequality: β2 ≤ ≤ 1 that is x2 the strip perpendicular to (pq) whose boundary are the lines Lβ and L1, where Lα = {(x, y), α2 二 2xqx − y2 + 2yqy}. We consider the segment defined by y = y yq inside P and its extremities cβ on Lβ and q c1 on L1. We partition P into Pr and Pe where Pr is the part of P on the right of [cβ, c1), and Pe the part on its left (see Figure 8.3).

By Combination lemma, if c ∈ Pr then hm[β,1] := Ell1 ∩ Ellβ ∩ HP, C rc and if c ∈ Pe then of G0 {hm, ,1,hm[θ,1]}

cβ and c1 have for regions the ellipses rcβ = Ellβ and rc1 = Ell1 with respectively β and 1 for aspect ratio. Furthermore, any parameter cr in P at infinity on the right of p♀ has its region that degenerates o     d    d  ss t  e (   e -  tt side, and the half-plane HPe).

4

cl

L1

Lβ

Pl

q

cβ

C1

p

●

Pr

Cr

HPè

HP

Figure 8.3: Left: The partition of space of parameters in R2 into {Pr, Pe}. Right: The two half-rhombuses Rhβ and Rhθ. In green, an ellipse whose parameter is in Pr, the ellipse contains Rhβ.

Ell1

p

Rhβ

β

Rh

q

Ellβ


<!-- p:80 -->


The problem now is that it may be complicated to comn[β,1] or hme n[β,1] pute an integral involving the area of hm To solve this issue, we consider a strictly smaller region. We could have used the axis-aligned right triangles ∆r and ∆e but their areas do not respect the order of magniue e se e e   (e   t call the half-rhombus. We define the rhombus Rhβ as the one whose vertices are the horizontal extreme points of rc1 and the vertical extreme points of rcβ. Then we separate it into two halves Rhβ and Rhβ, delimited by (pq). By con[β,1] (see Figure 8.3).

Ellβ

q

Rhβ

p

Ell1

Finally, we can say that G0 {Rhθ} is a super-graph of G0 {hm[β,1]} and that G0 {Rhβ} is a super-graph of G0 {hm[β,1]} Before proceeding to the computation of the expected degree, we introduce a lemma that provides properties on the involved integral. It is proven in Appendix A.2.

Lemma 8.10. Let t &gt; 0, β ∈]0, 1[, and Iβ(t) = ∫R ∫R Re−t√(x2+y2)(β2x2+y2)dydx,

$$I _ { \beta } ( t ) = \frac { 1 } { t } I _ { \beta } ( 1 ) \leq \frac { \pi } { t } \left ( 1 + \ln ( \frac { 1 } { \beta } ) \right ) .$$

And we can proceed to the computation of the expected degree in the half-rhombus graph:

Lemma 8.11. Let X be a Poisson point process with intensity λ in R2, and β ∈ (0, 1). The expected (X ∪ {p}) is O(ln

Proof. We first compute the area of the rhombus Rhβ(p, q). We identify its width and height as being respectively + y2 and √β2x2 + y2 so that the value of its area i given by (x2 + y2) (β2x2 + y2). b Then we can compute the expected degree of p in G0R (X): {Rhθ , Rhj }

$$Then we can compute the expected degree of p in G _ { \{ R h , R h \} } ^ { 0 } ( X ) \colon \\ \\ \mathbb { E } \left [ \deg \left ( p , G _ { \{ R h , R h \} } ^ { 0 } \right ) \right ] = \mathbb { E } \left [ \sum _ { q \in X } 1 _ { \{ R h \} \cap X = \emptyset } \lor R h ^ { \beta } \cap X = 0 \right ] \\ = \mathbb { E } \left [ \sum _ { q \in X } 1 _ { \{ R h , \rho \} \cap X = 0 } \right ] + 1 _ { \{ R h , \rho \} \cap X = 0 } ] - 1 _ { \{ R h \} \cap X = 0 } \right ] \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( \mathbb { P } \left [ R h ^ { \beta } , \cap X = \emptyset \right ] + \mathbb { P } \left [ R h ^ { \beta } _ { \ell } \cap X = \emptyset \right ] - \mathbb { P } \left [ R h ^ { \beta } \cap X = \emptyset \right ] \right ) d q \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( 2 e ^ { - \lambda \frac { 1 } { 2 } | R h ^ { \beta } | } - e ^ { - \lambda | R h ^ { \beta } | } \right ) d q \\ = \int _ { \mathbb { R } } \int _ { \mathbb { R } } \lambda \left ( 2 e ^ { - \frac { \lambda } { 4 } \sqrt { ( x ^ { 2 } + y ^ { 2 } ) ( \beta ^ { 2 } x ^ { 2 } + y ^ { 2 } ) } } - e ^ { - \frac { \lambda } { 2 } \sqrt { ( x ^ { 2 } + y ^ { 2 } ) ( \beta ^ { 2 } x ^ { 2 } + y ^ { 2 } ) } } \right ) d y d x \\ = \lambda ( \frac { 2 I _ { \theta } } { \beta } \left ( \frac { \lambda } { 4 } \right ) - I _ { \theta } \left ( \frac { \lambda } { 2 } \right ) ) \\ = \lambda \left ( \frac { \delta } { \beta } - \frac { 2 } { \lambda } \right ) I _ { \beta } ( 1 ) \\ \leq 6 \pi ( 1 - \ln \beta ) & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & &$$


<!-- p:81 -->


##### 8.3.2 A lower bound on the expected degree

We obtain a tight lower bound, when β goes to 0, by identifying, for each q, a particular region, named β-Ell(p, q), such that β-Ell(p, q) is or contains an element of e[β,1](p, q). To achieve this, we partition the plane into two parts (see Figure 8.4):

- if q ∈ Sβ := {(x, y), β|x| &lt; |y| &lt; |x|}, then, as in Lemma 8.7, we define β-Ell(p, q) := xy-Ell(p, q),
- otherwise β-Ell(p, q) := R2, that is another way to say that q is not a neighbor of p.

Lemma 8.12. G0 is a sub-graph of Gdl {β-Eu} E[β,1] ·

Proof. We prove the inclusion part-wise.

If q ∈ R2 such that β|xq| &lt; |yq| &lt; |xq|, we have to prove that β-Ell(p, q), i.e. xy-Ell(p, q), is in ε[β,1](p, q). This is true because the aspect ratio of β-Ell(p, q) is yq |, and verifies β &lt; yq &lt; 1 if xq xq β|xq| &lt; |yq| &lt; |xq|.

Otherwise, it is clear that β-Ell, i.e. R2, is larger than any other ellipse from e[β,1].

Figure 8.4: Left: Some β-Ell ellipses for points in Sβ. Right: An instance of G0β {β-Ell} where p is the red point. A far point reduces strongly its probability to be a neighbor of p because it cannot anymore be close to the axes.

R2\Sβ

●

Sβ

R2\Sβ

p

Lemma 8.13. Let X be a Poisson point process ith intensity λ in R2. The expected degree E [deg (p,Gβ-Eu)] G(β-Eu}(X ∪ {p}) is Ω (1n ). of the origin p in G0θ

Proof. β-Ell(p, q) is actually chosen to simplify the computation. Remind that Sβ is the domain {(x, y), β|x| &lt; |y| &lt; |x|},


<!-- p:82 -->


$$\mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ \beta - \Gamma _ { 1 } \} } ^ { \emptyset } \right ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X } 1 _ { [ \beta - \Gamma _ { 1 } ( p , q ) \cap X = \emptyset ] } \right ] \\ & = \int _ { \mathbb { R } ^ { 2 } } \lambda \, \mathbb { P } \left [ \beta - \text {El} ( p , q ) \cap X = \emptyset \right ] d p \\ & = \int _ { S _ { \beta } } \lambda \, \mathbb { P } \left [ \beta \, \text {El} ( p , q ) \cap X = \emptyset \right ] d p \\ & = \int _ { S _ { \beta } } \lambda - \lambda | \beta - \text {El} ( p , q ) | d p \\ & = 4 \int _ { 0 } ^ { \infty } \int _ { \beta x } ^ { x } \lambda - \pi ^ { \frac { \pi } { 2 } } \, \text {d} y d x \\ & = 4 \int _ { \tan } ^ { \frac { \pi } { 4 } } \, \int _ { ( \beta ) } ^ { \infty } \lambda r e ^ { - \lambda \pi ^ { \frac { \pi } { 2 } } \frac { \pi \cos ( \theta ) \sin ( \theta ) } { 2 } } d r d \theta \\ & = 4 \int _ { \tan } ^ { \frac { \pi } { 4 } } \lambda \, \frac { 1 } { \pi \cos ( \theta ) \sin ( \theta ) } d \theta \\ & = \frac { 4 } { \pi } \left ( \ln ( \tan ( \frac { \pi } { 4 } ) ) - \ln ( \beta ) \right ) & \quad \text {since } \frac { d } { d \theta } \ln ( \tan ( \theta ) ) = \frac { 1 } { \cos ( \theta ) \sin ( \theta ) } , \\ & = \frac { 4 } { \pi } \ln ( \frac { 1 } { \beta } ) . \\ & \quad \text {o} \\ \text {So that we can finally conclude:}$$

So that we can finally conclude:

Theorem 8.14. Let X be a Poisson point process with intensity λ in R2. The expected degree E [deg (p, GE[β,1)] of the origin p in Gkts,] (X ∪ {p}) is Θ (ln 1)

Proof. We apply Lemmas 8.9 to 8.13:

$$\Box$$

Since for any pair (p, q), and any positive number α, Ell (p, q) corresponds to Ellα(p, q) up to a rotation of 90°, if we had choose a β greater than 1, then we would have:

$$\mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \mathfrak { E } ^ { [ 1 , \beta ] } } ^ { \emptyset } \right ) \right ] = \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \mathfrak { E } ^ { [ \frac { 1 } { 3 } , 1 ] } } ^ { \emptyset } \right ) \right ] = \Theta \left ( \ln \beta \right ) .$$

#### 8.4 On empty axis-aligned ellipse graphs with a single aspect ratio

To complete the analysis, we might wonder what happens in the case of an empty axis-aligned ellipse graph with a single aspect ratio, like the Delaunay triangulation but instead of disks we have ellipses with another aspect ratio than 1.

By considering the transformation φ : (x, y) → (βx, y), the ellipses are transformed into circles, and we fall back in the Delaunay triangulation, but the sample points X have been changed also, and if X ( oe o ot oo re os se s oont o oont poo  oos

Suppose that we consider a positive β, and the empty region graph GR where for any pair (p, q) of points in R2, R(p, q) is the set of ellipses with aspect ratio β passing through p and q.


<!-- p:83 -->


Actually this is not a problem, since the empty region graph remains a triangulation, and since all points of X are equivalent, it is clear that their expected degree is 6.

We show why this has no impact in the computation: in the expression of the expected degree, we just have to replace the λ by β, and since

$$\frac { 1 } { 2 } \left ( \frac { \lambda } { \beta } \right ) ^ { 2 } \int _ { \mathbb { R } ^ { 2 } } \int _ { \mathbb { R } ^ { 2 } } e ^ { - \frac { \lambda } { \beta } | \mathcal { D } ( p , q , r ) | } d r d q = \frac { 1 } { 2 } \lambda ^ { 2 } \int _ { \mathbb { R } ^ { 2 } } \int _ { \mathbb { R } ^ { 2 } } e ^ { - \lambda | \mathcal { D } ( p , q , r ) | } d r d q ,$$

the result is indeed the same. We can conclude:

Lemma 8.15. Let X be a Poisson point process in R2 and p a point of R2. Let β be a positive number, and for any pair (p, q) of points in R2, let β(p, q) the family of ellipses with aspect ratio β with p and q on their boundary. The graph G is a triangulation and the expected degree E [deg (p, G)] of the origin p in G% β (X ∪ {p}) is 6.

This provides a way to construct a triangulation where the triangles are stretched in a given direction.


<!-- p:84 -->


72 Chapter 8. Empty axis-aligned ellipse graphs


<!-- p:85 -->


## Chapter 9

### On the probability of the existence of far neighbors

In this chapter, we compute, for the 2D-Delaunay triangulation and some empty axis-aligned ellipse graph, the probability that there exists a neighbor of p at a given distance. We show that this probability decreases exponentially with the distance.

#### 9.1 In the Delaunay triangulation

At some point, for a given graph G and a positive number t, we may be interested in computing the probability for p to have a neighbor in G at a distance greater than t.

As before, for illustration on a simple case, we start by the Delaunay triangulation:

Lemma 9.1. Let X be a Poisson point process with intensity λ in R2, p a point of R2, and t a positive number. The probability that p has some Delaunay neighbor at a distance greater than t is smaller than 8e−λ\_2t2.

Proof. If q is a Delaunay neighbor of p, Let σ be an empty disk whose boundary passes through p and q. If q is at distance greater than t from p, then the diameter of σ is obviously also greater than t, so its homothet σ' toward p that has exactly diameter t is included in σ and by consequence empty.

One can notice that, at least one triangle is included in σ': the one whose angular sector from p contains the center of σ'.

(√2t, ), and (1t, t) and its seven adjacent copies around p Consider the triangle with vertices p, ( (see Figure 9.1). We name them tri for i ∈ {1, . . . , 8}. Their area is |tr1| = √2t2. 8

So we get:

$$P \left [ \exists q \in X , \ ( p , q ) \in D e l ( X \cup \{ p \} ) \ | \ | p q | > t \right ] & \leq P \left [ \exists i \in [ 1 , \dots , 8 ] , \text {tr} _ { i } \cap X = \emptyset \right ] \\ & = \sum _ { i = 1 , \dots , 8 } \ \mathbb { P } \left [ \text {tr} _ { i } \cap X = \emptyset \right ] \\ & = 8 \mathbb { P } \left [ \text {tr} _ { 1 } \cap X = \emptyset \right ] \\ & = 8 e ^ { - \lambda \frac { \sqrt { 8 } t ^ { 2 } } { 8 } t ^ { 2 } } .$$

□

#### 9.2 In the empty axis-aligned graph with bounded aspect ratio.

We establish in the next lemma a similar bound for the empty axis-aligned ellipse graph with bounded aspect ratio in [β, 1]. We are mainly interested in the behavior of the probability when β is small, thus we assume β &lt; 12.


<!-- p:86 -->


Figure 9.1: If |pq| &gt; t, any disk passing through p and q contains one of the 8 triangles.

y

σ

σ0

C

o

tr2

tr1

t

x

Lemma 9.2. Let X be a Poisson point process with intensity λ in R2, p a point of R2, t and β two (e−λxβt2 + e−λxβ2t2). than t is smaller than 4

Proof. The idea of the proof is similar to the previous one, except that we apply a homothety on the empty ellipse σ until its image σ fits inside the axis-aligned square inscribed in the circle of radius t (see Figure 9.2).

We consider eight triangles (tri)1≤i≤8, that have the property that for any ellipse σ, σ′ contains one of them.

To this aim we define the four points:

$$v _ { 1 } = & ( \frac { 1 } { 2 } t , 0 ) , & v _ { 2 } = & ( \frac { \sqrt { 2 } } { 4 } t , \frac { \sqrt { 2 } } { 4 } \beta t ) , \\ v _ { 3 } = & ( \frac { \sqrt { 2 } \beta } { 4 } t , \frac { \sqrt { 2 } } { 4 } \beta t ) , & v _ { 4 } = & ( 0 , \frac { 1 } { 2 } \beta t ) .$$

The triangles tr1 and tr2 are respectively [pv1v2] and [pv3v4]. Their respective areas are √2 βt2 and 2 β t2. We will show that any ellise tangent to the square in the first quadrant (x, y ≥ 0) contains tr1 16 16 or tr2. We complete the set of triangles by their symmetrical copies with respect to the x-axis, to the y-axis and to the point p, and name them according to the trigonometric order from tr1 to tr8 to cover the ellipses tangent to other parts of the square.

Without loss of generality, we assume that the center c' of σ' is in the upper right quadrant. In such a case, the right most point of σ' has abscissa √2 t, its left most point has negative abscissa, and its center 2 verifies 0 ≤ xc′ ≤ 4

p and the symmetric of p, and thus is inside σ'. We prove that such ellipses, with xc′ ≥ 1t, also contain on Figure 9.2), with aspect ratio β. Since the abscissa of v2 is between p and v1, moving the center c' upward or to the left or increasing β imply that v2 remains inside σ'. So as long as xc' ≥ t, the triangle tr1 is inside σ'.

Suppose now that xc′ ≤ 1t. An equation of σ′, if its aspect ratio is α, is

$$\alpha ^ { 2 } x ^ { 2 } - 2 \alpha ^ { 2 } x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } \leq 0 .$$

For a fixed α, the lowest possible center is reached when xc′ = t and since σ' is tangent to the right side of the square at 2t, yc'), by substitution we have:


<!-- p:87 -->


Figure 9.2: If |pq| &gt; t, any ellipse passing through p and q contains one of the 8 triangles.

y

σ

U3

tr1

t

p

$$\frac { 1 } { 2 } \alpha ^ { 2 } t ^ { 2 } - \sqrt { 2 } \alpha ^ { 2 } t \frac { 1 } { 4 } t - y _ { c ^ { \prime } } ^ { 2 } = 0 .$$

Thus yc is minimized for α = β, and so:

$$y _ { c ^ { \prime } } = \frac { 1 } { 2 } \sqrt { 2 - \sqrt { 2 } } \, \beta t \simeq 0 . 3 8 3 \beta t .$$

We can deduce, by symmetry with respect to the horizontal axis of σ', that all those ellipses contain the segment between p and (0, √2 − √2 βt), including v4.

To prove that v3 ∈ σ', we make a distinction between the side of tangency of σ'. We call contact point of an ellipse, the point of the ellipse in which it is tangent to the square, for σ' we name it q'. Suppose first that σ' is tangent to the right side of the square. We consider the two extreme ellipses σhigh and σlow, with highest and lowest contact points Qhigh and qlow, at respectively t and √2 − √2βt for ordinate. They both contain v3:

- v3 ∈ σlow since

$$\beta ^ { 2 } \left ( \frac { \sqrt { 2 \beta } t } { 4 } \right ) ^ { 2 } - \beta ^ { 2 } \left ( \frac { \sqrt { 2 \beta } } { 4 } t \right ) \frac { t } { 4 } & + \left ( \frac { \sqrt { 2 } } { 4 } \beta t \right ) ^ { 2 } - 2 \left ( \frac { \sqrt { 2 } } { 4 } \beta t \right ) \frac { \sqrt { 2 - \sqrt { 2 } } } { 2 } \beta t \\ & = \beta ^ { 2 } t ^ { 2 } \left ( \frac { \beta } { 8 } - \frac { \sqrt { 2 \beta } } { 1 6 } + \frac { 1 } { 8 } - \frac { \sqrt { 4 - 2 \sqrt { 2 } } } { 8 } \right ) \leq 0 \quad \text {since } \beta \leq 0 . 6$$

- v3 ∈ σhigh since

$$\left ( \frac { \sqrt { 2 \beta } t } { 4 } \right ) ^ { 2 } - 0 & + \left ( \frac { \sqrt { 2 } } { 4 } \beta t \right ) ^ { 2 } - 2 \left ( \frac { \sqrt { 2 } } { 4 } \beta t \right ) \frac { \sqrt { 2 } } { 4 } t \\ & = \beta t ^ { 2 } \left ( \frac { 1 } { 8 } + \frac { \beta } { 8 } - \frac { 2 } { 8 } \right ) \leq 0 \quad \text {since } \beta \leq 1$$


<!-- p:88 -->


We call bottom part of the ellipse, the counterclockwise arc from p to the contact point, and top part the following arc from the contact point to the intersection with the y-axis.

We show that the bottom part of σ' is below the bottom part of σhigh. We apply a vertical affine transformation that flatten σhigh until its contact point becomes q'. The new ellipse clearly has its bottom part lower since the transformation lowered every point. Then we shift horizontally the center into c', maintaining the points p and q'. Since that makes the aspect ratio grow, here again we lowered the bottom part. So the bottom part of σ' is below the bottom part of σhigh.

y

Chigh

qhigh

C

v3

p

x

2

On the other hand we apply a homothetic transformation on σlow centered on its contact point such that the length of the horizontal axis is the same as the length as σ', followed by a vertical translation until the contact point coincides with q', finally completed by a vertical affine transformation that makes it reach the correct aspect ratio, that is greater. All those transformations make the upper part of the ellipse goes upward. We deduce that any ellipse tangent to the right side of the square and whose center has abscissa smaller than 1t contain tr2.

y

v3

Clow

qlow

#t

x

2

Then we can go to ellipses tangent to the top side of the square. The proof is quite identical so we do not develop it but keep in mind that the important point is that v3 belongs to circle centered at (0, √2 t) 4 because v3 lies on the parabola y = 2√2 2x2, that is above the circle for y &lt; √2 t. t 4

Above arguments proved that any ellipse whose center is in the upper right corner of the triangle contains either tr1 or tr2. By extension, we deduce that any ellipse contains at least one of the 8 triangles tri.


<!-- p:89 -->


So we get:

$$S o w e g t \colon \\ & \mathbb { P } \left [ \exists q \in X , \ ( p , q ) \in \mathcal { G } _ { \mathfrak { G } [ \vartheta , \mathfrak { n } ] } ^ { \emptyset } ( X \cup \{ p \} ) \ | \, | p q | > t \right ] \leq \mathbb { P } \left [ \mathbb { I } \ni [ 1 , \dots , 8 ] , \text {tr} _ { i } \cap X = \emptyset \right ] \\ & = 4 \left ( \mathbb { P } \left [ \text {tr} _ { i } \cap X = \emptyset \right ] + \mathbb { P } \left [ \text {tr} _ { 2 } \cap X = \emptyset \right ] \right ) \\ & = 4 \left ( e ^ { - \lambda \frac { \sqrt { 2 } \beta t ^ { 2 } } { \beta t ^ { 2 } } + e ^ { - \lambda \sqrt { 2 } \beta t ^ { 2 } } } \right ) \\ & = \theta \left ( e ^ { - \lambda \frac { \sqrt { 2 } \beta t ^ { 2 } } { \beta t ^ { 2 } } t } \right )$$

□


<!-- p:90 -->


78 Chapter 9. On the probability of the existence of far neighbors


<!-- p:91 -->


## Chapter 10

### Analysis of two additional empty region graphs

The empty region graphs we studied were all defined by axis-aligned ellipses, especially because they correspond to what we observe on surfaces. They will be useful in Parts III and IV. But more generally, we might also be interested in the cases where either the ellipses are not axis-aligned, either the regions are not ellipses. We present two such examples.

#### 10.1 Empty ellipse graph with bounded aspect ratio

We consider the graph in which two points p and q are neighbors if there exists an empty ellipse passing through p and q whose aspect ratio is between β and 1, for β ∈ [0, 1]. For two points p and q, we define Gtβ,], the corresponding empty region graph.

Figure 10.1: An ellipse Ell, and the triangles [pqsr] and [pqse]. At least of them is included inside Ell.

b

θ

Ell

sl

[β,1]

hm

p

The case where β = 1 corresponds to the Delaunay triangulation, and the case where β = 0 corresponds to the complete graph, as long as there are no three points aligned, since we can consider that a segment between two points is an ellipse with aspect ratio 0. Thus we assume that β ∈ (0, 1).

Consider two points in R2, p at the origin, and q, and an ellipse ell passing through p and q. Since ell is not anymore axis-aligned but has its great axis in some direction θ, we can consider the regions hm [β,1] r,θ and hme,1 [β,1] as in the previous sections but parameterized by direction θ. Clearly the circle Cβ centered at the midpoint of [p, ] and of diameter β|pq| is inside hmr,1] [β,1] ∪ hme,θ1 [β,1] (see Figure 10.1). Consider the isosceles triangles [pqsr] and [pqsę] such that se, sr ∈ Cβ with sr on the right of pÀ and se on its left. Then [β,1]


<!-- p:92 -->


Since this is true for any ellipse, we can assume that any ellipse whose aspect ratio is between β and 1 and passing through p and q contains either [pqsr] or [pqse]. Notice that these triangles are independent of the direction θ. So we can apply the Partition lemma to yield that G t[s,1] is a sub-graph of G0 {[pqsr],[pqse]}·

Now we consider a Poisson point process X of intensity λ, and we compute an upper bound on the expected degree of p in G∅ Ge[s,1] (X U {p}).

$$Now we consider a Poisson point process X of intensity \lambda , and we compute an upper bound on the
expected degree of p in \mathcal { G } _ { \ell , \lambda , l } ^ { \emptyset } ( X \cup \{ p \} ) . \\ \\ \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ p s , r \} , \left [ p s , \right \} } \right ) \right ] = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { 1 } _ { \{ p s , r \} \cap X = 0 } \vee \left [ p s , \mathcal { N } \times \emptyset \right ] \right ] \\ = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { 1 } _ { \{ p s , r \} \cap X = 0 } + \mathbb { 1 } _ { \{ p s , \ell \} \cap X = 0 } \right ] - \mathbb { 1 } _ { \{ p s , \cup \left [ p s , \right \} \cap X = 0 \} } \right ] \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( \mathbb { P } \left [ p s , r \right ] \cap X = \emptyset \right ) + \mathbb { P } \left [ p s , \ell \right ] \cap X = \emptyset \right ] \\ & - \mathbb { P } \left [ \left [ p s , r \right ] \cup \left [ p s , \ell \right ] \cap X = \emptyset \right ] \right ) d q \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( 2 e ^ { - \lambda | [ p s , r ] | } - e ^ { - 2 \lambda | [ p s , r ] | } \right ) d q \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( 2 e ^ { - \frac { \beta } { 3 } | [ p q | ^ { 2 } } - e ^ { - \frac { \beta } { 4 } | p q | ^ { 2 } } \right ) d q \\ = \int _ { \mathbb { R } ^ { 2 } } \int _ { \infty } ^ { \pi } \lambda \left ( 2 e ^ { - \beta ^ { - \beta } } - e ^ { - \beta ^ { - \beta } } \right ) r d r d \theta \\ = 2 \pi \frac { 1 } { \beta } ( 8 - 2 ) \\ = \frac { 1 2 \pi } { \beta } . \\ \intertext { On the other hand, among ellipses passing through p and q , we can choose the ellipse E l ^ { p } \, whose great
axis is the segment [ p , q ] and aspect ratio \beta to obtain a sub-graph of G _ { \ell , \lambda , l } ^ { 0 } . The expected degree of p in this graph is$$

On the other hand, among ellipses passing through p and q, we can choose the ellipse Ellβ whose great i5  -ns o  a ede   d xs t se stnot e[8,1] .

The expected degree of p in this graph is

$$\degree of p \text { in this graph is} \\ \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ E I I _ { * } ^ { \beta } \} } \right ) \right ] = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { I } _ { [ E I I _ { * } ^ { \beta } \cap X = 0 ] } \right ] \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda \left ( \mathbb { P } \left [ E I I _ { * } ^ { \beta } \cap X = \emptyset \right ] \text { d q} \\ = \int _ { \mathbb { R } ^ { 2 } } \lambda e ^ { - \lambda | E I I _ { * } ^ { \beta } | } d q \\ = \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } \lambda e ^ { - \lambda \frac { \pi } { 4 } \beta r ^ { 2 } } r d r d \theta \\ = 2 \pi \frac { 2 } { \pi \beta } \\ = \frac { 4 } { \beta }$$

We deduce the following theorem:

Theorem 10.1. Let X be a Poisson point process in R2. The expected degree of the origin p in G0 Gtls,] (X ∪ {p}) is θ


<!-- p:93 -->


#### 10.2 Empty 4/2-ball graph

Additionally, we propose a computation for the expected degree of a point in an empty region graph whose regions are not defined by second order equations. We call 4/2-ball in R2 any region of equation

$$( x - x _ { c } ) ^ { 4 } + ( y - y _ { c } ) ^ { 2 } < k , \text { for a positive } k \text { and } a \text { center } ( x _ { c } , y _ { c } ) .$$

The more k is small, the more the 4/2-ball flattens along the x-axis. This kind of region appears as intersection of sphere and surface, at Z points for a sphere close to the medial sphere.

We consider the graph in which two points p and q are neighbors if there exists an empty 4/2-ball passing through p and q. For two points p and q, we define the family B4/2(p, q) of all 4/2-balls passing

As usual we consider a point p at the origin and a point q. A 4/2-ball passing through the origin p has equation:

$$( x - x _ { c } ) ^ { 4 } + ( y - y _ { c } ) ^ { 2 } = x _ { c } ^ { 4 } + y _ { c } ^ { 2 } .$$

For such a curve to pass also through q, c must verify:

$$( x _ { q } - x _ { c } ) ^ { 4 } + ( y _ { q } - y _ { c } ) ^ { 2 } = x _ { c } ^ { 4 } + y _ { c } ^ { 2 } .$$

Figure 10.2: The family of regions B4/2(p, q). In yellow, the region b4/2 [p, q].

y

p

x

We define the curve of possible pairs (xc, yc) by isolating yc in the above equation:

$$\begin{array} { r l r } { 1 } & { ( y _ { q } - y _ { c } ) ^ { 2 } } & { = } & { ( x _ { c } ^ { 4 } + y _ { c } ^ { 2 } } & { = } & { ( x _ { q } - x _ { c } ) ^ { 4 } + ( y _ { q } - y _ { c } ) ^ { 2 } } \\ & { \Leftrightarrow } & { y _ { c } ^ { 2 } - ( y _ { q } - y _ { c } ) ^ { 2 } } & { = } & { ( x _ { q } - x _ { c } ) ^ { 4 } - x _ { c } ^ { 4 } } \\ & { \Leftrightarrow } & { 2 y _ { c } y _ { q } - y _ { q } ^ { 2 } } & { = } & { ( x _ { q } - x _ { c } ) ^ { 4 } - x _ { c } ^ { 4 } } \\ & { \Leftrightarrow } & { y _ { c } } & { = } & { \frac { ( x _ { q } - x _ { c } ) ^ { 4 } - x _ { c } ^ { 4 } + y _ { q } ^ { 2 } } { 2 y _ { q } } . } \end{array}$$


<!-- p:94 -->


In other words, a 4/2-ball centered on c has equation Ec(x, y) &lt; 0 where:

$$E _ { c } ( x , y ) & = ( x - x _ { c } ) ^ { 4 } + ( y - y _ { c } ) ^ { 2 } - x _ { c } ^ { 4 } - y _ { c } ^ { 2 } \\ & = ( x - x _ { c } ) ^ { 4 } - x _ { c } ^ { 4 } + y ^ { 2 } - 2 y y _ { c } \\ & = ( x - x _ { c } ) ^ { 4 } - x _ { c } ^ { 4 } + y ^ { 2 } - 2 y \frac { ( x _ { q } - x _ { c } ) ^ { 4 } - x _ { c } ^ { 4 } + y _ { q } ^ { 2 } } { 2 y _ { q } } . \\ \\ T U _ { c } ( x , y ) & \colon _ { 1 } n ( x _ { c } / 2 ) \quad _ { 2 } n ( x _ { q } / 2 ) \quad _ { 3 } n ( x _ { q } - x _ { c } ) ^ { 2 } - x _ { c } ^ { 2 } + y _ { q } ^ { 2 } \\$$

Lemma 10.2. The family B4/2(p, q) of 4/2-balls passing through p and q is a 1-dimensional good pencil of R2.

Proof. To be a 1-dimensional good pencil in R2, the family B4/2(p, q) must verify the two following conditions:

- for any b ∈ B4/2(p, q), there exists c ∈ R1 and Ec : R2 → R such that b = {r ∈ R2, Ec(r) &lt; 0}, and
- for any r ∈ R2, there exists at most one point cr for which c → Ec(r) changes of sign when c varies.

The first condition is true since the 4/2-balls are already defined by such an equation. The second is more difficult. In other words, it corresponds to: for any r different than p and q, there exists a single 4/2-ball whose boundary passes p, q and r. Since the expression of Ec(x, y) is a bi-variate expression of degree 4, a direct algebraic approach is not trivial.

This seems obvious graphically, but to get rid of any doubt, we chose to prove it analytically. This is done in Appendix A.3. □

We denote by b0 4/2 2(p, q) the 4/2-ball centered on the middle m of p and q, and compute its area. This region has equation:

$$b _ { 0 } ^ { 4 / 2 } ( p , q ) \colon ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } - ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } < 0 .$$

We express the upper part of its boundary i.e. for y &gt;

$$\text {ress the upper part of } & \text {its boundary } \imath . e . \text { for } y > \frac { \frac { } { 2 } y _ { q } , \text { as the graph of a function of } x \colon \\ & \quad ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } - ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } = 0 \text { and } y > \frac { 1 } { 2 } y _ { q } , \\ & \Leftrightarrow \ ( y - \frac { 1 } { 2 } y _ { q } ) ^ { 2 } = ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } \text { and } y > \frac { 1 } { 2 } y _ { q } , \\ & \Leftrightarrow \ y - \frac { 1 } { 2 } y _ { q } = \sqrt { ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } } , \\ & \Leftrightarrow \ y = \frac { 1 } { 2 } y _ { q } + \sqrt { ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } - ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } } .$$

From what we deduce the area:

$$From what we deduce the area: \\ \left | b _ { 0 } ^ { 4 / 2 } ( p , q ) \right | = \int _ { \mathbb { R } ^ { 2 } } \mathbb { I } _ { [ u \in b _ { 0 } ^ { 4 / 2 } ( p , q ) ] } d u \\ = 2 \int _ { \mathbb { R } ^ { 2 } } \mathbb { I } _ { [ u \in b _ { 0 } ^ { 0 } \ ( p , q ) \ \{ y _ { u } > y _ { m } \} ] } d u \\ = 2 \int _ { ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } < ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } } \sqrt { ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } } - ( x - \frac { 1 } { 2 } x _ { q } ) ^ { 4 } d x \\ = 2 \int _ { x ^ { 4 } < ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } } \sqrt { ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } } - x ^ { 4 } d x \\ = \frac { 2 \sqrt { 2 } } { 3 } E I _ { K } ( \frac { \sqrt { 2 } } { 2 } ) \left ( ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } + ( \frac { 1 } { 2 } y _ { q } ) ^ { 2 } \right ) ^ { \frac { 3 } { 4 } } \quad ( M a p l e ) , \\ \intertext { h e r $ E I _ { K } ( k ) $ is the complete elliptic integral of the first kind: }$$

where Ellk(k) is the complete elliptic integral of the first kind:

$$E l l _ { K } ( k ) = \int _ { 0 } ^ { 1 } \frac { 1 } { \sqrt { 1 - t ^ { 2 } } \sqrt { 1 - ( k t ) ^ { 2 } } } d t .$$


<!-- p:95 -->


On the other hand, we can observe that the extreme regions are still half-planes, since the leading coefficient with respect to xc in the expression of the region is -4(yqx − xqy). Thus we can consider the regions br/ 4/2 :=1 b0 4/2 ∩HPr and b4k/ 4/2 := b0 4/2 ∩ HPe, and claim by Combination lemma, that any 4/2-ball passing through p and q contains either b4/ 4/2 4/2

From what we deduce the expected degree of a point in G (X ∪ {p}): ,be

$$\mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ b , 4 ^ { 2 } , b _ { l } ^ { 4 / 2 } \} } ^ { 0 } \right ) \right ] & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } \mathbb { P } \left [ b _ { r } ^ { 4 / 2 } \cap X = \emptyset \right ] + \mathbb { P } \left [ b _ { \ell } ^ { 4 / 2 } \cap X = \emptyset \right ] - \mathbb { P } \left [ b _ { 0 } ^ { 4 / 2 } \cap X = \emptyset \right ] d q \\ & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } 2 e ^ { - \lambda | b | _ { 4 } ^ { 4 / 2 } } | _ { - \ e ^ { - \lambda | b _ { 0 } ^ { 4 / 2 } } | _ { d q } } \\ & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } 2 e ^ { - \frac { \lambda } { 2 } | \lambda | _ { 0 } ^ { 4 / 2 } } | _ { - \ e ^ { - \lambda | b _ { 0 } ^ { 4 / 2 } } | _ { d q } } .$$

First we compare the integrals of both terms:

$$\int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | b _ { 0 } ^ { 4 / 2 } | } d q & = \int _ { \mathbb { R } } e ^ { - \lambda \frac { 2 \sqrt { 2 } } { 3 } E _ { \text {Lin} } ( \frac { \sqrt { 2 } } { 2 } ) ( \frac { q _ { q } } { 2 } ) ^ { 4 } + ( \frac { y _ { q } } { \frac { q _ { q } } { 2 } } ) ^ { 2 } ) ^ { \frac { 3 } { 4 } } d x _ { q } d y _ { q } \\ & = 4 \int _ { \mathbb { R } ^ { + } } \int _ { e ^ { - \lambda \frac { 2 \sqrt { 2 } } { 3 } E _ { \text {Lin} } ( \frac { \sqrt { 2 } } { 2 } ) } ( ( \frac { q _ { q } ^ { ^ { \prime } } } { 2 } ) ^ { 2 } + ( \frac { y _ { q } } { 2 } ) ^ { 2 } ) ^ { \frac { 3 } { 4 } } \frac { 1 } { \sqrt { 2 x _ { q } ^ { \prime } } } d x _ { q } ^ { \prime } d y _ { q } \text { by posing } ( \frac { 1 } { 2 } x _ { q } ) ^ { 4 } = ( \frac { 1 } { 2 } x _ { q } ^ { \prime } ) ^ { 2 } ,$$

pue

$$\int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \frac { \xi } { 2 } \lambda | b _ { 0 } ^ { 4 / 2 } } | d q & = \int _ { \mathbb { R } } e ^ { - \frac { \sqrt { 2 } } { 3 } \text {E11} _ { K } ( \frac { \sqrt { 2 } } { 2 } ) ( ( \frac { q } { 2 } ) ^ { 4 } + ( \frac { y _ { q } } { 2 } ) ^ { 2 } ) ^ { \frac { 1 } { 4 } } } d x _ { q } d y _ { q } \\ & = 4 \int _ { \mathbb { R } ^ { + } } \int _ { \mathbb { R } ^ { + } } e ^ { - \frac { \lambda \sqrt { 2 } \text {E11} _ { K } ( \frac { \sqrt { 2 } } { 2 } ) } { 3 } \left ( ( \frac { q } { 2 } ) ^ { 2 } + ( \frac { y _ { q } } { 2 } ) ^ { 2 } \right ) ^ { \frac { 1 } { 4 } } \frac { 1 } { \sqrt { 2 r _ { q } ^ { \prime } } } d x _ { q } ^ { \prime } d y _ { q } \text { by posin } \left ( \frac { 1 } { 2 } x _ { q } \right ) ^ { 4 } = \left ( \frac { 1 } { 2 } x _ { q } ^ { \prime } \right ) ^ { 2 } ,$$

then we do a variables substition such that 2 + (#) 2 314 = q 2 yq 2 3|4 , i.e. 2% X = xq and 2 2 23 Y = yq:

$$\int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \frac { 1 } { 2 } \lambda | b _ { 0 } ^ { 4 / 2 } | } d q & = 4 \int _ { \mathbb { R } ^ { + } } \int _ { \mathbb { R } ^ { + } } e ^ { - \lambda ^ { 2 } \frac { \mathcal { Z } ^ { 3 } } { 3 } E l _ { K } ( \frac { \lambda ^ { 2 } } { 2 } ) ( ( \frac { 2 } { 2 } ) ^ { 2 } ) ^ { \frac { 3 } { 2 } } } \frac { \frac { 2 \S } { \sqrt { 2 ( 2 \mathcal { Z } ^ { 3 } ) } } } { \sqrt { 2 ( 2 \mathcal { Z } ^ { 3 } ) } } d X d Y \\ & = 4 \left ( 2 ^ { \frac { 4 } { 3 } - \frac { 1 } { 3 } } \right ) \int _ { \mathbb { R } ^ { + } } \int _ { \mathbb { R } ^ { + } } e ^ { - \lambda ^ { 2 } \frac { \mathcal { Z } ^ { 3 } } { 3 } E l _ { K } ( \frac { \lambda ^ { 2 } } { 2 } ) ( ( \frac { 2 } { 2 } ) ^ { 2 } + ( \frac { 2 } { 2 } ) ^ { 2 } ) ^ { 3 } } \frac { 1 } { \sqrt { 2 X } } d X d Y \\ & = 2 \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | b _ { 0 } ^ { 4 / 2 } | } d q .$$


<!-- p:96 -->


We deduce that:

$$We deduce that: \\ \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ b , ^ { 4 } , b ^ { 4 } \} } ^ { 0 } \right ) \right ] & = \lambda \int _ { \mathbb { R } ^ { 2 } } 2 ^ { - \frac { \lambda } { 1 } \lambda | b ^ { 4 } | ^ { 2 } } d q - \lambda \int _ { \mathbb { Q } ^ { 2 } } e ^ { - \lambda | b ^ { 4 } | ^ { 2 } } d q \\ & = \lambda \int _ { \mathbb { Q } ^ { 2 } } 2 ^ { - \frac { \lambda } { 1 } \lambda | b ^ { 4 } | ^ { 2 } } d q - \lambda \int _ { \mathbb { Q } ^ { 2 } } \frac { 1 } { 2 } \frac { - \lambda | b ^ { 4 } | ^ { 2 } } { 2 } d r _ { q } \\ & = \frac { 3 } { 2 } \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \frac { \lambda } { 1 } \lambda | b ^ { 4 } | ^ { 2 } } d q \\ & = 6 \lambda \int _ { \mathbb { R } ^ { + } } \int _ { \mathbb { R } ^ { + } } e ^ { - \lambda \frac { \sqrt { 2 } E _ { K } } { 3 } \left ( \frac { \sqrt { 2 } } { 2 } \right ) ( \frac { \gamma ^ { 2 } } { 2 } ) ^ { + } ( \frac { \gamma ^ { 2 } } { 2 } ) ^ { + } } \frac { 1 } { \sqrt { 2 x ^ { \prime } } } d x ^ { \prime } d y _ { q } \\ & = \frac { 6 } { \sqrt { 2 } } \lambda \int _ { [ 0 , \frac { \xi } { 1 } ] } \int _ { [ 0 , \infty ] } e ^ { - \lambda \frac { 1 } { 3 } E _ { K } \left ( \frac { \sqrt { 2 } } { 2 } \right ) \frac { \frac { 1 } { 2 } } { r } \frac { r _ { q } } { q } d r _ { q } d \theta _ { q } } \, by \, \text {posing} \, r _ { q } ^ { 2 } = x _ { q } ^ { \prime } + y _ { q } ^ { 2 } \\ & = \frac { 6 } { \sqrt { 2 } } \lambda \int _ { [ 0 , \frac { \xi } { 1 } ] } \frac { 1 } { \sqrt { \cos \theta _ { q } } } \int _ { [ 0 , \infty ] } e ^ { - \lambda \xi _ { K } E _ { K } \left ( \frac { \sqrt { 2 } } { 2 } \right ) \frac { \frac { 1 } { 2 } } { r } \frac { r _ { q } } { q } d r _ { q } d \theta _ { q } } \, by \, \text {posing} \, r _ { q } ^ { 2 } = x _ { q } ^ { \prime } + y _ { q } ^ { 2 } \\ & = \frac { 6 } { \sqrt { 2 } } \lambda \int _ { [ 0 , \frac { \xi } { 1 } ] } \frac { 1 } { \sqrt { \cos \theta _ { q } } } \frac { 1 } { \sqrt { \theta _ { q } } } E _ { K } ( \frac { \sqrt { 2 } } { 2 } ) \\ & = \frac { 2 4 } { \sqrt { 2 } E _ { K } ( \frac { 2 } { 2 } ) } \sqrt { 2 } E _ { K } ( \frac { 2 } { 2 } ) \pmod { ( \mathbf A } ( \mathbf A ) } \\ & = 2 4 . \\ \intertext { A direct lower bound is given by the sub-graph } & \mathcal { G } _ { \{ b , ^ { 2 } \} } ^ { 0 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } { 2 } \intertext { [ e q n ] } & = \frac { 1 } {$$

A direct lower bound is given by the sub-graph Gh

$$\mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ b _ { 0 } ^ { 4 / 2 } \} } \right ) \right ] & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | b _ { 0 } ^ { 4 / 2 } | } d q \\ & = \frac { 1 } { 2 } \lambda \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \frac { 1 } { 2 } \lambda | b _ { 0 } ^ { 4 / 2 } | } d q \\ & = \frac { 1 } { 3 } \, \mathbb { E } \left [ d e r \left ( p , \mathcal { G } _ { \{ b _ { r } ^ { 4 / 2 } , b _ { \ell } ^ { 4 / 2 } \} } \right ) \right ] \\ & = 8 .$$

We deduce the following theorem:

Theorem 10.3. Let X be a Poisson point process with intensity λ in R2. The expected degree E [deg (p, G4/2)] of the origin p in G04 GB4/2(X ∪ {p}) is between 8 and 24.

Proof.

$$8 = \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ b _ { 0 } ^ { 4 / 2 } \} } ^ { 0 } \right ) \right ] \leq \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \mathcal { B } ^ { 4 / 2 } } ^ { \theta } \right ) \right ] \leq \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \{ b _ { r } ^ { 4 / 2 } , b _ { \ell } ^ { 4 / 2 } \} } ^ { \theta } \right ) \right ] = 2 4 . \\$$

By analogy with the Delaunay triangulation where the bounds are half of these one, and where the lower bound given by the Gabriel graph is also one third of the upper bound given by the half-moon graph, we might conjecture that:

Conjecture 10.4. Let X be a Poisson point process with intensity λ in R2. The expected degree E [deg (p, G04/2)] of the origin p in GB4/2(X ∪ {p}) is 12.


<!-- p:97 -->


## Chapter 11

### On nearest-neighbor-like graphs, a way to compute some integrals

In this chapter, we present some features on what we call nearest-neighbor-like graphs. As the usual nearest-neighbor graph, they are empty region graph, where, for any pair (p, q) the family R(p, q) of regions is a singleton region. For the nearest-neighbor graph, this region is the disk centered on p and with radius |pq|. For nearest-neighbor-like graphs, the region is not a disk, but the graph still has similar properties.

#### 11.1 The nearest-neighbor graph

As mentioned in Section 7.1, the nearest-neighbor graph is an empty region graphs, where for a pair (p, q) the family of regions is reduced to the singleton containing the disk Dp(q) centered on p and with q on its boundary, except for p (otherwise any such region would at least contain p). Since the region for the pair (p, q) is not the same than for the pair (q, p), we consider the directed graph in which there i the edge (p, q) if and only if the punctured disk Dp(q) \ {p} is empty. We denote this graph by NNĠ. A property of such a graph is that, if X is a data sample in general position, then for any p ∈ X, we have the outer degree deg (p, NN) of p is 1. Consequently, we also have that if X is a Poisson point process, then E [deg (p, NNG)] = 1, since a Poisson point process is in general position almost surely.

On the other hand, it might be interesting to proceed anyway in the computation of the expected degree in the same way as we did in the previous chapter. As we said q is a neighbor of p in NNĠ if Dp(q) is empty, so we express the expected degree in the following way:

$$\mathbb { E } \left [ \overrightarrow { \deg \left ( p , \overrightarrow { N N G } \right ) } \right ] & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } \mathbb { P } \left [ \mathcal { D } _ { p } ( q ) \cap X = \emptyset \right ] \mathbf d q \\ & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | \mathcal { D } _ { p } ( q ) | } \mathbf d q \\ & = \lambda \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \lambda \pi | p q | ^ { 2 } } \mathbf d q \\ & = \lambda \int _ { x \in \mathbb { R } ^ { 2 } } \int _ { y \in \mathbb { R } ^ { 2 } } e ^ { - \lambda \pi ( x ^ { 2 } + y ^ { 2 } ) } \mathbf d y d x . \\ \intertext { w e a i d o v e , w e c a n d e d u c e w i n t u o w h o u t a n y c o p u t a t i o n , t h a t }$$

From what we said above, we can deduce without any computation, that

$$\int _ { x \in \mathbb { R } ^ { 2 } } \int _ { y \in \mathbb { R } ^ { 2 } } e ^ { - \lambda \pi ( x ^ { 2 } + y ^ { 2 } ) } d y d x = \frac { 1 } { \lambda } .$$


<!-- p:98 -->


Of course, we know how to compute the integral, but suppose that in the exponential, there were the expression of the area of a more complex region, it might be interesting to see the integral as the expression of an expected degree in some empty region graph. We describe a class of graphs, called nearest-neighbor-like graphs, that are good candidate to help in such computations, and can also be used as graphs in which we know that their expected degree is constant. For instance we use one in Section 13.5.4.

#### 11.2Formalization

Basically, one can search the nearest neighbor of a point p by consider concentric disks growing around p until they touch another point, this point is the nearest neighbor of p. Suppose that the regions are no longer disks but still "increasing" regions as it goes along. Then the expected degree of a point in an empty region graph defined by such regions cannot be greater than 1. We define the notion of monotonic pencil of regions and nearest-neighbor-like graphs:

Definition 11.1. Let S be a subset of Rd for d ∈ N*, we call monotonic pencil of regions on S, an ordered (by inclusion) set M of closed regions such that:

- the Lebesgues measure of ∂m is 0,
- for m1 and m2 in M, m1 ≠ m2 ⇒ ∂m1 ∩ ∂m2 = ∅, and
- ∪m∈ ∂m = S.

For instance, the family of disks centered on the origin is a monotonic pencil on R2.

Proposition 11.2. The smallest region of monotonic pencil of regions on S has Lebesgues measure 0. Its greatest region is S.

The definition suggests an empty region graph notion similar to the nearest-neighbor graph:

Definition 11.3. Let S be a function which associates to any p ∈ Rd a domain S(p) ∈ Rd. A S-nearest{m} where for any p ∈ Rd, M(p) := {m(p, q), q ∈ S(p)} is a monotonic pencil of regions on S(p).

We may pay attention that the pencil used here has not the same role than in previous empty region os    s    ( )     t    dty regions that formed a pencil. Here, for each pair (p, q) there is only one possible region. For a point p, e  pa   ,  v.

In such graphs, the expected degree is obviously bounded by 1 as stated by the following lemma:

{m}, and a Poisson point process X. If G is a {m}

{m}(X) is 1 almost surely.

Proof. We count the number of neighbors of p by developing the monotonic pencil M(p) = {m(p, q), q ∈ S(p)} from the empty set Ø∅ to S(p). Two cases arise: either S(p) ∩ X = ∅, in which case the degree of p is 0, either S(p) ∩ X ≥ 1, and there exists a first region r0 with a point of X on its boundary. With probability 1, no other points lie on the boundary of that region and the point, that we denote qo is unique. By definition, qo is a neighbor of p, and there does not exist other neighbor since all other region of the pencils contain at least qo. In that case, the degree of p is then 1. □

Additionally, we consider this utility lemma:

Lemma 11.5. Let 2 puν be two directed empty region graphs where for any pair (p, q), R(p, q) = R R′ {r(p, q)} and R′(p, q) = {r'(p, q)}, i.e. they are singleton region. Consider a Poisson process X. If Proof. We consider that X is distributed with intensity λ on S. We go from the expression of E [deg to the expression of E by rewriting them:


<!-- p:99 -->


$$\mathbb { E } \left [ \stackrel { \longrightarrow } { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { R } } \right ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { 1 } _ { [ r ( p , q ) \cap X = 0 ] } \right ] \\ & = \int _ { q \in S } \mathbb { P } \left [ r ( p , q ) \cap X = \emptyset \right ] \lambda d q \\ & = \int _ { q \in S } \mathbb { P } \left [ r ^ { \prime } ( p , q ) \cap X = \emptyset \right ] \lambda d q , \text { since } | r ^ { \prime } ( p , q ) | = | r ( p , q ) | , \\ & = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { 1 } _ { [ r ^ { \prime } ( p , q ) \cap X = 0 ] } \right ] \\ & = \mathbb { E } \left [ \stackrel { \longrightarrow } { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { R } ^ { \prime } } \right ) \right ] .$$

#### 11.3 Application of nearest-neighbor-like graphs

####### Example 1:

As a first application, we show that we could have computed the expected degree of a point in the Gabriel graph without any computation:

Alternative proof of Lemma 6.3. Consider the directed Yao graph Y-Gπ divided into 4 sectors [Yao82, KB96]. Except on the boundary, the degree of any point p in Y-Gp (X U {p}) is 4 since Y-Gp is actually the reunion of 4 nearest-neighbor-like graphs where the monotonic pencil of regions on each sector is the set of disjoint quarter of disks centered on p. Consider a point q ∈ R2, and a quarter of disk with q on its boundary. Its area is π(x2 + y2). On the other hand the area of gab(p, q) is π ((−xq)2 + ( ̄yq)2) 1π(x2 + y2). Consequently, by Lemma 11.5, Gab and Y-Gπ have the same expected degre, namely 4.

####### Example 2:

As a second application, we consider the S-nearest-neighbor-like graph, with S(p) = R2 \ {p} for any p, such that the monotonic pencil is a pencil of lemniscates. More precisely, if p is the origin, we denote by M(p) the pencil {ma : x4 − a2x2 + y2 &lt; 0, for a ∈ [0, +∞)} (see Figure 11.1). It is clearly a monotonic pencil of lemniscates. Basically, if 0 ≤ a ≤ b, then x4 − a2x2 + y2 ≥ x4 − b2y2 + y2 and ma ⊂ mb. Consequently, if we consider a Poisson process on R2, then the degree of p in the graph would be 1 almost surely by Lemma 11.4.

On the other hand, we can see this S-nearest-neighbor-like graph as the empty region graph G0 G{m} where ( )p = (d)      t     {( } ( d) a  g) of M(p) passing through q. Since maq (p) passes through q, we must have, x4 2 2 + y2 = 0, i.e. 十 yq 2 . We compute the area of m(p, q) by isolating the y coordinate in its equation. We will xq compute the size of only the upper right quarter of the lemniscate and so, assume that x ≥ 0 and y ≥ 0.

$$\begin{array} { r l r } { x ^ { 4 } - a _ { q } ^ { 2 } x ^ { 2 } + y ^ { 2 } } & { = } & { 0 , } \\ { \Leftrightarrow } & { y ^ { 2 } } & { = } & { a _ { q } ^ { 2 } x ^ { 2 } - x ^ { 4 } , } \\ { \Leftrightarrow } & { y } & { = } & { \sqrt { a _ { q } ^ { 2 } x ^ { 2 } - x ^ { 4 } } , } \\ { \Leftrightarrow } & { y } & { = } & { x \sqrt { a _ { q } ^ { 2 } - x ^ { 2 } } . } \end{array}$$

□


<!-- p:100 -->


Figure 11.1: A monotonic pencil of lemniscates issue from p. In yellow, the lemniscate m(p, q) passing through q.

m(p, q)

y

M(p)

Thus the area of m(p, q) is given by:

$$\text {given by} & \colon \\ & | m ( p , q ) | = 4 \int _ { [ 0 , a _ { q } ] } x \sqrt { a _ { q } ^ { 2 } - x ^ { 2 } } d x \\ & = 4 \left [ - \frac { 1 } { 3 } ( a _ { q } ^ { 2 } - x ^ { 2 } ) ^ { \frac { 3 } { 2 } } \right ] _ { 0 } ^ { a _ { q } } \\ & = \frac { 4 } { 3 } a _ { q } ^ { 3 } \\ & = \frac { 4 } { 3 } \left ( x _ { q } ^ { 2 } + \left ( \frac { y _ { q } } { x _ { q } } \right ) ^ { 2 } \right ) ^ { 3 } . \\ \top & \left [ \overrightarrow { d _ { q } } \left ( \overrightarrow { c } \wp \right ) \right ] _ { q } f _ { q } - \overrightarrow { c } \wp \left ( X \circ \left ( \overrightarrow { c } \wp \right ) \right ) \colon$$

And the expected degree E [deg (p, {m})] of p in (m}(X ∩{p}) is:

$$\left [ \begin{array} { c } \left [ \begin{array} { c } - \left ( \vec { \sigma } ^ { 0 } \right ) \left \{ \mathbf m \right \} \right ] \\ \left \{ \mathbf m \right \} \right \} \end{array} \right ] \\ \mathbb { E } \left [ \begin{array} { c } \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \{ \mathbf m \} } ^ { \emptyset } \right ) \right ] = \int _ { q \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | m | } \lambda d q \\ \end{array} \right ] \\ = \lambda \int _ { \mathbb { R } ^ { 2 } } e ^ { - \frac { 4 } { 3 } \lambda \left ( x _ { q } ^ { 2 } + \left ( \frac { y _ { q } } { x _ { q } } \right ) ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } d x _ { q } d y _ { q } . \\ \\ \longrightarrow ( \, \rightarrow _ { 0 } , \, \rightarrow _ { 1 } )$$

But we already know that E [deg (p,  m})] = 1, so that we can conclude:

$$\int _ { \mathbb { R } ^ { 2 } } e ^ { - \frac { 4 } { 3 } \lambda \left ( x ^ { 2 } + \left ( \frac { y } { x } \right ) ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } d x d y = \frac { 1 } { \lambda } .$$

Of course, this example is custom-made, furthermore, the integral is actually directly computable. But we might consider that in some cases, more complex, it can be useful.


<!-- p:101 -->


Part III

3D-Delaunay triangulation for two specific surfaces: the right cylinder and the oblate spheroid


<!-- p:102 -->


####### Preamble of Part III

We briefly recall what a 3-dimensional Delaunay triangulation is. Consider a set X of points in R3 in a generic position. The 3-dimensional Delaunay triangulation of X is the 3D-triangulation in which no point of X is inside a sphere circumscribing a tetrahedron of the 3D-triangulation. We will often use the word "triangulation" alone (without "3D") even if it is actually made of tetrahedrons. To simplify our study, we only take into account the property that an edge (p, q) is in the triangulation if there exists an empty sphere passing through p and q.

This property suggests an empty region graph approach of the Delaunay triangulation where the regions are spheres. In the case where the data points are distributed on surface embedded in R3, the study of Delaunay spheres has interest only on a negligible part of the sphere, namely, its intersection with the surface. Then we can propose a slightly different definition that fits with surfaces.

For each pair (p, q) of the data sample X, we consider the set R(p, q) of intersections of the surface with spheres passing through p and q. Then we say that an edge (p, q) is a Delaunay edge, if there exists a region in R(p, q) that does not contain other points of X.

That definition enlightens the behavior of the Delaunay triangulation of points on surface. Indeed, firstly, it brings back the problem to a 2-dimensional empty region graph that enables a comparison with the classic 2-dimensional Delaunay triangulation and the empty region graphs studied in the previous part. Secondly, the comparison makes more understandable the complexity of the triangulation. As we wng    o n s - o    s ns s ns on the surface on which the graph is studied, the behavior will resemble more like an empty axis-aligned ellipses graph with bounded aspect ratio or not.

We divide this part into three chapters. Chapter 12 is dedicated to the cylinder case, that had already been studied in the literature. Here, it is here mostly used as a pedagogical example and to show the efficiency of our method. Chapter 13 is dedicated to a specific surface, that is general enough to represent efficiently the case of generic surfaces. This surface is a flattened ellipsoid of revolution, also called oblate spheroid. This chapter gives a first example of surface on which a 3D-Delaunay triangulation of random points is linear in expectation. It permits also to introduce the method and some lemmas that will be reused in the last part of the thesis. Finally, in Chapter 14, we illustrate our results on two ellipsoid of revolution. One that is flattened, as in Chapter 13, and one that is elongated, for which Delaunay triangulation is suppose to have a behavior similar than on a cylinder.


<!-- p:103 -->


## Chapter 12

##### Expected size of the Delaunay triangulation of a Poisson point process on a right circular cylinder

In this chapter, we compute an upper bound on the expected number of edges of the Delaunay triangulation of a Poisson point process distributed on a right cylinder and show that the size of the Delaunay triangulation is O(λ ln λ) where λ is the intensity of Poisson process. This problem has already been solved for random uniform sample in [DEG08]. In this chapter, we propose a proof that uses the method described in Chapter II. The case of the cylinder being a relatively simple case, this chapter can serve as a groundwork for the next chapters.

Figure 12.1: A right circular circular cylinder embedded in R3. The axis of the cylinder is the v-axis, its radius is r and length l.

C

m

v

#### 12.1 The right circular cylinder

We analyze the expected size of the Delaunay triangulation of random points distributed on a right circular cylinder C embedded in R3. What we call a right circular cylinder is a truncated cylinder of revolution whose boundaries are circles perpendicular to the axis of the cylinder. We consider that the cylinder has length l and radius r. We use a global system of Cartesian coordinates (u, v, w) to describe the cylinder: without loss of generality, we can assume that C = {u2 + (w − r)2 = r2, |v| &lt; ν} (see Figure 12.1), in which the cylinder is tangent the uv-plane at the origin.

At any point p on the cylinder, we consider the inner orientation. We are interested in three geometric values: the two principal curvatures κ1(p) and κ2(p), and the inner medial radius r*(p). For the specific case of the cylinder, those three values are actually constants and so independent of p, so can denote them without the "(p)". Additionally, it is clear that r* = r.


<!-- p:104 -->


Since κ1 corresponds to the curvature of the first inner sphere osculating at p, and since such a sphere has obviously r for radius, we have κ1 = 1 and the inner medial sphere σ*(p) and the osculating sphere coincide. Since the cylinder is a surface of revolution, they do not coincide only for a single point p, but for the set Syminn(p), called symmetrical set of p, and defined as follows: Syminn(p) := C ∩ σ*(p). This set contains an infinity of points that forms a circle on the cylinder.

On the other hand, the outer medial sphere is the tangent plane Tc(p) at p, that can be seen as a sphere with infinite radius. The curvature κ2 is given by the curvature of a generator line, that is 0. In other words, κ2 = 0 and the outer medial sphere and the osculating sphere coincide again. By analogy, we consider the line Symout (p) = C ∩ Tc(p).

The property κ1 = r* is characteristic of the points on Z, it is actually its definition. This property happens to be true on the whole surface in the cylinder case, that is why we say that the cylinder is not a generic surface. This is the reason why the Delaunay triangulation of homogeneous random points on the cylinder has quasi-linear expected size.

When homogeneous points are distributed in R2, the probability that two points are Delaunay neighbors decreases highly with their distance, see Section 9.1. Because of the property described above, this probability does not decrease that fast on the cylinder. As a brief illustration, consider a random sample X and the two points p and q of X that minimizes |vp − vq| among points of X (we name |vp − vq| the v-distance). Then, consider the sphere centered on the medial axis of the cylinder and, passing through p and q. Its intersection with the cylinder, is the parallel strip around the cylinder between p and q. That strip is obviously empty since q has minimal v-distance with p. Thus those two points are almost surely Delaunay neighbors. By extension one may admit that the point with second smallest v-distance with p has still great chances to be neighbor of p, and so on. And that is also the case for the external part of cylinder, considering points that have a small u-distance.

Thus we prove the following theorem:

Theorem 12.1. The 3-dimensional Delaunay triangulation of a homogeneous Poisson point process distributed, with intensity λ, on a right circular cylinder, has expected size Θ(λln λ).

The proof consists, for each point p on the cylinder, in computing an upper and a lower bound on the expected degree of p in the Delaunay triangulation. We obtain the upper bound by considering a super-graph of the Delaunay triangulation, that is an empty region graph defined for each pair (p, q) by a family Fc(p, q) of fundamental regions on the cylinder that have the property that there always exists a sphere passing through p and q that contains a region of FC(p, q). We obtain the lower bound by considering a sub-graph of the Delaunay triangulation, that is also an empty region graph in which, for each pair (p, q), we select one sphere, denoted σo(p, q), among all the spheres passing through p and q, and say that (p, q) is an edge if σo(p, q) is empty. Then we obtain the upper and lower bounds on the expected size of triangulation by integrating, on the cylinder, the bounds on the expected degree.

Because of its geometry, we can study the cylinder in its entirety, while for generic surface, we will have to deal with approximation of the surface, projected in the tangent plane of the point whom we compute the expected degree. The approach we take will be slightly different for the cylinder than for a generic surface in the next chapters.

#### 12.2Description of the fundamental regions on the cylinder

-   o so o o e t  d-s  Dn  urs o an empty region graph defined by four regions for each pair of points.

Let p be a point on C and consider the Monge coordinate system (x, y, z) of p for the inner orientation. Then we consider a second point q ∈ C. We start by defining a notion of interval on the cylinder, for pairs of points that are on a common symmetrical set. For a point q that lies on Syminn(p), we denote by [p, q]c, the smallest section of Syminn(p) that has p and q for endpoints. By analogy, and to maintain a coherence in the notations, if q ∈ Symout (p), we denote [p, q]c the segment [p, q].


<!-- p:105 -->


Figure 12.2: Left: The cylinder and its intersections with specific spheres. Right: Their images under the unroll map i. In red, the intersection with the sphere σsym(p, q), in yellow and blue the intersections with the planes parallel to PMed(p, q), and in green with the plane PDiag(p, q). Those curves delimit the regions of Fc (p).

q

ā

 ̄ā2

q2

b

△2

∆2

∆1

b

q1

p


q1

p

q2

y


x


To explain the constructions of fundamental regions, we define two points, q1 and q2 that depends on p and q:

- q1 = Syminn(p) ∩ Symout (q), and
- q2 = Symout (p) ∩ Syminn(q).

The four curves [p, q1]c, [p, q2]c, [q, q1]c, and [q, q2]c define a region on C whose vertices are p, q, q1 and q2, that we call a cylindrical rectangle and denote R(p, q). Note that, if the cylinder is unrolled, the cylindrical rectangles become exactly 2-dimensional rectangles.

Finally we consider the plane PDiag(p, q) passing through p, q, p, and q. Its intersection with C is t     p    d o dd   gp delimited by [p, q1]c, [q, q1]c, and dg(p, q), and the cylindrical triangle ∆2(p, q) delimited by [p, q2]c, [q, q2]c, and dg(p, q). Note that, once unrolled, the cylindrical triangles are not 2-dimensional triangles. By symmetry dg(p, q) divides R(p, q) into ∆1(p, q) and ∆2(p, q) that are the respective reflection of ∆1(p, q) and ∆2(p, q) with respect to PMed(p, q).

Then we consider the plane PMed(p, q) parallel to the plane passing through p, q, q1, and q2, and containing the medial axis of the cylinder. For any point u ∈ C, the reflection of u with respect to PMed lies on C, we note it u. Consequently we denote by R(p, q) the reflection of R(p, q) with respect to PMed.

The four cylindrical triangles define the family of regions:

$$\mathcal { F } ^ { \mathcal { C } } ( p , q ) = \{ \Delta _ { 1 } ( p , q ) , \Delta _ { 2 } ( p , q ) , \overline { \Delta } _ { 1 } ( p , q ) , \overline { \Delta } _ { 2 } ( p , q ) \} ,$$

and the graph Gθc (X) in which two points p and q of X are neighbors if at least one of the regions of Fc(p, q) does not contain any point of X. Since FC(p, q) = FC(q, p), this empty region graph is undirected.

#### 12.3 Proof of the graph inclusion

We now prove that G GFc is actually a super-graph of the Delaunay triangulation when points are distributed on a cylinder.

Lemma 12.2. Consider a right circular cylinder C embedded in R3 and a data sample X distributed on C. Gσc (X) is a super graph of Del(X).

Proof. Let p and q be two points on C. We have to show that if a sphere passes through p and q, it contains at least one the four regions of FC (p, q).


<!-- p:106 -->


Without loss of generality, we consider the oriented orthogonal direct frame where p is the origin, the xy plane is the tangent plane of C at p the x axis is orthogonal to the axis of the cylinder and where the y axis is chosen such that the normal axis z points toward the interior of C.

In order to apply the Combination lemma, we have to prove that the set of spheres passing through p and q is a good pencil of regions. But this is clear since the centers of such spheres lie in a plane, the bisector plane PBis(p, q) of (p, q).

Among all the spheres passing through p and q, including those that are degenerate, we select five of them that we parameterize by their center. Actually four of the fives selected spheres are half-spaces.

The first center is csym(p, q), at the intersection of the medial axis of the cylinder and the bisector plane of [p, q]. It also corresponds to the center of the sphere passing through p, q, q1, q2 and their symmetrical points with respect to PMed(p, q). We denote by σsym(p, q) this sphere. It has for intersection with C a circular strip between Syminn(p) and Syminn(q).

Finally, we consider the half-spaces H1(p, q) and H2(p, q) that are spheres such that the centers c) (p, q) and c% (p, q) are at infinity in the direction orthogonal to PDiag(p, q) and such that H1(p, q) contains q1 and H2(p, q) contains q2.

Then we consider the centers cR (p, q) and cx (p, q) at infinity in the direction orthogonal to the plane passing through p, q, q1 and q2. Those centers define respectively the half-spaces HR and HR(p, q) whose intersection with C are cylindrical rectangles delimited by Symout(p) and Symout(q). We distinguish HR and HR(p, q) by assuming that HR(p, q) is the half-space containing p.

For a sphere σ, we denote by B(σ) the ball for which σ, is the boundary. To lighten the notations, we assume that all centers, spheres and regions refer to the pair (p, q), and then we hide "(p, q)" in their expressions.

We can observe that:

and then:

$$R = \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } ) \cap \mathcal { H } _ { R } ,$$

$$\overline { R } \subset \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } ) \cap \mathcal { H } _ { \overline { R } } ,$$

$$\Delta _ { 1 } & = \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } ) \cap \mathcal { H } _ { R } \cap \mathcal { H } _ { 1 } , \\ \Delta _ { 2 } & = \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } ) \cap \mathcal { H } _ { R } \cap \mathcal { H } _ { 2 } , \\ \overline { \Delta } _ { 1 } & \subset \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } ) \cap \mathcal { H } _ { \overline { R } } \cap \mathcal { H } _ { 1 } , \\ \overline { \Delta } _ { 2 } & = \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } )$$

$$\overline { \Delta } _ { 2 } \subset \mathcal { C } \cap \mathcal { B } ( \sigma _ { S y m } ) \cap \mathcal { H } _ { \overline { R } } \cap \mathcal { H } _ { 2 } .$$

Finally the four rays from csym, following the four infinite directions, partition the bisector plane of [p, q] into the four tiles (see Figure 12.3):

$$\mathcal { T } _ { \Delta _ { 1 } } & = ( c _ { 1 } ^ { \infty } , c _ { S y m } , c _ { R } ^ { \infty } ) , \\ \mathcal { T } _ { \Delta _ { 2 } } & = ( c _ { 2 } ^ { \infty } , c _ { S y m } , c _ { R } ^ { \infty } ) , \\ \mathcal { T } _ { \overline { \Delta } _ { 1 } } & = ( c _ { 1 } ^ { \infty } , c _ { S y m } , c _ { \overline { R } } ^ { \infty } ) , \\ \mathcal { T } _ { \overline { \Delta } _ { 2 } } & = ( c _ { 2 } ^ { \infty } , c _ { S y m } , c _ { \overline { R } } ^ { \infty } ) , \\ \text {gular sector delimited by the rank} \\ \text {gular sector delimited by the rank}$$

where (a, b, c) denotes the convex angular sector delimited by the rays [b, a) and [bc).

And since the bisector plane is partitioned by the set of tiles {T∆1, T∆2, T1, T2}, we can apply the Partition lemma to claim that G0c (X) is a super graph of Del(X). □

So that we can apply the Combination lemma to claim that: For any region r ∈ FC (p, q), if c belongs to Tr then the ball centered in c contains r.

#### 12.4 Computation of an upper bound on E [ Del(X)]

Now we know that GFe (X) is a super graph of Del(X), we can compute the expected degree of a point p in Gσc (X ∪ {p}) to get an upper bound on the expected degree of p in Del(X ∪ {p}).


<!-- p:107 -->


Figure 12.3: Partition of the bisector plane PBis(p, q) of p and q into four tiles. In black the vertices, their corresponding intersection with the cylinder is framed next to them. In red the fundamental regions corresponding to each tile.

C∩HR

R

∆2

∆1

C ∩H1

C ∩ B(σSym)

C ∩ H2

cSym

△1

D2

cR

C∩HR

Lemma 12.3. Let C be a right circular cylinder with length l and radius r. Let p be a point of C, and X a Poisson point process distributed on C with intensity λ. The expected degree of p in Ġ#c (X) is smaller than 50 ln(λlr) + O(1). 3

Proof. We consider the isometry i from C to the rectangle [− −2, 2] × [−πr, πr] that consists of unrolling the cylinder into its tangent plane at p. Let q be a point on C. To simplify the notations, we omit again to write (p, q) in most expressions. We compute the area of the regions of Fc. For any point u ∈ C, we denote by (xu, yu) the image of u by i. By construction and isometry, it is clear that |R| = |x′qy′|. We can observe, by symmetry that

$$| \Delta _ { 1 } | = | \Delta _ { 2 } | = | \overline { \Delta } _ { 1 } | = | \overline { \Delta } _ { 2 } | = \frac { | x _ { q } ^ { \prime } y _ { q } ^ { \prime } | } { 2 } .$$

Then we can compute the expected degree of p in Gσc (X):

$$\mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { J } ^ { 0 } \right ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X } \mathbb { 1 } _ { \mathfrak { R } } \varepsilon \mathcal { F } _ { \mathfrak { c } } , \mathfrak { r } \cap X = \emptyset \right ] \\ & = \int _ { q \in C } \lambda \, \mathbb { P } \left [ \exists \mathfrak { r } \in \mathcal { F } ^ { \mathcal { C } } , \, \mathfrak { r } \cap X = \emptyset \right ] d q \text { by Slivnysak-Mecke theorem.}$$

We use the formula below to expand the expression of the probability. Assume that E1, E2, E3 and E4 are independent events with equal probability:

$$\mathbb { P } \left [ E _ { 1 } \vee E _ { 2 } \vee E _ { 3 } \vee E _ { 4 } \right ] & = 1 - \prod _ { i = 1 } ^ { 4 } ( 1 - \mathbb { P } \left [ E _ { i } \right ] ) \quad \text { by independent of the } E _ { i } , \\ & = 1 - ( 1 - \mathbb { P } \left [ E _ { 1 } \right ] ) ^ { 4 } \\ & = 4 \mathbb { P } \left [ E _ { 1 } \right ] - 6 \mathbb { P } \left [ E _ { 1 } \right ] ^ { 2 } + 4 \mathbb { P } \left [ E _ { 1 } \right ] ^ { 3 } - \mathbb { P } \left [ E _ { 1 } \right ] ^ { 4 } .$$

Since all r in Fc have same area, the probabilities P [r ∩ X = Ø] are equal, and since the regions r are disjoint, the events "r ∩ X = 0" are independent. We can therefore apply the formula,


<!-- p:108 -->


$$\mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { f } ^ { \flat } \right ) \right ] & = \int _ { q \in \mathcal { C } } \lambda \left ( 4 \mathbb { P } \left [ \Delta _ { 1 } \cap X = \emptyset \right ] - 6 \mathbb { P } \left [ \Delta _ { 1 } \cap X = \emptyset \right ] ^ { 2 } \\ & + 4 \mathbb { P } \left [ \Delta _ { 1 } \cap X = \emptyset \right ] ^ { 3 } - \mathbb { P } \left [ \Delta _ { 1 } \cap X = \emptyset \right ] ^ { 4 } \right ) d q \\ & = \lambda \int _ { q \in \mathcal { C } } 4 e ^ { - \lambda | \Delta _ { 1 } | } - 6 e ^ { - 2 \lambda | \Delta _ { 1 } | } + 4 e ^ { - 3 \lambda | \Delta _ { 1 } | } - e ^ { - 4 \lambda | \Delta _ { 1 } | } \, d q \\ & = \lambda \int _ { - \frac { 1 } { 2 } } ^ { \frac { 1 } { 2 } } \int _ { - \pi r } ^ { \pi r } 4 e ^ { - \lambda | \frac { x | y } { 2 } } - 6 e ^ { - \lambda | x | } + 4 e ^ { - 3 \lambda | \frac { x | y } { 2 } } - e ^ { - 2 \lambda | x | } \, d y d x \\ & = 4 \lambda \int _ { 0 } ^ { \frac { 1 } { 2 } } \int _ { 0 } ^ { \pi r } 4 e ^ { - \lambda \frac { x y } { 2 } } - 6 e ^ { - \lambda x y } + 4 e ^ { - 3 \lambda \frac { x y } { 2 } } - e ^ { - 2 \lambda y } \, d y d x \\ & = 4 \lambda \left ( 4 I _ { \frac { 1 } { 2 } , \pi r } ( \frac { \lambda } { 2 } ) - 6 I _ { \frac { 1 } { 2 } , \pi r } ( \lambda ) + 4 I _ { \frac { 1 } { 2 } , \pi r } ( \frac { \lambda } { 2 } ) - I _ { \frac { 1 } { 2 } , \pi r } ( 2 \lambda ) \right ) \\ \intertext { w h e r e } \intertext { i n } I _ { L , l } ( t ) = \int _ { 0 } ^ { L } \int _ { 0 } ^ { l } e ^ { - t x y } d y d x \, ( s e e \, \text {proof of lemma } 8 . 4 ) ,$$

where IL,t(t) = ∫ cl e−txydydx (see proof of Lemma 8.4),

$$& \leq 4 \lambda \left ( \frac { 8 } { \lambda } ( 1 + \ln ( \frac { \pi \lambda l r } { 4 } ) ) - \frac { 6 } { \lambda } \ln ( \frac { \pi \lambda l r } { 2 } ) + \frac { 8 } { 3 \lambda } ( 1 + \ln ( \frac { 3 \pi \lambda l r } { 4 } ) ) - \frac { 1 } { 2 \lambda } \ln ( \pi \lambda l r ) \right ) \\ & = \frac { 5 0 } { 3 } \ln ( \lambda l r ) + O ( 1 ) .$$

□

Now we have an upper bound on the expected degree of a point in G%o GFe. We can integrate this bound

Lemma 12.4. Let C be a right circular cylinder with length l and radius r aņd let X be a Poisson point

Proof. Let N be the number of edges in GFc (X).

$$1$$

$$P r o f . \, \text { Let } N \, \text { be the number of edges in } \mathcal { G } _ { \mathcal { F } _ { c } } ^ { \circ } ( X ) . \\ N & = \frac { 1 } { 2 } \sum _ { p \in X } \deg \left ( p , \mathcal { G } _ { \mathcal { F } _ { c } } ^ { \circ } \right ) \\ \mathbb { E } [ N ] & = \mathbb { E } \left [ \frac { 1 } { 2 } \sum _ { p \in X } \deg \left ( p , \mathcal { G } _ { \mathcal { F } _ { c } } ^ { \circ } \right ) \right ] \\ & = \frac { 1 } { 2 } \int _ { p \in X } \mathbb { E } \left [ \deg \left ( p , \mathcal { G } _ { \mathcal { F } _ { c } } ^ { \circ } \right ) \right ] \lambda d p & \quad \text { by Slivnyanak-Mecke Theorem,} \\ & \leq \frac { \lambda } { 2 } \int _ { p \in X } \left ( \frac { 5 0 } { 3 } \ln ( \lambda l r ) + O ( 1 ) \right ) d p & \quad \text { by Lemma 12.3,} \\ & = \frac { \lambda } { 2 } \int _ { [ - \frac { 5 } { 2 } , \frac { 5 } { 2 } ] \times [ - \pi , \pi r ] } ^ { 5 0 } \, \frac { \ln ( \lambda l r ) d w d y + O ( \lambda ) } { 3 } \\ & = \frac { 5 0 } { 3 } \lambda \pi l r \ln ( \lambda l r ) + O ( \lambda ) \\ & = O ( \lambda l r \ln ( \lambda l r ) ) . \\$$

□

And we can prove the upper bound part of the main theorem of the chapter. Remember that, by Property 2.2, # Del(X) = Θ(E) where E is the set of edges of Del(X).


<!-- p:109 -->


Lemma 12.5. The 3-dimensional Delaunay triangulation of a homogeneous Poisson point process distributed, with intensity λ, on a right circular cylinder, has expected size O(λln λ).

Proof. We apply Lemmas 12.2 and 12.4 to get an upper bound on the number of edges in the Delaunay triangulation, and deduce:

$$\mathbb { E } \left [ \mathfrak { H } \, D e l ( X ) \right ] \leq \mathbb { E } \left [ \mathfrak { H } _ { \mathcal { F } ^ { c } } ^ { \wp } ( X ) \right ] = O ( \lambda l r \ln ( \lambda l r ) ) .$$

#### 12.5 A lower bound on E [# Del(X)]

In order to complete the proof of Theorem 12.1, we have to show that the bound is actually tight. To this end, we propose to show off a sub-graph of the Delaunay triangulation of points distributed on a cylinder. A way to consider a sub-graph is to restrict the set of possible empty sphere. Thus we will consider an empty region graph in which, for all pairs of points (p, q), is associated a single sphere, that we name σ0(p, q), and we will say that p and q are neighbors if σo(p, q) is empty. We have to choose σ0(p, q) carefully enough so that the expected degree of p is still Ω (λ ln λ) when the graph is applied on a Poisson point process with parameter λ distributed on a cylinder.

As the previous section suggests, the 3D-Delaunay triangulation of points on a cylinder is highly related with the empty axis-aligned ellipse graph with unbounded aspect ratio. In Section 8.2, we had found a tight lower bound on the empty axis-aligned ellipse graph by identifying an axis-aligned ellipse for each pair (p, q). More precisely, for p at the origin and a point q = (xq, yq), we selected the ellipse passing through q with equation:

$$\frac { y _ { q } ^ { 2 } } { x _ { q } ^ { 2 } } \left ( x - \frac { 1 } { 2 } x _ { q } \right ) ^ { 2 } + \left ( y - \frac { 1 } { 2 } y _ { q } \right ) ^ { 2 } = \frac { 1 } { 2 } y _ { q } ^ { 2 } ,$$

$$\frac { y _ { q } ^ { 2 } } { x _ { q } ^ { 2 } } x ^ { 2 } - x \frac { y _ { q } ^ { 2 } } { x _ { q } } + y ^ { 2 } - y y _ { q } = 0 .$$

This ellipse has an area that is Θ(xqyq), and that induced the logarithmic degree of p. The parameter c y2 corresponding to this ellipse was c = ( 2

Let's go back to the 3-dimensional case, in the Monge coordinate system of p, and consider that q is a point on the cylinder with coordinates (xq, yq, zq). We have to find, for each q, a sphere whose intersection with C has area Θ(xqyq). An idea could be to reuse the parameter used in Section 8.2, a bit adapted to y2 the 3D case. Following this idea, we consider the center c0 = (xo, yo, z0) with x0 = 2xq , y0 = yq 2 and z0 such that c0 ∈ PBis(p, q), and expect that the sphere σ0 centered on c0 has an intersection with C with the required area.

We recall that the cylinder is parameterized by the equation:

$$\mathcal { C } \colon x ^ { 2 } + ( z - r ) ^ { 2 } = r ^ { 2 } .$$

We start by identifying the coordinate z0. The equation of PBis is:

$$0 = \left ( x - \frac { x _ { q } } { 2 } \right ) x _ { q } + \left ( y - \frac { y _ { q } } { 2 } \right ) y _ { q } + \left ( z - \frac { z _ { q } } { 2 } \right ) z _ { q } ,$$

also rewritable as:

□


<!-- p:110 -->


so c0 must verify:

$$\tilde { y } \colon & & 0 = \left ( x _ { 0 } - \frac { x _ { q } } { 2 } \right ) x _ { q } + \left ( y _ { 0 } - \frac { y _ { q } } { 2 } \right ) y _ { q } + \left ( z _ { 0 } - \frac { z _ { q } } { 2 } \right ) z _ { q } \\ & = \left ( \frac { y _ { q } ^ { 2 } } { 2 x _ { q } } - \frac { x _ { q } } { 2 } \right ) x _ { q } + \left ( \frac { y _ { q } } { 2 } - \frac { y _ { q } } { 2 } \right ) y _ { q } + \left ( z _ { 0 } - \frac { z _ { q } } { 2 } \right ) z _ { q } \\ & = \frac { 1 } { 2 } \left ( y _ { q } ^ { 2 } - x _ { q } ^ { 2 } \right ) + \left ( z _ { 0 } - \frac { z _ { q } } { 2 } \right ) z _ { q } \\ & = \frac { 1 } { 2 } \left ( y _ { q } ^ { 2 } - x _ { q } ^ { 2 } \right ) + z _ { q } z _ { 0 } - \frac { 1 } { 2 } z _ { q } ^ { 2 } , \text { and so} \\ & = z _ { 0 } = \frac { 1 } { 2 } \frac { x _ { q } ^ { 2 } - y _ { q } ^ { 2 } + z _ { q } ^ { 2 } } { z _ { q } } \\ & = \frac { 1 } { 2 } \frac { r ^ { 2 } - ( z _ { q } - r ) ^ { 2 } - y _ { q } ^ { 2 } + z _ { q } ^ { 2 } } { z _ { q } } \\ & = \frac { - 2 z _ { q } r - z _ { q } ^ { 2 } - y _ { q } ^ { 2 } + z _ { q } ^ { 2 } } { z _ { q } } \\ & = \frac { - 2 z _ { q } r - y _ { q } ^ { 2 } } { z _ { q } } \\ & = r - \frac { 1 } { 2 } \frac { y _ { q } ^ { 2 } } { z _ { q } } \\ \intertext { s o n f t h e a l l B ( \sigma _ { 0 } ) is given by: B _ { 0 } ( x , y , z ) < 0 , where: } B _ { 0 } ( x , y , z ) = x ^ { 2 } - 2 x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } + z ^ { 2 } - 2 z z _ { 0 }$$

The equation of the ball B (σ0) is given by: B0(x, y, z) &lt; 0, where:

$$a t i o n o f t h e b a l l \, \mathcal { B } ( \sigma _ { 0 } ) & \text { is given by: } \, B _ { 0 } ( x , y , z ) < 0 , \text { where: } \\ B _ { 0 } ( x , y , z ) & = x ^ { 2 } - 2 x x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } + z ^ { 2 } - 2 z z _ { 0 } \\ & = x ^ { 2 } - 2 x x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } + z ^ { 2 } - 2 z \left ( r - \frac { y _ { q } ^ { 2 } } { 2 z _ { q } } \right ) \\ & = - 2 x x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } + x ^ { 2 } + z ^ { 2 } - 2 z r + z \frac { y _ { q } ^ { 2 } } { z _ { q } } \\ & = z \frac { y _ { q } ^ { 2 } } { z _ { q } } - 2 x x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } + x ^ { 2 } + ( z - r ) ^ { 2 } - r ^ { 2 } . \\ \intertext { y } y \, \text { point on } \mathcal { C } \, \text { verifies } x ^ { 2 } + ( z - r ) ^ { 2 } - r ^ { 2 } = 0 , \text { then any point of } \mathcal { B } ( \sigma _ { 0 } ) \cap \mathcal { C } \, \text { verifies} .$$

Since any point on C verifies x2 + (z − r)2 − r2 = 0, then any point of B (σ0) ∩ C verifies:

$$z \frac { y _ { q } ^ { 2 } } { z _ { q } } - 2 x x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } < 0 .$$

We consider now the projection onto Tc(p) of the intersection B (σ0) ∩ C. We can ask ourselves if we should better consider the intersection with the lower part or the upper part of the cylinder. But since y2 the center of σ0 verifies z0 = r − 2 xq 1 that is smaller than r, we have good chance to think that the intersection with the lower part of the cylinder is more significant. Thus we substitute z by:

$$f _ { p } ( x , y ) = r - \sqrt { r ^ { 2 } - x ^ { 2 } } ,$$

that is the graph of the lower part. The projection of the intersection is given by E0(x, y) ≤ 0 where

$$1 ^ { 0 } & \quad \text {0} ^ { 2 } \quad \text {j} ^ { 3 } \quad \text {c} ( \begin{matrix} 1 & y _ { q } ^ { 2 } \\ 0 & z _ { q } \end{matrix} ) \\ E _ { 0 } ( x , y ) & = \frac { y _ { q } ^ { 2 } } { z _ { q } } \left ( r - \sqrt { r ^ { 2 } - x ^ { 2 } } \right ) - 2 x x _ { 0 } + y ^ { 2 } - 2 y y _ { 0 } \\ & = \frac { y _ { q } ^ { 2 } } { z _ { q } } \left ( r - \sqrt { r ^ { 2 } - x ^ { 2 } } \right ) - \frac { y _ { q } ^ { 2 } } { x _ { q } } x + y ^ { 2 } - y _ { q } y$$


<!-- p:111 -->


We search for an upper bound on the region defined by the above equation. Finding the extreme x and y coordinates of the region is enough. For now we bound from below the expression using the inequalities: t2 ≤ r − √r2 − t2 ≤ t2 for |t| ≤ r: 2r r

$$r - \sqrt { r ^ { 2 } - t ^ { 2 } } & \leq \frac { t } { r } \text { for } | t | \leq r \colon \\ E _ { 0 } ( x , y ) & = \frac { y _ { q } ^ { 2 } } { z _ { q } } \left ( r - \sqrt { r ^ { 2 } - x ^ { 2 } } \right ) - \frac { y _ { q } ^ { 2 } } { x _ { q } } x + y ^ { 2 } - y _ { q } y \\ & \geq \frac { 1 } { 2 } \frac { y _ { q } ^ { 2 } } { z _ { q } } \frac { x ^ { 2 } } { r } - \frac { y _ { q } ^ { 2 } } { x _ { q } } x + y ^ { 2 } - y _ { q } y \text { for } | x | \leq r \\ & \geq \frac { 1 } { 2 } \frac { y _ { q } ^ { 2 } } { x _ { q } ^ { 2 } } x ^ { 2 } - \frac { y _ { q } ^ { 2 } } { x _ { q } } x + \frac { 1 } { 2 } y ^ { 2 } - y _ { q } y \text { for } | x _ { q } | \leq r . \\ \intertext { s i n s e x p r e s s i o n g e l l i p o s e }$$

We rewrite this expression to make appear the corresponding ellipse:

$$\text {we rewrite this expression to make appear the corresponding engine.} \\ \frac { 1 } { 2 } \frac { \frac { y _ { q } ^ { 2 } } { x _ { q } } x ^ { 2 } - \frac { y _ { q } ^ { 2 } } { x _ { q } } x + \frac { 1 } { 2 } y ^ { 2 } - y _ { q } y & = \frac { y _ { q } } { x _ { q } } \left ( \frac { 1 } { 2 } \frac { y _ { q } } { x _ { q } } x ^ { 2 } - y _ { q } x + \frac { 1 } { 2 } \frac { x _ { q } } { y _ { q } } y ^ { 2 } - x _ { q } y \right ) \\ & = \frac { y _ { q } } { x _ { q } } \left ( \frac { 1 } { 2 } \frac { y _ { q } } { x _ { q } } \left ( x ^ { 2 } - 2 x _ { q } x \right ) + \frac { 1 } { 2 } \frac { x _ { q } } { y _ { q } } \left ( y ^ { 2 } - 2 y _ { q } y \right ) \right ) ,$$

y2 so that we can deduce that 12 x+ 22 xq through p, centered on the orthogonal projection πp(q) of q on Tc(p). Its extreme x coordinates are reached for y = yq and verify:

$$f \text { for } y & = y _ { q } \text { and verify:} \\ & = \frac { 1 } { 2 } \frac { y _ { q } } { x _ { q } } \left ( x ^ { 2 } - 2 x _ { q } x \right ) + \frac { 1 } { 2 } \frac { x _ { q } } { y _ { q } } \left ( y _ { q } ^ { 2 } - 2 y _ { q } y _ { q } \right ) \\ & = \frac { 1 } { 2 } \frac { y _ { q } } { x _ { q } } \left ( x ^ { 2 } - 2 x _ { q } x \right ) - \frac { 1 } { 2 } x _ { q } y _ { q } , \, \text {rewritten} \\ & 0 = x ^ { 2 } - 2 x _ { q } x - x _ { q } ^ { 2 } , \, \text {by multiplying by } 2 \frac { x _ { q } } { y _ { q } } , \\ & 0 = \left ( x - \left ( 1 - \sqrt { 2 } \right ) \right ) x _ { q } \right ) \left ( x - \left ( 1 + \sqrt { 2 } \right ) x _ { q } \right ) , \, \text {after factorization} . \\ \text {analogy, its extreme y coordinates verify:}$$

By analogy, its extreme y coordinates verify:

$$0 = \left ( y - \left ( 1 - \sqrt { 2 } \right ) y _ { q } \right ) \left ( y - \left ( 1 + \sqrt { 2 } \right ) y _ { q } \right ) .$$

In other words, the projection of the intersection is contained in the rectangle [xq ±√2xq] × [yq ±√2yq]. To ensure that the intersection stay inside the lower part of the cylinder, we only take into account the points q such that [xq ± √2xq] × [yq ± √2yq] is inside [−r*, r*] × [−2 only if it verifies |xq| ≤ || + r

Then, for a pair (p, q), we consider the fundamental singleton of region FC(p, q) defined as follow:

$$\mathcal { F } _ { 0 } ^ { \mathcal { C } } ( p , q ) = \left \{ \begin{array} { l l } { \{ \mathcal { B } \left ( \sigma _ { 0 } \right ) \cap \mathcal { C } \} , \, i f \, q \in N ( p ) } \\ { \{ \mathcal { C } \} , \, o t h e r w i s e . } \end{array}$$

Since C contains the data sample, it is never empty, and this is another way to say that q is not a neighbor of p if q does not belong to N(p). Note that, in general, since σ0(p, q) ≠ σ0(q, p) then FC (p, q) ≠ FC (q, p).

Finally, for a data sample X, we consider the directed graph (X) in which the directed edge (p, q) exists if q belongs to N(p) and the sphere σ0(p, q) is empty.

We prove the following lemma:

Lemma 12.6. Let C be a right circular cylinder with length l and radius r. Let p be a point of C, and X a Poisson point process distributed on C with intensity λ. The expected degree of p in (X) is greater of than ln(λlr) π


<!-- p:112 -->


Proof. We consider again the isometry i from C to the rectangle [- , ] × [−πr, πr] that consists of 2, unrolling the cylinder into its tangent plane at p. Recall that for a point u ∈ C, we denoted by (xu, y′) the image of u by i.

We consider a point q ∈ N(p) and compute an upper bound on the area of the region B (σo(p, q)) ∩C. Since its projection πp (B (σ0(p, q)) ∩C) is included in the rectangle [xq ± √2xq] × [yq ± √2yq], we can ou ot e o r o  o on s or  os n n oe t udr indeed we can say that:

$$\text {indeed we can say that:} \\ | \mathcal { B } \left ( \sigma _ { 0 } ( p , q ) \right ) \cap \mathcal { C } | & \leq \pi _ { p } ^ { - 1 } \left ( [ x _ { q } \pm \sqrt { 2 } x _ { q } ] \times [ y _ { q } \pm \sqrt { 2 } y _ { q } ] \right ) \\ & = 2 \sqrt { 2 } | y _ { q } ^ { \prime } | \pi _ { p } ^ { - 1 } \left ( [ x _ { q } \pm \sqrt { 2 } x _ { q } ] \right ) \text { since } y _ { q } = y _ { q } ^ { \prime } \\ & \leq 2 \sqrt { 2 } | y _ { q } ^ { \prime } | \times \frac { \pi } { 2 } \sqrt { 2 } | x _ { q } ^ { \prime } | \text { since for any } u \text { in the lower part of } \mathcal { C } , | x _ { u } | \leq \frac { \pi } { 2 } | x ^ { \prime } _ { u } | , \\ & = 4 \pi | x _ { q } ^ { \prime } y _ { q } ^ { \prime } | . \\$$

Then we can compute an upper bound on expected degree of p in (X): ∂f

$$& \quad \, \text {an compute an upper bound on expected degree of } p \text { in } \overrightarrow { \mathcal { G } } _ { \mathcal { I } _ { 0 } } ^ { \emptyset } ( X ) \colon \\ & \quad \, \vec { g } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { F } } ^ { \emptyset } \right ) \right ] = \mathbb { E } \left [ \sum _ { q \in X \cap N ( p ) } \mathbb { I } _ { [ \mathcal { G } ( \sigma _ { 0 } ( p , q ) ) \cap X = 0 ] } \right ] \\ & \quad \, = \int _ { q \in N ( p ) } \lambda \, \mathbb { P } \left [ \mathcal { B } \left ( \sigma _ { 0 } ( p , q ) \right ) \cap X = \emptyset \right ] d q \text { by Slivnyak-Mecke theorem} , \\ & \quad \, = \int _ { q \in N ( p ) } \lambda e ^ { - \lambda | \mathcal { B } ( \sigma _ { 0 } ( p , q ) ) \cap C | } d q \\ & \quad \, = \int _ { q ^ { \prime } \in i ( N ( p ) ) } \lambda e ^ { - \lambda | \mathcal { B } ( \sigma _ { 0 } ( p , q ) ) \cap C | } d q ^ { \prime } \text { since } i \text { is an isometry} , \\ & \quad \, = \int _ { ( x ^ { \prime } _ { q } , y ^ { \prime } _ { q } ) \in i ( N ( p ) ) } \lambda e ^ { - \lambda | \mathcal { B } ( \sigma _ { 0 } ( p , q ) ) \cap C | } d x ^ { \prime } _ { q } d y ^ { \prime } _ { q } \\ & \quad \, \geq \iint _ { ( x ^ { \prime } _ { q } , y ^ { \prime } _ { q } ) \in i ( N ( p ) ) } \lambda e ^ { - 4 \pi \lambda | x ^ { \prime } _ { q } y ^ { \prime } _ { q } | } d x ^ { \prime } _ { q } d y ^ { \prime } _ { q } \\ & \quad \geq \int _ { | q ^ { \prime } _ { q } | \leq \frac { 1 } { 2 + 2 / 2 } } \int _ { | x ^ { \prime } _ { q } | \leq \frac { r } { 1 + \sqrt { 2 } } } \lambda e ^ { - 4 \pi \lambda | x ^ { \prime } _ { q } y ^ { \prime } _ { q } | } d x ^ { \prime } _ { q } d y ^ { \prime } _ { q } \text { since } | x _ { q } | \leq | x ^ { \prime } _ { q } | \\ & \quad = 4 \lambda \int _ { 0 } ^ { \frac { 1 } { 2 + 2 / 2 } } \int _ { 0 } ^ { \frac { r } { 1 + \sqrt { 2 } } } e ^ { - 4 \pi \lambda x ^ { \prime } _ { q } y ^ { \prime } _ { q } d x ^ { \prime } _ { q } d y ^ { \prime } _ { q } } . \\ & \text {recognize the already computed integral } I _ { a , b } ( t ) = \int _ { 0 } ^ { a } \int _ { 0 } ^ { b } e ^ { - t x y } d y d x \text { for } a = \frac { l } { 2 + 2 / 2 } , b = \frac { r } { 1 + \sqrt { 2 } } \\ & \text {since we had shown that} .$$

Where we recognize the already computed integral Ia,b(t) = ∫θ So cb e−txydydx for a = l b = r 2+2√2 1+√2 and t = 4πλ. Since we had shown that:

$$I _ { a , b } ( t ) > \frac { \ln ( a b t ) } { t } ,$$

$$\left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { F } _ { 0 } ^ { c } } ^ { \emptyset } \right ) & \geq 4 \lambda \frac { \ln \left ( \frac { 1 } { 2 } \frac { l r } { ( 1 + \sqrt { 2 } ) ^ { 2 } } 4 \pi \lambda \right ) } { 4 \pi \lambda } \\ & \geq \frac { \ln ( \lambda l r ) } { \pi } .$$

we can conclude that :

□

Since we have an lower bound on the expected degree of a point in on the whole cylinder to get a lower bound on the expected number of directed edges of We consider the undirected version GFg FC FC Note that the degree of a point in the undirected graph is necessarily greater, since we also count the edges that were in the opposite direction. Then we deduce Lemma 12.7. Let C be a right circular cylinder with length l and radius r and let X be a Poisson point process distributed on C with intensity λ. The expected number of edges in GF (X) is Ω(λlr ln(λlr)). FC


<!-- p:113 -->


Proof. Let N0 be the number of edges in Gσg GFe (X).

$$p r o f . \, \text { Let } N _ { 0 } \, \text { be the number of edges in } \mathcal { G } _ { \mathcal { F } _ { 0 } ^ { c } } ^ { \emptyset } ( X ) . \\ N _ { 0 } = \frac { 1 } { 2 } \sum _ { p \in X } \deg \left ( p , \mathcal { G } _ { \mathcal { F } _ { 0 } ^ { c } } ^ { \emptyset } \right ) \\ \geq \frac { 1 } { 2 } \sum _ { p \in X } \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { F } ^ { c } } ^ { \emptyset } \right ) \quad \text {for } w \\ \mathbb { E } \left [ N _ { 0 } \right ] \geq \mathbb { E } \left [ \frac { 1 } { 2 } \sum _ { p \in X } \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { F } ^ { c } } ^ { \emptyset } \right ) \right ] \\ = \frac { 1 } { 2 } \lambda \int _ { p \in \mathcal { C } } \mathbb { E } \left [ \overrightarrow { \deg } \left ( p , \overrightarrow { \mathcal { G } } _ { \mathcal { F } ^ { c } } ^ { \emptyset } \right ) \right ] d p \\ \geq \frac { \lambda } { 2 } \int _ { p \in \mathcal { C } } \frac { 1 } { \pi } \ln ( \lambda l r ) d p \\ = \frac { \lambda } { 2 } \int _ { [ - \frac { 1 } { 2 } , \frac { 1 } { 2 } ] \times [ - \pi r , \pi r ] } \frac { 1 } { \pi } \ln ( \lambda l r ) d v _ { p } d u _ { p } \\ = \lambda l r \ln ( \lambda l r ) . \\ \\ \text {And we can prove the lower bound part of the } m$$

for which we compute the expected value:

by Slivnyak-Mecke Theorem,

by Lemma 12.6,

And we can prove the lower bound part of the main theorem of the chapter:

Lemma 12.8. The 3-dimensional Delaunay triangulation of a homogeneous Poisson point process distributed, with intensity λ, on a right circular cylinder, has expected size Ω(λln λ).

Proof. It is clear that G0 is a sub-graph of the Delaunay triangulation since we restricted both of the possible neighbors and the possible empty spheres. So we apply Lemma 12.7 to get a lower bound on the number of edges in the Delaunay triangulation:

$$\mathbb { E } \left [ \mathbb { H } \, \text {Decl} ( X ) \right ] \geq \mathbb { E } \left [ \mathbb { H } \, \mathcal { G } _ { \mathcal { F } _ { 0 } ^ { c } } ^ { \emptyset } ( X ) \right ] = \Omega \left ( \lambda l r \ln ( \lambda l r ) \right ) .$$

□


The main theorem follows directly as a corollary of Lemma 12.5 and Lemma 12.8.

Theorem 12.1. The 3-dimensional Delaunay triangulation of a homogeneous Poisson point process distributed, with intensity λ, on a right circular cylinder, has expected size Θ(λln λ).

#### 12.6 Conjecture on two classes of surface

We finish the chapter dedicated to the triangulation of random points on a cylinder, by conjecturing a generalization of the obtained result. A cylinder of revolution has an important property for the Delaunay triangulation: whatever is the chosen orientation, the maximal principal curvature corresponds everywhere to the curvature of the osculating sphere (degenerate into a plane for the outer orientation). Thus we can consider two classes of surfaces: the first class contains surfaces for which any inner medial sphere is osculating: the canal surfaces; and the second class contains surfaces whose outer osculating spheres are planes: cylinder whose basis is not necessary a circle. The cylinder of revolution enters in both of these categories.

We deduce the following conjecture:


<!-- p:114 -->


Conjecture 12.9. Let S be a piece-wise C2 closed surface embedded in R3, and X a Poisson point process distributed on S with intensity λ. If S is a canal surface with no spherical part or a cylinder not degenerated into a plane, then

$$\mathbb { E } \left [ \mathfrak { H } \text {Del} ( X ) \right ] = \Theta ( \lambda \ln \lambda ) .$$

For classical examples, such class of surfaces includes the torus, the prolate spheroid, and the right circular cones. The idea is again to prove that a point has expected degree Θ(ln λ). We can do that by considering the fact that a medial sphere whose radius is slightly increased, has an intersection with S that is almost a strip on the surface, so that we fall back into the case of the right cylinder of revolution.

In the conclusion of the thesis, we propose a conjecture that gives the expected size of the Delaunay triangulation with respect to the medial axis of the surface.


<!-- p:115 -->


## Chapter 13

##### Expected size of the Delaunay triangulation of a Poisson point process on an oblate spheroid

In R3, we consider an ellipsoid of revolution, also called spheroid. We distribute on this spheroid a homogeneous Poisson point process and try to evaluate the size of the Delaunay triangulation of the distributed -  t t s  tat e sls e    ie ds   so ear. A flattened sphere is not really a generic surface, but it shares properties with generic surfaces. We demonstrate in that chapter that the 3-dimensional Delaunay triangulation has indeed a linear expected size. The proof goes through an analytic study of intersection of sphere with the spheroid of revolution. Since it is a very specific surface, namely a quadric of revolution, we could have used algebraic methods to compute the exact intersections between Delaunay spheres and the spheroid. But this would not have helped us to introduce the generic cases of surfaces, that are not necessary quadrics. Thus we preferred to use an analytic approach, easier to generalize. The proof reuses the notion of empty axis-aligned region graph and the Combination and Partition lemmas. The proof may be a bit complicated for such a specific surface, but most parts will be reused in Part IV to lighten the proof for the general case. It is decomposed into 3 sections, each corresponds to a different neighborhood in which we compute the ppa    o   pod se d o e t  od     de details on spheroids.

#### 13.1 The oblate spheroid

##### 13.1.1 Some generalities on the oblate spheroid

####### General description

A spheroid can be seen as a sphere that has been stretched in a given direction with a factor k &gt; 0. This direction corresponds to the axis of revolution of the spheroid. This axis passes through through the two poles of the spheroid. On a spheroid, two symmetries naturally arise: an axial symmetry around the axis of the spheroid, and a reflection with respect to the bisector plane of the two poles of the spheroid. We denote by PMed this plane. If k &lt; 1, we say that the spheroid is oblate, if k &gt; 1, we say that it is prolate. They have fundamentally different properties. Perhaps the most important of them is the nature of their medial axis. On the prolate spheroid, the medial axis is segment, included in the axis of revolution, and whose endpoints are the centers of the two spheres osculating at the poles. On the oblate spheroid, it is a disk included in PMed. This plane has a large importance in the following analysis, we named it PMed, as another plane present in Chapter 12, since they play a similar role.

Highly related with the medial axis, is the set Z of points with a principal curvature that is locally maximal along a line of curvature. If E is prolate, Z is the whole spheroid, for the reason that the circles that compose the spheroid are curvature lines, and then the curvature is constant along them, and thus in particular, local maxima. We expect that the Delaunay triangulation of points on such a surface will behave as if the points were on a cylinder, but this was already discussed in Section 12.6. In this section we assume that the surface, that we name E, is an oblate spheroid (we keep the letter "E" for spheroid because this word is more common). In that case, the set Z is the circle E ∩ PMed. Since Z is a 1-dimensional object, we can consider that E enters in what we characterize as a generic surface. The Il    e     s s  o o et-ed linear size.


<!-- p:116 -->


Figure 13.1: An oblate spheroid with some parallels and meridians, Z is the red parallel, it lies in PMed.

E

m

U

u

####### Different parameterizations of E

Without loss of generality, and up to a similarity, we consider that the spheroid E, with stretch factor k &lt; 1, is the surface of R3 defined by:

$$\mathcal { E } \colon \left \{ p \in \mathbb { R } ^ { 3 } , \ \frac { u _ { p } ^ { 2 } } { k ^ { 2 } } + v _ { p } ^ { 2 } + ( w _ { p } - 1 ) ^ { 2 } = 1 \right \} .$$

To describe globally the spheroid, we use the Cartesian coordinates (u, v, w). We call this coordinates system, the global coordinate system. As for the cylinder case, we use it to make a difference with the Monge coordinate systems that we will use later. In the global coordinate system, the spheroid is tangent to the plane with equation w = 0 at (0, 0, 0), that is both the lowest point of the spheroid and a point of Z. The maximal curvature κsup is equal to k and correspond to the maximal curvature of any point on Z. The minimal curvature is equal to k, i.e. to 1 is reached at the two poles of the spheroid. √κsup The coordinates of theses poles are (1, 0, 1) and (− of revolution the spheroid. The global frame representation will be helpful to study the behavior of the Delaunay triangulation of the points distributed close to Z.

Let p be a point on ε. We denote by Tε(p) the plane tangent to ε at p and by nε(p) its normal, that we choose to orient inward ε. If p is not a pole of ε, then it is crossed by two perpendicular lines of curvature, better known as meridian and parallels. Meridians lie in the planes that pass through the poles while parallels lie in the planes parallel to PMed. They define the principal directions and curvatures of p: the principal directions are the directions of the tangent directions at p of the meridian and the parallel in Tε(p), and principal curvatures are the curvatures of the intersection of E with the two planes perpendicular to Tε(p) and directed by the principal directions. Note that the maximal curvature at p is the curvature of the meridian at p, since its supporting plane is perpendicular to Tε(p), but its minimal curvature is not the curvature of the parallel, since the plane of the parallel at p is not perpendicular Tε(p). We denote respectively by κ1(p) and κ2(p) the maximal and minimal curvatures. When it is clear that we consider the curvatures at p, we will only write κ1 and κ2 to lighten the notations.


<!-- p:117 -->


The principal directions define the Monge coordinates system at p. For the Monge coordinates system, we use the Cartesian coordinates (x, y, z) where the x-axis is the maximal principal direction, the y-axis is the minimal principal direction, and the z-axis is the normal at p. We choose, for any p, to orient the x-axis in the direction of the closest pole to p. Since the z axis is already chosen inward, this determines uniquely the y-axis direction, except for points on Z or at the poles. Since Z and the poles have measure 0, a point from a Poisson process will not be distributed on them almost surely, so it is not necessary to treat such point. Note that in the Monge coordinates system of p, p is the origin and then (xp, yp, zp) = (0, 0, 0).

In the Monge coordinates system of p, the spheroid can be locally described by the equation z = fp(x, y) where:

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + R _ { 3 } ( x , y ) , \quad \text {from } ( 1 . 4 )$$

where |R3(x y)| ≤ O (|x|3 + |y|3)). This local description holds for √x2 + y2 ≤ √2 Such a neigh2κsup borhood guarantees that fp is locally a smooth homeomorphism. When it is not necessary to have the second order coefficients, we can use the approximation:

$$| f _ { p } ( x , y ) | \leq \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) , & & \text {from } ( 1 . 3 )$$

that is also true for √x2 + y2 ≤ √2 2κsup

####### Medial radius

On E, each point p has an inward symmetrical point p that is the reflection of p with respect to PMed. We assume that a point on Z is its own inward symmetrical point. We note r*(p) the medial radius, remember that in fact, it is the radius of the largest ball inside E, tangent to E at p and such that its interior has an empty intersection with E. More generally this sphere defines p, has the only other contact point of the sphere with ε. Here again we will just write r* instead of r*(p) when it is clear from the context. We recall we have r* ≤ 1 for all p ∈ E and r* = 1 on Z and only on Z. κ1 κ1

Since a spheroid is a convex surface, no point has outward symmetrical point. By symmetry, p and p have the same principal curvatures. At p, the medial plane PMed has equation:

$$\mathcal { P } _ { M e d } \colon z = r ^ { * } + x \tan ( \theta _ { p } ) ,$$

ht   t o p o   dt e       e ore t  de ot o nes s d  e  =  s se oe o

At some stage of the chapter, we will be interested in some geometric quantities on E at p with respect to the distance of p with Z. To simplify, since ε is a surface of revolution, we assume without loss of generality that p = (up, 0, wp) with up &gt; 0, and wp &lt; 1. Thus, the geometric quantities will be expressed with respect to up.

#### 13.2Overview of the proof

We present, in this section, the lemmas that lead to our result: The 3D-Delaunay triangulation of a Poisson point process distributed on a prolate spheroid has a linear expected size. The lemmas are proven in the following sections.

####### Reminder of the general idea

We recall briefly the general idea of the proof: to obtain an upper bound on the expected size of the 3D-Delaunay triangulation, we consider a super-graph of the Delaunay graph, simpler to study, and compute an upper bound on the degree in this super-graph. As explained in Chapter 2, the number of Delaunay edges also bounds the number of triangles and tetrahedra. Since the number is the half-sum of the degrees of the vertices of the graph, we actually compute an upper bound on the expected degree of the vertices. In the Delaunay triangulation, two points p and q are neighbors if and only if there exists an empty sphere passing through those points. Like in the previous examples, we will reduce our study to a finite number of spheres passing through p and q. We will choose those spheres such that their intersection with the surface has an area large enough to obtain the required expected degree. The choice of spheres will provide a partition of the bisector plane PBis(p, q) of p and q, defined by the centers of the spheres. Each tile of the partition is associated with a region of the surface depending on p and q. By the Combination and Partition lemmas, we then claim that the empty region graph based upon the regions is a super-graph of the Delaunay graph. Depending on the precision of the bound on the degree of p in Del({p} ∪ X) we want to obtain, we will consider different partitions. To simplify the notation, we will denote by deg(p), the degree of in the Delaunay triangulation. If the graph G in which we express the degree is not the Delaunay triangulation, we will mention it like this: deg(p, G).


<!-- p:118 -->


We present now the main lines of the proof. First we consider a point p ∈ ε for which we will compute an upper bound on the degree. In a first section, we bound the number of expected neighbors in a close neighborhood of p. Unfortunately, the size of this neighborhood goes to 0 when p goes to Z. Consequently we bound again the number of expected neighbors in a greater neighborhood of p, that we call middle-range neighborhood, the bound we obtain is less precise but still sufficiently small. Then we will divide the spheroid into a part far enough from Z where the degree of a point is O(1), and a part around Z, where the degree of a point depends on its distance with Z. Finally we sum up all results to obtain the expected number of edges.

####### Main lemmas

We recall that κ1, κ2 and r* depend on p. We define βr* = 1 1−κ1r* that also depends on p. It can be 1−κ2r* seen as the aspect ratio of the elliptic-like region defined by the intersection of ε with a sphere passing through p and close to its medial sphere. Note that we will prove in Lemma 13.11 that βr* = Θ(up).

We start in Section 13.3 to prove that a point q that is far enough from the medial sphere σ* of p has low chance of being a Delaunay neighbor of p. This is proven in Lemma 13.7. That induces that the neighbors of p are close to ε ∩ B(σ*), and so are close either to p or to p.

The next lemma provides an upper bound on the expected number of what we call the close neighbors of p. We denote by CN(p) the set of close neighbors of p. The points in CN(p) are either close to p or close to p. We do not describe CN(p) here, it is precisely defined in Section 13.4. For now, keep in mind that it is the union of two axis-aligned rectangles on ε, centered on p or p, and with sides Ω(βr) and Ω(β2*) along the principal directions of p and p. This lemma is proven in Section 13.4.

Lemma 13.1. Let E be an oblate spheroid and X a Poisson point process distributed on E with intensity λ. For any p ∈ ε \ Z, the expected number of close neighbors of p in Del(X ∪ {p}) is:

$$O \left ( \ln \frac { 1 } { \beta _ { r ^ { * } } } \right )$$

That being said, some points that are not in the close neighborhood of p may be neighbors of p nevertheless. We prove, as a corollary of Lemma 13.7 applied to points outside CN(p) that such neighbors exist with low probability.

Lemma 13.2. Let E be an oblate spheroid, p a point of E, and X a point set on E whose restriction to the close neighborhood of p is a Poisson point process with intensity λ. The probability that p has a neighbor in Del(X ∪ {p}) outside the close neighborhood of p is:

$$\begin{cases} \ e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \ i f \, u _ { p } \leq \frac { 1 } { 2 \kappa _ { \sup } } , \\ \ e ^ { - \Omega ( \lambda ) } \ o t h e r w i s e . \end{cases}$$


<!-- p:119 -->


The expected numbers E [deg (p)] of neighbors of p could then be counted this way:

$$\mathbb { E } \left [ \deg ( p ) \right ] & = \mathbb { E } \left [ \sum _ { q \in X \cap C ( p ) } \mathbb { 1 } _ { ( p , q ) \in D \left ( X \cup \{ p \} \right ) } \right ] + \mathbb { E } \left [ \sum _ { q \in X \ \{ C ( N ) ( p ) } \ \mathbb { 1 } _ { ( p , q ) \in D \left ( X \cup \{ p \} \right ) } \right ] \\ & = O \left ( \ln \frac { \frac { 1 } { \beta _ { * } } } { \beta _ { * } r } \right ) + \lambda \int _ { q \in \mathcal { E } \ \{ C ( N ) ( p ) } \ \mathbb { 1 } \left ( [ p , q ) \in D \left ( X \cup \{ p , q \} \right ) \right ] d q \\ & \leq O \left ( \ln \frac { \frac { 1 } { \beta _ { * } r } } { \beta _ { * } r } \right ) + \lambda \int _ { q \in \mathcal { E } \ \{ C ( N ) ( p ) } \ \mathbb { 1 } \left [ p \text { has a neighbor outside } C ( N ) \right ] d q . \\ \intertext { T h u s  as long as n is far enough from Z \, we can bound \beta _ { * } \text {, from below by a constant and the expected } }$$

Thus, as long as p is far enough from Z, we can bound βr* from below by a constant and the expected degree of p in Del(X ∪ {p}), given by

$$\mathbb { E } \left [ \deg ( p ) \right ] = O \left ( \ln \frac { 1 } { \beta _ { r ^ { * } } } \right ) + \lambda e ^ { - \Omega ( \lambda ) } ,$$

is bounded by a constant and the total number of edge with an endpoint far from Z is linear.

When p approaches Z, the expected degree of p in Del(X ∪ {p}) is given by

$$\mathbb { E } \left [ \deg ( p ) \right ] = O \left ( \ln \frac { 1 } { \beta _ { r ^ { * } } } \right ) + \lambda e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } ,$$

and, to obtain the total number of edges, we may be tempted to integrate this value with up. Close to Z, remind that βr* = Ω(up). The global number of edges with an endpoint close to Z is given by a half of the sum of the degree of such points. Suppose that we only count the number of edges with an endpoint p such that |up| &lt; 2κsup . The expected number of such edges is given, up to a constant factor, by:

$$\lambda \int _ { 0 } ^ { \frac { 1 } { 2 \kappa _ { s u p } } } \left ( \ln \frac { 1 } { u _ { p } } + \lambda e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \right ) d u _ { p } .$$

If the term λ ∫02 f 2κsup ln 1 dup remains linear with λ, it is unfortunately not the case for the term up λe u10Ω(λ)dup that is Θ (λ10) This is not so surprising since, as p approaches Z, the second order of fp is not sufficient to make a significant difference between the oblate spheroid E and the prolate spheroid with same curvatures, and for which we expect a super linear triangulation. Actually the behavior of the Delaunay triangulation should be similar than its behavior on a cylinder, where r* = 1 κ1 In other words, we may be able to find a logarithmic bound on their number of neighbors. On the other hand, the farther a point is from Z, the less the spheroid locally resembles to a cylinder, and we may be able to use the previous bound to measure the closeness of the degree with the logarithmic bound, with respect to the distance to Z. As a consequence, we need to consider differently the analysis of hn oo e  oe  oes se  sse ose  oe  se oe o e thhoe &gt; |dn| 3 ∂ d} =: dns +Z :srd   rds }, and ε \ Z+ 2κsup 2κsup

The following lemma states a bound on the expected number of middle-range Delaunay neighbors of a point p ∈ Z+2κsup .

By Lemmas 13.1 and 13.2, we can already claim that a point p in ε \ Z+2rsup has expected degree O(1). The following lemma provides an upper bound on the expected number of neighbors of a point p in Z+2κsup . We consider a second specific neighborhood for p, made of what we call middle-range neighbors. We note it MRN(p), it will be precisely defined in Section 13.5, for now, keep in mind that it consists only on points that are not in CN(p), are farther than p from Z, and at a distance O(1) from p or p.

Lemma 13.3. Let E be an oblate spheroid, p a point of Z+ 2κsup , and X a Poisson point process distributed on E with intensity λ. The expected number of middle-range neighbors q of p in Del(X ∪ {p}) is:

$$O ( \ln \lambda ) e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } .$$


<!-- p:120 -->


A noticeable difference with the bound from Lemma 13.1 is that the middle-range neighborhood remains large enough around Z. It is proven in Section 13.5

We finish the part-wise analysis by bounding the number of the remaining neighbors of p for p close to Z, those that are not in CN(p), neither in MRN(p). We call them the far neighbors and note the neighborhood FN(p).

Lemma 13.4. Let E be an oblate spheroid, p a point of Z+ 2κsup , and X a Poisson point process distributed on E with intensity λ. The expected number of far neighbors of p in Del(X ∪ {p}) is:

$$\lambda e ^ { - \Omega ( \lambda ) } .$$

Finally we obtain an upper bound on the expected number of edges by integrating those bounds on the spheroid E. Following those lemmas, we have the decomposition:

$$\mathbb { E } \left [ \mathfrak { H } \text {Del} ( X ) \right ] & = \frac { 1 } { 2 } \sum _ { p \in X } \mathbb { E } \left [ \deg ( p ) \right ] \\ & = \frac { 1 } { 2 } \lambda \int _ { p \in \mathcal { E } } \mathbb { F } \left [ \deg ( p ) \right ] d p \\ & = \frac { 1 } { 2 } \lambda \int _ { p \in \mathcal { E } \left \langle Z ^ { + } \frac { 1 } { 2 * \sup } \right \rangle } \mathbb { E } \left [ \deg ( p ) \right ] d p + \frac { 1 } { 2 } \lambda \int _ { p \in Z ^ { + } \frac { 1 } { 2 * \sup } \right \rangle } \mathbb { E } \left [ \deg ( p ) \right ] d p .$$

For all p ∈ ε \ Z+2sup , we decompose between the neighbors that are in CN(p) and those who are not:

$$\mathbb { E } \left [ \deg \left ( p \right ) \right ] & = \mathbb { E } \left [ \{ \{ ( p , q ) \in D e l ( X ) \} , \ q \in C N ( p ) \} + \mathbb { E } \left [ \{ ( p , q ) \in D e l ( X ) \} , \ q \notin C N ( p ) \right ] \right ] \\ & = O \left ( \ln \frac { 1 } { \beta _ { * } } \right ) + \lambda e ^ { - \Omega \left ( \lambda \right ) } \text { by Lennmass 13.1 and 13.2.} \\ & = O ( 1 ) \text { since } \min _ { p \in \mathcal { E } \ \left \langle Z ^ { + \frac { 1 } { 2 * \wp } } \right \rangle } ( \beta _ { * } ) \text { is strictly positive by compactity of } \mathcal { E } \ \left \langle Z ^ { + \frac { 1 } { 2 * \wp } } \right \rangle .$$

2κsup p∈ε\z+2ksup

d   o  t   d t s    o p  o   dns +  d  ods to an orientation of the Delaunay triangulation, that we denote by Del. Note that ∑ (d)sp p∈Z 2κsup 2∑ (p, De1). p∈Z 2κsup

$$\mathbb { E } \left [ \stackrel { \longrightarrow } { \deg } ( p , \stackrel { \longrightarrow } { D } ) \right ] & \leq \mathbb { E } \left [ \mathbb { H } \left \{ ( p , q ) \in D e l ( X ) \right \} , \ q \in C N ( p ) \right ] + \mathbb { E } \left [ \mathbb { H } \left \{ ( p , q ) \in D e l ( X ) \right \} , \ q \in M N R ( p ) \right ] \\ & \quad + \mathbb { E } \left [ \mathbb { H } \left ( p , q \right ) \in D e l ( X ) \right \} , \ q \in F N ( p ) ] \\ & = O \left ( \ln \frac { 1 } { u _ { r } } \right ) + O \left ( \ln \lambda \right ) e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } + \lambda e ^ { - \Omega ( \lambda ) } \text { by Lemmas 13.1, 13.3 and 13.4 } \, .$$

F   ee  (  s     n  t   tie over E. Note that to integrate on p ∈ Z+2rsup , we parameterize p by up that we integrate on [0, 1 2Ksup and multiply the integral by the length |Z| of Z that only produces a constant factor.


<!-- p:121 -->


$$and \text { multiply the integral by the length } | Z | \text { of } Z \text { that only produces a constant factor.} \\ \mathbb { E } [ \mathcal { D } \text { Del} ( X ) ] & \leq \frac { 1 } { 2 } \int _ { p \in \mathcal { V } ^ { \geq \frac { 1 } { Z ^ { \ast \inf } _ { \ }wp } } \mathbb { E } \left [ \deg ( p ) \right ] d p + \lambda \int _ { p \in \mathcal { Z } ^ { \ast \inf } _ { \ }wp } \mathbb { E } \left [ \overrightarrow { \deg ( p , \overrightarrow { D } ) } \right ] d p \\ & \leq \lambda \int _ { p \in \mathcal { V } ^ { \geq \frac { 1 } { Z ^ { \ast \inf } _ { \ }wp } } \mathbb { O } ( 1 ) d p + \lambda \int _ { p \in \mathcal { Z } ^ { \ast \inf } _ { \ }wp } \left ( O \left ( \ln \frac { 1 } { \vartheta _ { p } } \right ) + O \left ( \ln \lambda \right ) e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } + \lambda e ^ { - \Omega ( \lambda ) } \right ) d p \\ & \leq | \mathcal { E } | O ( \lambda ) + O ( | Z | ) \lambda \int _ { \mathbb { U } _ { p } \in [ 0 , \frac { Z \varphi } { 2 \xi _ { \inf } } ] } \left ( O \left ( \ln \frac { 1 } { \varpi _ { p } } \right ) + O \left ( \ln \lambda \right ) e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \right ) d u _ { p } + \lambda ^ { 2 } \int _ { \mathbb { Z } ^ { \infty } _ { p } } + \frac { \sigma ^ { - \Omega ( \lambda ) } d p } { \Lambda ^ { 2 } \Omega ^ { \infty } } \int _ { \mathbb { Z } ^ { \infty } _ { p } } \\ & \leq O ( \lambda ) + O ( \lambda ) \int _ { \mathbb { U } _ { p } \in [ 0 , \frac { 1 } { 2 \varphi } ] } \ln \frac { 1 } { \varpi _ { p } } d u _ { p } + O \left ( \lambda \ln \lambda \right ) \int _ { u _ { p } \in [ 0 , \frac { 1 } { 2 \varphi } ] } e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } d u _ { p } + \lambda ^ { 2 } e ^ { - \Omega ( \lambda ) } \\ & = O ( \lambda ) + O ( \lambda ) + O \left ( \lambda ^ { \frac { 1 } { 2 } } \ln \lambda \right ) + \lambda ^ { 2 } e ^ { - \Omega ( \lambda ) } \\ & = O ( \lambda ) , \\ \text {that proves the following theorem:}$$

that proves the following theorem:

Theorem 13.5. The 3-dimensional Delaunay triangulation of a homogeneous Poisson point process distributed, with intensity λ, on any oblate spheroid, has expected complexity Θ(λ).

The proofs of the lemmas stated above are given in the following three sections: the first one computes the probability that a point p has a Delaunay neighbor far from its medial sphere, this computation will permit to bound the number of neighbors that are not in the neighborhood CN(p). In a second section, we prove Lemma 13.1, that bounds the number of neighbors of p in CN(p) and Lemma 13.2, that bounds the probability of existence of Delaunay neighbors of p outside CN(p). This section is quite long and tedious in computation. Finally in the third section, we prove Lemma 13.3 and Lemma 13.4, that respectively bound, for p ∈ Z+ 2sup , the number of neighbors of p in MRN(p) and in FN(p).

#### 13.3 On the probability of existence of neighbors far from the medial sphere.

We prove in this section that a point p has a low probability to have a Delaunay neighbor far from its medial sphere.

####### On regions included in sphere passing through a point q far from σ*.

We use the Monge coordinates system of p. We call σ* the inner medial ball of p. We consider a positive number δ, and q ∈ ε a point at distance greater than δ from σ*. We compute an upper bound on the probability with respect to δ that q is a Delaunay neighbor of p in a Poisson point process distributed on ε.

Still denoting by B(σ) the ball for which σ is the boundary, we prove the following lemma:

Lemma 13.6. Let 0 ≤ δ ≤ 2κsup √2 and q ∈ E at distance greater than δ from σ*. If a sphere σ passes through p and q then B(σ) ∩ E contains either a region whose projection on Tε(p) is a disk with radius min δ cos (θp)) and with p on its boundary, or a region whose projection on Tε(p) is a disk 8 Ksup ,8,4 with radius min δ cos (θp)) and with p on its boundary. 16, 4

Proof. We divide the proof into two parts, the first one for zc ≥ 0 and the second one for zc ≤ 0. Since q is at distance greater than δ from σ*, we consider the ball B+δ(σ*), centered at c* and with radius r* + δ, outside of which lies q.

In both cases, we prove that the center of the sphere σ is significantly shifted with respect to the lines (pc*) or (pc*).


<!-- p:122 -->


Figure 13.2: The center c' of the shrunken sphere σ′ from p lies on the spheroid Prs. Indeed, the sum of distances |pc'| + |c'c*| is constant equal to r* + δ, and that defines a spheroid.

B+δ(σ*)

σ′

r*+δ

d

Prδ

p

If zc ≥ 0.

We show, in that case, that σ can be shrank toward p into a smaller sphere that remains both great enough and shifted enough from the normal, either at p or at p.

The first thing to note is that, since q is outside B+δ(σ*), and since σ passes through q, then σ intersects the boundary of B+δ(σ*). Thus we can shrink σ toward p, until it is tangent to the boundary of B+δ(σ*). We call σ' this new sphere and c′ = (xc', yc′, zct) its center. This sphere passes through p, and is included in σ but does not pass through q anymore. As explained in Figure 13.2, the center of σ' lies on the prolate spheroid Prδ with focuses p and c*, and great axis r* + δ.

The projection of the intersection of B(σ') with ε is locally given by Ec' (x, y) ≤ 0 where:

$$E _ { c ^ { \prime } } ( x , y ) & = x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) z _ { c ^ { \prime } } \\ & \leq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( f _ { p } ( x , y ) ) ^ { 2 } & \text { since } - 2 f _ { p } ( x , y ) z _ { c ^ { \prime } } \leq 0 , \\ & \leq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) ) ^ { 2 } & \\ & \leq 2 x ^ { 2 } - 2 x x _ { c ^ { \prime } } + 2 y ^ { 2 } - 2 y y _ { c ^ { \prime } } & \text { for } x ^ { 2 } + y ^ { 2 } \leq \frac { 1 } { \kappa _ { \sup } ^ { 2 } } ,$$

where the equation:

$$2 x ^ { 2 } - 2 x x _ { c ^ { \prime } } + 2 y ^ { 2 } - 2 y y _ { c ^ { \prime } } \leq 0 ,$$

is the equation of a disk passing through p and centered on (xc', yc'), i.e. with radius /x2t + y2 . We show that, either this quantity is bounded from below with δ, or B(σ') ∩ε has a large enough area around p.

We consider the following two cases:

- with vertex c*, growing upward in the direction pc*, and with angle x. In that case, p is roughly above p. It actually corresponds to the case θp Consider the cylinder Cyl around (pc*) with radius . If c' is outside Cyl i, then √x2 + y2 ≥ and πp (B(σ′) ∩ ε) contains a disk of radius s0|8 according to is said above.

Conversely, if c' is inside the cylinder Cyl , then it lies on the roof top of Prδ, more precisely, inside the cone The distance |pc'| is greater than r* + ∩ Prδ, we have |pc*| ≤ r*, because of the angle of the cone. And consequently, σ' contains a sphere centered on  with radius δ that it-self contains a sphere centered on the tangent plane of Tε(p), with radius δ and whose 4, 8, intersection with the surface around p, has a projection on Tε(p) that contains a disk of radius δ 16 passing through p as long as δ ≤ 1 Ksup Note that in the figures we made, everything lies in the same plane, but it is not the case in general.


<!-- p:123 -->

Cylδ

p ∈

4

p

3

*

B+δ(σ*)

Cyl δ

4

c' ∈ Cyl δ

五

p

*

Prδ

B+δ

σ*

- We consider two cylinders Cylt and Cylt of radius t, respectively around (pc*) and (pc*). We show that we can choose t small enough such that their intersection lies inside Pr8. Recall that we named θp the angle between the tangent plane of p and the medial plane of p. By construction, the furthest point of the intersection of the two cylinders from c* is at distance t So we choose t = ¿ cos (θp), and then if σ′ is centered on Prδ, its . (dθ)so) center is either outside Cylt, or it lies above the medial plane, and then is also outside Cylt. Thus we have:
- − either c′ is outside Cylt, then the projection of B(σ) ∩ E on Tε(p) contains a disk passing
- − or c' is inside Cylt and then above the medial plane so σ' can be shrank from c' until it passes through p, while its center is still outside Cylt. Then the projection of B(σ) ∩ ε on Tε(p) contains a disk passing through p with radius

p∉C#

3

Cylt

c′∉Cylt

p

Cylt

p∉C#

π3

Cylt

c' ∈ Cylt

Cylt

B+δ

(σ*)

If zc ≤ 0.

Consider a point q ∈ ε outside B+δ(σ*) and consider a sphere passing through p and q, and centered below Tε (p). Consider the set of points on E at distance δ from p. Since δ ≤ √2 , they form a topological 2κsup circle around p on E. By convexity of ε and because zc ≤ 0, the sphere σ intersects the set of points at distance δ. So we can shrink σ toward p into σ' until all points of σ'∩ ε are inside the set of points at distance smaller than δ from p and, in particular, until they verify √x2 + y2 ≤ √2 κsup. So at least one 2 point of σ ∩ ε verifies √x2 + y2 = √2 2κsup The expression of the projection of the intersection B(σ') ∩ ε around p is given by Ec'(x, y) ≤ 0 for Ec' (x, y) = x2 − 2xxc′ + y2 − 2yyc′ + (fp(x, y))2 − 2 fp(x, y)zc′ . We search for a region that contains Ec' (x, y) ≤ 0. So we show a lower bound on Ec' (x, y), for this purpose, we introduce the absolute minimal curvature κinf of E and a lower bound on any Monge patch: fp(x, y) ≥  κinf (x2 + y2):


<!-- p:124 -->


$$E _ { c ^ { \prime } } ( x , y ) & = x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) z _ { c ^ { \prime } } \\ & \geq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } - 2 f _ { p } ( x , y ) z _ { c ^ { \prime } } \\ & \geq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } - \kappa _ { \inf } ( x ^ { 2 } + y ^ { 2 } ) z _ { c ^ { \prime } } , \, \sin c \, z _ { c ^ { \prime } } \leq 0 \\ & \geq ( 1 - \kappa _ { \inf } z _ { c ^ { \prime } } ) x ^ { 2 } - 2 x x _ { c ^ { \prime } } + ( 1 - \kappa _ { \inf } z _ { c ^ { \prime } } ) y ^ { 2 } - 2 y y _ { c ^ { \prime } } ,$$

where (1 − κinfzc')x2 − 2xxc′ + (1 − κinfzct)y2 − 2yyc′ = 0 is the expression of a circle passing through p and with radius 1−κinfzc′ x21 +y2 Since σ′ ∩ε contains a points such that √x2 + y2 = 2κsup √2 we deduce that x2, +y2, √2 2 1−κinfzc′ ≥ 2κsup

On the other hand, we compute an inner region of the intersection B(σ') ∩ε:

$$E _ { c ^ { \prime } } ( x , y ) & = x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) z _ { c ^ { \prime } } \\ & \leq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) ) ^ { 2 } - 2 \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) z _ { c ^ { \prime } } \text { since } z _ { c ^ { \prime } } \leq 0 , \\ & \leq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + x ^ { 2 } + y ^ { 2 } - 2 \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) z _ { c ^ { \prime } } \text { for } x ^ { 2 } + y ^ { 2 } \leq \frac { 1 } { \kappa _ { \sup } ^ { 2 } } \\ & = 2 ( 1 - \kappa _ { \sup } z _ { c ^ { \prime } } ) x ^ { 2 } - 2 x x _ { c ^ { \prime } } + 2 ( 1 - \kappa _ { \sup } z _ { c ^ { \prime } } ) y ^ { 2 } - 2 y y _ { c ^ { \prime } } ,$$

where

$$2 ( 1 - \kappa _ { s u p } z _ { c ^ { \prime } } ) x ^ { 2 } - 2 x x _ { c ^ { \prime } } + 2 ( 1 - \kappa _ { s u p } z _ { c ^ { \prime } } ) y ^ { 2 } - 2 y y _ { c ^ { \prime } } \leq 0 ,$$

1 √x21 +y2, is the equation of a disk passing through p and with radius 2 1−κsupze'

So if a sphere σ with zc &lt; 0 passes through a point q at distance greater than δ from σ*, it contains a sphere σ′ centered on c' and verifying x21 +y21 ≥ √2 δ , and the projection of B(σ) ∩ε contains a disk 1−κinfzc′ 4 x2, +y2 of radius 2 1−κsupzc′ 1 but:

$$1 √x21 + yc x21 + y2 1 − κinf Zc′ ≥ /x21 + y2 κinf ≥ √2 δ Kinf 2 1 − κsupZc′ 2 1 − κinfZc′ 1 − κsupZc′ 2 1 − κinfZc′ κsup 8 Kκsup$$

$$B+δ(σ*)$$

3

*2●

b

p

6

•c


<!-- p:125 -->


####### On the probability of existence of far neighbors.

We use Lemma 13.6 and adapt the proof of Lemma 9.1 from Part II, Chapter 9 to prove that a point p

has neighbors at distance from σ* greater than δ with a probability that decreases exponentially quickly with δ. Before introducing the new lemma, we consider the number γ := min √2 k inf δ, δ δ cos θp) , that is 8 κsup 0, 16, 4 a lower bound on all possible sizes of radius of the disks used in Lemma 13.6. Then we consider the isosceles triangle in Tε(p) with vertices p, (√2γ, 0) and (γ, γ), its seven copies around p such that they cover an octagon, and their symmetrical triangles on Tε(p) with respect to PMed. That makes a total of 16 triangles around p or p. We call Fγ (p) the family of fundamental regions made of their reciprocal projection on ε by π−1 for the triangles on Tε (p), and by π−1 f for the triangles on Tε(p) (see Figure 13.3). Note that the area of each region is greater than √2 2

Lemma 13.7. Let 0 ≤ δ ≤ √2 . Let X be a data sample distributed on E and, p and q in X. If q is at 2κsup Fγ (X). If X is a Poisson point process distributed on E with intensity λ, the probability that the point p ∈ X has

√2γ

is  e   t    e  e   t    : ,n Tε(p). Their reciprocal projections on ε compose the family F (p).

Proof. Let q be at distance greater than δ from σ*(p) and let σ passing through p and q. Consider the intersection r = B(σ)∩ε, and its local projections πp (r) and πp (r). By Lemma 13.6, either πp (r) contains a disk of radius γ with p on its boundary, or πp (r) contains a disk of radius γ with p on its boundary. Then we can adapt the proof of Lemma 9.1 with 2γ in place of t and the 16 regions of Fγ (p) such that one them is contained in B(σ) ∩ ε.

We deduce that:

$$\mathbb { P } \left [ \exists q \in X , ( p , q ) \in \text {Del} ( X \cup \{ p \} ) \ | \ d i s t ( q , \sigma ^ { * } ) > \delta \right ] & \leq \mathbb { P } \left [ \exists q \in X , ( p , q ) \in \text {Del} ( X \cup \{ p \} ) \ | \ d i s t ( q , \{ p , \bar { p } \} ) > \gamma \right ] \\ & \leq \mathbb { P } \left [ \exists t r \in \mathcal { F } _ { 0 } ^ { \gamma } ( p ) , t r \cap X = \emptyset \right ] \\ & \leq 1 6 e ^ { - \lambda \frac { \sqrt { 2 } } { 2 } \gamma ^ { 2 } } .$$

□

At the end of Section 13.4, we will use this lemma to quantify the probability a point q ∉ CN(p) is a neighbor of p. To use it, we need a relation between the fact that q ∉ CN(p) and the distance of q from σ*.

####### On the dimension of the intersection B+δ(σ*) ∩ ε.

It remains to know that, if q ∉ CN(p), then what is its minimal distance from σ*.


<!-- p:126 -->


Thus, we consider the slightly augmented medial sphere B+δ (σ*) and compute its intersection with ε. The equation of the projection of ε ∩ B+δ (σ*) is given by:

$$E _ { \delta } ^ { * } ( x , y ) \leq 0 ,$$

where Ex (x, y) = x2 + y2 + (fp(x, y) − r*)2 − (r* + δ)2. We bound from below the expression Ex (x, y) to obtain an including neighborhood:

$$E _ { \delta } ^ { * } ( x , y ) & = x ^ { 2 } + y ^ { 2 } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 r ^ { * } f _ { p } ( x , y ) + r ^ { * 2 } - r ^ { * 2 } - 2 r ^ { * } \delta - \delta ^ { 2 } \\ & \geq x ^ { 2 } + y ^ { 2 } - 2 r ^ { * } f _ { p } ( x , y ) - 3 \delta r ^ { * } \text { since } ( f _ { p } ( x , y ) ) ^ { 2 } \geq 0 \text { and } \delta \leq r ^ { * }$$

we use the form fp(x, y) = 2κ1x2 + 2κ2y2 + 1 −m3,0x3 + R3+(x, y):

$$E _ { \delta } ^ { * } ( x , y ) & \geq x ^ { 2 } + y ^ { 2 } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 r ^ { * } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \frac { 1 } { 6 } m _ { 3 , 0 } x ^ { 3 } + R _ { 3 + } ( x , y ) \right ) - 3 \delta r ^ { * } \\ & = ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - \frac { 1 } { 3 } r ^ { * } m _ { 3 , 0 } x ^ { 3 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 r ^ { * } R _ { 3 + } ( x , y ) - 3 \delta r ^ { * }$$

|x| 1−κ1r* r*m3,0

$$E _ { \delta } ^ { * } ( x , y ) \geq \frac { 2 } { 3 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 2 } { 3 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } + - 2 r ^ { * } R _ { 3 + } ( x , y ) - 3 \delta r ^ { * }$$

and, since |R3+(x, y)| ≤ (x2 + y2) (M3|y| + M4x2), we can say that for |y| ≤ 1−κ1r* and x2 ≤ 21−M , −|2r*R3+(x, y)| ≥ −3(1 − κ1r*)x2 − 3(1 − k2r*)y2, and so: 24 12r*M3 r* M4 ,

$$E _ { \delta } ^ { * } ( x , y ) \geq \frac { 1 } { 3 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 3 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 3 \delta r ^ { * } .$$

But we can recognize, in 1(1 − κ1r*)x2 + 1(1 − κ2r*)y2 − 3δr* = 0, the equation of the axis-aligned ellipse with aspect ratio √ 1−κ2r* 1−κ1r* and great axis 6√ √1−κ1r* δr* (and then small axis: 61 1−κ2r* δr* ). To be able to consider the full ellipse we need to take δ small 'enough so that it fits inside the rectangle:

$$\left \{ | x | \leq \min \left ( \frac { \sqrt { 2 } } { 2 \kappa _ { s u p } } , \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } m _ { 3 , 0 } } , \sqrt { 2 \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } M _ { 4 } } } \right ) , | y | \leq \min \left ( \frac { \sqrt { 2 } } { 2 \kappa _ { s u p } } , \frac { 1 - \kappa _ { 1 } r ^ { * } } { 1 2 r ^ { * } M _ { 3 } } \right ) \right \} ,$$

that is inside all neighborhoods used above. What is important to note here, is that the rectangle and the ellipse have the same aspect ratio when p approaches Z, namely Ω(√1 – κ1r*) as we will show in Section 13.4.7. Consequently, for any δ small enough, ε ∩ B+δ (σ*) is inside CN(p). In other words, we can say that if q ∉ CN(p), then we can find a δ such that q is not in the ellipse:

$$\frac { 1 } { 3 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 3 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } \leq 3 \delta r ^ { * } ,$$

proving that q is at distance greater than δ from σ*.

#### 13.4 Expected number of close neighbors (Proof of Lemma 13.1)

In this section, we give an upper bound on the expected number of Delaunay neighbors of p that lie in CN(p). We study the intersection of ε with specific spheres passing through p and a second point q on E. These intersections can have various shapes that depends obviously on the center of the spheres but also on p and more specifically on its principal curvatures κ1 and κ2, and its medial radius r*. We briefly recall that, in this section, we use the Monge coordinates system of p, in which the x and y axis lie in the tangent plane of E at p, and the normal is oriented inward E.


<!-- p:127 -->


##### 13.4.1 General scheme

To compute an upper bound on the expected degree of p, we consider an empty region graph that is a super-graph of the Delaunay triangulation restricted to points close enough to p. For each pair (p, q) with q ∈ CN(p), we denote by F1(p, q) the set of associated fundamental regions. In Section 13.4.2, we define those regions, in Section 13.4.3, we identify which spheres are sufficient to apply the Combination lemma, in Section 13.4.4, we spell out the partition of the bisector plane of p and q that allows us to prove that bound on the expected degree (Lemma 13.1). Finally, in Section 13.4.8, we complete Section 13.4.6 to give an upper bound on the probability of existence of neighbors of p that are not close to p, proving (Lemma 13.2).

In order to use the Partition lemma to prove that the Delaunay triangulation is indeed a sub-graph of the empty region graph associated to F1, we have to define F1, a finite subset of intersections of ε with spheres passing through p and q. By analogy, in 2D we used the Gabriel sphere and the two half-planes to define the half-moons, here the situation is a bit more complicated so when we will have defined the specific spheres, the regions of F1 will be conservative approximations of the intersection of these spheres with E.

More precisely, the ball B(σc) inside a sphere σc of center c = (xc, yc, zc) passing through p = (0, 0, 0) has equation:

$$x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } + z ^ { 2 } - 2 z z _ { c } \leq 0 ,$$

and, in a neighborhood of p, ε is the graph of a function fp(x, y). Then it is convenient to work in the tangent plane Tε(p) where the projection of the intersection B(σc) ∩ε has equation

$$E _ { c } ( x , y ) = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } + f _ { p } ^ { 2 } ( x , y ) - 2 f _ { p } ( x , y ) z _ { c } \leq 0 .$$

Using a Taylor expansion of fp(x, y):

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + O ( x ^ { 3 } + y ^ { 3 } ) ,$$

it is possible to rewrite Ec and split it in three terms, one linear in x, y, one quadratic in x, y and a rest of higher degree. The linear and quadratic terms give the equation of an ellipse approximating πp (B(σ) ∩ ε) but without any certainty of inclusion. So the rough idea is to identify a neighborhood in which we can bound the remaining higher degree term by a fraction of the quadratic term to obtain an expression greater than Ec that defines a smaller ellipse, tangent in p that is certainly inside πp (B(σc) ∩ε).

##### 13.4.2 Description of the regions of F1 on the spheroid

Before giving clearly the regions of F1, we show a rough approximation of the behavior of the intersection of a sphere passing through p and the surface ε. If we substitute fp in Ec(x, y) and gather the quadratic terms, we obtain:

$$E _ { c } ( x , y ) = ( 1 - \kappa _ { 1 } z _ { c } ) x ^ { 2 } - 2 x x _ { c } + ( 1 - \kappa _ { 2 } z _ { c } ) y ^ { 2 } - 2 y y _ { c } + O ( x ^ { 3 } + y ^ { 3 } ) .$$

The equation Ec(x, y) ≤ 0 describes a region that approaches an axis-aligned ellipse with aspect ratio 1−κ1ze and center xc yc 1−κ2zc 1−κ1zc,1−κ2zc

We deduce some specific regions on Tε(p) or Tε(p)

- If zc goes to −∞, the projection πp(rc) of rc = B(σc) ∩ ε resembles to an ellipse axis-aligned with aspect ratio β-∞ = √ /k1. Conversely if zc goes to +∞, πp(rc) will approximate the complementary κ2 of the above mentioned ellipse.
- If zc is close to 0, πp(rc) resembles to a disk.


<!-- p:128 -->


- If c is on PMed, then the sphere passes also through p and has one connected component close to p and one close to p. If in addition (xc, yc) is close to (0, 0) then zc must be close to r*, and πp(rc) will resemble to an axis aligned ellipses with aspect ratio βr* = 1-κ1r* passing through p, while 1−κ2r* πp(rc) will be the symmetrical region of πp(rc) with respect to PMed.
- If zc is finite but xc or yc are not, that means that the sphere degenerates into a plane orthogonal to the tangent plane Tε(p) and that the boundary of πp(rc) is the line (pq).

####### Regions included in the projection of the intersection of E with a sphere.

We consider now a point q ∈ ε close enough to p, in the sense that q ∈ CN(p) and closer from p than from p. We recall CN(p) will be precisely described in the next section. Assume that σc passes also through q. We need to have a quantification of the area of B(σc) ∩ E according to the position of q with respect to p. More precisely we obtain a lower bound on the area of those regions by showing that their projection on Tε(p) or Tε(p) contains a specific ellipse.

We list here those specific ellipses with respect to p and q, and other regions that will be used as inner regions. The regions that are projections on Tε(p) are denoted with bar above them.

- ellα(p, q) is the axis-aligned ellipse on Tε(p) passing through p and p+πp(q) centered on p+πp(q) 2 4 and with aspect ratio α &gt; 0. It is parameterized by the equation:

$$\text {ell} ^ { \alpha } ( p , q ) \colon 2 a ^ { 2 } x ^ { 2 } - a ^ { 2 } x x _ { q } + 2 b ^ { 2 } y ^ { 2 } - b ^ { 2 } y y _ { q } \leq 0 , \text {with } \left | \frac { a } { b } \right | = \alpha .$$

As examples, below are the ellipses ell‡ (p, q), ell1 (p, q) and ell2(p, q):

π(q)


ell (p, q)

ell1(p, q)

ell2(p, q)

p


- ellα(p, q) is the axis-aligned ellipse on Tε(p) passing through p and p+πp(q) centered on p+πp( ̄) 2 4 and with aspect ratio α. It is the symmetrical ellipse of ellα(p, q) with respect to PMed. On the figure below are illustrated ell (p, q) and ell (p, q), each on their plane separated by PMed, in red.
- rhα (p, q) is the rhombus whose vertices are x and y extreme points of ell1 (p, q) ∩ ellα (p, q). Using p+π(q) 2

π(ā)

π(q)

ell (p, q)


p


To give an upper bound on the size of the 2D-Delaunay triangulation, we cut the Gabriel disk of two points into two half-moons that have the property to be included in any disk with p and q on its boundary. We mimic this splitting and consider the following half-regions:

- The line (p, πp(q)) separates Tε(p) into two half-planes: HPe(p, q) that contains πp(p), and HPr(p, q). They are denoted with l and r for left and right because we assumed that up &gt; 0 in the global


<!-- p:129 -->


frame, and thus, πp(p) is on the left. Note that left and right are not related with a side of pπp(q), unlike in the 2-dimensional cases that we saw in Part II.

We consider the halves of ellα (p, q) and rhα (p, q):

- − ell (p, q) = ellα (p, q) ∩ HPe(p, q) and ellα (p, q) = ellα (p, q) ∩ HPr(p, q),
- − rhx (p, q) = rhα (p, q) ∩ HPe(p, q) and rhα (p, q) = rhα (p, q) ∩ HPr (p, q).
- We also consider the same separations for ellα (p, q) where ell% (p, q) is the symmetrical of ell% (p, q) with respect to PMed and ell% (p, q) is the symmetrical of ellα (p, q).

At some point we will need to consider the degenerate ball whose boundary is the plane passing through p, q, p, and consequently  ̄, and that verifies zc &gt; 0 in the Monge coordinates system of p. We its projection on Tε(p) is ñot convex. In order to apply the Combination lemma, we will need to consider

- rhr (p, q) is defned as πp(r+∞) ∩rh (p, q). We will show that the part of rh (p, q) cut by πp(r+∞) is actually negligible.
- Finally we consider ellr(p,q) defined as πp(rs) ∩ell(p, ).

For u ∈ E, we denote by π−1 the reciprocal function of the projection πu in a neighborhood of u on ε. Then we consider the family F1(p, q) of regions on ε:

$$\mathcal { F } _ { 1 } ( p , q ) = \left \{ \begin{array} { c } \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r } * } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } ( p , q ) \right ) , \\ \pi _ { \overline { p } } ^ { - 1 } \left ( \text {ell} _ { \ell } ^ { \beta _ { r } * } ( p , q ) \right ) , \pi _ { \overline { p } } ^ { - 1 } \left ( \overline { \tilde { \ell } } h _ { r } ^ { \beta _ { r } * } ( p , q ) \right ) \end{array} \right \} .$$

is a super graph of the Delaunay triangulation for pairs (p, q) close enough, and to compute the expected degree of a point p in this graph. When q is close to p, we will use an argument to show that a sphere passing through p and q contains a region of F1(p, ī) or F1(p, q). This closeness relation between p and q will be expressed by q ∈ CN(p) where CN(p) denotes a neighborhood on ε around p or p. This neighborhood will be constructed all along the proof.

##### 13.4.3 Choice of specific spheres for q on the side of p with respect to PMed

We have to prove, using Combination lemma that any sphere passing through p and q contains at Partition Lemma. In order to apply those lemmas, we choose specific spheres whose centers will guide the partitioning of the bisector plane PBis of p and q.

Some of the centers we consider are finite, and their sphere are usual sphere, but some others have to be seen as directions at infinity, and their sphere are actually half-space whose boundary is the plane passing through p and q and that is orthogonal to the direction of the center. A finite center can be defined as intersection of three planes, one of them being obviously PBis. Among the two others, one is chosen to determine the value of zc, while the other is chosen to determine the direction of tangency of the intersection at p. That last plane will be determined by its equation in the Monge coordinates system . An infinite center can be seen as one of the two infinite extremities of the intersection of PBis and a second plane that is not parallel. Since all centers are at least in PBis, reference is only made to the other plane(s).

We list below the spheres and, through a claim, show up the fundamental region on E that is inside. A sphere σ, its center c, and its intersection r with ε are denoted with the same indices and exponents if there are any. We consider eight specific spheres (or half-space), and their associated claims. Most of the claims are proved following the same scheme: we compute the exact coordinate of the center of the sphere, and we substitute the coordinates in the inequality. The exact coordinates usually have a complicated coefficient named Cq that we put in factor of the equation. We bound by below this coefficient. Then we bound the remaining terms by the quadratic terms.


<!-- p:130 -->


####### Sphere σLow·

The center cLow is in the tangent plane Tε(p) whose equation is z = 0, and in the vertical plane PLow with equation yxq − xyq = 0. The equation of the second plane guarantees that the projection of the intersection region πp (rLow) = B(στ) ∩ ε is tangent with ell1(p, q). The more q is close to p, the closer is the sphere σLow to the Gabriel sphere of p and q.

The surface E and two points p and q, and the tangent plane Tε(p) at p in yellow.

Tε(p)

The sphere σLow centered at cLow and passing through p and q.

σLow

The 3 three planes whose intersection is cLow: Tε(p), PBis in blue, and PLow : xyq − yxq = 0 in green.

PLow

πp(q)

Tε(p)

The projection of the intersection in green, and ell1 in blue.

πp(q)

ell1

π(rLow)

Tε(p)

p

We consider the neighborhood VLow(p) = {max (|x|, |y|) ≤ 2 κsup }, and the following claim:

Claim a. If q ∈ π−1 (VLow(p)), then πp (rLow) contains ell (p, q).

Proof. The center cLow of the sphere σLow is at the intersection of the three following planes:

- The bisector plane of p and q, with equation:

$$0 = ( \frac { x _ { q } } { 2 } - x ) x _ { q } + ( \frac { y _ { q } } { 2 } - y ) y _ { q } + ( \frac { z _ { q } } { 2 } - z ) z _ { q } .$$

- The plane tangent to E at p, with equation:


<!-- p:131 -->


- The plane with equation:

0 = xyq − yxq.

The center cLow = (xc, yc, zc) verifies then zc = 0 and yc = yq xc. We compute xc using the equation xq of the bisector plane:

$$0 & = ( \frac { x _ { q } } { 2 } - x _ { c } ) x _ { q } + ( \frac { y _ { q } } { 2 } - y _ { c } ) y _ { q } + ( \frac { z _ { q } } { 2 } - z _ { c } ) z _ { q } \\ & = \frac { x _ { q } ^ { 2 } } { 2 } - x _ { c } x _ { q } + \frac { y _ { q } ^ { 2 } } { 2 } - \frac { y _ { q } ^ { 2 } } { x _ { q } } x _ { c } + \frac { z _ { q } ^ { 2 } } { 2 } ,$$

$$x _ { c } & = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } \frac { x _ { q } } { 2 } \\ & = \left ( 1 + \frac { z _ { q } ^ { 2 } } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } \right ) \frac { x _ { q } } { 2 } ,$$

$$y _ { c } = \left ( 1 + \frac { z _ { q } ^ { 2 } } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } \right ) \frac { y _ { q } } { 2 } .$$

We consider the points (x, y, z) of ε close enough to p to be parameterized by (x, y, fp(x, y)), i.e. at a distance smaller than √2 from p. πp(rLow) can then be described by the inequality Eτ(x, y) ≤ 0 2κsup obtained by substituting fp(x, y) to z in the equation of σLow:

$$E _ { L o w } ( x , y ) & = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) z _ { c } \\ & = x ^ { 2 } - x \left ( 1 + \frac { z _ { q } ^ { 2 } } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } \right ) x _ { q } + y ^ { 2 } - y \left ( 1 + \frac { z _ { q } ^ { 2 } } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } \right ) y _ { q } + ( f _ { p } ( x , y ) ) ^ { 2 } \, ,$$

since zc = 0.

We note Cq = 1 + and rewrite ELow(x, y): +y2 q

$$E _ { L o w } ( x , y ) = C _ { q } \left ( \frac { 1 } { C _ { q } } x ^ { 2 } - x x _ { q } + \frac { 1 } { C _ { q } } y ^ { 2 } - y y _ { q } + \frac { 1 } { C _ { q } } \left ( f _ { p } ( x , y ) \right ) ^ { 2 } \right ) .$$

Since 0 &lt; 1 ≤ Cq, it is clear that:

$$E _ { L o w } ( x , y ) \leq C _ { q } \left ( x ^ { 2 } - x x _ { q } + y ^ { 2 } - y y _ { q } + ( f _ { p } ( x , y ) ) ^ { 2 } \right ) .$$

As seen in Section 1.2.2, for x2 + y2 ≤ 1 we have |fp(x, y)| ≤ κsup(x2 + y2) and then we can bound the remaining term (fp(x, y))2 this way:

$$( f _ { p } ( x , y ) ) ^ { 2 } & \leq \kappa _ { \sup } ^ { 2 } ( x ^ { 2 } + y ^ { 2 } ) ^ { 2 } \\ & \leq x ^ { 2 } + y ^ { 2 } .$$

$$E _ { L o w } ( x , y ) \leq C _ { q } \left ( 2 x ^ { 2 } - x x _ { q } + 2 y ^ { 2 } - y y _ { q } \right ) ,$$

pre d   ip  o    0  ( − z + xx − x  0 &lt; b s n centered on p+πp(q) 4

This proves that the projection of rLow on Tε(p) contains ell1(p, q) for points that verify √x2 + y2 V 1 , but if πp(q) ∈ VLow(p), it is the case of all points of ell1 (p, q) and thus π (rLow) contains ell1 (p, q). Ksup

and then:

and:

and finally we have:


<!-- p:132 -->


####### Sphere σMed·

We named this sphere σMed since it tends to the medial sphere of p when q goes to p. The center cMed is in the plane PMed and the plane Pβr* with equation y(1 − κ1r*)xq − x(1 − κ2r*)yq = 0. The center cMed = (xc, yc, zc) verifies that zc is close to r* when q is close to p. Since cMed belongs to the plane PMed, the intersection is symmetrical with respect to PMed. Moreover, since cMed also belongs to Pβ* , the projection of the intersection region rMed = B(σMed) ∩ε is tangent with ellβr* (p, q) at p.

Two parts of E around p and p, and their medial plane PMed in red.

PMed

q

Tε(p)

The sphere σMed centered at cMed and passing through p and q.

σMed

Tε(p)

The 3 three planes whose intersection is cMed, Pβr* : (1 − κ1r*)xyq − (1 − κ2r*)yxq = 0 in green, PBis in blue, and PMed.

Pβ,

PBis

PMed

CMed

Tε(p)

The projection on Tε(p) of the intersection in green, and the ellipse eliβ* that is included inside, in blue.

πp(q)

ellβr*

π(rMed)

Tε(p)

p

The computations to find inner regions are quite tedious. To simplify the computations, we give here a lemma that can be seen as a pre-computation for the spheres centered on PMed. The lemma provides an upper bound on the expression of projection of the intersection. In the provided upper bound, one will notice that we let a remaining term, this is because this term depends on xc, whose behavior varies with q, and we might wait to consider the bisector plane of p and q to bound it, that is not the case in Lemma 13.8.

We recall the Monge form of the surface at p, with the remainder R3+(x, y), from Equation 1.6:

$$f _ { p } ( x , y ) = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \frac { 1 } { 6 } m _ { 3 , 0 } x ^ { 3 } + R _ { 3 + } ( x , y ) ,$$

$$| R _ { 3 + } ( x , y ) | \leq \left ( x ^ { 2 } + y ^ { 2 } \right ) \left ( M _ { 3 } | y | + \frac { 1 } { 2 4 } M _ { 4 } x ^ { 2 } \right ) .$$

Lemma 13.8. Let p be a point on E and z = fp(x, y) be the Monge form of E at p. Let σ be a sphere passing through p and centered on a point c = (xc, Yc, zc) in the medial axis PMed of E. Let Ec(x, y) ≤ 0 be an expression of the projection of B(σ) ∩ε on the tangent plane Tε(p), and VMed(p) be the rectangle

with around p in Tε(p):


<!-- p:133 -->


$$\left \{ | x | \leq \min \left ( \frac { 1 } { 2 ^ { \kappa _ { \sup } } } , \sqrt { 2 } \frac { \sqrt { 1 - \kappa _ { r } r ^ { * } } } { 8 \kappa _ { \sup } } , \frac { \sqrt { 6 } } { 4 } \sqrt { 2 \frac { 1 - \kappa _ { r } r ^ { * } } { M _ { 4 } r ^ { * } } } , 3 \frac { 1 - \kappa _ { r } r ^ { * } } { 1 6 | m _ { 3 , 0 } | r ^ { * } } \right ) , | y | \leq \min \left ( \frac { 1 } { 2 \kappa _ { \sup } } , \sqrt { 2 } \frac { \sqrt { 1 - \kappa _ { r } r ^ { * } } } { 8 \kappa _ { \sup } } , \frac { 1 - \kappa _ { r } r ^ { * } } { 3 2 M _ { 3 } r ^ { * } } \right ) \right \} .$$

If (x, y) ∈ VMed(p) then

$$E _ { c } ( x , y ) \leq \frac { 5 } { 4 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - 2 x x _ { c } + \frac { 5 } { 4 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 y y _ { c } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) .$$

Proof. An equation of the ball B(σ) is:

$$x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - y y _ { c } + z ^ { 2 } - z z _ { c } \leq 0 .$$

By substituting z by fp(x, y) for points (x, y) such that √x2 + y2 ≤ √2 , we obtain an expression of 2κsup the projection of the intersection B(σ) ∩ ε given by Ec(x, y) ≤ 0 where:

$$E _ { c } ( x , y ) = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - y y _ { c } + ( f _ { p } ( x , y ) ) ^ { 2 } - f _ { p } ( x , y ) z _ { c } .$$

Then we substitute zc by r* + xc tan(θp) since c ∈ PMed, and fp(x, y) by 2κ1x2 + 2k2y2 + −m3,0x3 + R3+(x, y), but only in the term −2fp(x, y)r*:

$$R _ { 3 + } ( x , y ) , & \text { but only in the term } - 2 f _ { p } ( x , y ) r ^ { * } \intertext { R _ { 3 + } ( x , y ) , } E _ { c } ( x , y ) & = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) \left ( r ^ { * } + x _ { c } \tan ( \theta _ { p } ) \right ) \\ & = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) r ^ { * } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) \\ & = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - 2 y y _ { c } - 2 \left ( \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \frac { 1 } { 6 } m _ { 3 , 0 } x ^ { 3 } + R _ { 3 + } ( x , y ) \right ) r ^ { * } \\ & \quad + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) \\ & = ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - \frac { 1 } { 3 } r ^ { * } m _ { 3 , 0 } x ^ { 3 } - 2 x x _ { c } + ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 y y _ { c } - 2 r ^ { * } R _ { 3 + } ( x , y ) \\ & \quad + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) \\ & \leq ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 3 } r ^ { * } | m _ { 3 , 0 } | | x | ^ { 3 } - 2 x x _ { c } + ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 y y _ { c } + 2 r ^ { * } | R _ { 3 + } ( x , y ) | \\ & \quad + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) . \\ \intertext { W e b o u d f o r a b i v e the t e r m } & \text { } \frac { 1 } { 3 } r ^ { * } | m _ { 3 , 0 } | | x | ^ { 3 } + 2 r ^ { * } | R _ { 3 + } ( x , y ) | + ( f _ { p } ( x , y ) ) ^ { 2 } \text { using the bounds on } f _ { p } ( x , y )$$

We bound from above the term and R3+(x, y) for √x2 + y2 ≤ √2 see Section 1.2.2: 2κsup

$$| R _ { 3 + } ( x , y ) | \leq \left ( M _ { 3 } | y | + \frac { 1 } { 2 4 } M _ { 4 } x ^ { 2 } \right ) \left ( x ^ { 2 } + y ^ { 2 } \right ) \text { and } | f _ { p } ( x , y ) | \leq \kappa _ { s u p } ( x ^ { 2 } + y ^ { 2 } ) .$$

For |y| ≤ 1−κ1r* , and x2 ≤ 31−κ1r* 32M3r* 4−M4r*

$$^ { 2 } 3 M _ { 3 } r ^ { * } & \, / \, \int 4 \, M _ { 4 } r ^ { * } \\ & \, 2 r ^ { * } | R _ { 3 + } ( x , y ) | \leq 2 r ^ { * } \left ( M _ { 3 } \frac { 1 - \kappa _ { 1 } r ^ { * } } { 3 2 M _ { 3 } r ^ { * } } + \frac { 1 } { 2 4 } M _ { 4 } \frac { 3 } { 4 } \frac { 1 - \kappa _ { 1 } r ^ { * } } { M _ { 4 } r ^ { * } } \right ) ( x ^ { 2 } + y ^ { 2 } ) \\ & = 2 r ^ { * } \left ( \frac { 1 - \kappa _ { 1 } r ^ { * } } { 3 2 r ^ { * } } + \frac { 1 - \kappa _ { 1 } r ^ { * } } { 3 2 r ^ { * } } \right ) ( x ^ { 2 } + y ^ { 2 } ) \\ & = \frac { 1 } { 8 } ( 1 - \kappa _ { 1 } r ^ { * } ) ( x ^ { 2 } + y ^ { 2 } ) \\ & \leq \frac { 1 } { 8 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 8 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } ,$$

since κ1 ≥ κ2. For x2 + y2 ≤ 1−κ1r*

$$( f _ { p } ( x , y ) ) ^ { 2 } & \leq \left ( \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) \right ) ^ { 2 } \\ & \leq \frac { 1 } { 1 6 } ( 1 - \kappa _ { 1 } r ^ { * } ) ( x ^ { 2 } + y ^ { 2 } ) \\ & \leq \frac { 1 } { 1 6 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 1 6 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } .$$


<!-- p:134 -->


And for |x| ≤ 3 1−κ1r* 16|m3,0|r* :

$$\frac { 1 } { 3 } r ^ { * } m _ { 3 , 0 } | x | ^ { 3 } & \leq \frac { 1 } { 3 } r ^ { * } | m _ { 3 , 0 } | \frac { 3 ( 1 - \kappa _ { 1 } r ^ { * } ) } { 1 6 m _ { 3 , 0 } r ^ { * } } x ^ { 2 } \\ & \leq \frac { 1 } { 1 6 } ( 1 - \kappa _ { 1 } r ^ { * } ) ( x ^ { 2 } + y ^ { 2 } ) \\ & \leq \frac { 1 } { 1 6 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 1 6 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } .$$

It follows that, if x and y verify the above bounds, then:

$$\frac { 1 } { 3 } r ^ { * } m _ { 3 , 0 } | x | ^ { 3 } + 2 r ^ { * } | R _ { 3 + } ( x , y ) | + ( f _ { p } ( x , y ) ) ^ { 2 } \leq \frac { 1 } { 4 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 4 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } .$$

Note that, for any positive a, the condition, |x| &lt; √2 a and |y| &lt; √2 a implies x2 + y2 ≤ a2, so that 2 2 we can deduce that, in the rectangle VMed(p) defined by:

$$\left \{ | x | \leq \min \left ( \frac { 1 } { 2 \kappa _ { \varepsilon _ { u p } } } , \sqrt { 2 } \frac { \sqrt { 1 - \kappa _ { 1 } r ^ { * } } } { 8 \kappa _ { s u p } } , \frac { \sqrt { 6 } } { 4 } \sqrt { 2 \frac { 1 - \kappa _ { 1 } r ^ { * } } { M _ { 4 } r ^ { * } } } , 3 \frac { 1 - \kappa _ { 1 } r ^ { * } } { 1 6 r ^ { * } | m _ { 3 , 0 } | } \right ) , | y | \leq \min \left ( \frac { 1 } { 2 \kappa _ { s u p } } , \sqrt { 2 } \frac { \sqrt { 2 - \kappa _ { 1 } r ^ { * } } } { 8 \kappa _ { s u p } } , \frac { 1 - \kappa _ { 1 } r ^ { * } } { 3 2 M _ { 3 } r ^ { * } } \right ) \right \} ,$$

we have:

$$E _ { c } ( x , y ) \leq \frac { 5 } { 4 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - 2 x x _ { c } + \frac { 5 } { 4 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 y y _ { c } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) .$$

□

The important point here is that, as long as p is far enough from Z (by a constant distance), the rectangle VMed(p) has a size Ω(1) × Ω(1), but when p approaches Z, its size goes to 0.

We use directly this lemma for the proof of the following claim. In this claim, we consider the neighborhood VMed(p) around p in Ts(p), in which πp(q) needs to be, for our equations to be valid:

$$V _ { M e d } ^ { \prime \prime } ( p ) = \left \{ | x _ { q } | \leq \min \left ( \frac { \sqrt { 2 } } { 2 \kappa _ { \omega u p } } , \frac { 3 } { 1 4 } \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } | m _ { 3 , 0 } | } , \sqrt { \frac { 6 } { 7 } } \sqrt { \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } M _ { 4 } } } , \frac { 1 } { 7 } \frac { 1 } { \kappa _ { \sup } \tan \theta _ { p } } \right ) , | y _ { q } | \leq \min \left ( \frac { \sqrt { 2 } } { 2 \kappa _ { \omega u p } } , \frac { 1 } { 2 8 } \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } M _ { 3 } } \right ) \right \} .$$

And we define VMed(p) as the greatest axis-aligned ellise in VMed(p) ∩ VMed(p) that is centered on p and has aspect ratio βr* .

Claim b. If q ∈ π−1 (VMed(p)), then πp(rMed) contains ellβr* (p, q) and πp(rMed) contains elβr* (p, q).

Proof. We consider the points (x, y, z) of ε close enough to p to be parameterized by (x, y, fp(x, y)), i.e. at a distance smaller than √2 from p. Since cMed ∈ PMed, by Lemma 13.8, πp(rMed) can then be 2ksup described by the inequality EMed(x, y) ≤ 0 where:

$$E _ { M e d } ( x , y ) \leq \frac { 5 } { 4 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - 2 x x _ { c } + \frac { 5 } { 4 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 y y _ { c } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) ,$$

for points (x, y) ∈ VMed(p).

Then we compute the coordinates of cMed. Since it belongs to PMed and to the plane Pβ* whose equation is:

$$0 = ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } x - ( 1 - \kappa _ { 1 } r ^ { * } ) y ,$$

we have zc = r* + xc tan(θp) and yc = 1−κ2r* yq xc. 1−κ1r* xq

We compute xc using the equation of the bisector plane:

$$\text {we compute } x _ { c } \text { using the equation of the bisector plane} \colon \\ 0 & = ( \frac { x _ { q } } { 2 } - x _ { c } ) x _ { q } + ( \frac { y _ { q } } { 2 } - y _ { c } ) y _ { q } + ( \frac { z _ { q } } { 2 } - z _ { c } ) z _ { q } \\ & = \frac { x _ { q } ^ { 2 } } { 2 } - x _ { c } x _ { q } + \frac { y _ { q } ^ { 2 } } { 2 } - \frac { ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } } { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } } x _ { c } + \frac { z _ { q } ^ { 2 } } { 2 } - ( r ^ { * } + x _ { c } \tan ( \theta _ { p } ) ) \, z _ { q } ,$$

then we factorize the terms with xc:

$$x _ { c } \left ( x _ { q } + \frac { ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } } { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } } + \tan ( \theta _ { p } ) z _ { q } \right ) = \frac { 1 } { 2 } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } \right ) .$$


<!-- p:135 -->


and finally we isolate xc to obtain,

$$x _ { c } & = \frac { 1 } { 2 } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } \right ) \frac { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } } { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } ^ { 2 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } + ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } \tan ( \theta _ { p } ) z _ { q } } \\ & = ( 1 - \kappa _ { 1 } r ^ { * } ) \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } ^ { 2 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } + ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } \tan ( \theta _ { p } ) z _ { q } } \frac { x _ { q } } { 2 } , \\$$

we note Cq the central factor so that:

$$q \\ x _ { c } = ( 1 - \kappa _ { 1 } r ^ { * } ) C _ { q } \frac { x _ { q } } { 2 } , \\ y _ { c } = ( 1 - \kappa _ { 2 } r ^ { * } ) C _ { q } \frac { y _ { q } } { 2 } \text { and,} \\ z _ { c } = r ^ { * } + ( 1 - \kappa _ { 1 } r ^ { * } ) C _ { q } \tan ( \theta _ { p } ) \frac { x _ { q } } { 2 } .$$

By substituting the expressions of the coordinates in the upper bound of EMed(x, y) we have:

$$By substituting the expressions of the coordinates in the upper bound of E _ { M e d } ( x , y ) \, we \, have \colon \\ E _ { M e d } ( x , y ) & \leq \frac { 5 } { 4 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - 2 x x _ { c } + \frac { 5 } { 4 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - 2 y y _ { c } - 2 f _ { p } ( x , y ) x _ { c } \tan ( \theta _ { p } ) \\ & = \frac { 5 } { 4 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - ( 1 - \kappa _ { 1 } r ^ { * } ) C _ { q } x x _ { q } + \frac { 5 } { 4 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - ( 1 - \kappa _ { 2 } r ^ { * } ) C _ { q } y y _ { q } \\ & - f _ { p } ( x , y ) ( 1 - \kappa _ { 1 } r ^ { * } ) C _ { q } \tan ( \theta _ { p } ) x _ { q } \\ & = C _ { q } \left ( \frac { 5 } { 4 C _ { q } } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } - ( 1 - \kappa _ { 1 } r ^ { * } ) x x _ { q } + \frac { 5 } { 4 C _ { q } } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } - ( 1 - \kappa _ { 2 } r ^ { * } ) y y _ { q } \\ & - f _ { p } ( x , y ) ( 1 - \kappa _ { 1 } r ^ { * } ) \tan ( \theta _ { p } ) x _ { q } \right ) \\ \\ \intertext { To lighton the expressions that becomo quite long, we choose the following notations: K _ { \cdot } = 1 - \kappa _ { r ^ { * } } }$$

To lighten the expressions that become quite long, we choose the following notations: K1 := 1 − κ1r*, K2 := 1 − κ2r*, and T := tan(θp).

And so we rewrite:

$$E _ { M e d } ( x , y ) \leq C _ { q } \left ( \frac { 5 } { 4 C _ { q } } K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + \frac { 5 } { 4 C _ { q } } K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } - f _ { p } ( x , y ) K _ { 1 } T x _ { q } \right )$$

At this stage, we need to study the behavior of Cq when q approaches p. A lower bound is enough.

$$At this stage, we need to study the behavior of C _ { q } \, when \, q \, \text {approaches} \, p . \ A \, \text {lower bound is enough.} \\ C _ { q } = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } x _ { q } T z _ { q } } \\ = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 r ^ { * } f _ { p } ( x _ { q } , y _ { q } ) } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } x _ { q } T f _ { p } ( x _ { q } , y _ { q } ) } \, b \text { substituting} \, z _ { q } \, by \, f _ { p } ( x _ { q } , y _ { q } ) , \\ = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } - 2 r ^ { * } f _ { p } ( x _ { q } , y _ { q } ) } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } x _ { q } T f _ { p } ( x _ { q } , y _ { q } ) } \, \sinc \, ( f _ { p } ( x , y ) ) ^ { 2 } \, \text {is positive and negative} \\ = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } - 2 r ^ { * } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } \gamma y _ { q } ^ { 2 } + \frac { r _ { 1 } m _ { 3 , 0 } x ^ { 3 } + R _ { 3 + } ( x _ { q } , y _ { q } ) } { 6 } } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } x _ { q } T f _ { p } ( x _ { q } , y _ { q } ) } \\ ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } ^ { 2 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } - \frac { 1 } { r ^ { * } m _ { 3 , 0 } x _ { q } ^ { 3 } - 2 r ^ { * } R _ { 3 + } ( x _ { q } , y _ { q } ) } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } x _ { q } T f _ { p } ( x _ { q } , y _ { q } ) } \\ \geq \frac { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } - \frac { 1 } { 3 } r ^ { * } | m _ { 3 , 0 } x _ { q } ^ { 3 } | - 2 r ^ { * } | R _ { 3 + } ( x _ { q } , y _ { q } ) | } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } | x _ { q } | T f _ { p } ( x _ { q } , y _ { q } ) } . \\ \text {We recall that } | R _ { 3 + } ( x _ { q } , y _ { q } ) | \leq \left ( M _ { 3 } | y _ { q } | + \frac { 1 } { 2 4 } M _ { 4 } x _ { q } ^ { 2 } \right ) ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) , \, S O \\$$

We recall that |R3+(xq, yq)| ≤ (M3|yq| + M4x2) + y2), so 24

- for |xq| ≤ 14 r*[m3,0], 3 K1 ≤ 14 K1x2 q V 14 (K1x2 + K2y2), and


<!-- p:136 -->


- for |yq| ≤ 1 K1 V 6 K1 2r*|R3+(xq, yq)| ≤ 1 (K1x2 + K1y2) ≤ (K1x2 + K2y2), 28 r* M3 r*M4 14 14 thus:

$$C _ { q } & \geq \frac { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } - \frac { 1 } { 7 } \left ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } \right ) } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } | x _ { q } | T f _ { p } ( x _ { q } , y _ { q } ) } \\ & = \frac { \frac { 6 } { 7 } K _ { 1 } x _ { q } ^ { 2 } + \frac { 6 } { 7 } K _ { 2 } y _ { q } ^ { 2 } } { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + K _ { 1 } | x _ { q } | T f _ { p } ( x _ { q } , y _ { q } ) }$$

then we bound from above the denominator: for |xq| ≤ Tκsup 1 we have K1|xq|T ksup(x2 + y2) ≤ K1 + y2) ≤ K1 十 K2 and then: 7 7 7

$$C _ { q } & \geq \frac { \frac { 6 } { 7 } K _ { 1 } x _ { q } ^ { 2 } + \frac { 6 } { 7 } K _ { 2 } y _ { q } ^ { 2 } } { \frac { 8 } { 7 } K _ { 1 } x _ { q } ^ { 2 } + \frac { 8 } { 7 } K _ { 2 } y _ { q } ^ { 2 } } \\ & = \frac { 3 } { 4 } .$$

Now we substitute this lower on Cq in EMed:

$$E _ { \text {Med} } ( x , y ) & \leq C _ { q } \left ( \frac { 5 } { 4 C _ { q } } K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + \frac { 5 } { 4 C _ { q } } K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } - f _ { p } ( x , y ) K _ { 1 } T x _ { q } \right ) \\ & \leq C _ { q } \left ( \frac { 5 } { 3 } K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + \frac { 5 } { 3 } K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } - f _ { p } ( x , y ) K _ { 1 } T x _ { q } \right ) \\ & \leq C _ { q } \left ( \frac { 5 } { 3 } K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + \frac { 5 } { 3 } K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } + \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) K _ { 1 } T | x _ { q } | \right ) .$$

Then it is enough to assume that |xq| ≤ 1 to provides the following inequality: 3Tκsup

$$E _ { M e d } ( x , y ) \leq C _ { q } \left ( 2 K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + 2 K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } \right ) .$$

$$0 \text { so: } & & 2 K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + 2 K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } \leq 0 \Rightarrow E _ { \text {Med} } ( x , y ) \leq 0 , \\ & & 2 K _ { 1 } x ^ { 2 } - K _ { 1 } x x _ { q } + 2 K _ { 2 } y ^ { 2 } - K _ { 2 } y y _ { q } \leq 0$$

But Cq &gt; 0 so:

and since

is an equation for ellβr* (p, q), this proves that EMed(x, y) ≤ 0 is the equation of a region containing ellβr* (p, q) ∩ VMed(p).

So we can consider the rectangular bound VMed(p) on (xq, yq) made of all involved bounds:

$$V _ { M e d } ^ { \prime \prime } ( p ) = \left \{ | x _ { q } | \leq \min \left ( \frac { \sqrt { 2 } } { 2 \kappa _ { e u p } } , \frac { 3 } { 1 4 } \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } | m _ { 3 , 0 } | } , \sqrt { \frac { 6 } { 7 } } \sqrt { \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } M _ { 4 } } } , \frac { 1 } { 7 } \frac { 1 } { \kappa _ { s u p } \tan \theta _ { p } } \right ) , | y _ { q } | \leq \min \left ( \frac { \sqrt { 2 } } { 2 \kappa _ { s u p } } , \frac { 1 } { 2 8 } \frac { 1 - \kappa _ { 1 } r ^ { * } } { r ^ { * } M _ { 3 } } \right ) \right \} ,$$

and claim that, if q ∈ π−1 (VMed(p)) then πp (rMed) contains ellβr* (p, q) ∩ VMed(p). In order to ensure that the ellipses considered are fully contained in VMed(p), we also need that q is inside π−1 (VMed(p)) but not too close to its boundary. Precisely, we chose VMed(p) as the greatest axis-aligned ellipse in VMed(p) ∩ VMed(p) centered on p and with aspect ratio βr*. If πp(g) is nside VMed(p) then πp(rMed) nA contains ellβr* (p, q). And by symmetry, π−(rMed) contains ellβr* (p, q). □

The spheres σLow and σMed are used to handle spheres whose centers are between the tangent plane Tε(p) at p and the medial plane PMed. In order to handle spheres whose center is below Tε(p), we consider the degenerate sphere σExt:


<!-- p:137 -->


is at the infinity of the direction in PBis given by the plane PExt with equation κ1yxq − κ2xyq = 0 in the half-space z &lt; 0. The direction of the center tends to the normal at p when q approaches p. The belonging to the plane PExt guarantees that the projection of the intersection region 8 = B(σExt) ∩ E is tangent with ellβ-∞ (p, q) at p. Ext

We recall that an equation of ellβ-∞(p, q) is given by:

$$2 \kappa _ { 1 } x ^ { 2 } - \kappa _ { 1 } x x _ { q } + 2 \kappa _ { 2 } y ^ { 2 } - \kappa _ { 2 } y y _ { q } \leq 0 .$$

We consider the rectangle VExt = {|x| ≤ √ κ2 κ2 , |y| ≤ κ2 and the following claim: κ1 6M3 6M3

ellB∞

πp(q)

πp(rExt)

The sphere centered at cLow and passing through The projection of the intersection in black, and p and q. ell1 in blue.

p

σExt

-∞

Claim c. If q ∈ π (VExt(p)), then π (rExt) contain ellβ∞(p, q).

of the sphere rExt 8 is centered at the negative extremity, in z coordinate, of the intersection of the following planes:

- The bisector plane of p and q, with equation:

$$0 = ( \frac { x _ { q } } { 2 } - x ) x _ { q } + ( \frac { y _ { q } } { 2 } - y ) y _ { q } + ( \frac { z _ { q } } { 2 } - z ) z _ { q } .$$

$$0 = \kappa _ { 1 } y x _ { q } - \kappa _ { 2 } x y _ { q } .$$

We search for a direction vector v for the intersection line of the two planes, one is given by the cross product of the vectors normal to the planes:

$$\vec { v } = \left ( \begin{matrix} x _ { q } \\ y _ { q } \\ z _ { q } \end{matrix} \right ) \times \left ( \begin{matrix} - \kappa _ { 2 } y _ { q } \\ \kappa _ { 1 } x _ { q } \\ 0 \end{matrix} \right ) = \left ( \begin{matrix} - z _ { q } \kappa _ { 1 } x _ { q } \\ - z _ { q } \kappa _ { 2 } y _ { q } \\ \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } \end{matrix} \right ) .$$

The half-space parameterized by is then:

- The plane with equation:

$$E _ { E x t } ^ { - \infty } \leq 0 ,$$

where Ext (x, y) = −κ1xqx − κ2yqy + z. zq

We substitute fp(x, y) in z to obtain an expression of the projection in the tangent plane:

$$E _ { E x t } ^ { - \infty } ( x , y ) = - \kappa _ { 1 } x _ { q } x - \kappa _ { 2 } y _ { q } y + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { z _ { q } } f _ { p } ( x , y )$$


<!-- p:138 -->


and fp(xq, yq) in zq:

$$& = - \kappa _ { 1 } x _ { q } x - \kappa _ { 2 } y _ { q } y + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { f _ { p } ( x _ { q } , y _ { q } ) } f _ { p } ( x , y ) \\ & = - \kappa _ { 1 } x _ { q } x - \kappa _ { 2 } y _ { q } y + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { \kappa _ { 2 } \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } } { \kappa _ { 2 } \kappa _ { 2 } y _ { q } ^ { 2 } + R _ { 3 } ( x _ { q } , y _ { q } ) } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + R _ { 3 } ( x , y ) \right ) . \\ \intertext { o w t o u t t o b o u d f u m o b e v o w t h e o w x p a c t i o n s y }$$

Then we start to bound from above the expression:

$$\text {Then we start to bound from above the expression:} \\ E _ { E x } ^ { \infty } ( x , y ) & \leq - \kappa _ { 1 } x _ { q } x ^ { - \kappa _ { 2 } y _ { q } } + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } y _ { q } ^ { 2 } - M _ { 3 } ( x _ { q } ^ { 2 } + y _ { 2 } ^ { 2 } ) ^ { \frac { 3 } { 2 } } } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } y _ { q } ^ { 2 } - M _ { 3 } ( x _ { q } ^ { 2 } + y _ { 2 } ^ { 2 } ) } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } y _ { q } ^ { 2 } - \frac { 1 } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { \kappa _ { 2 } y _ { q } ^ { 2 } } } \left ( \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { \kappa _ { 2 } y _ { q } ^ { 2 } } + \frac { 1 } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { \kappa _ { 2 } y _ { q } ^ { 2 } } } \right ) } \\ & \leq - \kappa _ { 1 } x _ { q } x ^ { - \kappa _ { 2 } y _ { q } } + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } y _ { q } ^ { 2 } - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \kappa _ { 2 } y _ { q } ^ { 2 } } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { \kappa _ { 2 } y _ { q } ^ { 2 } } } \left ( \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { \kappa _ { 2 } y _ { q } ^ { 2 } } + \frac { 1 } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { \kappa _ { 2 } y _ { q } ^ { 2 } } } \right ) }$$

for √x2 + y2 ≤ 6M3 κ2 and q + y2 ≤ 6M3, κ2

$$& = - \kappa _ { 1 } x _ { q } x - \kappa _ { 2 } y _ { q } y + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { \frac { \tau } { 3 } \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { \tau } { 3 } \kappa _ { 2 } y _ { q } ^ { 2 } } \left ( \frac { 2 } { 3 } \kappa _ { 1 } x ^ { 2 } + \frac { 2 } { 3 } \kappa _ { 2 } y ^ { 2 } \right ) \\ & = 2 \kappa _ { 1 } x ^ { 2 } - \kappa _ { 1 } x _ { q } x + 2 \kappa _ { 2 } y ^ { 2 } - \kappa _ { 2 } y _ { q } y ,$$

that is the equation of ellβ-∞ (p, q) when the expression equals 0.

We recall that ellβ-∞(p, q) is an ellipse with aspect ratio k1 To ensure that ellβ-∞(p, q) is fully κ2 contained in the neighborhood considered, we can take VExt(p) = {|x| ≤ √ K2 κ2 , |y| ≤ κ2 □ κ16M3 6M3

####### Degenerate spheres σl and σr.

For the next claim, we introduce the new neighborhood:

Their centers ce and cr are at the infinity of the line that is the intersection of PBis and the tangent plane Tε(p), with equation z = 0. The sphere σe (or σr) degenerates into the plane PDiag, passing through p and q, and containing the normal at p.

$$V _ { Z } ( p ) = \left \{ | x _ { q } | \leq \frac { \text {dist} ( p , Z ) } { 2 } , \, | y _ { q } | \leq \sqrt { 1 - \kappa _ { 1 } r ^ { * } } \frac { \text {dist} ( p , Z ) } { 2 } \right \} ,$$

that guarantees that if q ∈ π−1 (Vz(p)) then ellβr* (p, q) is fully inside Vz(p) and consequently π (ellβr* (p, q)) ∩ Z = ∅.

Claim d. If q ∈ π−1 (VLow(p)) then πp (re(p, q)) and πp (r(p, q)) contain respectively ellk(p, q) and ell1(p, q). If additionally q ∈ π−1 (Vz(p)), then π− (re(p, q)) contains ellθr* (p, q).

Proof. Since PDiag is orthogonal to Tε(p), the proof is actually trivial for πp (re(p, q)) and πp (rr(p, q)). The surface needs just to parameterizable, that is the case in π−1 (VLow(p)). To prove that πp (re(p, q)) contains ell t ae o    e t d  (      ( d (ellpr* is fully contained in re(p, q), we just need that q is not so close to Z with respect to p, so roughly, we can take q ∈ π− −1 (Vz(p)). □

Those claims, associated with the Combination lemma, are enough to prove that if q is close enough to p, then a sphere whose center is below (smaller in z coordinate) the center of σMed(p, q) contains either:

$$\pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta , * } \left ( p , q \right ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( r h _ { r } ^ { \beta , * } \left ( p , q \right ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta , \infty } \left ( p , q \right ) \right ) \ \text { or } \pi _ { p } ^ { - 1 } \left ( r h _ { r } ^ { \beta , \infty } \left ( p , q \right ) \right ) .$$

When a sphere gets higher two possibilities arise, the sphere can contain p or not. When its center get higher while not containing p, the center get farther from p, and we might be tempted to think that such a sphere should still contain π−1 (rhβr* (p, q)), but it is not true. This can be explained by the fact that the sphere at upper infinity of PMed has for intersection with the surface the complementary of an ellipse, which is not convex. Before explaining how we deal with this problem, we describe the degenerate spheres σ 十∞ and σEx +∞ Sym


<!-- p:139 -->


####### Degenerate sphere σ +∞ Sym

The center +∞ is at the infinity of the line in PBis and PMed, with a positive z coordinate. The Sym degenerate ball B(σ +∞ ) is actually a half-space whose boundary is the plane Psym passing through p, q, Sym p, and q. The interior of B(σ σs∞) is directed by the normal with positive z coordinate. Once projected Sym on the tangent plan, the intersection of B(σs∞) with ε is the exterior of an ellipse. As it is shown in the Sym following claim, at p that ellipse has the line with equation:

$$- y _ { q } ^ { 2 } x + ( y _ { q } f _ { p } ( x _ { q } , y _ { q } ) \tan ( \theta _ { p } ) + x _ { q } y _ { q } ) \, y = 0 ,$$

for tangent. We name HPr(p, q) the half-plane delimited by the tangent, and that does not contain p. By symmetry we name HPr(p, q) the symmetrical of HPr(p, q) with respect to PMed.

The intersection of ε with Psym in black, and with PDiag in gray. As we can see, the two curves are close between p and q.

Claim e. If q ∈ π−1 (VLow(p) ∩ Vz(p)) then πp (r+∞) contains HPr(p, q) ∩ ellβr* (p, q), and πp +∞ contains HPr(p, q) ∩ ellβr* (p, q).

Proof. The center c+∞m of the degenerate sphere σ +∞ is at the positive extremity, in z coordinate, of the Sym Sym intersection of the following planes:

- The bisector plane of p and q, with equation:

$$0 = ( \frac { x _ { q } } { 2 } - x ) x _ { q } + ( \frac { y _ { q } } { 2 } - y ) y _ { q } + ( \frac { z _ { q } } { 2 } - z ) z _ { q } .$$

$$z = r ^ { * } + x \tan ( \theta _ { p } ) .$$

We search for a direction vector σ for the intersection line of the two planes, one is given by the cross product of the vectors normal to the planes:

$$\begin{pmatrix} x _ { q } \\ y _ { q } \\ z _ { q } \end{pmatrix} \times \begin{pmatrix} \tan ( \theta _ { p } ) \\ 0 \\ - 1 \end{pmatrix} = \begin{pmatrix} - y _ { q } \\ z _ { q } \tan ( \theta _ { p } ) + x _ { q } \\ - y _ { q } \tan ( \theta _ { p } ) \end{pmatrix} .$$

We choose σ colinear to the vector above such that the z coordinate is positive by multiplying it by −yq:

$$\vec { v } = \left ( - y _ { q } z _ { q } \tan ( \theta _ { p } ) - x _ { q } y _ { q } \right ) .$$

- The plane with equation:


<!-- p:140 -->


The half-space parameterized by CSym +∞ is then:

$$^ { - \infty } _ { y m } ( x , y ) \leq 0 ,$$

where E+∞(x, y) = −y2x + (yq q tan(θp) + xqyq) y − y tan(θp)z.

We substitute fp(x, y) in z to obtain an expression of the projection in the tangent plane:

$$E _ { S y m } ^ { + \infty } ( x , y ) = - y _ { q } ^ { 2 } x + ( y _ { q } z _ { q } \tan ( \theta _ { p } ) + x _ { q } y _ { q } ) \, y - y _ { q } ^ { 2 } \tan ( \theta _ { p } ) f _ { p } ( x , y )$$

and fp(xq, yq) in zq:

$$= - y _ { q } ^ { 2 } x + ( y _ { q } f _ { p } ( x _ { q } , y _ { q } ) \tan ( \theta _ { p } ) + x _ { q } y _ { q } ) \, y - y _ { q } ^ { 2 } \tan ( \theta _ { p } ) f _ { p } ( x , y )$$

that we can bound by the following expression:

$$\leq - y _ { q } ^ { 2 } x + ( y _ { q } f _ { p } ( x _ { q } , y _ { q } ) \tan ( \theta _ { p } ) + x _ { q } y _ { q } ) \, y ,$$

The expression 0 = −y2x + (yq fp(xq, yq) tan(θp) + xqyq) y, that we can rewrite

$$0 = - y _ { q } x + ( f _ { p } ( x _ { q } , y _ { q } ) \tan ( \theta _ { p } ) + x _ { q } ) \, y ,$$

(r+∞) is the expression of the tangent to the projection of +∞ (p, q) in Tε (p) at p. Thus πp contains Sym HPr(p, q) where ε is parameterizable. Since it is the case in VLow(p) ∩ Vz(p), we can say that for π−1(q) ∈ VLow(p) ∩ Vz(p), πp (rs∞) contains HPr(p, q) ∩ ellβr* (p, q).

By symmetry if π−1(q) ∈ VLow(p) ∩ Vz(p), πp ( contains HPr(p, q) ∩ ellβr* (p, q).

One can notice that, when q tend to p, fp(xq, yq) tends quadratically to 0, and so the tangent tends to the line (p, πp(q)). □

####### Degenerate sphere σ+x. ∞+

The center cExt +∞ is at the infinity of the direction in PBis given by the plane PExt with equation ) contains actually the whole spheroid ε expect for a small region around p and q.

Claim f. If q ∈ π−1 (VLow(p) ∩ VExt(p) ∩ Vz(p)) then πp(rEx∞) contains ellβr* (p, q).

Proof. The equation of B(σ+xt) +∞ ) is

$$\kappa _ { 1 } x _ { q } x + \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { z _ { q } } z \leq 0 .$$

(x, y) ≤ 0 where:

$$E _ { E x t } ^ { + \infty } ( x , y ) = \kappa _ { 1 } x _ { q } x \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { z _ { q } } f _ { p } ( x , y ) .$$

Then we substitute fp(xq, yq) in zq:

$$E _ { E x t } ^ { + \infty } ( x , y ) & = \kappa _ { 1 } x _ { q } x + \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { f _ { p } ( x _ { q } y _ { q } ) } f _ { p } ( x , y ) \\ & = \kappa _ { 1 } x _ { q } x + \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { \frac { \kappa _ { 1 } x _ { q } x ^ { 2 } + \frac { \kappa _ { 2 } y _ { q } ^ { 2 } } { \kappa _ { 2 } y _ { q } ^ { 2 } + R _ { 3 } ( x _ { q } , y _ { q } ) } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + R _ { 3 } ( x , y ) \right ) .$$


<!-- p:141 -->


Then we start to bound from above the expression for q ∈ π−1 (VLow(p) ∩ VExt(p)):

$$E _ { E x t } ^ { + \infty } ( x , y ) & \leq \kappa _ { 1 } x _ { q } x + \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { \frac { 1 } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y _ { q } ^ { 2 } + M _ { 3 } ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) ^ { \frac { 3 } { 2 } } } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } - M _ { 3 } ( x ^ { 2 } + y ^ { 2 } ) ^ { \frac { 3 } { 2 } } \right ) \\ & \leq \kappa _ { 1 } x _ { q } x + \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y _ { q } ^ { 2 } + \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } } { \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { 6 } \kappa _ { 2 } y _ { q } ^ { 2 } } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } - \left ( \frac { 1 } { 6 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 6 } \kappa _ { 2 } y ^ { 2 } \right ) \right )$$

and since √x2 + y2 ≤ 6M3 κ2 and + y2 V 6M3 κ2 we have,

$$E _ { E x t } ^ { + \infty } ( x , y ) & \leq \kappa _ { 1 } x _ { q } x + \kappa _ { 2 } y _ { q } y - \frac { \kappa _ { 1 } x _ { q } ^ { 2 } + \kappa _ { 2 } y _ { q } ^ { 2 } } { 3 \kappa _ { 1 } x _ { q } ^ { 2 } + 3 \kappa _ { 2 } y _ { q } ^ { 2 } } \left ( \frac { 1 } { 3 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 3 } \kappa _ { 2 } y ^ { 2 } \right ) \\ & = - \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \kappa _ { 1 } x _ { q } x - \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \kappa _ { 2 } y _ { q } y .$$

But

$$- \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \kappa _ { 1 } x _ { q } x - \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + \kappa _ { 2 } y _ { q } y \leq 0$$

is the inequality of the exterior of the axis-aligned ellipse passing through p, centered on πp(q) and with aspect ratio K1 κ2 projection that is strictly included in that ellipse. But since the surface is a spheroid, i.e. the boundary of a convex volume, and since σ+xt +∞ is a actually a plane, there exists only one connected component in the intersection. So we just need to take a neighborhood around p for q such that the ellipse is far enough from p, more precisely we want the outer ellipse not to intersect Z. But this property is achieved in Vz.

We deduce that, if q ∈ π−1 (VLow(p) ∩ VExt(p) ∩ Vz(p)) then πp(rEx) contains, t least, eβr* (p, q). □

At the end of these claims, for any p ∈ ε and any q ∈ ε close enough to p or q, we have identified seven specific spheres. We showed that each of these spheres contains a region on the surface whose area is controlled by p and q. We can now partition the bisector plane on the basis of the centers of these spheres.

We end the section by defining V1(p) as the intersection of all involved neighborhoods:

$$V _ { 1 } ( p ) = V _ { L o w } ( p ) \cap V _ { S y m } ( p ) \cap V _ { E x t } ( p ) \cap V _ { Z } ( p ) .$$

In Section 13.4.7, we will show that V1(p) has size Ω(hp) × Ω(h2).

##### 13.4.4 Proof of the graph inclusion

We use Combination and Partition lemmas to prove that for any pair (p, q) such that q ∈ π−1 (Vi(p)),

(X). Note that the condition q ∈ π−1 (Vi(p)) implies that q is on the side of p with respect PBis(p, p). In Section 13.4.5, we will explain how we count the neighbors of p that are on the side of p with respect PBis(p, p). As in the cylinder case, we use Combination lemma to identify the tiles that pave the bisector plane of p and q, and the Partition lemma to show the super-graph property:

Lemma 13.9. Consider an oblate spheroid E embedded in R3 and a data sample X distributed on E. Let p and q two points of X such that q ∈ π−1 (V1(p)).

$$I f \left ( p , q \right ) \, i s \, a n \ e d g e \ o f \, \text {Del} ( X ) , \, \text {then} \, i t \, i s \, a n \ e d g e \ o f \, \overrightarrow { \mathcal { G } } _ { \mathcal { F } _ { 1 } } ^ { 0 } ( X ) .$$

Proof. Let p and q be two points of ε such that q ∈ π−1 (V1(p)). We consider the Monge coordinates system at p as used in the claims. We have to show that if a sphere passes through p and q, it contains at least one of the six regions of F1(p, q).

So we assume that q ∈ π−1 (V1(p)) and dist(p, q) ≤ dist(p, q). We consider a sphere σ passing though p and q, and call c, its center, that lies in PBis. We prove the lemma by partitioning PBis. The partition chosen is the following: (see Figure 13.4). PBis is separated into two half-planes by the tangent plane Tε(p) with equation z = 0 and on which are cLow, by definition, and ce and cr since they are at the infinity of an horizontal direction in PBis. The part of PBis below z = 0 is made of center of outer spheres, centered below the tangent plane of p. This part is separated by the ray [cLow, cExt). This partition divides the outer spheres into two categories, those who are rather in the direction of p, so rather on the left in the global frame and denoted with a "l" in index, and those who are rather in the opposite direction denoted with a "r".


<!-- p:142 -->


We start with the spheres centered below the tangent plane at p. By the Combination lemma we have:

- ∈ B(σc), by Claims a, c, and d, since

$$r h _ { \ell } ^ { \beta _ { \infty } } \subset e l l ^ { 1 } \cap e l l ^ { \beta _ { \ast \infty } } \cap e l l _ { \ell } ^ { 1 } .$$

And,

- if c ∈ (cExt, CLow, Cr), then π−1 (rhβ∞) ∈ B(σc), by the same claims, and since

$$r h _ { r } ^ { \beta _ { \infty } } \subset e l l ^ { 1 } \cap e l l ^ { \beta _ { \ast \infty } } \cap e l l _ { r } ^ { 1 } .$$

Then we consider the centers cMed and c+∞ Sym The polygon below the polyline and above z = 0 contains centers of medium-height spheres. We divide this polygon by the segment [cLow, cMed], that divides the medium-height spheres similarly than for the low spheres into left and right spheres.

By the Combination lemma we have:

- if c ∈ (ce, CMed, CLow, ce), then π−1 ∈ B(σc), by Claims a, b, and d, since

$$r h _ { \ell } ^ { \beta _ { r ^ { * } } } \subset e l l ^ { 1 } \cap e l l ^ { \beta _ { r ^ { * } } } \cap e l l _ { \ell } ^ { 1 } .$$

- (rhr rbβr* ∈ B(σc), by the same claims and since

$$\tilde { r } \tilde { h } _ { r } ^ { \beta _ { r } * } \subset \text {ell} _ { r } ^ { 1 } \cap \text {ell} ^ { 1 } \cap \text {ell} ^ { \beta _ { r } * } \cap \pi _ { p } \left ( r _ { S y m } ^ { + \infty } \right ) .$$

Note that we do not use yet Claim e, we will use it later to get a lower bound on the area of πp (rhβ*) and π−1

Finally we consider the additional center c+x +∞ +∞ contains the centers of high spheres. They all pass through p or contain it, since there centers are above PMed on PBis. This polygon can be seen as the symmetrical tile of the one described previously. The ray

By the Combination lemma we have:

- if c ∈ (ce, cMed, cEx) +∞ t ), then π−1 (rher βr* ∈ B(σc), by Claims b, d, and f since

$$\overline { r h _ { \ell } ^ { \beta _ { r ^ { * } } } } \subset \overline { e l l ^ { \beta _ { r ^ { * } } } } \cap \overline { e l l _ { \ell } ^ { 1 } } .$$

- +∞ (rhr βγ* ∈ B(σc), by Claims b, e, and f, and since

$$\overline { \tilde { r } h _ { r } ^ { \beta _ { r } * } } \subset \overline { e l l ^ { \beta _ { r } * } } \cap \overline { e l l _ { r } ^ { 1 } } \cap \pi _ { \overline { p } } \left ( \overline { r _ { S y m } ^ { + \infty } } \right ) .$$

And,

And, This decomposition partitions the bisector plane of p and q into six tiles and associates to each tile P of the partition, a region f ∈ F1 on E such that, if c ∈ P, then B(σ) contains f. In other words, it ensures, by the Partition lemma, that


<!-- p:143 -->


$$\mathcal { G } _ { \mathcal { F } _ { 1 } } ^ { \emptyset } = \bigcup _ { f \in \mathcal { F } _ { 1 } } \mathcal { G } _ { \{ f \} } ^ { \emptyset } ,$$

for pairs (p, q) such that q ∈ π−1 (V1(p)).

cExt

+∞

ellβr*

πp(r

Sym

cSym

∞

3

*

cl

ellβr*, ellβ*

cMed

*

rhe

ell, ell

ell1

el1

cl

0 = z

cLow

β

rhe

8


cExt

Cr

Figure 13.4: Partition of the bisector plane when q ∈ π−1 (V1(p)). The red ray is included in PMed.

##### 13.4.5 When q is on the side of p with respect to PMed

A point q that is not close to p may still have a good probability to be a Delaunay neighbor of p, but its only chance is to be close to p. We show that we can reduce the analysis to the previous case.

Intuitively, q is close to p if and only if q is close to p. In the case of the oblate spheroid, it is clear by symmetry. Remind that the four points p, q, p and q are coplanar and even cocyclic. In the plane that contains the four points, the edge (p, q) is now a diagonal of the convex quadrilateral formed by the four points. That implies that any sphere σc passing through p and q contains either p or ī (see Figure 13.5).

Suppose that σc contains  ̄, in other words, that its center c is on the side q with respect to the bisector plane PMed of p and p. Then we can consider the sphere σ0 included in σc that passes through p and q. σ0 is then the image of σc by a homothety of a factor smaller than 1 and centered at p. Since p and c are on the side of p, it is clear that it is also the case for the center c0 of σ0.

On the other hand, if σc contains p, then σc can be shrunk toward q into σ0 that touches p. The center c0 of σ0 lies now on the side of p with respect to PMed.

Then we can consider the following lemma:

Lemma 13.10. Let q be on the side of p with respect to the bisector plane of p and p, σ a sphere passing

□


<!-- p:144 -->


Figure 13.5: In the plane (pqp), the points p and q are opposite in the quadrilateral (p,  ̄, q, p), so the sphere σ passing p and q contains q. By a homothety, it can be reduced to the included sphere σ0 that d   oe e s  e asd   e ss  o s o o o    t ssd.

3

σ

σ0

b

ā

p


through p and q. If q ∈ π−1 (V1( ̄)), then B(σ) contains at least one region of:

$$\overline { \mathcal { F } } _ { 1 } ( p , q ) \colon = \left \{ \begin{array} { l l } { \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r ^ { * } } } ( p , \overline { q } ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r ^ { * } } } ( p , \overline { q } ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( p , \overline { q } ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( p , \overline { q } ) \right ) , } \\ { \pi _ { \overline { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r ^ { * } } } ( \overline { p } , q ) \right ) , \ \pi _ { \overline { p } } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r ^ { * } } } ( \overline { p } , q ) \right ) , \ \pi _ { \overline { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( \overline { p } , q ) \right ) , \ \pi _ { \overline { p } } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( \overline { p } , q ) \right ) } \end{array} \right \} .$$

Pprao   e   r  e  t se  ons  ta s oed above, consider the sphere σ0, included in σ, and passing through p and q. If q ∈ Vi(p), we can apply Lemma 13.9 to p and q to show that σ contains one the 8 regions of F1(p, ). But as we said, the center c0 of σ0 is on the side of p with respect to the bisector plane of p and p. In other words, in the partition of bisector plane PBis(p, ), c0 lies below the intersection line with PMed, so we can exclude the two regions whose parameter lies strictly above. It remains that σ0, and then σ, contain at least one region among the 4 following regions:

$$\left \{ \pi _ { p } ^ { - 1 } \left ( r \hbar { \ell } ^ { \beta _ { r } * } \left ( p , \overline { q } \right ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( \tilde { r } \hbar { r } ^ { \beta _ { r } * } \left ( p , \overline { q } \right ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( r \hbar { \ell } ^ { \beta _ { \infty } } \left ( p , \overline { q } \right ) \right ) , \ \pi _ { p } ^ { - 1 } \left ( r \hbar { r } ^ { \beta _ { \infty } } \left ( p , \overline { q } \right ) \right ) \right \} .$$

If we consider now that σ contains p, we can apply a similar argument to show that σ contains at least one region among the 4 following regions:

□

Then we can define CN(p) as the union of π−1(V1(p)) and π−1(V1( ̄)), and the family of fundamental regions F1 (p, q) for q ∈ CN(p):

$$\mathcal { F } _ { 1 } ^ { * } ( p , q ) = \left \{ \begin{array} { l l } { \mathcal { F } _ { 1 } ( p , q ) \text { if } q \in \pi _ { p } ^ { - 1 } \left ( V _ { 1 } ( p ) \right ) , \text { or } } \\ { \overline { \mathcal { F } } _ { 1 } ( p , q ) \text { if } q \in \pi _ { \overline { p } } ^ { - 1 } \left ( V _ { 1 } ( \overline { p } ) \right ) , } \end{array}$$

and we can say that for any p ∈ ε, the Delaunay neighbors of p that are in CN(p) are also neighbors of p in Thus we compute an upper bound on the expected degree of a point in that super-graph.

##### 13.4.6 Computation of an upper bound on the expected number of close neighbors.

Te    oe te n  te oue   o o e ng neighbors are treated in the next section. Before getting into the substance of the computation, it remains to evaluate the area of all the involved regions, in particular the regions denoted with a "~".

$$\left \{ \pi _ { \overline { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r } * } \left ( \overline { p } , q \right ) \right ) , \ \pi _ { \overline { p } } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } \left ( \overline { p } , q \right ) \right ) , \ \pi _ { \overline { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } \left ( \overline { p } , q \right ) \right ) , \ \pi _ { \overline { p } } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } \left ( \overline { p } , q \right ) \right ) \right \} .$$


<!-- p:145 -->


Figure 13.6: The disk sector Sec tiled in blue. In red is the projection on Tε(p) of the intersection +∞ When q is close enough to p, the disk sector is being slightly reduced.

πp(q)

Sec

ells

rhe

rhr

β

βr* βr* On the size of the fundamental regions rhr"*( * (p, q) and ellrν (p, q).

We start, using some computations from Claim e, by bounding from below the area of the regions rhr *(p, q) and ell,r* (p, q) that appears in F1 (p, q). The area of all other regions are well known and already studied in Part II.

We recall that rhTr* (p, q) = rhβr* (p, q) ∩HPr(p, q), where HPr (p, q) is a half-plane close to HPr(p, q). We show that the cut part is small enough, so that we still have:

$$\left | \tilde { r } \tilde { h } _ { r } ^ { \beta _ { r } * } ( p , q ) \right | = \Theta \left ( \left | r \tilde { h } _ { r } ^ { \beta _ { r } * } ( p , q ) \right | \right ) .$$

First we recall the area of rhβ* is:

$$\left | r h _ { r } ^ { \beta _ { r } * } \right | = \frac { 1 } { 8 } \left | R h ^ { \beta _ { r } * } \right | = \frac { 1 } { 1 6 } \sqrt { ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) \left ( \beta _ { r ^ { * } } { ^ { 2 } } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) } .$$

We show that the cut part has an area smaller than (x2 a + y2) (βr+2 + y2). 32 We consider the following two lines in Tε(p):

- (pq) with equation y = yq x, and xq
- Tr+∞ (p), the tangent line of r Ext +∞ at p with equation y = Tfp(xq,yq)+xq yq x, where T = tan(θp), as seen in Claim e. Ext

The cut part is included between the two lines and is inside the disk centered on p with radius |pπp(q)|. So what we compute is actually an upper bound on the area of this disk sector Sec (see Figure 13.6). The area of Sec is given by:

$$| \sec | = \frac { 1 } { 2 } \left | \arctan \left ( \frac { y _ { q } } { x _ { q } } \right ) - \arctan \left ( \frac { y _ { q } } { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } \right ) \right | | p \pi _ { p } ( q ) | ^ { 2 } .$$

We bound the quantity of Q = &amp; arctan xq yq - arctan (Tfp(xq,yq)+xq yq using classical trigonometric formulas:

$$Q & = \left | \arctan \left ( \frac { y _ { q } } { x _ { q } } \right ) - \arctan \left ( \frac { y _ { q } } { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } \right ) \right | \\ & = \left | \arctan \left ( \left ( \frac { y _ { q } } { x _ { q } } - \frac { y _ { q } } { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } \right ) \frac { 1 } { 1 + \frac { y _ { q } } { x _ { q } } \frac { \frac { y _ { q } } { y _ { q } } } { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } } \right ) \right |$$


<!-- p:146 -->


using arctan (a) − arctan (b) = arctan( a-b 1+ab),

$$\begin{array} { r l } & { \sin c \arctan ( a ) - \arctan ( b ) = \arctan ( \frac { a - b } { 1 + a b } ) , } \\ & { \leq \left | \left ( \frac { y _ { q } } { x _ { q } } - \frac { y _ { q } } { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } \right ) \frac { 1 } { 1 + \frac { y _ { a } } { x _ { a } } \frac { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } { T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } } } \right | \text { since } | \arctan ( x ) | \leq | x | , } \\ & { = \left | y _ { q } \frac { T f _ { p } ( x _ { q } , y _ { q } ) } { x _ { q } ( T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } ) } \frac { x _ { q } ( T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } ) } { x _ { q } ( T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } ) + y _ { q } ^ { 2 } } \right | } \\ & { = \frac { y _ { q } T f _ { p } ( x _ { q } , y _ { q } ) } { x _ { q } ( T f _ { p } ( x _ { q } , y _ { q } ) + x _ { q } ) + y _ { q } ^ { 2 } } \right | } \\ & { \leq \frac { T f _ { p } ( x _ { q } , y _ { q } ) | y _ { q } | } { x _ { q } + y _ { q } ^ { 2 } - | x _ { q } | T f _ { p } ( x _ { q } , y _ { q } ) } \\ & { \leq \frac { T \kappa _ { \sup } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) | y _ { q } | } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } - | x _ { q } | T \kappa _ { \sup } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) } } \\ & { \leq \frac { T \kappa _ { \sup } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) | y _ { q } | } { \frac { 1 } { 2 } ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) } \text { for } | x _ { q } | \leq \frac { 1 } { 2 T \kappa _ { \sup } } , } \\ & { = 2 T \kappa _ { \sup } | y _ { q } | } \\ & { \leq \frac { \beta _ { r ^ { * * } } } { 1 6 } \text { for } | y _ { q } | \leq \frac { \beta _ { r ^ { * * } } } { 3 2 T \kappa _ { \sup } } . } \\ & { \text {And then } | \sec | \leq \frac { \beta _ { r ^ { * * } } } { 3 2 } | p \pi _ { p } ( q ) | ^ { 2 } , \text { but since } 0 \leq \beta _ { r ^ { * * } } \leq 1 , \text { we have well } } \end{array}$$

And then |Sec| ≤ βr* |pπp(q)|2, but since 0 ≤ βr* ≤ 1, we have well 32

$$| \text {Sec} | \leq \frac { \beta _ { r } * } { 3 2 } | p \pi _ { p } ( q ) | ^ { 2 } = \frac { 1 } { 3 2 } \sqrt { ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) \left ( \beta _ { r ^ { * } } \, ^ { 2 } x _ { q } ^ { 2 } + \beta _ { r ^ { * } } \, ^ { 2 } y _ { q } ^ { 2 } \right ) } \leq \frac { 1 } { 3 2 } \sqrt { \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) \left ( \beta _ { r ^ { * } } \, ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) } ,$$

and so

Finally we can say that:

$$\overline { { { { { { { { { { { { { { r } ^ { * } } } } } } } } } } } } } } } ( p , q ) \Big | \, \geq \, \left | \, \mathrm r \, \right |$$

####### Upper bound on the expected number of close neighbors of p

Consider a Poisson point process X distributed on E with intensity λ. We have shown that (X) dx  sa   ot     s (  sda  (  d-ds  sa point in 0 (X) to have an upper bound on the expected degree of the same point in Del(X).

We recall that β(p) = V 1−κ1(p)r*(p) The lemma that we are going to prove is: 1−κ2(p)r*(p)

Lemma 13.1. Let E be an oblate spheroid and X a Poisson point process distributed on E with intensity λ. For any p ∈ ε \ Z, the expected number of close neighbors of p in Del(X ∪ {p}) is:

$$O \left ( \ln \frac { 1 } { \beta _ { r ^ { * } } } \right )$$

Proof. Consider the Monge coordinates system at p. We bound the expected number of close neighbors

$$| \text {Sec} | \leq \frac { 1 } { 2 } \left | \text {rh} _ { r } ^ { \beta _ { r } * } ( p , q ) \right | .$$


<!-- p:147 -->


of p in Del(X ∪ {p}), noted E [deg|CN (p, Del)]:

$$of p \, in \, Del ( X \cup \{ p \} ) , & \, noted \, E \left [ \deg _ { \text {CN} } ( p , \text {Del} ) \right ] \colon \\ & \quad \deg _ { \text {CN} } ( p , \text {Del} ) = \sum _ { q \in X \cap \text {CN} ( p ) } \frac { 1 _ { ( p , q ) \in \text {Del} ( X \cup \{ p \} ) } } { q \in X \cap \text {CN} ( p ) } \stackrel { \vartheta _ { q } } { = } \underset { X } { \varphi } _ { \mathbb { 1 } } \text { is a super-graph of Del} , \\ & \quad \leq \sum _ { q \in X \cap ( p ) \cap X } \frac { 1 _ { ( p , q ) \in \mathbb { 0 } _ { \mathbb { 1 } } ( X ) } } { q \in X \cap ( p ) \cap X } \stackrel { \vartheta _ { q } } { = } \underset { X } { \varphi } _ { \mathbb { 1 } } \text { is a super-graph of Del} , \\ [ \text {deg} \subset \text {CN} ( p , \text {Del} ) ] & \leq \left [ \sum _ { q \in X \cap ( p ) \cap X } \frac { 1 _ { ( p , q ) \in \mathcal { Q } _ { \mathbb { 1 } } ( X \cup \{ p \} ) } } { q \in X \cap ( p ) \cap X } \right ] \\ & \quad \leq \lambda \int _ { q \in X \cap ( p ) } \mathbb { P } \left [ ( p , q ) \in \mathbb { Q } _ { \mathbb { 1 } } ( X \cup \{ p \} ) \right ] d q \text { by Slivynak-Mecke Theorem} , \\ & = \lambda \int _ { q \in X \cap ( p ) } \mathbb { P } \left [ \exists \mathring { r } _ { 1 } ( p , ( q ) , r ) \cap X = \emptyset \right ] d q \\ & \quad \leq \lambda \int _ { q \in X \cap ( p ) } \sum _ { r \in \mathcal { F } _ { 1 } ^ { \dagger } ( p , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] d q \\ & = \lambda \int _ { q \in X \cap ( p ) } \sum _ { r \in \mathcal { F } _ { 1 } ^ { \dagger } ( p , q ) } e ^ { - \lambda | \cdot | d q } \\ & = \lambda \int _ { q \in X \cap ^ { \prime } ( V _ { 1 } ( p ) ) } \sum _ { r \in \mathcal { F } _ { 1 } ^ { \dagger } ( p , q ) } e ^ { - \lambda | \cdot | r } d q + \lambda \int _ { q \in \mathcal { F } _ { 1 } ^ { \dagger } ( V _ { 1 } ( p ) ) } \sum _ { r \in \mathcal { F } _ { 1 } ^ { \dagger } ( p , q ) } e ^ { - \lambda | r | } d q \\ & = \lambda \int _ { q \in X ^ { \prime } } \sum _ { \substack { ( V _ { 1 } ( p ) ) \in \mathcal { F } _ { 1 } ( p , q ) \\ r \in \mathcal { F } _ { 1 } ( p , q ) } } e ^ { - \lambda | r | } d q + \lambda \int _ { q \in \mathcal { F } _ { 1 } ^ { \dagger } ( V _ { 1 } ( p ) ) } \sum _ { r \in \mathcal { F } _ { 1 } ^ { \dagger } ( p , q ) } e ^ { - \lambda | r | } d q . \\ \text {We recall here the two families of regions:} \\ & \mathcal { F } _ { 1 } ( p , q ) = \int _ { \mathbb { 1 } } \left ( \lambda r _ { k } ^ { - 1 } ( r _ { k } , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( r _ { k } ^ { \lambda - \alpha } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \underline { r } _ { k } ^ { \lambda - \alpha } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \tilde { r } _ { k } ^ { \lambda - \alpha } ( p , q ) \right ) , \right ) \Big \} ,$$

We recall here the two families of regions:

$$\mathcal { F } _ { 1 } ( p , q ) = \left \{ \begin{array} { c } \pi _ { p } ^ { - 1 } \left ( \text {rh} _ { \ell } ^ { \beta _ { \infty } } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \text {rh} _ { r } ^ { \beta _ { \infty } } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \text {rh} _ { \ell } ^ { \beta _ { r } * } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \text {rh} _ { r } ^ { \beta _ { r } * } ( p , q ) \right ) , \\ \pi _ { \overline { p } } ^ { - 1 } \left ( \text {ell} _ { \ell } ^ { \beta _ { r } * } ( p , q ) \right ) , \pi _ { \overline { p } } ^ { - 1 } \left ( \text {rh} _ { r } ^ { \beta _ { r } * } ( p , q ) \right ) \end{array} \right \} ,$$

and

$$\overline { \mathcal { F } } _ { 1 } ( p , q ) = \left \{ \begin{array} { l l } { \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r } * } ( p , \bar { q } ) \right ) , \, \pi _ { p } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } ( p , \bar { q } ) \right ) , \, \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( p , \bar { q } ) \right ) , \, \pi _ { p } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( p , \bar { q } ) \right ) , } \\ { \pi _ { \bar { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r } * } ( \bar { p } , q ) \right ) , \, \pi _ { \bar { p } } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } ( \bar { p } , q ) \right ) , \, \pi _ { \bar { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( \bar { p } , q ) \right ) , \, \pi _ { \bar { p } } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( \bar { p } , q ) \right ) } \\ { \beta _ { r } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { r } * } ( \bar { p } , q ) \right ) , \, \pi _ { \bar { p } } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } ( \bar { p } , q ) \right ) , \, \pi _ { \bar { p } } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( \bar { p } , q ) \right ) , \, \pi _ { \bar { p } } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( \bar { p } , q ) \right ) } \end{array} \right \} ,$$

(rhβ-∞ (p, 9)|, and all (rhr * (p, q)). Then we obtain a lower bound on those area by considering the size of their projection on Tε(p) or Tε(p). So we have:

$$\mathbb { E } \left [ \deg _ { | C N } ( p , D e l ) \right ] & \leq \lambda \int _ { q \in \pi _ { p } ^ { \, 1 } ( V _ { 1 } ( p ) ) } \left ( 2 e ^ { - \lambda | \hslash r _ { r } ^ { \beta _ { * } } \in ( p , q ) | } + 4 e ^ { - \lambda | \tilde { r } _ { r } ^ { \beta _ { * } } \in ( p , q ) | } \right ) d q \\ & + \lambda \int _ { q \in \pi _ { p } ^ { \, 1 } ( V _ { 1 } ( p ) ) } \left ( 4 e ^ { - \lambda | \hslash r _ { r } ^ { \beta _ { * } } \in ( p , q ) | } + 4 e ^ { - \lambda | \tilde { r } _ { r } ^ { \beta _ { * } } \in ( p , q ) | } \right ) d q \\ & \leq \lambda \int _ { ( x _ { q } , y _ { q } ) \in V _ { 1 } ( p ) } \left ( 2 e ^ { - \lambda | \hslash r _ { r } ^ { \beta _ { * } } \in ( p , q ) | } + 4 e ^ { - \lambda | \tilde { r } _ { r } ^ { \beta _ { * } } \in ( p , q ) | } \right ) d x _ { q } d y _ { q } \\ & + \lambda \int _ { ( x _ { q } , y _ { q } ) \in V _ { 1 } ( \overline { p } ) } \left ( 4 e ^ { - \lambda | \hslash r _ { r } ^ { \beta _ { * } } \in ( p , q ) | } + 4 e ^ { - \lambda | \tilde { r } _ { r } ^ { \beta _ { * } } \in ( p , q ) | } \right ) d x _ { q } d y _ { q } .$$


<!-- p:148 -->


(  0 (    (d   (d       m

$$Then we can roughly go from V _ { 1 } ( p ) to \mathcal { T } _ { \varepsilon } ( p ) , \, and from V _ { 1 } ( \bar { p } ) \, to \, \mathcal { T } _ { \varepsilon } ( \bar { p } ) . \\ \mathbb { E } \left [ \deg _ { | \mathbf C } \left ( p , \text {Del} \right ) \right ] & \leq \lambda \int _ { ( \varepsilon , y _ { q } ) \in \mathcal { T } _ { \varepsilon } ( p ) } \left ( 2 ^ { - \lambda | \mathbf r } _ { \bar { r } ^ { * } } \sim ( p , q ) | + 4 e ^ { - \lambda | \bar { r } ^ { * } _ { \bar { r } ^ { * } } \left ( p , q \right ) | } \right ) d x _ { q } d y _ { q } \\ & + \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathcal { T } _ { \bar { \ } } ( \bar { P } ) } \left ( 4 e ^ { - \lambda | \mathbf r _ { * } ^ { * } \infty } + 4 e ^ { - \lambda | \bar { r } _ { \bar { r } ^ { * } } \left ( p , q \right ) | } \right ) d x _ { q } d y _ { q } \\ & \leq \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } \left ( 6 e ^ { - \lambda | \mathbf r _ { * } ^ { * } \infty } + p ; | + 8 e ^ { - \lambda | \bar { r } _ { \bar { r } ^ { * } } \left ( p , q \right ) | } \right ) d x _ { q } d y _ { q } \\ & \leq 6 \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | \mathbf r _ { * } ^ { * } \infty } \left ( p , q \right ) d x _ { q } d y _ { q } + 8 \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | \bar { r } _ { \bar { r } ^ { * } } \left ( p , q \right ) | } d x _ { q } d y _ { q } \\ & \leq 6 \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | \mathbf r _ { * } ^ { * } \infty } \left ( p , q \right ) d x _ { q } d y _ { q } + 8 \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } e ^ { - \lambda | \bar { r } _ { \bar { r } ^ { * } } \left ( p , q \right ) | } d x _ { q } d y _ { q } \\ \intertext { s i n c \, | r h _ { r ^ { * } } ^ { \beta } \sim ( p , q ) | = | r h _ { r ^ { * } } ^ { \bar { \frac { 1 } { 2 } } } \sim ( p , q ) | , \, b e c a u s e i t i s t h e s a m e r g o u p t u o a r tation o f \frac { \pi } { 2 } , \, a n d w e r u s e }$$

since |rhβ-∞(p, q)| = |rh-∞ (p, g)|, because it is the same region up to a rotation of and we reuse Lemma 8.10 in which we need to have an aspect ratio smaller than 1, so:

$$\mathbb { E } \left [ \deg _ { | C N } ( p , D e l ) \right ] & \leq 6 \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } e ^ { - \frac { \lambda } { 1 6 } \sqrt { ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) \left ( ( \frac { 1 } { \beta _ { \infty } } \right ) ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) } } d x _ { q } d y _ { q } \\ & + 8 \lambda \int _ { ( x _ { q } , y _ { q } ) \in \mathbb { R } ^ { 2 } } e ^ { - \frac { \lambda } { 3 2 } \sqrt { ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) \left ( ( \beta _ { r } * ) ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) } } d x _ { q } d y _ { q } . \\$$

We recall it:

Lemma 8.10. Let t &gt; 0, β ∈]0, 1[, and Iβ(t) = ∫R ∫R e−t√(x2+y2)(β2x2+y2)dydx,

$$I _ { \beta } ( t ) = \frac { 1 } { t } I _ { \beta } ( 1 ) \leq \frac { \pi } { t } \left ( 1 + \ln ( \frac { 1 } { \beta } ) \right ) .$$

So that we can finish the computation of the degree:

$$\mathbb { E } \left [ \deg _ { \text {CN} } \left ( p , \text {Del} \right ) \right ] & \leq 6 \lambda I _ { \frac { 1 } { \beta _ { \cdot } \infty } } \left ( \frac { \lambda } { 1 6 } \right ) + 8 \lambda I _ { \beta _ { r ^ { * } } } \left ( \frac { \lambda } { 3 2 } \right ) \\ & \leq 9 6 \pi \left ( 1 + \ln \beta _ { \infty } \right ) + 2 5 6 \pi \left ( 1 + \ln \frac { 1 } { \beta _ { r ^ { * } } } \right ) .$$

But β-∞ = Θ(1), so we can say that:

$$\mathbb { E } \left [ \deg _ { | C N } \left ( p , D e l \right ) \right ] = O \left ( \ln \frac { 1 } { \beta _ { r ^ { * } } } \right ) .$$

##### 13.4.7 On some geometric quantities close to Z.

Among the various bounds that define CN(p), three values regularly return. Up to a constant factor, those three values are √1 − κ1r*, 1=k1r+, and m3,0 tan(θp) We show that they actually have the same asymptotic behavior when p approaches Z. To help us in those computation, we use the global frame, and recall that we assume that up &gt; 0, vp = 0 and wp &lt; 1. Thus the origin (0, 0, 0) of the global frame, is the closest point on Z from p. We write w = fz(u, v) the graph of ε at the origin. From the expression ε: + v2 + (w − 1)2 = 1, we obtain: k2

$$f _ { Z } ( u , v ) = 1 - \sqrt { 1 - \kappa _ { s u p } u ^ { 2 } - v ^ { 2 } } .$$

In this section, since we study the behavior of values when p varies on E, we explicitly write "(p)" in the notations and evaluate κ1(p) and r*(p) when p is close to Z. We recall the different geometric values = (Z  s = (Z  :  Z   t  t Z ) , and κ2(Z) = 1. We start to Ksup :(d (d  − I     lr


<!-- p:149 -->


$$\L L { \text {ma} } \, 1 3 . 1 1 . \ I f \, | u _ { p } | & \leq \frac { 1 } { \sqrt { \kappa _ { \sup } } } , \, t h e n \, \sqrt { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } \leq \sqrt { \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) } u _ { p } . \\ \ I f \, \text {additionallly} \, | u _ { p } | & \leq \frac { 1 } { \sqrt { \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) } } , \, t h e n \, \sqrt { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } \geq \frac { \sqrt { 2 } } { 2 } \sqrt { \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) } u _ { p } .$$

Proof. We use basic geometry to compute the behavior of r*(p). We call c*(p) = (uc* , vc*, w*) the center of the medial sphere at p.

On the side figure, we consider the section of spheroid by the plane v = 0. In that plane, the section of the spheroid can be parameterized by w = f(u) for f(x) = fz(u, 0) = 1 − √1 − κsupu2. In the chosen Monge coordinates system, we have:

$$r ^ { * } ( p ) ^ { 2 } = u _ { p } ^ { 2 } + ( w _ { c ^ { * } } - w _ { p } ) ^ { 2 } .$$

The line (pc*) has equation:

$$( p c ^ { * } ) \colon u + f ^ { \prime } ( u _ { p } ) w = u _ { p } + f ^ { \prime } ( u _ { p } ) w _ { p } .$$

The w coordinate wc* of c* is given by substituting 0 in the place of u in the previous equation:

$$w _ { c ^ { * } } = \frac { u _ { p } } { f ^ { \prime } ( u _ { p } ) } + w _ { p } . \\ \i t u t e { w _ { * } } { \text { in the expression } }$$

m

C*

*

Wp

1.0

Up

n

We substitute wc* in the expression of r*(p):

$$* ( p ) ^ { 2 } & = u _ { p } ^ { 2 } + ( \frac { u _ { p } } { f ^ { \prime } ( u _ { p } ) } + w _ { p } - w _ { p } ) ^ { 2 } \\ & = u _ { p } ^ { 2 } \left ( 1 + \frac { 1 } { f ^ { \prime } ( u _ { p } ) ^ { 2 } } \right ) ,$$

$$\text { but } f ^ { \prime } ( u _ { p } ) = \frac { \kappa _ { 8 u p } u _ { p } } { \sqrt { 1 - \kappa _ { 8 u p } u _ { p } ^ { 2 } } } , \, S O$$

$$r ^ { * } ( p ) ^ { 2 } & = u _ { p } ^ { 2 } \left ( 1 + \frac { 1 - \kappa _ { 8 \cup } u _ { p } ^ { 2 } } { \kappa _ { \sup } ^ { 2 } u _ { p } ^ { 2 } } \right ) \\ & = \frac { 1 } { \kappa _ { \sup } ^ { 2 } } + \frac { \kappa _ { \sup } - 1 } { \kappa _ { \sup } } u _ { p } ^ { 2 } ,$$

$$r ^ { * } ( p ) & = \sqrt { \frac { 1 } { \kappa _ { \sup } ^ { 2 } } + \frac { \kappa _ { \sup } - 1 } { \kappa _ { \sup } } u _ { p } ^ { 2 } } \\ & = \frac { 1 } { \kappa _ { \sup } } \sqrt { 1 + \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } } \\$$

Then we compute an upper bound on κ1(p). Since the line of curvature lies in the plane y = 0, we can use the curvature formula for curves to deduce κ1(p) (see Part I, Chapter 1). In the plane y = 0, the maximal principal curvature at p is given by the formula:

$$\kappa _ { 1 } ( p ) = \frac { f ^ { \prime \prime } ( u _ { p } ) } { ( 1 + ( f ^ { \prime } ( u _ { p } ) ) ^ { 2 } ) ^ { \frac { 3 } { 2 } } } .$$

So we compute the second derivative:

$$f ^ { \prime \prime } ( u _ { p } ) = \frac { \kappa _ { \text {sup} } } { \left ( 1 - \kappa _ { \text {sup} } u _ { p } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } .$$

and, From what we can deduce:


<!-- p:150 -->


$$\tan d e d u c e \colon & & \kappa _ { \sup } & & 1 \\ & \kappa _ { 1 } ( p ) = \frac { 1 } { \left ( 1 - \kappa _ { \sup } u _ { p } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } \frac { 1 } { \left ( 1 + \left ( \frac { \kappa _ { \sup } u _ { p } } { \sqrt { 1 - \kappa _ { \sup } u _ { p } ^ { 2 } } } \right ) ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } \\ & = \frac { \kappa _ { \sup } } { \left ( 1 - \kappa _ { \sup } u _ { p } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } \left ( 1 - \kappa _ { \sup } u _ { p } ^ { 2 } \frac { 1 - \kappa _ { \sup } u _ { p } ^ { 2 } } { 1 - \kappa _ { \sup } u _ { p } ^ { 2 } } \right ) ^ { \frac { 3 } { 2 } } \\ & = \frac { \kappa _ { \sup } } { \left ( 1 - \kappa _ { \sup } u _ { p } ^ { 2 } + \kappa _ { \sup } u _ { p } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } . \\ & = \frac { \kappa _ { \sup } } { \left ( 1 + \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } . \\$$

And then 1 − κ1(p)r*(p) verifies:

$$\text {And then } 1 - \kappa _ { 1 } ( p ) r \left ( p \right ) \text { vertices:} \\ 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) & = 1 - \frac { \kappa _ { \sup } } { \left ( 1 + \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } \kappa _ { \sup } } \frac { 1 } { \sqrt { 1 + \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } } } \\ & = 1 - \frac { 1 } { 1 + \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } } \\ & = \frac { \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } } { 1 + \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } } . \\ \intertext { From where we deduce two bounds: }$$

From where we deduce two bounds:

$$\frac { 1 } { 2 } \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } \leq 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) \leq \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) u _ { p } ^ { 2 } ,$$

where the lower bound holds for u2 ≤ κsup(κsup−1), 1 while the upper bound is always true.

Then we find a lower bound on 1 tan(θp)

Lemma 13.12. If up ≤ 2κsup √2 then tan(θp) 1 ≥ κsupUp·

Proof. On the figure in the previous lemma, θp is the oriented angle from the tangent line of f at p, in green, to the vertical axis, so

$$\frac { 1 } { \tan ( \theta _ { p } ) } & = f ^ { \prime } ( u _ { p } ) \\ & = \frac { \kappa _ { \sup } u _ { p } } { \sqrt { 1 - \kappa _ { \sup } u _ { p } ^ { 2 } } } \text { for } u _ { p } \leq \frac { 1 } { \sqrt { \kappa _ { \sup } } } , \\ & > \kappa _ { \sup } u _ { p }$$

$$\geq \kappa _ { \sup } u _ { p } . \\$$

Note that in a further section, it is cos (θp) that appeared, but around Z, θp is close to and then cos (θp) ∼ tan(θp)·

Finally we find a lower bound on 1 We recall that m3,0(p) is the coefficient in front of the m3,0(p) term x3 in the Monge form of the surface at p.

Lemma 13.13. There exists Mz &gt; 0 such that, if up ≤ √2 then |m3,0(p)| ≤ MZ up. 2κsup


<!-- p:151 -->


∂3 fp Proof. We recall that m3,0(p) = (0, 0) in the Monge coordinate system of p. ∂x3

We consider now the function ñ3,0 defined as follows:

The set Z is defined as the set of points whose medial sphere is the osculating sphere. As seen in Part I, Chapter 1, all points of Z are maxima of curvature in the maximal direction, and this induces that m3,0(Z) = 0 (where m3,0(Z) corresponds to m3,0(p) for p ∈ Z).

$$\tilde { m } _ { 3 , 0 } \colon & \ \mathbb { R } \to \mathbb { R } , \\ & u _ { p } \mapsto m _ { 3 , 0 } ( p ) .$$

Since ε is at least a C4 surface, we can see ñ3,0 as a continuous function whose derivative is bounded on [0, √2 —]. We denote by MZ the value: 2κsup

$$M _ { 4 } ^ { Z } = \sup _ { u _ { p } \in [ 0 , \frac { \sqrt { 2 } } { 2 \kappa _ { 8 } u _ { p } } ] } \left | \frac { \partial \tilde { m } _ { 3 , 0 } } { \partial u } ( u _ { p } ) \right | .$$

That is enough to write that, if up ≤ √2 then: 2ksup

$$| m _ { 3 , 0 } ( p ) | = | \tilde { m } _ { 3 , 0 } ( u _ { p } ) - \tilde { m } _ { 3 , 0 } ( 0 ) | \leq M _ { 4 } ^ { Z } u _ { p } .$$

□

We finish the section by evaluating the size of CN(p). As long as p is far enough from Z, 1 − κ1(p)r*(p) is strictly positive, and it is clear that CN(p) corresponds to two rectangles on E of size Ω(1) × Ω(1). But if p is close to Z, we can apply the results above to evaluate the size of CN(p). We consider all quantities involved in CN(p), and evaluate them around Z:

$$\bullet \ \sqrt { 1 - \kappa _ { 1 } r ^ { * } } \geq \frac { 1 } { 2 } \sqrt { \kappa _ { \sup } ( \kappa _ { \sup } - 1 ) } u _ { p } = \Omega ( u _ { p } ) .$$

- κsup(Ksup−1)u2 1−κ1r* ≥ 114 = Ω(up). |m3,0| M4 up
- T 1 ≥ κsupup = Ω(up).

So we deduce that close to Z, CN(p) corresponds to two rectangles on ε of size Ω(up) × Ω(u2).

##### 13.4.8 On the probability of existence Delaunay neighbors outside CN(p).

We prove now Lemma 13.2 using Lemma 13.7 applied to the size of CN(p). We recall the value of the quantity γ:

$$\gamma \colon = \min \left ( \frac { \sqrt { 2 } } { 8 } \frac { \kappa _ { \inf } } { \kappa _ { \sup } } \delta , \frac { \delta } { 3 2 } , \frac { \delta } { 4 } \cos \theta _ { p } \right ) .$$

The value √2γ corresponds to the length of the diameter of the isosceles triangles of Fγ (p).

Lemma 13.7. Let 0 ≤ δ ≤ √2 . Let X be a data sample distributed on E and, p and q in X. If q is at 2κsup distance greater than δ from σ*(p) and if (p, q) is an edge of Del(X), then (p, q) is an edge of G Fγ (X). If X is a Poisson point process distributed on E with intensity λ, the probability that the point p ∈ X has some Delaunay neighbors at a distance greater than δ from σ*(p) is smaller than 16e−λ&gt; √2

We consider the intermediate lemma:

Lemma 13.14. Let X be a data sample distributed on ε and, p and q in X. If q ∈ CN(p), and if (p, q) is an edge of Del(X), then:

$$\bullet \ i f \, u _ { p } \leq \frac { 1 } { 2 \kappa _ { \text {sup} } } , \, ( p , q ) \ i s \ a n \ e d g e \ o f \, \overrightarrow { \mathcal { \mathcal { G } } } _ { \mathcal { F } _ { 0 } ^ { \Theta ( u _ { p } ^ { \delta } ) } } ^ { \to } ( X ) ,$$


<!-- p:152 -->


$$\bullet \ i f \, u _ { p } \geq \frac { 1 } { 2 \kappa _ { s u p } } , \, ( p , q ) \ i s \ a n \ e d g e \ o f \, \overrightarrow { \mathcal { G } } _ { \mathcal { F } _ { 0 } ^ { \Theta ( 1 ) } } ^ { \emptyset } ( X ) .$$

Proof. We consider that p is a point in Z+ 2κsup . We recall that V1 (p) is a rectangle with size Ω(up) ×Ω(u2). Consider any positive number 0 &lt; δ &lt; 2k/sup . In Section 13.3, we proved that πp (B+δ(σ*) ∩ ε) is included in the ellipse:

$$\frac { 1 } { 3 } ( 1 - \kappa _ { 1 } r ^ { * } ) x ^ { 2 } + \frac { 1 } { 3 } ( 1 - \kappa _ { 2 } r ^ { * } ) y ^ { 2 } \leq 3 \delta r ^ { * } .$$

For δ = Θ (u4), the ellipse has great axis 6ν 1−κ1r* δr* = 0 up = O(up), and small axis 6V 1−κ2r* δr* O(u2). Since it corresponds to the order of magnitude of V1(p), if q ∉ CN(p) then q is at distance greater then Θ (u4) from σ*. It follows, by Lemma 13.7, that if q ∉ CN(p) and if (p, q) is an edge of Del(X), then (p, q) is an edge of o (X). Fθ(u5) F0

If p is not close to Z, the quantities up, √1 − κ1r*, and γ are Θ(1), so if q outside CN(p) and if (p, q) is an edge of Del(X), then (p, q) is an edge of □

We prove the following lemma that quantity the probability that p has a neighbor outside CN(p):

Lemma 13.2. Let E be an oblate spheroid, p a point of E, and X a point set on E whose restriction to the close neighborhood of p is a Poisson point process with intensity λ. The probability that p has a neighbor in Del(X ∪ {p}) outside the close neighborhood of p is:

$$\begin{array} { r } { \left \{ \begin{array} { l l } { e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \, i f \, u _ { p } \leq \frac { 1 } { 2 \kappa _ { s u p } } , } \\ { e ^ { - \Omega ( \lambda ) } \, o t h e r w i s e . } \end{array} } \end{array}$$

Proof. The lemma is then a direct consequence of Lemma 13.14 since, for any γ, the regions of F have area Θ (γ2). □

#### 13.5 Expected degree of a point close to Z (Proof of Lemma 13.3).

In that section, we compute an upper bound on the expected degree of points p close to Z, i.e. in Z+ 2κsup , but we recall that we assume that in the global frame, p has coordinate (up, 0, wp) with 0 &lt; up &lt; 2κsup and wp &lt; 1.

We say that q is a middle-range point of p, if

- q ∉CN(p),
- |uq| &gt; |up|,
- ≤|ba| · √2-1 and 2κsup
- either |uq − up| ≤ √2-1 &gt; |αn − bn| .Io √2-1 2κsup 2κsup

We denote this neighborhood by MNR(p). It corresponds to the reunion of two axis-aligned rectangles of constant size, with p and p on their boundary. For any p ∈ Z+2ssup , a point q in MNR(p) verifies |uq| ≤ √2 2κsup

We prove that the expected number of middle-range neighbors of p in Del ({p} U X) is ln(λ)e−u10Ω(λ) for a Poisson point process X with intensity λ. This neighborhood is enough for the global enumeration of the edges since instead of counting an edge twice, one can charge it on a chosen endpoint. In that case, the edges are charged on the closest point to Z. Note that the case of an edge whose endpoints are equidistant from Z happens with probability 0 in a Poisson point process, so we do not develop it.


<!-- p:153 -->


##### 13.5.1 Description of fundamental regions on the spheroid

In that section, any point q we consider verifies wq &lt; 1, in other words, q is in the lower part of the spheroid. This is a largely necessary condition for q being a middle-range point of p. We denote by Ew&lt;1 the part of the spheroid such that w &lt; 1. Note that if we relax the hypotheses up &gt; 0, vp = 0, wp &lt; 1, the condition q ∈ Ew&lt;1 becomes: p and q lie in a common quarter of the spheroid.

We call parallel an intersection curve of E with a vertical plane of equation u = upar for — 1 k, and meridian an intersection curve of ε with a plane passing through the axis of revolution of ε. To clarify any misunderstanding, "horizontal" and "vertical" refer to w axis, to which a horizontal line is or orthogonal and a vertical line is parallel. In Ew&lt;1, meridians and parallels intersect exactly in one point.

We describe now a graph which we will be proven to be a super-graph of the Delaunay triangulation. This super-graph is defined for each pair (p, q) such that q ∈ Ew&lt;1, by a family F2(p, q) of regions on ε. We make a distinction between the case where p and q lie in the same side with respect to Z and the other. We describe then six regions that will provide a super-graph to the Delaunay triangulation.

First, we assume that p and q are in the same side of Z. We consider Tr(p, q), the trapezoid-like shape on ε delimited in Ew&lt;1 by the parallels and meridians of p and q. We name q1 and q2 the two other vertices of Tr(p, q), q1 at the intersection of the meridian of p and the parallel of q, i.e. in the direction of κ1, and q2 at the intersection of the parallel of p and the meridian of q, in the direction of κ2. Then we search for a curve inside Tr(p, q) that divides it into two regions of almost same area. A good candidate for this curve is the section of E with the plane PDiag passing through p and q and perpendicular to the plane of equation w = 0. We call dg(p, q) the part of the curve that is inside Tr(p, q). We call T1(p, q) the part with q1 for third vertex, in addition to p and q, and T2(p, q) the part with q2 for third vertex. To be clear with the notations, we have Tr = T1 ∪ T2. We also consider their symmetrical regions with respect to PMed, on the other side of Z: T1(p, q) := T1(p,  ̄) and T2(p, q) := T2(p,  ̄). Finally, we define the two last regions A(p, q) and A(p, q). To explain them, we consider the sphere passing through p, p , q,  and centered in the plane u = 0. We name this sphere σNorm and consequently rNorm the intersection of B(σNorm) with ε. A is the intersection of rNorm with the half-space delimited by PMed containing q e  a  o   '  o o a {0 = }   o-a  s e ovoid shape, the one that does not pass through q. A is the symmetrical of A with respect to PMed. See Figure 13.7-left for a summary of the six regions.

That dealt with the case where p and q are on the same side of Z. We consider now the other case, where p and q are on both sides of Z. Remember that it is not necessary to consider the case uq &lt; |up| because we can assume that an edge between p and q is charged on the closest point from Z. Thanks to the symmetries, we can reuse the exact same regions, i.e. if p and q are on both sides of Z, r(p, q) := r(p, q) for each region r among the six described above. See Figure 13.7-right.

In the end, we therefore count exactly six regions on ε, four in RT = {T1, T2, T1, T2} and two in RA = {A, A}. They define the family F2:

$$\mathcal { F } _ { 2 } = R _ { T } \cup R _ { A } .$$

##### 13.5.2 Choice of specific spheres

In order to show that the graph based upon those regions is a super graph of the Delaunay triangulation for pairs of points in a common quarter, we have to show that for any sphere σ passing through two points p and q, the intersection B(σ) ∩ ε contains at least one of the six regions of F2(p, q). Such a sphere can be parameterized by its center in PBis. We start by introducing, for a pair (p, q) of points, the specific lines and centers we will use to partition PBis. We name LTr the axis of the circumscribing circle of the cocyclic vertices of Tr(p, q), we label this line with "Tr" because all spheres centered on LTr passes through the vertices of Tr(p, q). We name Lsym the line of centers of spheres passing through p, q, p and ā, named after the fact that all of the intersections of such spheres with surface are symmetrical with respect to PMed. Note that LSym = PBis ∩ PMed.

Remember that for a center named clabel on PBis, we denote by σlabel the sphere centered on clabel passing through p (and q) and rlabel the intersection B(σlabel) ∩ ε. We describe those centers, their associated spheres, and, through claims, the fundamental regions of F2 the sphere contains. Most claims call on convexity-like properties on the spheroid stated here:


<!-- p:154 -->


Figure 13.7: The six fundamental regions of F2, they are delimited by the meridians and parallels of p, q, p and q, by the diagonals dg and dg and by the sphere σNorm. Left: when p and q are on same side of Z. Right: when p and q are on both sides of Z.

u


q1

w


v

A

Pi

p:

p2

T2

A

T1

q1

Proposition 13.15. Let a and b be two distinct points on Ew&lt;1 and σ a sphere centered on c ∈ PMed such that wc ≤ 1 and {a, b} ⊂ B(σ).

1. If a and b are on the same parallel, let [a, b]par be the part of the parallel between a and b inside Ew&lt;1. Then B(σ) contains [a, b]par.
2. If a and b are on the same meridian and on the same side of PMed, let [a, b]mer be the part of the meridian between a and b inside Ew&lt;1. Then B(σ) contains [a, b]mer and [ā, b]mer.

####### Proof.

1. We have a look in the plane P containing the parallel passing through a and b in which the cut of σ is a circle. Since {a, b} ∈ B(σ) ∩ P, then either ε∩ P ⊂ B(σ) ∩ P and it is done, either the two circles σ ∩ P and ε ∩ P have at most two intersections points. Since wc ≤ 1, the closest point h on E ∩ P to c also verifies wh ≤ 1. Note that the figure in P is symmetrical with respect to the line (ch). Because ε∩ P is a circle, for a point p on ε ∩ P, the distance dist(c, p) is continuously growing when p goes from h to its opposite on ε ∩ P. Thus, since a ∈ B(σ), [h, a]par lies completely inside B(σ) ∩ P, and so inside B(σ). The same holds for [h, b]par, and consequently for [a, b]par since both a and b verify w &lt; 1.
2. We have a look in the plane P containing the meridian passing through a and b in which the cut of σ is still a circle. The section by P contains the ellipse E∩P, the circle σ∩P and the line PMed∩P, passing through hn r   o  or o nrs o o orf ε, namely, a, b, ā and b. In view of the only possible configurations (see side figure), we can deduce that the whole part of the meridian between two points included in B(σ) on the same side of ε with respect to PMed remains included in B(σ). In other words B(σ) contains [a, b]mer and [ā, b]mer.

w

w = 1

b

a

w

u

We list here seven centers of spheres and as many claims that state which regions of F2 are inside the associated sphere. We provide two figures for each, on the left, the case where p and q, the red points are on the same side of Psym, and on the right, where p and q on both sides. Note that the regions depends on the positions of p and q that we chose quite generically on ε. Without loss of generality, we assume that vq &gt; 0. (We preferred to show figures, projected in the w direction viewed from below.)


<!-- p:155 -->


- The center csym is the intersection of LTr with Lsym, the sphere σsym passes through p and q, and also through q1, q2, p, and q.

Claim a. B(σsym) contains Tr and Tr.

u↑

u

w


v

T1

T

T2

p:

T2


T1


Note that depending on the position of q with respect to p, the intersection rsym can have one or two connected components.

Proof of Claim a. First we prove that csym has w coordinate wsym smaller than 1. Consider the center c = (0, 0, 1) of the spheroid, and the sphere centered at c passing through q. Note that it also passes through q by symmetry, and through q1 and  ̄1 by revolution. It does not contain p, because the spheroid is oblate and |up| &lt; |uq|. Then we move c in the w direction and maintaining contact with q and q1 until the sphere touches p. By symmetry with the bisector plane of q and q1 (one of the two bisector planes of the meridians of p and of q), σ also passes through q2. This sphere is σsym. Since wp &lt; wq, c moves downward. Thus wsym &lt; 1. We consider the case where p and q are on same side. By Proposition 13.15, since [p, q1]par and [q, q2]par are inside B (σsym). And by the same proposition any meridian part from [p, q1]par to [q, q2]par is also in pthσsym. Therefore, B(σsym) contains Tr(p, q). By symmetry it contains also Tr(p, q). And by symmetry again, the claim holds when p and q are on both sides of Z.

- The center cNorm is the center of the sphere σNorm, that passes through p and q and also passes through p and q, and is symmetric with respect to u = 0 and v = 0. It lies on Lsym.

Claim b. B(σNorm) contains T1, T1, A and A.

u↑

u

w

0

w

v

A

T1

y

T

p:

P

A

T1

A

T1

Proof of Claim b. We consider the case where p and q are on same side. We first prove that dg(p, q) is inside B(σNorm).


<!-- p:156 -->


We can define σNorm in another way: consider the sphere passing through p and p and that is tangent to E, it is the medial sphere of p, then send up its center upward (along the w coordinate) while maintaining the contact with p and p. That generates a pencil of spheres. Since |up| &lt; |uq|, at some point the sphere touches q (and q at the same time), this sphere is σNorm. The spheres of the pencil just described contain a common circle C.

w

EDiag

CNorm

p

Consider the section with the plane PDiag. The intersection EDiag with ε is an ellipse whose great axis is parallel to the w axis, the intersection with C is {p, p'} where p′ is inside EDiag since the medial sphere is inside ε, and the intersection with σNorm is a circle CNorm passing through p, q, p'. Since the axis of the pencil is directed by w, p and p' have the same z coordinate, and since p′ is inside EDiag, the center c' of CNorm, that is the orthogonal projection of cNorm on PDiag, is on the same side of p with respect to the great axis of EDiag. Now consider the bisector line of [p, q]. Its intersection with the great axis of EDiag is the center of a sphere that contains dg(p, q) by Proposition 13.15-2. Consider the pencil of circles passing though p and q, from the one described above and whose center progresses along the bisector line toward c'. By the self-intersecting structure of such a pencil, and by convexity of EDiag, it is clear that CNorm contains dg(p, q) (in red on the side figure.) (It can also be seen in the context of the Partition lemma.)

The whole region T1 is then completely included in B(σNorm) by Proposition 13.15 since q1 ∈ B(σNorm).

From its side, the region A is included in B(σNorm) by definition.

Here again, the conclusion holds when q is on the other side, by symmetry.

We complete this set of spheres with centers at infinite directions. We denote them with a ∞ (possibly signed) at the exponent. Keep in mind that such spheres are then degenerated into planes and thus the intersection with E are ellipses.

- cx, at the infinite extremity of Lsym, such that B(σx) does not contain q. The plane bounding B(σx) passes through p and q and also passes through q1 and q2.

Claim c. B(σx) contains Tr.

w

u

w

Proof of Claim c. Remind that σx is centered at the infinite extremity of LTr toward the external part of ε.

As said above, σx is the plane passing through p, q, q1, and q2. So B(σx) ∩ε is the interior of the ellipse passing through those four points. By convexity of the ellipse, B(σx) ∩ε contains Tr.

- ∞ and +∞ at the infinite extremity of respectively [cNorm, csym) and [csym, cNorm), the plane Sym, bounding B(σsy∞) and B(σ passes through p and q and also passes through p and ī. Sym


<!-- p:157 -->


Claim d. B(σ +∞ contains A and A. Sym

u

w


A

À

A

contains the whole part defined by {yyq &lt; 0 and |x| &gt; |xp|}. This region clearly contains A and A.

contains T2 and T2.

w⊗

w

T2

Proof of Claim e. Whether p and q are on the same side or not, it is clear that dg and dg are inside □

- passes through p and q and is symmetrical with respect to the plane v = 0.

Claim f. B(σxan) contains Tr and A.

w


T.

T2

À

T1

Proof of Claim f. This one is clear considering that B(σxan) contains the whole part of ε delimited by the parallel of p and containing q. □

- 8 , at the infinite extremity of the normal direction of PDiag, such that B(σDiag) contains q1.


<!-- p:158 -->

Claim g. B(σDiag) contains T1 and A.

u↑

w

u

A

T1

Proof of Claim g. σPiag is the plane PDiag, and B(σDiag) the half-space containing q1, so, if p and q are on the same side of PMed it is clear that B(σDiag) contains T1 and A. If p and q are on both □

##### 13.5.3 Proof of the graphs inclusion

Now we prove, using the Partition lemma, that the empty region graph GF2 based upon the regions of F2 is indeed a super graph of the Delaunay triangulation, for all pairs of points that lie in a common quarter of ε where we call a quarter an angular sector of measure from the axis of revolution of ε.

Lemma 13.16. Consider an oblate spheroid E embedded in R3 and a data sample X distributed on E. Let p and q two points of X in a comon quarter, and such that p is closer to Z than q. If (p, q) is an edge of Del(X), then it is an edge of (X). F2

Proof. Let p and q be two points on a common quarter E. Without loss of generality, assume that p is the closest to Z, and consider the frame used in the claims. We have to show that if a sphere passes through p and q, it contains at least one the six regions of F2(p, q).

Figure 13.8: The bisector plane of p and q partitioned for F2. For example, any sphere passing through contains T1.

A, A

Sym

+∞

cxan

T1, T1, A, A

cDiag

T1

CNorm

VT

cSym

T1, T2, T1, T2

T1

T2


0 = m

m

∞

cx

T2, T2

T1, T2

We prove this by partitioning PBis. The partition chosen is the following: (see Figure 13.8). PBis is separated into two half-planes by Lsym on which are csym and cNorm. This line separates the centers into

u

w

v


<!-- p:159 -->


those whose sphere contains either T1, T2 or A and those whose center contains either T1, T2 or A. We complete the partition by the rays from csym to cT, and from cNorm to cDiag, in the side of q, and by the rays from csym and cNorm to cTan. This partition provides six tiles, each of them is associated with one of the six regions of F2 by the following relation: Let σ be a sphere centered on c and passing through p and q:

- if c ∈ (csym, CSym, cx), then T2 ∈ B(σ),
- if c ∈ (cDiag, CNorm, csm), then A ∈ B(σ), +∞
- if c ∈ (csy∞, CNorm, Cxan), then A ∈ B(σ),
- if c ∈ (cxan, Norm, CSym, cxan), then T1 ∈ B(σ), and
- if c ∈ (cxan, CSym, C ̄y∞), then T2 ∈ B(σ).

This is a direct consequence of the Claims a-g and of the Partition lemma. Finally, suppose that (p, q) is an edge of Del(X), then it exists an empty sphere passing through p and q, but this sphere is centered in one of the six tiles so the sphere contains one the six regions of F2, and that region is, in turn, also (X) for F2 pairs of points that lie in the same quarter. □

##### 13.5.4 Computation of an upper bound on the expected degree

,(X) is therefore a super-graph of Del(X) for pairs in a same quarter, we can get an upper bound on the expected degree of middle-range neighbors of points close to Z. We recall that we place the spheroid in the global coordinate system, and without loss of generality, assume that up ≥ 0, vp = 0 and wp &lt; 1. We recall that a middle-range neighbor q verifies

- q ∉CN(p),
- |uq| &gt; |up|,
- |vq| ≤ √2-1 , and 2κsup
- either |uq − up| ≤ √2-1 &gt; |dn − bn| Io √2-1 2κsup 2κsup

At this stage we can go to the proof of Lemma 13.3.

Lemma 13.3. Let E be an oblate spheroid, p a point of Z+ 2κsup , and X a Poisson point process distributed on E with intensity λ. The expected number of middle-range neighbors q of p in Del(X ∪ {p}) is:

$$O ( \ln \lambda ) e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } .$$

Proof. Consider X a Poisson point process on E, we bound the expected number of middle-range neighbors of p in Del(X ∪ {p}), noted E [deg|MRN (p, Del)].

To be a middle-range Delaunay neighbor of p, a point q must be a neighbor of p in 2(X) and a s ss     s   ( s on s s    s s d CN(p), then if (p, q) is an edge of Del(X), then it is an edge of G θ(u5) (X).

With this in mind, we can compute an upper bound on the expected degree:

$$\text {with this in mind, we can compute an upper bound on the expected
 } \\ \deg _ { | M R N } ( p , Del ) = \sum _ { q \in X \cap M R N ( p ) } \mathbb { 1 } _ { [ ( p , q ) \in Del ( X \cup \{ p ) ] } \\ \leq \sum _ { q \in X \cap M R N ( p ) } \mathbb { 1 } _ { [ ( p , q ) \in \widehat { \mathcal { G } } _ { F _ { 2 } } ^ { \circ } ( X ) \cap \widehat { \mathcal { G } } ^ { \circ } } \\$$


<!-- p:160 -->


since both are super-graph of Del in MRN(p), and then by Slivnyak-Mecke:

$$\mathbb { E } \left [ \deg _ { | M R N } \left ( p , D e l \right ) \right ] \leq \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ ( p ,$$

since both are super-graph of Del in MRN(p),

$$\mathbb { E } \left [ \deg _ { | M R N } \left ( p , \text {Del} \right ) \right ] & \leq \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { 2 } } ^ { 0 } ( X ) \left | ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { 0 } ^ { ( e , u _ { p } ) } } ^ { 0 } ( X ) \right ] \mathbb { P } \left [ ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { 0 } ^ { ( e , u _ { p } ) } } ^ { 0 } ( X ) \right ] \text {d} q \\ & \leq \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { 2 } } ^ { 0 } ( X ) \left | ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { 0 } ^ { ( e , u _ { p } ) } } ^ { 0 } ( X ) \right ] e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \text {d} q \text { by Lemma 13.2.}$$

Θ(us) unfortunately makes this probability greater than P [(p, q) ∈  F2 (X)]. To of an empty region in F0 cope with this difficulty we introduce a new family of regions:

$$\mathcal { F } _ { 2 } ^ { * } ( p , q ) \colon = R _ { T } ( m , q ) \cup R _ { A } ^ { * } ( p , q )$$

where

- m is the point on Ew&lt;1 such that (um, vm) = (−(up + uq), −vq). RT(m, q) is then a set of smaller triangles on E.

$$\bullet \ R _ { A } ^ { * } ( p , q ) = \{ A ( p , q ) \ \vee \ F _ { 0 } ^ { \Theta ( u _ { p } ^ { 5 } ) } ( p )$$

Θ(up) The regions of F2 (p, q) and F0 (p) are now disjoint (see Figure 13.9) and then the event "(p, q) ∈ GF2 (p, q) ∈ G0 Θ(u5) 79 " F0

q

m

Up

Figure 13.9: The new family of regions F2 (p, q), in oange. (p) is the set of 8 triangles around p (in green), since they have radius O(u), and since q is utside CN(p), the point m is well outside F0 (p). Thus F2 (p, q) andEou(p)aro.well.-disjoint.Or-tis-figu,weonlyrepresent the part u &gt; 0, but the ,θ(u5) same occurs for u &lt; 0.


<!-- p:161 -->


Then we obtain:

$$Then we obtain: \\ \mathbb { E } \left [ \deg | _ { M R N } \left ( p , \text {De} \right ) \right ] & \leq c ^ { - u _ { p } ^ { 0 } \Omega } \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ \left ( p , q \right ) \in \mathcal { G } _ { \Sigma _ { R } ^ { * } ( X ) } ^ { 0 } \right ] d q \\ & = e ^ { - u _ { p } ^ { 0 } \Omega } \lambda \left \langle \lambda \right \rangle \int _ { q \in M R N ( p ) } \mathbb { P } \left [ \mathbb { r } \in \mathcal { F } _ { 2 } ^ { * } ( p , q ) , \ r \cap X = \emptyset \right ] d q \\ & \leq e ^ { - u _ { p } ^ { 0 } \Omega } \lambda \left \langle \lambda \right \rangle \int _ { q \in M R N ( p ) } \sum _ { r \in \mathcal { F } _ { 2 } ^ { * } ( p , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] d q \\ & = e ^ { - u _ { p } ^ { 0 } \Omega } \lambda \left \langle \lambda \right \rangle \int _ { q \in M R N ( p ) } \left ( \sum _ { r \in \mathcal { F } _ { 2 } ^ { * } ( p , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] + \sum _ { r \in R _ { T } ( m , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] \right ) d q \\ & = e ^ { - u _ { p } ^ { 0 } \Omega } \lambda \left ( \lambda \int _ { q \in M R N ( p ) } \sum _ { r \in R _ { T } ( p , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] + \lambda \int _ { q \in M R N ( p ) } \sum _ { r \in R _ { T } ( m , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] \right ) d q \\ & = e ^ { - u _ { p } ^ { 0 } \Omega } \lambda \left ( \mathbb { E } \left [ \deg | _ { M R N } \left ( p , \vec { G } _ { R } \right ) \right ] \right ) + \lambda \int _ { q \in M R N ( p ) } \sum _ { r \in R _ { T } ( m , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] d q \right ) . \\ \intertext { B y L mma 11 . 4 , s i n c R a $ I $ a s is the reunion of two growingi g r e n g i o n s , we have: }$$

By Lemma 11.4, since R* is the reunion of two growing regions, we have:

$$\mathbb { E } \left [ \deg _ { | M R N } ( p , \text {Del} ) \right ] & \leq e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + \lambda \int _ { q \in M R N ( p ) } \sum _ { r \in R r ( m , q ) } \mathbb { P } \left [ r \cap X = \emptyset \right ] d q \right ) \\ & = e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + \lambda \int _ { q \in M R N ( p ) } \sum _ { r \in R t ( m , q ) } e ^ { - \lambda | r | } d q \right ) \\ \intertext { T h e w use the graph of the lower part of the spheroid: }$$

Then we use the graph of the lower part of the spheroid:

$$f _ { Z } ( u , v ) = 1 - \sqrt { 1 - ( \kappa _ { \sup } u ^ { 2 } + v ^ { 2 } ) } ,$$

as a variable substitution. With that parameterization, a surface element is given by:

$$\left \| \left ( \frac { \partial f _ { Z } } { \partial u } , \frac { \partial f _ { Z } } { \partial v } , 1 \right ) \right \| = \sqrt { \left ( \frac { \partial f _ { Z } } { \partial u } \right ) ^ { 2 } + \left ( \frac { \partial f _ { Z } } { \partial v } \right ) ^ { 2 } + 1 } .$$

Since p ∈ Z+2κsup , any q ∈ MRN(p) verifies |uq| &lt; √2 and then it is clear that 2κsup max ∂fz (uq, vq)|, ∂fz z (uq, vq))2 2 十 ∂fz (uq, vq)) 2 + 1 ≤ √3. So: ∂u ∂u ∂v

$$\mathbb { E } \left [ \deg _ { | M R N ( p ) } \left ( p , \text {Del} \right ) \right ] \leq e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + \sqrt { 3 } \int _ { q \in M R N ( p ) } \sum _ { r \in R _ { T } ( m , q ) } e ^ { - \lambda | r | } \, d v _ { q } d u _ { q } \right ) .$$

Now we compute a lower bound on |r(p, q)| for r ∈ RT(m, q). We consider the orthogonal projection π0 on the plane w = 0. Since any region has a greater area than its orthogonal projection, it is clear that |r(p, q)| ≥ |π0(r(p, q))|. Since π0(T1(m, q)) is an axis-aligned right rectangle whose hypotenuse has vertices p and q, we get:

$$| T _ { 1 } ( m , q ) | \geq | \pi _ { 0 } ( T _ { 1 } ( m , q ) ) | = \frac { 1 } { 8 } | ( u _ { q } - u _ { p } ) ( v _ { q } - v _ { p } ) | = \frac { 1 } { 8 } | u _ { q } - u _ { p } | | v _ { q } | .$$


<!-- p:162 -->


Because the region T2(p, q) is delimited by a two dimensional ellipse embedded in R3, its projection remains convex and we can assume that |π0(T1(m, q))| ≤ |π0(T2(m, q))|, and so:

$$| T _ { 2 } ( m , q ) | \geq \frac { 1 } { 8 } | u _ { q } - u _ { p } | | v _ { q } | .$$

The same inequalities hold for T1(m, q) and T2(m, q).

We recall q ∈ MNR(p) implies to |uq| &gt; |up|, |vq| ≤ √2-1 and either |uq − up| ≤ √2-1 or |uq − up| ≤ 2κsup 2κsup √2-1 Thus we finally obtain: 2κsup

$$\mathbb { E } \left [ \deg _ { | M R N } ( p , \text {Del} ) \right ] \leq e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + 2 \sqrt { 3 } \lambda \sum _ { \substack { | u _ { q } | > | u _ { p } | \\ | v _ { q } | \leq \frac { \sqrt { 2 } } { 2 \xi _ { \sup } } 1 } } 4 e ^ { - \lambda | T _ { 1 } ( m , q ) | } \, d v _ { q } d u _ { q } \right )$$

where we went from the condition "either |uq − up| ≤ √2-1 or |uq − up| ≤ √2-1" to "|uq − up| ≤ √2-1" 2κsup 2κsup 2κsup by adding a factor 2 in front of the interal,

$$E \left [ \deg _ { | M R N } \left ( p , D \right ) \right ] & \leq e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + 8 \sqrt { 3 } \lambda \right ) \int _ { | u _ { q } | > | u _ { p } | } e ^ { - \lambda | \xi _ { 1 } ^ { 1 } u _ { q } - u _ { p } | | v _ { q } | } \, d v _ { q } d u _ { q } \\ & \leq e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + 8 \sqrt { 3 } \lambda \right ) \int _ { 0 } ^ { 2 } e ^ { - \lambda | \xi _ { 1 } ^ { 1 } u _ { q } | ^ { a } } \, d v _ { q } d u _ { q } ^ { \prime } \, \text {by} \, \rho \, \text {posing} \, u ^ { \prime } = u _ { q } - \mathcal { U } _ { p } , \\ & = e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + 1 6 \sqrt { 3 } \lambda \int _ { \real ^ { 0 } _ { 0 } } ^ { \frac { 2 } { 2 } 1 } \int _ { 0 } ^ { \frac { 2 } { 2 } 1 } e ^ { - \lambda | \xi _ { 1 } ^ { 1 } v _ { q } | } \, d v _ { q } d u _ { q } ^ { \prime } \right ) \\ & = e ^ { - u _ { p } ^ { 1 0 } \Omega ( \lambda ) } \left ( 2 + 1 6 \sqrt { 3 } \lambda \int _ { \real ^ { 2 } _ { 0 } } ^ { \frac { 2 } { 2 } 1 } \frac { \sqrt { 2 } - ( \frac { \lambda } { 2 } ) } { \sqrt { 2 } \xi _ { p } } \left ( \frac { \lambda } { 2 \xi _ { p } } \right ) , \\ \intertext { w h e r e } \text {where } I _ { L } ( t ) = \int _ { 0 } ^ { L } \int _ { 0 } ^ { L } e ^ { - t x y } d y d x \leq \frac { 1 } { 4 } \left ( 1 + \ln ( t L L ) \right ) \left ( y \text { Lemma } 8 . 5 \right ) ,$$

where IL,l(t) = fL fl e−txydydx ≤ 1 (1 + ln(tLl)) (by Lemma 8.5),

$$\mathbb { E } \left [ \deg _ { | M R N } ( p , \text {Del} ) \right ] & \leq e ^ { - u ^ { 1 0 } \Omega } ( \lambda ) \left ( 2 + 1 6 \sqrt { 3 } \lambda \frac { 8 } { \lambda } \left ( 1 + \ln \left ( \frac { ( 3 - 2 \sqrt { 2 } ) \lambda } { 3 2 ^ { \mu } \sup } \right ) \right ) \right ) \\ & \leq e ^ { - u ^ { 1 0 } \Omega } ( \lambda ) \left ( 2 + 1 2 8 \sqrt { 3 } + 1 2 8 \sqrt { 3 } \ln \left ( \frac { ( 3 - 2 \sqrt { 2 } ) \lambda } { 3 2 ^ { \kappa } \& \sup } \right ) \right ) \\ & = O \left ( \ln \lambda \right ) e ^ { - u ^ { 1 0 } \Omega } ( \lambda ) .$$

##### 13.5.5 On the probability of existence Delaunay neighbors outside MRN(p).

We finish this chapter by proving that, for a point p ∈ Z+ 2κsup , a far Delaunay neighbor of p has little chance of existing. The lemma is the following:


<!-- p:163 -->


Lemma 13.4. Let E be an oblate spheroid, p a point of Z+ 2κsup , and X a Poisson point process distributed on E with intensity λ. The expected number of far neighbors of p in Del(X ∪ {p}) is:

$$\lambda e ^ { - \Omega ( \lambda ) } .$$

Proof. Consider a point q in FN(p). The point here is that, since MRN(p) has a size bounded from below by a constant, then there exists δ &gt; 0 such that min (dist(p, q), dist(p, q)) &gt; δ and any sphere passing through p and q has a not empty intersection with the surface.

We call disk of radius t on E, the intersection of E with a ball or radius t centered on E for a t small enough such that the disks are actual topological disk. Let call rδ the radius such that any sphere σ passing through and p and q contains a disk on ε of radius rs. Because of what we just said, rδ is strictly positive.

As seen in Chapter 5, we can consider a maximal disjoint set Mδ on E of a finite number mδ of disks number of far neighbors of p in Del(X ∪ {p}):

$$number of \tan b h o r s \, & \, p \, \text {in} \, D ( X \cup \{ p \} ) ; \\ & \, \mathbb { E } \left [ \deg _ { \text {rn} } ( p , D ) \right ] = \lambda \int _ { q \in F ( \text {pn} ) } \mathbb { P } \left [ ( p , q ) \in D ( X \cup \{ p \} ) \right ] d q \, \text {by Slivnyak-Mecke theorem,} \\ & \quad = \lambda \int _ { q \in F ( \text {pn} ) } \mathbb { P } \, \exists \, \text {passing through $p$ and $q$ such that $\mathcal{B}(\sigma) \cap X = \emptyset$} \, d q \\ & \quad \leq \lambda \int _ { q \in F ( \text {pn} ) } \mathbb { P } \left [ \text {There exists a disk $D$ on $\mathcal{E}$ of radius $r$ such that $\mathcal{D}\cap X = \emptyset$} \right ] d q \\ & \quad \leq \lambda \int _ { q \in F ( \text {pn} ) } \mathbb { P } \left [ \text {There exists a disk $D$ of $M_{s}$ such that $D^{\prime}\cap X = \emptyset$} \right ] d q \\ & \quad \leq \lambda \int _ { q \in F ( \text {pn} ) } m _ { \delta } \cdot \lambda \pi ( \frac { \frac { r } { 4 } } { 3 } ) ^ { 2 } \, d q \\ & \quad = \lambda e ^ { - \Omega ( \lambda ) } \text { since } m _ { \delta } \, \text {is finite and } r _ { \ }text { strictly positive} . \\$$

□


<!-- p:164 -->


## Chapter 14

### Experimental results

We confirm our results with experimental observations. We simulate a homogeneous Poisson point process X on both kinds of surface, one verifying generic properties and one that does not.

The chosen surfaces are spheroids of revolution with vertical flattening factor k, they can be described in R3, by the equation:

$$\mathcal { E } _ { k } \colon x ^ { 2 } + y ^ { 2 } + k ^ { 2 } z ^ { 2 } = 1 .$$

Figure 14.1: The two spheroids E2 and E1 with respective flattening factors: 2 and 1. Only E2 has generic surface properties.

E2

What is interesting with those surfaces, is that depending on the value of k, they may verify or not genericity properties so that we can observe both of the linear and quasi-linear behaviors of the Delaunay triangulation of X.

For k &lt; 1, the spheroid Ek is elongated along the z axis. Then it can be seen as a canal surface e-a  a tt  #     ar   - ea  ar behavior.

For k = 1, the equation describes a sphere that is a too much degenerated surface to be classically triangulated, and would require symbolic perturbations as described in [DT11].

For k &gt; 1, the spheroid Ek is flattened along the z axis. In that case, Ek is a generic surface, probably the simplest. Z is on the equator of Ek, its medial axis is a disk. According to Chapter 13, E [ Del(X)] must have a linear behavior.


<!-- p:165 -->


Figure 14.2: Left: Cartesian, spherical and cylindrical coordinates. Right: Differential area element on the sphere of radius 1.

z

p

4

dA

dφ

sin(φ)

dθ

ρ

y

θ

V

r

θ

x

#### 14.1 Simulation

We simulate incrementally a homogeneous Poisson point process X on Ek, for any k &gt; 0.

This simulation generates N points where N follow a Poisson distribution with intensity λ.

We divide the simulation of a point p into two steps, first we distribute p uniformly on the sphere ε1, then we apply a rejection algorithm on p such that, once E1 is vertically stretched into Ek, p is homogeneously distributed on Ek.

####### Simulation on the sphere E1

with ρ ∈ [0, +∞], θ ∈ [0, 2π] and φ ∈ [0, π].

We start by simulate a uniform distribution on the sphere E1 of radius 1 defined in R3 by the equation x2 + y2 + z2 = 1 or ρ = 1 using spherical coordinates (Figure 14.2, left):

$$x & = \rho \sin \varphi \cos \theta , \\ y & = \rho \sin \varphi \sin \theta , \\ z & = \rho \cos \varphi ,$$

A differential area element in those coordinates is dA(φ, dθ, dφ) = sin(φ)dφdθ (see Figure 14.2, right), and since the total area of E1 is 4π, we can deduce that the random couple (Θ, Φ) on E1 parameterizes a uniformly distributed point on E1 under the joint distribution:

$$f _ { \Theta , \Phi } ( \theta , \varphi ) = \frac { 1 } { 4 \pi } \sin ( \varphi ) .$$

$$= \int ^ { \pi } \frac { 1 } { \sin ( \alpha ) d \alpha } - \frac { 1 } { 2 }$$

The marginal distributions are then:

$$f _ { \Theta } ( \theta ) & = \int _ { 0 } ^ { \pi } f _ { \Theta , \Phi } ( \theta , \varphi ) d \varphi = \int _ { 0 } ^ { \pi } \frac { 1 } { 4 \pi } \sin ( \varphi ) d \varphi = \frac { 1 } { 2 \pi } , \\ f _ { \Phi } ( \varphi ) & = \int _ { 0 } ^ { 2 \pi } f _ { \Theta , \Phi } ( \theta , \varphi ) d \theta = \int _ { 0 } ^ { 2 \pi } \frac { 1 } { 4 \pi } \sin ( \varphi ) d \theta = \frac { 1 } { 2 } \sin ( \varphi ) .$$

The distribution of Θ is then uniform on [0, 2π], so that we can simulate it :


<!-- p:166 -->


where U1 is a uniform distribution on [0, 1].

We simulate the distribution of Φ by using the inverse transform sampling [Dev06]. The cumulative distribution function of Φ is:

$$F _ { \Phi } ( \varphi ) = \int _ { 0 } ^ { \varphi } f _ { \Phi } ( \phi ) d \phi = \int _ { 0 } ^ { \varphi } \frac { 1 } { 2 } \sin ( \phi ) d \phi = \frac { 1 } { 2 } ( 1 - \cos ( \phi ) ) ,$$

$$\Phi = F ^ { - 1 } ( U _ { 2 } ) = \arccos ( 1 - 2 U _ { 2 } ) ,$$

where U2 is a uniform distribution on [0, 1].

We separately simulate the variables Θ and Φ, thus a point parameterized by (Θ, Φ) is uniformly distributed on E1.

####### Simulation on the spheroid Ek

transformation does not keep the distribution uniform, and thus we use a rejection algorithm to restore the uniformity. Note that we preferred to use a rejection algorithm because a direct approach would have led to elliptic integrals.

We switch to cylinder coordinates (Figure 14.2, left):

$$x & = r \cos \theta , \\ y & = r \sin \theta , \\ z & = z ,$$

thus we deduce that:

with r ∈ [0, +∞], θ ∈ [0, 2π].

On Ek, we consider the differential ring element dRk(r, dr) (see Figure 14.3, left), and compare dRk(r, dr) with dR1(r, dr). For any α ∈ [0, 2π], we consider the intersections of E1 and Ek by the plane Pα: α = θ. They respectively are a circle and an ellipse for which we denote ds1(r, dr) and dsk(r, dr) the differential length elements (see Figure 14.3, right).

It is clear that dRk(r, dr) = 2πrdsk(r, dr) so that (()dr) dRk(r,dr) dsk(r,dr) ds1(r,dr), and we only compute dsk(r, dr). For any α, in Pα, the circle can be described by z = ±f1(r) and the ellipse by z = ±fk(r)

Figure 14.3: Left: The differential ring elements dRk, darker, on sections of ε1 (in green) and E2 (in blue). Right: The differential length elements dsk for k ∈ {1, 1, 3}.

z

2

ds1

1

ds1

13

ds3

●

I up


<!-- p:167 -->


Since fk(r) = − k √1−r2, 1 r the differential length element is:

$$d s _ { k } ( r , d r ) & = \sqrt { 1 + f _ { k } ^ { \prime } ( r ) ^ { 2 } } d r \\ & = \sqrt { 1 + \left ( - \frac { 1 } { k } \frac { r } { \sqrt { 1 - r ^ { 2 } } } \right ) ^ { 2 } } \, d r \\ & = \sqrt { 1 + \frac { 1 } { k ^ { 2 } } \frac { r ^ { 2 } } { 1 - r ^ { 2 } } } d r \\ & = \frac { 1 } { k } \sqrt { \frac { k ^ { 2 } - ( k ^ { 2 } - 1 ) r ^ { 2 } } { 1 - r ^ { 2 } } } d r . \\ \intertext { t e n t i n g r a l f o r m a t i o n m u l t i p l y t h e d f i r e n t i a l l e g t r a l l e s }$$

In other words, the flattening transformation multiply the differential length element by the factor:

$$\frac { d s _ { k } ( r , d r ) } { d s _ { 1 } ( r , d r ) } = \frac { \frac { 1 } { k } \sqrt { \frac { k ^ { 2 } - ( k ^ { 2 } - 1 ) r ^ { 2 } } { 1 - r ^ { 2 } } } d r } { \sqrt { \frac { 1 } { 1 - r ^ { 2 } } } d r } = \frac { 1 } { k } \sqrt { k ^ { 2 } - ( k ^ { 2 } - 1 ) r ^ { 2 } }$$

If k &gt; 1, the expected proportion of points per differential length element ds1 that we keep is dsk(r,dr) d (s) dr) That quantity has 1 for upper bound. We reach that proportion by, for each point p, simulate a number u uniform on [0, 1] and keep p if u &lt; dsk(r,dr) d (s) dr)

Consequently, we apply the following rejection algorithm to all points on the sphere, assuming they are parameterized by (r, θ, z).

If k &lt; 1, the differential length element grows from ds1 to dsk. The growth factor ranges from 1 to k. To preserve uniformity while being able to perform the rejection method, we switch from dsk to kdsk and keep a point with probability k dsk isp

```
Consequently, we apply the following rejection algorithm to all points on the sphere, assucess the
        are parameterized by (r, \theta, z).

            Rejection algorithm:
              input:
                a point p = (r, \theta, z),
                a number k > 0, k \neq 1.

            m <- min(1, k)
              (With probability m=ds(r,dr), we project p on \mathcal { E } _ { k}, otherwise we delete it)
              let u be a random number uniformly chosen in [0, 1]
              if u < m\ds(r,dr):
                p.z <- p.z/k
              else:
                delete p


        14.2    Experimental results.

```

#### 14.2Experimental results

We simulate a homogeneous Poisson process X with intensity λ on E2 and on E1. We vary the parameter λ in a geometric progression from 23 to 219 and realize 20 experiments for each.

In first step, we distribute X on E2 since the oblate spheroid verifies generic properties. The size of the triangulation (in number of edges) is illustrated in Figure 14.4. Since we expect to obtain a linear size, we show the average number of edges up to a factor

T      t   t ( e    s s n 6λ. This is quite small relatively to our expectations. Indeed, a 6λ number of edges provides an average degree (over the vertices) that is around 12. We know that the convex hull bring a contribution of 6 edges per vertices. Note that the convex hull is given by the empty region graph for which the regions defined by (p, q) are half-spaces whose boundary passes through p and q, i.e. degenerate spheres. Considering lower spheres might bring a constant contribution. Thus the number of remote Delaunay neighbors of a point p (those which are close to p) is necessarily smaller than 6. We can actually consider that the Delaunay remote spheres passing through p and q have an intersection with the surface that are ellipses with the only aspect ratio 1−κ1(p)r* (p) 1−κ1(p)r*(p) By Lemma 8.15, this would also bring a contribution of 6 in the expected degree.


<!-- p:168 -->


Figure 14.4: Average number of edges in the 3D-Delaunay triangulation of points on E2, with respect to the logarithm (base 2) of the intensity λ. The number of edges seems to tends to 6λ.

10

8

Average number of edges / λ

6

4

2

0

4

6

8

10

12

14

16

18

log(λ)

Figure 14.5: Average number of edges in the 3D-Delaunay triangulation of points on E1. The number of edges seems to remain just below λ log λ.

2.00

1.75

W

Average number of edges / λ log (

1.50

1.25

1.00

0.75

0.50

0.25

0.00

4

6

8

10

12

14

16

18

log(λ)

In a second step, we distribute X on E1 that is definitely not a generic surface since its medial axis is a segment. We observe that the expected number of edges is, as expected, close to λlog λ.


<!-- p:169 -->


160 Chapter 14. Experimental results Part IV


<!-- p:170 -->


Expected size of the 3D-Delaunay triangulation of a Poisson point process distributed on a generic surface


<!-- p:171 -->


####### Preamble of Part IV

As we have seen in Part III, when a Poisson point process of intensity λ is distributed on a surface, its Delaunay triangulation has an expected size that can range, at least, from linear to quasi-linear. We illustrated this by showing that, on a cylinder, the expected size of the Delaunay triangulation is Θ (λ ln λ), while on an oblate spheroid, the expected size is Θ (λ).

In this part, we consider a generic surface S. Its genericity makes it share properties with the oblate spheroid, that are significant with for the Delaunay triangulation of points distributed on the surface. We describe those properties in Chapter 15, conjointly with the differences we observe. This gives rise to a scheme of proof that we explain in the end of the chapter. Broadly speaking, we adapt the scheme of proof used for the spheroid. One of the important generic properties is that the set Z of S, of points p such that r*(p) = , is a finite reunion of finite curves. On the spheroid case, we illustrated that the κ1 (p) degree of a point depends highly on its distance to Z. Then we denote by hp the distance from p to Z.

Then, each following chapter describes a partial analysis of the expected degree of a point p ∈ S in the Delaunay triangulation depending on the position of p on S and of its possible neighbor q. In chapter 16, we compute the local degree of a point. By "local", we mean that the neighbors we count are geodesically close to p. We denote by Loc(p) the local neighborhood of p. In the local neighborhood of p, we can fit a quadric approximating S, and so will be able to reuse or adapt most of the computations already done in Chapter 13. In the local neighborhood, we can find a super-graph of the Delaunay triangulation for which the degree of p is relevant. We will show that Loc(p) is a circular local neighborhood of radius Θ(1) when p is far from Z, or of radius Θ(h3) when p is close to Z. We distinguish in this chapter, the computation for points that are on, or close to the convex part of the surface, where the two principal curvature have same sign, and points that are far from the convex hull, whose medial radius is finite.

In Chapter 17, we compute the remote expected degree of a point, i.e. the expected number of neighbors that are close to the symmetrical points of p. We will denote by Rem(p) this neighborhood. Here again we have to differentiate the counting depending on the position of p. Indeed, if p is close to S', the set of points with two symmetrical points, then p may have remote neighbors in multiple places on S. For this chapter we introduce the notion of supplementary symmetrical points, in order to count the remote neighbors of a point p whose medial sphere is close to a medial sphere with a greater contact type.

Finally, in Chapter 18, we count the remaining edges. For edges (p, q) such that p is far from Z, a packing argument will show that their number is o(λ). Conversely, if p is close to Z, its local and remote neighborhood are too small to use the packing argument. So we will consider a greater local neighborhood, called middle-range neighborhood as in the previous part. We prove that p have O(log λ) such neighbors but with a probability exponentially decreasing with the distance to Z. As for the spheroid case, this allows us to integrate the expected degree around Z, to obtain a linear expected number of edges with an endpoint close to Z.


<!-- p:172 -->


## Chapter 15

### Generic surfaces

Through this chapter, we explain how we can reuse the proof of the computation of the expected size of the Delaunay triangulation of a Poisson point process distributed on an oblate spheroid for the case of more general surfaces.

#### 15.1 What is generic or not in an oblate spheroid

We start by listing the set of common points and differences we might encounter between a generic surface S and an oblate spheroid E, and we explain how we will deal with those differences. The reader may refer to Part I, Chapter 1 for generic notions, and in particular to Section 1.3.3 for a summary of the different contact points and how we denote them.

##### 15.1.1 Common points between an oblate spheroid and a generic surface

Even if an oblate spheroid can hardly be considered as a generic surface, it shares sufficient properties with a generic surface to be used as a generic example. In a sense, we could say that an oblate spheroid is the simplest generic closed smooth surface. We start by pointing out the properties that an oblate spheroid shares with a generic surface. Those common points will allow us to reuse as much as possible what we have demonstrated in Chapter 13. For instance the general method used in the proof will be reused.

On an oblate spheroid, almost all points have exactly one symmetrical point. We recall that a symmetrical point p of a point p is another contact point of the medial sphere of p with the surface. In other words, almost all medial spheres of an oblate spheroid have A2 contact type. That is also the case for any generic surface. For all of such points, we were able to give a neighborhood, in which their expected degree in the Delaunay triangulation of a Poisson point process were finite. We computed an upper bound on their expected degree, using an empty rhombus. Since for such points, we limit our analysis to the order two of the equations, and since the rhombuses of the rhombus graph are defined by ellipses, i.e. curves of degree 2, we will be able to reuse such graphs for generic surfaces.

Unfortunately, the size of this neighborhood tends to 0 at the approach of Z, and we needed to consider a second analysis for points close to Z. On an oblate spheroid, the set Z of points where the medial radius equals the first osculating radius, is a curve, i.e. a one-dimensional object. So we considered the set we called E2, that is a strip around Z, and computed another upper bound on the expected degree of a point in this strip. On a generic surface, we explained in Part I that Z remains a one dimensional object. Thus we will again consider a strip around Z and use similar argument to bound the global expected number of edge with an endpoint close to Z. The expected degree of such points was calculated using empty right-triangle graph that we will be able to reuse up to some deformation. For the points close to Z, we will still be able to quantify the behavior of some geometric value, like the curvatures.

For these reasons, the general scheme of the proof will be the same. We detail, in the next section, how we deal with the generic properties that an oblate spheroid does not have.


<!-- p:173 -->


##### 15.1.2 Differences between an oblate spheroid and a generic surface

We said that we could see an oblate spheroid as "the simplest" generic surface, but actually such a surface is too specific to be generic, and lots of its properties are not verified generically. In this section we state all such properties that are involved in the computation of the expected size of the Delaunay triangulation.

First, an oblate spheroid is the boundary of a convex volume. Generically a surface is not convex, but we will show that this does not really change the problem. As a consequence of this non-convexity, some woi  s s d e  r s    id t  dr that each p ∈ S can be seen as a point with inside features: pinn and with outside features: pout. Among those features, there is the so called oriented expected degrees deg(pinn, Del) and deg(pout, Del), where deg(pinn, Del) is the number of neighbors of p for which there exists an empty sphere centered in the positive side (with respect to an orientation of S) of the tangent plane at p, and where deg(pout, Del) is defined similarly for the negative side. They verify deg(p, Del) ≤ deg(pinn, Del) +deg(pout, Del). With such notation, we can make a difference orientation-wise in the study of the degree of a point. In particular, even if p ∈ Z it is not necessary that pinn ∈ Zinn but only pout ∈ Zout, and we can still consider that pinn has a local neighborhood not reduced to 0.

Still related with the orientation, a point on an oblate spheroid has no symmetrical point in the outer direction. On a generic surface, a point can have symmetrical points on both sides of its tangent plane, and even on its tangent plane. Considering the oriented points allow to enumerate how many symmetrical points are on each side. For instance, suppose that p has four neighbors, that is generically possible. With the oriented points, we can distinguish the cases: either pinn and pout have two neighbors, either pinn has one neighbor and pout has three, either the contrary. In the sequel, once an orientation is chosen, p will systematically refer to one of the two oriented points. As a consequence, a point p with three symmetrical points, has its three symmetrical points on the same side of its tangent plane.

As well as points with multiple symmetrical points, we recall that a generic surface has also Y points (symmetrical points of extremities of Z). Such points don't exist on oblate spheroids because Z is a closed curve. A special section will be dedicated to compute their remote expected degree.

Finally, we can consider that almost all symmetries that we found on the spheroid do not anymore exist on a generic surface. This will have a significant consequence in two cases. First, for the position of symmetrical points, that were in the x-direction in the Monge coordinate system, and as a consequence we had equation for their bisector plane that did not involve the y coordinate. Actually, since the spheroid was symmetrical with respect to its medial plane, some properties that were related with this plane were simple, like the fact that a circle passing through p, q and p, passes also through q. This is not anymore d p - oo   o  e os  o o  o o o os to Z (in £2 for the oblate spheroid case), we used very specific spheres, that depended on the parallels and meridians. Obviously we cannot define sphere in the same way anymore. Nevertheless, we will show that we can find a super-graph using similar spheres. Another difference lies in the neighborhood where we can apply this super-graph, the middle-range neighborhood, that covered the lower half of the spheroid. For a generic surface, this neighborhood will be related with the coefficients of fourth order of the Taylor expansion of the surface at point of Z.

#### 15.2 Sketch of proof

We consider a generic regular orientable closed surface S. Taking into account what we pointed out in the previous section, we adapt the proof used for the oblate spheroid. We start, in the coming section, by explaining how we decompose the surface, first with respect to an orientation, secondly with respect to the nature of the contact type of the medial sphere. Since some computations can only be made for point under a given distance from specific subsets of the surface S, we will consider strips around Z, S' and H'. We denote by Z+, S'+ and H'+ the respective strips around Z, S' and H'. Their width is not necessary the same, they will be specified all along the proof until it reaches a minimal value that satisfies all necessary conditions.

Once the decomposition is clear, we show out the important lemmas of the proof as we did for the spheroid. This gives rise to a plan for the remaining chapters, each one being dedicated to a group of lemmas.


<!-- p:174 -->


Figure 15.1: A 2D view of the choice of orientation on self-including surface. Left: The outer orientation, defined by the most outer connected component. Right: The inner orientation.

##### 15.2.1 Decomposition of the generic surface

We have to decompose this surface according to the way we will compute the degree of a point. A first step is to consider the two orientations of the surface. Since it is closed, we name outer the orientation that points outward the surface, and inner the other. One might remark that a surface may have multiple connected components self-including, but in that case the "most outer" connected component defines the outer orientation, and the others follow by alternating successively (see Figure 15.1).

Then we choose an orientation, and decompose the surface according to this orientation. We recall what we explained in Part I: once an orientation chosen, a point p belongs to Z if and only if the medial sphere in chosen orientation is osculating and its intersection with S is reduced to p. The same holds for the other subsets of the surface: the set Z' of extremities of Z, the set Y of symmetrical points of Z' points, the set S of points with an A2 contact medial sphere, the set S' of points with an A3 contact medial sphere, the S" of points with an A4 contact medial sphere. And specifically for the outer orientation, the sets H, H' and H" of points one the convex part of S with respectively exactly 0, 1 and 2 symmetrical (finite) points. We denote by Ks the set of the specific subsets described above:

$$\mathcal { K } _ { \mathcal { S } } \colon = \{ S ^ { \prime } , S ^ { \prime \prime } , H ^ { \prime } , H ^ { \prime \prime } , Z , Z ^ { \prime } , Y \} .$$

We consider strips around S', H' and Z, and disks around S", H", Z′ and Y whose width or radius is small enough for us to be able to use some properties of the surface. For a positive number δ, and a subset U C S of the surface, we denote by U+δ the sets on the surface:

$$U ^ { + \delta } = \mathcal { S } \cap \{ \mathcal { B } ( p , \delta ) , \ p \in U \}$$

Thus, for any U ∈ Ks, we associate a positive number δu, and define U+ := U+δv. We choose this notation to simplify the expressions. The different δv can be related to each other but we may pay attention not to define them circularly.

By default, we consider that all δu for U ∈ Ks are smaller than the half-reach ¿rch of the surface. We recall that rch is the smallest medial radius of S, that is strictly positive for any C2 non intersecting surface. All the δU must also be small enough so that, S' ∪ S" ∪ H' ∪ H′′ ∪ Z ∪ Z′ ∪ Y′ and S'+ ∪ S"+ ∪ H'+ ∪ H′+ ∪ Z+ ∪ Z'+ ∪ Y'+ have the same topology. In the end of the proof, we will have an upper bound on each δU that are constants of the surface. In particular, they are independent of the intensity of the Poisson point process.

##### 15.2.2 Approach of the proof

As we said, we keep almost the same approach than for the oblate spheroid.

We consider a Poisson point process distributed on X on S with intensity λ. Without loss of generality, we assume that the area of S is 1. Thus λ corresponds to the expected number of points in X. Tacitly, λ is supposed to be great. For each point p ∈ S, we compute an upper bound on the expected degree E [deg(p, Del)] of p in Del(X ∪ {p}). As we said, we compute separately the degree according to each orientation. So we choose an orientation, and a point p ∈ S. We divide the computation of the expected degree of p in Del(X ∪ {p}) into three degrees: the local degree, the remote degree, and the far degree.


<!-- p:175 -->


Figure 15.2: A 2D view of the decomposition of surface depending on the orientation. In black, blue and yellow far enough from S' ∪ H' ∪ Z. The blue points are specifically on the convex part. In yellow are the strips S'+ and H'+. In red are the strips Z+.

The  o  o  e e o  de  e p, i.e. in a geodesic neighborhood of p on S called Loc(p). It will be defined in Chapter 16. As long as p is not in Z+, we will show that the expected local degree of p is O(1) and that the local neighborhood Loc(p) correspond to a disk around p with radius Ω(1). We will decompose the proof depending on the position of p. If p ∈ H, the two curvatures of p are negative, and we can obtain a constant expected local degree quite efficiently. By smoothness of S, we extend this bound to p ∈ H+. Then all remaining points p have a finite medial radius, and at least one symmetrical point on S. We treat them as we did in the ellipsoid case, taking into account that the size Loc(p) depends not only on the geometric value of S at p, but also at p. In the end of Chapter 16, we treat the cases of points p ∈ Z+. For such a point p, we denote by hp its distance to Z. The local neighborhood of p corresponds to a disk with radius Θ(h3), and its expected local degree is O (ln we show that their expected local degree is O(1).

In Chapter 17, we evaluate the expected number of remote neighbors of p. We count the expected remote degree of a point by using a symmetry relation: if a sphere passes through p and q, it contains either a sphere that has been treated for the local neighborhood of p, or a sphere that has been treated for the local neighborhood of p. For this chapter, we can exclude the cases of points in H \ H'+. Since they don't have symmetrical points, they don't have remote neighbors. The difficult cases are those close to S' and H', for which we will consider supplementary symmetrical points. For any point p in S\ (S'+ ∪ H+), p has a single symmetrical point p. We will show that their expected remote degree has the same order of magnitude than their expected local degree. For points in H'+, we have to take into account that a point in H ∩ H'+ can have Delaunay neighbors on an other connected component of H. For them, we consider a supplementary symmetrical point or two if they are close to H". We treat the points of S'+ \ (Z'+ ∪ Y+) similarly, and show that they have an expected remote degree that is O(1). For the case of points in Z'+ ∪ Y+, since we count the remote neighbors, we choose to orient the Delaunay edges and count only edges issue from Z'+. We show that the expected number of remote neighbors of p in Z′+ is O(ln hp

In chapter 18, we count the remaining neighbors, called far neighbors. For all points of p far from Z+, both the local and remote neighborhood have size Ω(1), and using a packing argument, we show that their remaining Delaunay neighbors, the far neighbors, are O(λ). For a point p in Z+, we show that the probability that p has a Delaunay neighbor outside Loc(p) and Rem(p) is e−λΩ(h26). Then we consider an intermediate neighborhood, the middle-range neighborhood MRN(p) of size Ω(1), and show that the number of neighbors in MRN(p) is e−λΩ(h26)O(ln λ). By integrating this bound, we obtain that the global expected number of such edges isO(λ), and so is the size of the Delaunay triangulation.


<!-- p:176 -->


## Chapter 16

### Expected local degree of a point

In this chapter, we count what we call the expected local degree of a point p in the Delaunay triangulation of a Poisson point process X on S. The local degree correspond to the number of Delaunay neighbors that lie in a given neighborhood, called local neighborhood, that is a small topological disk around p. Its size depends on the position of p on S, in particular to the distance hp from p to Z.

As we saw in Part III Chapter 13, the distance hp from p to Z is Θ (√1 − κ1(p)r*(p)). Since r* is infinite on the convex part of the surface, we decompose the chapter into two sections: a first section for the convex part and a little beyond, and a second section for bounded medial radius.

#### 16.1 Local degree of a point on the convex hull and a little beyond

In this section, we consider the outer orientation of S and we treat the points of H ∪ H+ i.e. the set of points of S that are in H or that are in S but close to the boundary H' of H. We recall that p is considered as an oriented point, and that deg(p, Del) takes only into account the spheres whose center has a positive z coordinate in the Monge coordinate system of p.

We call local degree of p, the set of points q such that (p, q) is an edge of the Delaunay triangulation, and |pq| is small enough. We will show that the expected local degree of a point p ∈ H+ is bounded by a constant.

Consider a point p on the convex part H of S, and the Monge coordinate system at p. By genericity, at p, the two principal curvatures are negative. We denote by κí, the maximum of first principal curvature on H:

$$\kappa _ { H } \coloneqq \sup _ { p \in H } \left ( \kappa _ { 1 } \right ) .$$

It is a strictly negative constant. By smoothness of S, κ1(p) remains negative a little beyond H. This give an upper bound on δH: it must be small enough so that all points of H'+ have two negative principal curvatures. This defines the condition (CH')

$$\text {For any } p \in H ^ { \prime + } , \kappa _ { 1 } ( p ) \leq \frac { 1 } { 2 } \kappa _ { H } . & & ( C _ { H ^ { \prime } } )$$

A point p in H'+ \ H, i.e. beyond the convex part, has a symmetrical point p. That induces that it has remote neighbors around p, but that also reduces the probability that a high sphere passing through p is empty, since the sphere may touch S around p. We can count the number of local neighbors of such a point p as if there were no symmetrical points, similarly than what happens on the convex hull. That provides an upper bound on the number of local neighbors.

Since we reuse the method used in Part III, we will consider a point q ∈ S, close to p, and partition the bisector plane PBis(p, q) to obtain a super-graph. We start by defining the set of spheres whose centers help in the partitioning of PBis(p, q). To be exact, since we have oriented the surface, we only partition PBis(p, q)out := PBis(p, q) ∩ {z ≥ 0}. In order to lighten the notations, we keep the notation PBis, since it is clear from the context.


<!-- p:177 -->


##### 16.1.1 Choice of the specific spheres

At any point of H ∪ H'+ the surface is locally convex. So we can more or less see it as the external part of a spheroid, and we can reuse exactly some spheres that were already used in Section 13.4. For the spheroid, we partitioned completely PBis(p, q) and considered the inner orientation. So, what we need to partition here corresponds, in the spheroid case, to the part of PBis(p, q) where z &lt; 0.

We partition this part with four centers, one with zc = 0, close to the middle of p and q, its corresponding sphere has an intersection with S that resembles to a disk with diameter [pq]. One at the infinity, such that the corresponding sphere is a plane that has an intersection with S that resembles to an axis-aligned ellipse centered on the middle of [pq] and with aspect ratio k1. And the two last centers κ2 at the extremities of PBis(p, q) ∩ {z = 0}. Their spheres are degenerate planes directed by the line (pq) and n(p). They cut in half the surface into a left and a right side. Since the claims are exactly the same than those from Section 13.4, we don't reprove them.

####### Sphere σLow

We consider the neighborhood of p in Ts(P): VLow(p) = {max (|x|, |y|) ≤  κsup }, and recall that "(a). We state the following claim: ell1(p, q) is the disk in Ts(p), with diameter p and 2

The center cLow is in the tangent plane Tε(p) whose equation is z = 0, and in the vertical plane PLow with equation yxq − xyq = 0. The equation of the second plane guarantees that the projection of the intersection region πp (rLow) = B(σLow) ∩ ε is tangent with ell1 (p, q). The more q is close to p, the closer is the sphere σLow to the Gabriel sphere of p and q.

Claim a. If q ∈ π−1 (VLow(p)), then πp (rLow) contains ell1 (p, q).

####### Degenerate sphere σHigh·

We recall that the surface at p can be seen as the graph of:

The center cHigh is at the infinity in the direction, in PBis, given by the plane PHigh with equation from Claim c, Section 13.4, in the opposite orientation. The direction of the center tends to the normal at p when q approaches p. We consider β∞ =: 1 k1 The fact that cHigh ∈ PHigh guarantees that the projection of the intersection κ2 region rHigh = B(σHigh) ∩ ε is tangent with ellβ∞ (p, q) at p.

$$f _ { p } = \frac { 1 } { 2 } \kappa _ { 1 } x ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y ^ { 2 } + R _ { 3 } ( x , y ) ,$$

where there exists a positive M3 such that |R3(x, y)| ≤ M3(x2 + y2) γ , and consider the rectangle VHigh = {|x| ≤ |κ11 ,|y|≤√ {1 |κ11 } and the following claim: 6M3, κ26M3S

Claim b. If q ∈ π−1 (VHigh(p)), then πp (rHigh) contains ellβ∞ (p, q).

####### Degenerate spheres σl and σr.

Their centers ce and cr are at the infinity of the line that is the intersection of PBis and the tangent plane Ts(p), with equation z = 0. The spheres degenerate into the vertical plane PDiag passing through p and q, and containing the normal at p. If we look at the tangent plane from an outer point of view (with respect to S) then ce is defined on the left of pπp(q) and cr on its right.

Claim c. If q ∈ π−1 (VLow(p)) then πp (re(p, q)) contains ellk (p, q) and πp (rr(p, q)) contains ell1(p, q).

Finally, for any point of H+, we denote by VH (p) := VLow(p) ∩ VHigh (p) and define Loc(p) as:

$$L o c ( p ) \colon = \pi _ { p } ^ { - 1 } \left ( V _ { H } ( p ) \right ) .$$

The local neighborhood Loc(p) constitutes a strictly positive neighborhood for all points in H+. Those claims are enough to consider a super-graph of the Delaunay triangulation restricted to spheres centered above Ts(p) and neighbors in Loc(p).


<!-- p:178 -->


##### 16.1.2 Proof of the graph inclusion

We consider the two regions in the tangent plane:

- rhβ∞ := ell1 ∩ ellβ∞, and
- rhβ∞ := ell ∩ellβ∞.

And we can apply Combination lemma to prove that if q ∈ Loc(p), then any sphere σ passing through p and q and centered on c verifies:

- If c ∈ (cHigh, CLow, Cr), then B (σ) ∩S contains π−1 1 (rhβ∞), and
- if c ∈ (cHigh, CLow, ce), then B (σ) ∩S contains π−1 (rh∞).

Then we consider the family FLoc(p, q) of fundamental regions on S for p ∈ H+ and q ∈ Loc(p):

$$\mathcal { F } _ { L o c } ( p , q ) \colon = \left \{ \pi _ { p } ^ { - 1 } \left ( r h _ { \ell } ^ { \beta _ { \infty } } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( r h _ { r } ^ { \beta _ { \infty } } ( p , q ) \right ) \right \} ,$$

and the empty region graph 00 in which there is an edge (p, q) if and only if q ∈ Loc(p) and there exists r ∈ FLoc(p, q) such that r ∩ X = ∅. We can partition the part of PBis(p, q) such that z &gt; 0, into (cHigh, CLow, cr) ∪ (cHigh, CLow, ce) to deduce by Partition lemma:

Lemma 16.1. Let p ∈ H ∪ H′+ and q ∈ Loc(p).

If (p, q) is an edge of Del(X ∩ {p}) then it is an edge of GFL.c C0 c(X ∩ {p}).

##### 16.1.3 Computation of the expected local degree

We use the super-graph provided by the previous section, to compute an upper bound on the expected local degree of a point of H ∪ H′+ in the Delaunay triangulation Del(X ∪ {p}).

Lemma 16.2. Let p ∈ H∪H'+, the expected number E [deg|Loc (p, Del)] of neighbors of p in Del(X∪{p}) that are in Loc(p) is:

$$\mathbb { E } \left [ \deg _ { | L o c } ( p , D e l ) \right ] = O ( 1 ) .$$

Proof. The important point here is that −κsup ≤ κ2 ≤ κ1 ≤ κH &lt; 0 since p is in H+ and the curvature is bounded. Thus the super-graph f is an empty half-rhombus graph with finite aspect ratio for any p, for which we know that the expected degree is finite. □

Note that, in this counting we did not take into account the symmetrical part of H'+ \ H, thus the points in H'+ \ H have actually a lesser expected local degree, but it is important that we counted the local neighbors of such points in the same way than points of H, because their medial radius tends to +∞ when they approach H', and that would have been a problem.

For the points of H ∪ H'+, it remains to count the remote neighbors (close to the symmetrical points) and the far neighbors (neither close to p nor to p). We will count such neighbors in a farther section. For now, we just make the remark that, points of H \ H'+ don't have remote neighbors, but only far neighbors. Points of H'+ \ H have a natural symmetrical point, so it has remote and far neighbors. For the remaining points, in H'+ ∩ H, it is a bit more complicated: they don't have a symmetrical point, but since they are close to the boundary of the convex part, they can have neighbors on another connected component of H'+. So we will have to count them.


<!-- p:179 -->


#### 16.2 Local degree of a point far from the convex hull, and far from Z and Y

In this section, we consider a point p in S but not in H ∪ H'+ since we dealt with them in the previous section, and not in Z+, where 1 − κ1r* approaches 0, and not in Y+, where 1 − κ1r* approach 0. Thus, for a given orientation, the medial sphere of p is finite and not osculating at p or p. It is important that 1 − κ1r* &gt; 0 since, as in the spheroid case, a sphere passing through such a point p has an intersection with the surface that is almost elliptic, with an aspect ratio that does not exceed 1−κ1r* 1−κ2r*

We count the expected number of Delaunay neighbors of p that are in a local neighborhood of p on S. This neighborhood will be refined as we go along the proof. For now we can assume that we consider points of S at a distance smaller than rch from p. This provides a guarantee that they lie geodesically close to p, and in a part of the surface that can be represented as the graph of a function in the Monge coordinate system of p.

Since p ∉ H+δ, p has at least one symmetrical point. For this section, it is not important how many they are. If there is only one, we call it p. If there are more, one of them is closer to p than the others. We name this one p. Since p ∉ H ∪ H+, we can consider its medial sphere σ*, with medial center c* and medial radius r*.

We count the expected number of local neighbors of p. As usual, we start by defining the specific -s  d      ed  sn ses degree. For this section, we cannot reuse as directly as in the previous section the claims and the partition we had in Chapter 13 because S does not have all the symmetries of an oblate spheroid.

##### 16.2.1 Choice of the specific spheres

For a point q close to p, we have to define some specific spheres whose center are vertices of the partition of PBis(p, q) that we use to find a super-graph of the Delaunay triangulation. We try to reuse, as much as possible, the spheres we chose in Section 13.4, but we will have to adapt some of them since, by definition, S has less symmetries than a spheroid. At least two noticeable differences arise: p is not anymore above the x-axis of Monge coordinate system at p, and the principal curvatures at p are different from those at p and moreover, the principal directions are not anymore symmetrical with respect to PBis(p, p).

Low spheres σLow, σl and σr

We still consider the same spheres as usual, σLow, σe and σr centered on PBis ∩ {z = 0}

Claim a. If q ∈ π−1 (VLow(p)), then πp (rLow) contains ell1(p, q) or ell1(p, q).

Before introducing the next sphere, we make some remarks concerning the point p. We denote by κ1 and κ2 its principal curvatures. To be more precise, κ1(p) = κ1(p), and κ2(p) = κ2(p). In the Monge coordinate system of p, the bisector plane of p and p, renamed PMed has equation:

$$\mathcal { P } _ { \text {Med} } \colon 0 = x x _ { \overline { p } } + y y _ { \overline { p } } + ( z - r ^ { * } ) \, z _ { \overline { p } } ,$$

since c* ∈ PMed and PMed ⊥ (pp). We can rewrite its equation this way to isolate z:

$$\mathcal { P } _ { M e d } \colon z = r ^ { * } - \frac { x x _ { \overline { p } } + y y _ { \overline { p } } } { z _ { \overline { p } } } .$$

The center cMed is in the plane PMed and the plane Pβ* with equation y(1− κ1r*)xq−x(1− κ2r*)yq = 0. The center cMed is close to the medial ceņter c* of p when q is close to p. We consider the neighborhood VMed(p) = { max(|xq|, |yq|) ≤ (1−κ1r*)κsup |z词| 1−κ1r |z词| }. The values inr*M3 [xp], 1−κ2r* [yp| volved in the definition of VMed appear in the proof of the following claim.

Sphere σMed

Claim b. If q ∈ π−1 (VMed(p)), then πp(rMed) contains ellβr* (p, q).


<!-- p:180 -->


Proof. The proof is very similar than the proof of Claim b, Chapter 13, except than yp ≠ 0. We start by identifying the coordinates of cMed = (xc, yc, zc). It verifies:

$$C _ { M e d } \colon & \left \{ \begin{array} { l l } { 0 } & { = } & { ( x _ { q } - 2 x _ { c } ) \, x _ { q } + ( y _ { q } - 2 y _ { c } ) \, y _ { q } + ( z _ { q } - 2 z _ { c } ) \, z _ { q } , \, ( 1 ) } \\ { z _ { c } } & { = } & { r ^ { * } - \frac { x _ { \overline { z } } } { z _ { \overline { z } } } x _ { c } - \frac { y _ { \overline { E } } } { z _ { \overline { z } } } y _ { c } , } & { ( 2 ) } \\ { 0 } & { = } & { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } y _ { c } - ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } x _ { c } . } \end{array}$$

In (1), we substitute zc by its expression given by (2):

$$\text {In } ( 1 ) , \text { we substitute } z _ { c } \text { by its expression given by } ( 2 ) \colon \\ 0 = ( x _ { q } - 2 x _ { c } ) \, x _ { q } + ( y _ { q } - 2 y _ { c } ) \, y _ { q } + z _ { q } ^ { 2 } - 2 \left ( r ^ { * } - \frac { x _ { c } x _ { \overline { p } } } { z _ { \overline { p } } } - \frac { y _ { c } y _ { \overline { p } } } { z _ { \overline { p } } } \right ) z _ { q } \\ = x _ { q } ^ { 2 } - 2 x _ { c } x _ { q } + y _ { q } ^ { 2 } - 2 y _ { q } u _ { + } + z _ { q } ^ { 2 } - 2 \left ( r ^ { * } - \frac { x _ { c } x _ { \overline { p } } } { z _ { \overline { p } } } - \frac { y _ { c } y _ { \overline { p } } } { z _ { \overline { p } } } \right ) z _ { q } \\ = x _ { q } ^ { 2 } - 2 \left ( x _ { q } - \frac { x _ { \overline { p } } } { z _ { \overline { p } } } z _ { q } \right ) x _ { c } + y _ { q } ^ { 2 } - 2 \left ( y _ { q } - \frac { y _ { \overline { p } } } { z _ { \overline { p } } } z _ { q } \right ) y _ { c } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } . \\ \text {Then we rewrite } ( 3 ) \text { into } y _ { q } = \frac { ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } } { 2 } x _ { q } \text { and substitute } y _ { q } \colon$$

Then we rewrite (3) into yc = (1−κ2r*)yq and substitute yc: (1−κ1r*)xq

$$0 = x _ { q } ^ { 2 } - 2 \left ( x _ { q } - \frac { x _ { \overline { p } } } { z _ { \overline { p } } } z _ { q } \right ) x _ { c } + y _ { q } ^ { 2 } - 2 \left ( y _ { q } - \frac { y _ { \overline { p } } } { z _ { \overline { p } } } z _ { q } \right ) \frac { ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } } { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } } x _ { c } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } ,$$

and isolate xc:

$$x _ { c } & = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { x _ { q } - \frac { x _ { \overline { z } } } { z _ { \overline { p } } } z _ { q } + \left ( y _ { q } - \frac { y _ { \overline { z } } } { z _ { \overline { p } } } z _ { q } \right ) \left ( \frac { 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } } { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } } \right ) } \\ & = \frac { 1 } { 2 } ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } \frac { x _ { q } ^ { 2 } } { ( x _ { q } z _ { \overline { p } } - x _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 1 } r ^ { * } \right ) x _ { q } + ( y _ { q } z _ { \overline { p } } - y _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 2 } r ^ { * } \right ) y _ { q } } { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } z _ { \overline { p } } , \\ \intertext { a n d d u e a } x _ { c } & = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { x _ { q } z _ { \overline { p } } - x _ { \overline { p } } z _ { \overline { p } } } \left ( 1 - \kappa _ { 1 } r ^ { * } \right ) x _ { q } + ( y _ { q } z _ { \overline { p } } - y _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 2 } r ^ { * } \right ) y _ { q } }$$

and deduce yc:

$$y _ { c } = \frac { 1 } { 2 } ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { ( x _ { q } z _ { \overline { p } } - x _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 1 } r ^ { * } \right ) x _ { q } + ( y _ { q } z _ { \overline { p } } - y _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 2 } r ^ { * } \right ) y _ { q } } z _ { \overline { p } } . \\$$

We denote by Cq the right factor in both xc and yc:

$$C _ { q } = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { ( x _ { q } z _ { \overline { p } } - x _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 1 } r ^ { * } \right ) x _ { q } + ( y _ { q } z _ { \overline { p } } - y _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 2 } r ^ { * } \right ) y _ { q } } z _ { \overline { p } } .$$

We obtain the coordinate of cMed in function of q and p:

$$C o n d i m a t c \, o r \, C _ { M e d } \, i n d \, i n c t i o n \, o r \, q \, a n d \, p . \\ x _ { c } = \frac { 1 } { 2 } ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } C _ { q } , \\ y _ { c } = \frac { 1 } { 2 } ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } C _ { q } , \\ z _ { c } = r ^ { * } - \frac { 1 } { 2 } \left ( ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } x _ { \overline { p } } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } y _ { \overline { p } } \right ) \frac { C _ { q } } { z _ { \overline { p } } } .$$

We analyze we only need a lower bound. We obtain it by using the Taylor development of zq = fp(xq, yq) = κ1x2 2 十 κ2yq + R3(q):

$$z _ { q } & = f _ { p } ( x _ { q } , y _ { q } ) = \frac { 1 } { 2 } \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y _ { q } ^ { 2 } + R _ { 3 } ( q ) \colon \\ & \quad C _ { q } = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } z _ { q } } { ( x _ { q } z _ { \overline { p } } - x _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 1 } r ^ { * } \right ) x _ { q } + ( y _ { q } z _ { \overline { p } } - y _ { \overline { p } } z _ { q } ) \left ( 1 - \kappa _ { 2 } r ^ { * } \right ) y _ { q } } z _ { \overline { p } } \\ & = \frac { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } \left ( \frac { 1 } { 2 } \kappa _ { 1 } x _ { q } ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } y _ { q } ^ { 2 } + R _ { 3 } ( q ) } { \left ( ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } ^ { 2 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } \right ) z _ { \overline { p } } - \left ( ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { \overline { p } } x _ { q } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { \overline { p } } y _ { q } \right ) z _ { q } ^ { 2 } } \\ & = \frac { ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } ^ { 2 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } R _ { 3 } ( q ) } { ( ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { q } ^ { 2 } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { q } ^ { 2 } ) \left ( ( 1 - \kappa _ { 1 } r ^ { * } ) x _ { \overline { p } } x _ { q } + ( 1 - \kappa _ { 2 } r ^ { * } ) y _ { \overline { p } } y _ { q } \right ) z _ { q } } z _ { \overline { p } } ,$$


<!-- p:181 -->


to lighten the expression, we replace 1 − κ1r* by K1, and 1 − κ2r* by K2, and we name Nq the numerator (up to zp) and Dq the denominator:

$$C _ { q } & = \frac { K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } R _ { 3 } ( q ) } { ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } - ( K _ { 1 } x _ { \overline { p } } x _ { q } + K _ { 2 } y _ { \overline { p } } y _ { q } ) \, z _ { q } } z _ { \overline { p } } \\ & = \frac { N _ { q } } { D _ { q } } z _ { \overline { p } } .$$

Then we provide a neighborhood around p for q in which this quantity is greater than 7 We bound from above the numerator Nq for∥πp(q)|2 ≤ 1 K1 16 r*M3

$$N _ { q } & = K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } + z _ { q } ^ { 2 } - 2 r ^ { * } R _ { 3 } ( q ) \\ & \geq K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } - 2 r ^ { * } | R _ { 3 } ( q ) | \\ & \geq K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } - 2 r ^ { * } M _ { 3 } \| \pi _ { p } ( q ) \| _ { 2 } ^ { 3 } \\ & \geq K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } - \frac { 1 } { 8 } K _ { 1 } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) \\ & \geq K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } - \frac { 1 } { 8 } \left ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } \right ) \\ & = \frac { 7 } { 8 } \left ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } \right ) .$$

And we bound from below the denominator Dq for |xq| ≤ 1|zp| and |yq| ≤ 16 K2 −sup|yp]: 1 K1|zp| 16 κsup|xp|

$$D _ { q } & = ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } - ( K _ { 1 } x _ { \overline { p } } x _ { q } + K _ { 2 } y _ { \overline { p } } y _ { q } ) \, z _ { q } \\ & \leq ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } + ( K _ { 1 } | x _ { \overline { p } } x _ { q } | + K _ { 2 } | y _ { \overline { p } } y _ { q } | ) \, \kappa _ { \text {supp} } \, \| \pi _ { p } ( q ) \| _ { 2 } ^ { 2 } \\ & \leq ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } + \frac { 1 } { 8 } \, K _ { 1 } x _ { \overline { p } } \| \pi _ { p } ( q ) \| _ { 2 } ^ { 2 } \\ & \leq ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } + \frac { 1 } { 8 } \, ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } \\ & = \frac { 9 } { 8 } \, ( K _ { 1 } x _ { q } ^ { 2 } + K _ { 2 } y _ { q } ^ { 2 } ) \, z _ { \overline { p } } .$$

Thus, in such a neighborhood,

$$C _ { q } \geq \frac { 7 } { 9 } .$$

Let σ be a sphere passing through p and q. An equation of the ball B(σ) is:

$$x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - y y _ { c } + z ^ { 2 } - z z _ { c } \leq 0 ,$$

where c = (xc, yc, zc) is the center of σ. By substituting z by fp(x, y) for points (x, y) such that √x2 + y2 ≤ √2 we obtain an expression of the projection of the intersection B(σ) ∩ ε given by 2ksup Ec(x, y) ≤ 0 where:

$$E _ { c } ( x , y ) = x ^ { 2 } - 2 x x _ { c } + y ^ { 2 } - y y _ { c } + ( f _ { p } ( x , y ) ) ^ { 2 } - f _ { p } ( x , y ) z _ { c } .$$


<!-- p:182 -->


Finally we substitute the coordinate of c in the equation:

$$1 6 . 2 \quad & \text {Local degree of a point far from the convex hull and from Z} \\ & \text {Finally we substitute the coordinate of c in the equation:} \\ E _ { c } ( x , y ) = x ^ { 2 } - 2 x _ { c } + y ^ { 2 } - 2 y _ { p } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) z _ { c } \\ & = x ^ { 2 } - x K _ { 1 } x _ { q } C _ { q } + y ^ { 2 } - y K _ { 2 } y _ { q } C _ { q } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) \left ( r ^ { * } - \frac { 1 } { 2 } \left ( K _ { 1 } x _ { q } x _ { p } + K _ { 2 } y _ { q } y _ { \overline { z } } \right ) \frac { C _ { q } } { z _ { \overline { p } } } \right ) \\ & = x ^ { 2 } - K _ { 1 } x _ { q } C _ { q } x + y ^ { 2 } - K _ { 2 } y _ { q } C _ { q } y + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) r ^ { * } - f _ { p } ( x , y ) \left ( K _ { 1 } x _ { q } x _ { p } + K _ { 2 } y _ { q } y _ { \overline { z } } \right ) \frac { C _ { q } } { z _ { \overline { p } } } \\ & = K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } C _ { q } x + K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } C _ { q } y \\ & \quad + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 r ^ { * } R _ { 3 } ( x , y ) - f _ { p } ( x , y ) \left ( K _ { 1 } x _ { q } x _ { p } + K _ { 2 } y _ { q } y _ { \overline { z } } \right ) \frac { C _ { q } } { z _ { \overline { p } } } \\ & = C _ { q } \left ( \frac { 1 } { C _ { q } } K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } x + \frac { 1 } { C _ { q } } K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } y \\ & \quad + C _ { q } ( f _ { p } ( x , y ) ) ^ { 2 } - 2 \frac { 1 } { C _ { q } } r ^ { * } R _ { 3 } ( x , y ) - f _ { p } ( x , y ) \left ( K _ { 1 } x _ { q } x _ { p } + K _ { 2 } y _ { q } y _ { \overline { z } } \right ) \frac { 1 } { z _ { \overline { p } } } \\ & \leq C _ { q } \left ( \frac { \frac { 9 } { 7 } K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } x + \frac { 9 } { \frac { 7 } { 2 } } K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } y \\ & \quad + \frac { \frac { 8 } { 7 } \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) ^ { 2 } + \frac { 1 8 } { 7 } r ^ { * } M _ { 3 } \left ( x ^ { 2 } + y ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } + \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) \left | K _ { 1 } x _ { q } x _ { p } + K _ { 2 } y _ { q } y _ { \overline { z } } \right ) \frac { 1 } { z _ { \overline { p } } } \right ) \\ & \leq C _ { q } \left ( \frac { \frac { 9 } { 7 } K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } x + \frac { 9 } { \frac { 7 } { 2 } } K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } y \\ & \quad + \frac { \frac { 9 } { 7 } \kappa _ { \sup } ( x ^ { 2 } + y ^ { 2 } ) ^ { 2 } + \frac { 1 8 } { \pi } r ^ { * } M _ { 3 } \left ( x ^ { 2 } + y ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } + \frac { 1 } { g } ( K _ { 1 } x ^ { 2 } + K _ { 2 } y ^ { 2 } ) \right ) , \\ & \text {as we saw in the bounding of $D_{q}$} ,} \\ & E _ { c } ( x , y ) < C _ { q } \left ( \frac { \frac { 7 } { 9 } K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } x + \frac { 7 } { \overline { 2 } } K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } y + \frac { 9 } { \kappa _ { \sup } } ( x ^ { 2 } + y ^ { 2 } ) ^ { 2 } + \frac { 1 8 } { \pi } r ^ { * } M _ { 3 } \left ( x ^ { 2 } + y ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } \right ) .$$

as we saw in the bounding of Dq,

$$E _ { c } ( x , y ) \leq C _ { q } \left ( \frac { 7 9 } { 5 6 } K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } x + \frac { 7 9 } { 5 6 } K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } y + \frac { 9 } { 7 } \kappa _ { \sup } ^ { 2 } ( x ^ { 2 } + y ^ { 2 } ) ^ { 2 } + \frac { 1 8 } { 7 } r ^ { * } M _ { 3 } \left ( x ^ { 2 } + y ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } \right ) .$$

We find a neighborhood in which the remainder term (x2 + y2)2 + 18 r*M3 (x2 + y2) 3|2 , is smaller sup in than 33 56 K1x2 + 33 56 K2y2. We choose √x2 + y2 ≤ min 4κsup 1 √2K1, 3 1 r* M3 K1 to obtain:

$$\text {If $\frac{9}{6} K_{1}x^{2} + 5^{6}K_{2}y^{-1} \cdot \text {we can use $\frac{7}{4}$}x^{\frac{7}{4}$} \cdot 3^{\frac{7}{3}$} ) , 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0 \, 0$$

And we can deduce that:

and for q is:

$$E _ { c } ( x , y ) \leq C _ { q } \left ( 2 K _ { 1 } x ^ { 2 } - K _ { 1 } x _ { q } x + 2 K _ { 2 } y ^ { 2 } - K _ { 2 } y _ { q } y \right ) .$$

But 2K1x2 − K1xqx + 2K2y2 − K2yqy ≤ 0 is the equation of ellβr* (p, q). The neighborhood in which the equation holds for (x, y) is:

$$\sqrt { x ^ { 2 } + y ^ { 2 } } \leq v _ { 1 } \colon = \min \left ( \frac { 1 } { 4 \kappa _ { \text {sup} } } \sqrt { 2 K _ { 1 } } , \frac { 1 } { 3 } \frac { K _ { 1 } } { r ^ { * } M _ { 3 } } \right ) ,$$

$$\sqrt { x _ { q } ^ { 2 } + y _ { q } ^ { 2 } } \leq v _ { 2 } \colon = \frac { 1 } { 1 6 } \min \left ( \frac { K _ { 1 } } { r ^ { * } M _ { 3 } } , \frac { | z _ { \overline { p } } | } { \kappa _ { \sup } | x _ { \overline { p } } | } , \frac { K _ { 1 } } { K _ { 2 } } \frac { | z _ { \overline { p } } | } { \kappa _ { \sup } | y _ { \overline { p } } | } \right )$$


<!-- p:183 -->


Figure 16.1: The point ωp(q) is defined as the fourth intersection point of the circle passing through p, q, and p with S.

p

ωp(q)

b

Thus, we choose vMed = min (v1, v2), and deduce that if ∥πp(q)|2 ≤ vMed then πp (B (σMed) ∩S) contains ellβr* (p, q) ∩ D(p, vMed) that itself contains ellβr* (p, q) ∩ ell1 (p, q). □

As on the oblate spheroid, the quantities that define the neighborhood tend to 0 when p goes to Z, since we still have 1 − κ1r* = Θ (h2) (recall that hp denote the distance from p to Z). Despite this, one might notice that this analysis was not that fine, and instead of having a rectangular neighborhood with sides Θ (√1 − κ1r*) × Θ (1 − κ1r*), we have a square neighborhood with radius Θ (1 − κ1r*). A more subtle approach, in which we would have considered the third order coefficient of fp, could have given a rectangular neighborhood, but the spheroid example showed that it was not necessary to be tight on this quantity.

The problem now is to define a notion of symmetrical point of q. Naturally we could have taken  ̄, ns n n  dns -s o  r  p    nn d ne the point denoted ωp(q) defined as follows: consider the circle passing through p, q, and p. If q is close enough to p then this circle has a single forth intersection with S around p. This intersection is ωp(q) (see Figure 16.1).

Note that ωp(q) depends both on p and q. For the spheroid case, ωp(q) corresponds to q by symmetry. In the following lemma, we evaluate the distance |pωp(q)| with respect to |pq| :

Lemma 16.3. For any δ smaller than 1rch, there exists two positive constants ε and Ksym such that if p ∉ (H ∪ S′ ∪ Z ∪ Y)+δ and if |pq| &lt; ε then |pωp(q)| ≤ Ksym|pq|.

Proof. Consider a positive δ and p ∉ (H ∪ S' ∪ Z ∪ Y)+δ. Consider the plane Psym(p, q) := (pqp), and c the center of the circle passing through p, q, and p. We consider the orthogonal projections πp and πp on the tangent planes of p and p in Psym. We denote by κsym, Ksym, and ršym, respectively the curvatures of the curve Psym ∩S at p, p, and the radius of Psym ∩σ*. They are defined as long as Psym(p, q) is not tangent with S at p or p.

There exists ε such that, if |pq| &lt; ε, in the plane Psym(p, q), we have (see Figure 16.2):

But p ∉ (H' ∪ Z ∪ Y)+δ so the plane Psym(p, q) is always far from being tangent, and since σ* is not osculating, it remains true that (1 − κsymrsym) and (1 – κsym^sym) are greater than a positive constant.

$$\begin{cases} \, \begin{array} { l l l } | p \pi _ { p } ( c ) | & \simeq & \frac { 1 } { 2 } ( 1 - \kappa _ { S y m } r _ { S y m } ^ { * } ) | p \pi _ { p } ( q ) | , \, a n d \\ | \overline { p } \pi _ { \overline { p } } ( c ) | & \simeq & \frac { 1 } { 2 } ( 1 - \overline { \kappa } _ { S y m } r _ { S y m } ^ { * } ) | \overline { p } \pi _ { \overline { p } } ( \omega _ { p } ( q ) ) | . \end{array} \end{cases}$$

This is just the 2D version of almost all computations of intersection surface/sphere we did previously.


<!-- p:184 -->


Figure 16.2: A view of S and σ* in the plane Psym(p, q). On the figure, we have more or less, Thus |pωp(q)| ≈ |pπp(c)| = |pπp(c)| ≈ 1|pq|. 2κSym 2κSym

πp(c)

ωp(q)

p

S

Ts(p)

*

Sym

*

c

Ts(p)

p

(ə)d1

(b)dμ

And by projection of the center c:

$$| p \pi _ { p } ( c ) | = | \overline { p } \pi _ { \overline { p } } ( c ) | .$$

In other words:

$$| \overline { p } \pi _ { \overline { p } } ( \omega _ { p } ( q ) ) | & \simeq \frac { 1 - \kappa _ { S y m } r _ { S y m } ^ { * } } { 1 - \overline { \kappa } _ { S y m } r _ { S y m } ^ { * } } | p \pi _ { p } ( q ) | , \text { and } \\ | \overline { p } \omega _ { p } ( q ) | & \simeq \frac { 1 - \kappa _ { S y m } r _ { S y m } ^ { * } } { 1 - \overline { \kappa } _ { S y m } r _ { S y m } ^ { * } } | p q | ,$$

$$\simeq \frac { \simeq \frac { \Im y ^ { * } \Im m } { 1 - \overline { \kappa } _ { S y m } r _ { S y m } ^ { * } } | p q \\ \, w h e r e \, \frac { 1 - \overline { \kappa } _ { S y m } r _ { S y m } ^ { * } } { 2 }$$

since the projection affects the distance in a negligible way. And if we denote by Ksym the maximal value of 1-κSymrSym 1−κSymrSym , for all p in (H' ∪ Z ∪ Y)+δ and all possible planes Psym(p, q), we have:

$$| \bar { p } \omega _ { p } ( q ) | \leq K _ { S y m } | p q | .$$

By construction, the sphere σMed passes through ωp(q). Unfortunately, the principal directions at p, are not symmetrical to the principal directions at p with respect to the reflection by PBis(p, p), as it is the case on a spheroid. Indeed, as long as p is far from Z, the principal directions at p are not related with those at p. As a consequence, the intersection B (σMed) ∩S around p may not contain the expected ellipse, i.e. the ellipse with aspect ratio √ 1−κ1r* and centered on ωp(q), but a shifted ellipse. To correct 1−κ2r* that shift, we consider the sphere σMed.

####### Sphere σMed

We define σMed(p, q) as the sphere σMed(p, ωp(q)), and the neighborhood around p:  ̄Med(p) as the set of q such that ωp(q) ∈ VMed(p).

Then we consider the number βr* := 1−κ1r* 1−κ2r*


<!-- p:185 -->


Claim c. If q ∈ π−1 (VMed(p)), then π−(īMed) contains ellβr* (p, ωp(q)).

Proof. Direct by Lemma 16.3 and the previous claim.

####### Degenerate spheres σ + +∞ and σ+∞ .

Thus we consider the neighborhood for q: V∞(p) := {|xq| ≤ zp βr* , |yq| ≤ zp βr*}, and 128κsupyp 128κsupxp show that the boundary of the intersection does not overcome the strip defined by:

The degenerate balls B (σ+∞) and B (σ+∞) are actually the half-spaces on both sides of the plane Psym passing through p, q, p. Once projected on the tangent plane, the intersection of Psym with S between p and q is very close to the segment [pπp(q)]. In the spheroid case, we knew that the intersection was an ellipse, and in particular a convex body. Now, it is not anymore the case, and we just show that, locally, the boundary of the projection of the intersection πp(S∩Psym) is caught between two lines parallel with the line (pπp(q)).

$$S t ( p , q ) \colon = | y _ { q } x - x _ { q } y | \leq \frac { 1 } { 3 2 } \beta _ { r ^ { * } } ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) ,$$

in the disk D(p, πp(q)), see Figure 16.3. This strip has width βr*√ + y2. 16

Figure 16.3: The projection of the intersection S ∩ Psym (in blue) is locally contained in a strip St(p, q) with width 1 βr* x2 + y2 for q close enough to p. 16

p

Claim d. If q ∈ π−1 (V∞(p)), then πp (rt∞) contains ellk (p, q)\St(p, q), and πp (r+∞) contains ell1(p, q)\ St(p, q).

Proof. We search for an equation of Psym(p, q). Its normal vector is given by the cross product of the vectors normal to the planes PBis and PMed:

$$\left ( \begin{matrix} x _ { q } \\ y _ { q } \\ z _ { q } \end{matrix} \right ) \times \left ( \begin{matrix} x _ { \overline { p } } \\ y _ { \overline { p } } \\ z _ { \overline { p } } x _ { \overline { p } } - x _ { q } z _ { \overline { p } } \\ x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } \end{matrix} \right ) .$$

An equation of Psym(p, q) is then:

$$\mathcal { P } _ { \text {sym} } ( p , q ) \colon 0 = ( y _ { q } z _ { \overline { p } } - z _ { q } y _ { \overline { p } } ) \, x + ( z _ { q } x _ { \overline { p } } - z _ { \overline { p } } x _ { q } ) \, y + ( x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } ) \, z .$$

We show that, if q is close enough to p, then projection of the portion of the intersection of the surface with the plane is close to the line (p, πp(q)). The projection of the intersection S∩Psym(p, q) is given by substituting z by fp(x, y):


<!-- p:186 -->


$$0 & = ( y _ { q } z _ { \overline { p } } - z _ { q } y _ { \overline { p } } ) \, x + ( z _ { q } x _ { \overline { p } } - z _ { \overline { p } } x _ { q } ) \, y + ( x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } ) \, f _ { p } ( x , y ) \\ & = ( y _ { q } x - x _ { q } y ) \, z _ { \overline { p } } + ( x _ { \overline { p } } y - y _ { \overline { p } } x ) z _ { q } + ( x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } ) \, f _ { p } ( x , y )$$

Thus (x, y) verifies:

$$s \left ( x , y \right ) \text { Verifies} & \colon \\ & y _ { q } x - x _ { q } y = \frac { 1 } { z _ { \overline { p } } } \left ( \left ( x _ { \overline { p } } y - y _ { \overline { p } } x \right ) z _ { q } + \left ( x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } \right ) f _ { p } ( x , y ) \right ) \text { and,} \\ & | y _ { q } x - x _ { q } y | = \frac { 1 } { z _ { \overline { p } } } | ( x _ { p } y - y _ { p } x ) z _ { q } + ( x _ { q } y _ { p } - y _ { q } x _ { p } ) \, f _ { p } ( x , y ) | \\ & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { w h e r d } \intertext { o n d } \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { o n d } & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { o n d } & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { o n d } & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \left ( x ^ { 2 } + y ^ { 2 } \right ) \\ & \intertext { s u p } & \intertext { o n d } & \intertext { s u p } & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { \overline { p } } y - y _ { \overline { p } } x | \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) + \frac { \kappa _ { \sup } } { z _ { \overline { p } } } | x _ { q$$

+ y2:

$$& \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } \left ( | x _ { \overline { p } } y - y _ { \overline { p } } x | + | x _ { q } y _ { \overline { p } } - y _ { q } x _ { \overline { p } } | \right ) \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) \\ & \leq \frac { \kappa _ { \sup } } { z _ { \overline { p } } } \left ( | x _ { \overline { p } } y | + | y _ { \overline { p } } x | + | x _ { q } y _ { \overline { p } } | + | y _ { q } x _ { \overline { p } } | \right ) \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) \\ & \leq \frac { 1 } { 3 2 } \beta _ { r ^ { * } } \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) , \\ \right ) < \beta _ { q } \sum _ { z _ { \overline { p } } } \, o r d \, m o y _ { \overline { q } } ( | x _ { \overline { p } } | \, | x _ { q } | ) < \beta _ { q } \sum _ { z _ { \overline { p } } } \, z _ { \overline { p } }$$

for max (|x|, |xq|) ≤ βr* zp and max (|y|, |yq|) ≤ βr* zp 128κsup|yp| 128ksup|xp|

Then we denote by V® (p) the neighborhood around p defined as the set of q such that ωp(q) ∈ V∞(p), and St(p, ωp(q)) as the strip with width 16βr* pπp(ωp(q))| around the line (p, πp(ωp(q))) in Ts(p). Similarly, we obtain:

Claim e. If q ∈ π−1 ( ̄∞(p)), then π− (rx) contains ellk(p, ωp(q)) \ St(p, ωp(q)), and πp (rx) contains ell1(p, ωp(q)) \ St(p, ωp(q)).

Then we can choose Loc(p) = π−1 (VLow(p) ∩ VMed(p) ∩VMed(p) ∩V∞(p) ∩V∞ (p))

####### Degenerate sphere σHigh. +∞

For this lasts sphere, we can choose any infinite center cHigh +∞ in PBis such that its corresponding halfspace contains ell1(p, ωp(q)).

$$\text {Claim } f . \ I f \, q \in L o c ( p ) \ t h e n \ \pi _ { \overline { p } } ( r _ { E x t } ^ { + \infty } ) \ c o n t a i n s \ e l l ^ { 1 } ( \overline { p } , \omega _ { p } ( q ) ) .$$

Now that every sphere has been chosen, we can use the Combination and Partition lemmas to show the graph inclusion.

##### 16.2.2 Proof of the graph inclusion

We consider the two regions in the tangent plane Ts(p):

$$\bullet \, \tilde { \ r h } _ { r } ^ { \beta _ { r ^ { * } } } ( p , q ) \coloneqq \text {ell} _ { r } ^ { 1 } ( p , q ) \cap \text {ell} ^ { \beta _ { r ^ { * } } } ( p , q ) \ \text {St} ( p , q ) , \text { and}$$

$$\bullet \ \tilde { r } \tilde { h } _ { \ell } ^ { \beta _ { r } * } ( p , q ) \colon = \text {ell} _ { \ell } ^ { 1 } ( p , q ) \cap \text {ell} ^ { \beta _ { r } * } ( p , q ) \ \ S t ( p , q ) ,$$

and the two regions in the tangent plane Ts(p):

$$\bullet \ \tilde { r } \tilde { h } _ { r } ^ { \beta _ { r } * } ( \overline { p } , \omega _ { p } ( q ) ) \colon = \text {el} _ { r } ^ { 1 } ( \overline { p } , \omega _ { p } ( q ) ) \cap \text {el} ^ { \beta _ { r } * } ( \overline { p } , \omega _ { p } ( q ) ) \ \vee \text {St} ( p , q ) , \text { and}$$


<!-- p:187 -->


$$\bullet \ \tilde { r } \tilde { h } _ { \ell } ^ { \beta _ { r } * } ( \overline { p } , \omega _ { p } ( q ) ) \colon = \text {el} _ { \ell } ^ { 1 } ( \overline { p } , \omega _ { p } ( q ) ) \cap \text {el} ^ { \beta _ { r } * } ( \overline { p } , \omega _ { p } ( q ) ) \ \{ S t ( \overline { p } , \omega _ { p } ( q ) ) .$$

All of those four regions are half-rhombuses that have been truncated by St(p, q) or St(p, ωp(q)). o Gsnd  os n  (o    t rd o a o o n y and q and centered on c verifies (remind that we assume zc &gt; 0):

- 1 (rhr (p, 9),
- if c ∈ (c% , Med, CLow, ce), then B (σ) ∩S contains π−1
- (rhr (D, p()), and · if c ∈ (cx , CMed, CHigh), then B (σ) ∩S contains π−1
- (rhe (,, wp(a). t  ()   ( )

Note that, one of these regions may be a triangle even if gave four vertices, but what is important is that the triangle is included in the region defined by the four vertices (see Figure 16.4)

Figure 16.4: Partition of the upper part of PBis for p ∈ S \ H ∪ H'+ and q ∈ Loc(p). It is decomposed into four parts. A sphere passing through p and q centered in any part contains a region of S whose projection on Ts(p) or Ts(p) is one of the four "reduced" half-rhombuses.

cHigh

+∞

ell1(p, ωp(q))

ell1(p, q) \ St(p, q),

(p, ωp(q))

ell1(p, ωp(q)) \ St(p, ωp(q))

ellβr (p, ωp(q))

cMed


ellβr+ (p, q)

rh

(p,

q)

3

ell

(p,

, q)

ell1

el1

ce

0 = z

cLow

Cr

ci

ellk(p, q) \ St(p, q),

ell(p, ωp(q)) \ St(p, ωp(q))

Then for p ∈ S \ (H ∪ H′+) and q ∈ Loc(p), we consider the family FLoc(p, q) of fundamental regions on S:

$$\mathcal { F } _ { L o c } ( p , q ) & \colon = \left \{ \begin{array} { c } \pi _ { p } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } ( p , q ) \right ) , \pi _ { p } ^ { - 1 } \left ( \tilde { r } h _ { \ell } ^ { \beta _ { r } * } ( p , q ) \right ) \\ \pi _ { \overline { p } } ^ { - 1 } \left ( \tilde { r } h _ { r } ^ { \beta _ { r } * } ( \overline { p } , \omega _ { p } ( q ) ) \right ) , \pi _ { \overline { p } } ^ { - 1 } \left ( \tilde { r } h _ { \ell } ^ { \beta _ { r } * } ( \overline { p } , \omega _ { p } ( q ) ) \right ) \end{array} \right \} ,$$

and the empty region graph in which there is an edge (p, q) if and only if there exists r ∈ FLoc(p, q) such that r ∩ X = ∅.

Since the four regions partition PBis(p, q) ∩ {z &gt; 0}, we deduce by Partition lemma:


<!-- p:188 -->


Lemma 16.4. Let p ∈ S \ (H ∪ H′+δ) and q ∈ Loc(p).

##### 16.2.3 Computation of the expected degree

Then we compute an upper bound on the local expected degree E [deg|Loc(p, Del)] of a point p ∈ S\ (H ∪ H′+ ∪ Z+ ∪ Y +). We use Gf as a super-graph. Since the regions of FLoc are half-rhombuses and since |pωp(q)| = Θ(|pq|), the degree behaves as expected. Keep in mind that |rhr* (p, q)| = |rher* (p, q)|.

Since rh* (p, q) corresponds to a half rhombus for with deleted a strip, we have to compute the new area:

Since 0 ≤ βr* ≤ 1, we have well:

Recall that rhβr* (p, q) has area 1 √(xa + y)(βr+2x2− + y2) . Since the width of St(p, q) is βr*√ + y2 16 16 and it diameter is 2y /x2 i + y2, St(p, q) has an area smaller than  βr* (x2 + y2). The part of St(p, q) that we delete from rhβr* (p, q) is only one quarter of St(p, q).

$$\frac { 1 } { 4 } | S t ( p , q ) | \leq \frac { 1 } { 4 } \frac { \beta _ { r ^ { * } } } { 8 } ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } ) \leq \frac { 1 } { 3 2 } \sqrt { \left ( x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) \left ( \beta _ { r ^ { * } } ^ { 2 } x _ { q } ^ { 2 } + y _ { q } ^ { 2 } \right ) } \leq \frac { 1 } { 2 } \left | \mathfrak { rh } _ { r } ^ { \beta _ { r ^ { * } } } ( p , q ) \right | .$$

Thus we have:

and we can compute the expected local degree:

$$\text {have} \colon & \quad \left | \tilde { r } \hbar { ^ } { r * } \left ( p , q \right ) \right | \geq \left | \text {rh} _ { r } ^ { \beta _ { r ^ { * } } } \left ( p , q \right ) \right | - \frac { 1 } { 4 } | \text {St} ( p , q ) | \geq \frac { 1 } { 2 } \left | \text {rh} _ { r } ^ { \beta _ { r ^ { * } } } \left ( p , q \right ) \right | , \\ \intertext { h a v e \colon } & \quad \text {computo the evo-ooted local degree} \colon$$

$$and we can compute the expected local degree: \\ \\ \mathbb { E } \left [ \deg _ { \text {Loc} } ( p , \text {Del} ) \right ] & = \lambda \int _ { q \in \text {Loc} } \mathbb { P } \left [ ( p , q ) \in \text {Del} ( X \cup \{ p \} ) \right ] d q \\ & \leq \lambda \int _ { q \in \text {Loc} } \mathbb { P } \left [ ( p , q ) \in \mathcal { G } _ { \mathbb { F } _ { \text {Loc} } } ^ { \overline { 0 } } ( X \cup \{ p \} ) \right ] d q \\ & \leq \lambda \int _ { q \in \text {Loc} } \sum _ { \mathcal { F } _ { \text {Loc} } } \mathbb { P } \left [ r \cap X \right ] d q \\ & \leq 2 \lambda \int _ { q \in \text {Loc} } \mathbb { P } \left ( \pi _ { p } ^ { - 1 } \left ( \bar { r } _ { r ^ { * } } ^ { \beta * } ( p , q ) \right ) \cap X \right ] + \mathbb { P } \left [ \pi _ { \bar { r } } ^ { - 1 } \left ( \bar { r } _ { r ^ { * } } ^ { \overline { \beta } ^ { * } } ( \bar { p } , \omega _ { p } ( q ) ) \right ) \cap X \right ] d q \\ & = 2 \lambda \int _ { q \in \text {Loc} } e ^ { - \lambda | \pi _ { p } ^ { - 1 } \left ( \bar { r } _ { r ^ { * } } ^ { \beta * } ( p , q ) \right ) | } + e ^ { - \lambda | \pi _ { r } ^ { - 1 } \left ( \bar { r } _ { r ^ { * } } ^ { \overline { \beta } ^ { * } } ( \bar { \tau } _ { \omega } , \omega _ { p } ( q ) ) \right ) } | d q \\ & \leq 2 \lambda \int _ { q \in \text {Loc} } e ^ { - \lambda | \bar { r } _ { r ^ { * } } ^ { \beta * } ( p , q ) | } + e ^ { - \lambda | \bar { r } _ { r ^ { * } } ^ { \overline { \beta } ^ { * } } ( \bar { \tau } _ { \omega } , \omega _ { p } ( q ) ) } | d q \\ & \leq 2 \lambda \int _ { q \in \text {Loc} } e ^ { - \lambda | \bar { r } _ { r ^ { * } } ^ { \beta * } ( p , q ) | } + e ^ { - \lambda K _ { \text {sym} } ^ { 2 } \left | \bar { r } _ { r ^ { * } } ^ { \overline { \beta } ^ { * } } ( p , q ) \right | } d q \\ & \leq 2 \lambda \int _ { q \in \text {Loc} } \frac { \bar { e } ^ { | \bar { r } _ { r ^ { * } } ^ { \beta * } ( p , q ) | } + e ^ { - \bar { r } _ { r ^ { * } } ^ { K _ { r ^ { * } } } \left | \bar { r } _ { r ^ { * } } ^ { \overline { \beta } ^ { * } } ( p , q ) \right | } d q } { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } \ln \frac { 1 } { 1 - \bar { \kappa } _ { 1 } ( p ) r ^ { * } ( p ) } \right ) . \\ \\ \text {Lemma 16.5.  Let p \in S \ (H \cup H ^ { + } \cup Z ^ { + } \cup Y ^ { + } ) , \text { the expected number } \mathbb { E } \left [ \deg _ { \text {Loc} } ( p , \text {Del} ) \right ] \text { of neighbors } \\ \text {of } p \text { in } \text {Del} ( X \cup \{ p \} ) \text { that are in } \text {Loc} ( p ) \text { is:}$$

Lemma 16.5. Let p ∈ S \ (H ∪ H'+ ∪ Z+ ∪ Y+), the expected number E [deg|Loc (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Loc(p) is:

$$\mathbb { E } \left [ \deg _ { | L o c } ( p , D e l ) \right ] = O ( 1 ) .$$

c(X ∩ {p}).


<!-- p:189 -->


Proof. We apply the result above for p a distance greater than a constant from H ∪ Z ∪ Y. Since the value minp∈s\(H∪H'+∪z+∪Y+) (1 − κ1(p)r*(p), 1 − κ1r*(p)) reaches a strictly positive minimum. □

At this stage, we know that the expected local degree of a point far from δ from Z or Y is O(1). The only part of the surface that remains undone with the local degree is Z+ ∪ Y+. We treat it in the next section.

#### 16.3 Local degree of a point close to Z or Y

In this section, we compute the expected local degree of point close to Z or Y. In a first part, we recall geometric results already present in [ABL03]. It will allow to express the expected degree of p with respect to its distance to Z. Then we divide the remaining into 2 parts, depending on if p is close to Z or close to Y.

##### 16.3.1 On the position of p and the value 1 − κ1(p)r*(p)

Consider a point pz ∈ Z, and the medial sphere at p. Recall that on Z the medial sphere corresponds to the first osculating sphere. We place the surface in Monge coordinate system of pz, thus we use the notations (u, v, w) for the coordinates, as we did in Chapter 13, to make a difference with the coordinate systems at p in which p is the origin.

The Taylor approximation of a sphere σ tangent to pz and with radius r is z = fσ(u, v) where:

$$f _ { \sigma } ( u , v ) = \frac { 1 } { 2 r } ( u ^ { 2 } + v ^ { 2 } ) + \frac { 1 } { 8 r ^ { 3 } } \left ( u ^ { 2 } + v ^ { 2 } \right ) ^ { 2 } + O \left ( \left ( u ^ { 2 } + v ^ { 2 } \right ) ^ { 3 } \right ) ,$$

and that the Taylor approximation of the graph z = fp(u, v) of the surface is:

$$f _ { p _ { Z } } ( u , v ) = \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } v ^ { 2 } + \frac { 1 } { 6 } \left ( m _ { 3 , 0 } u ^ { 3 } + 3 m _ { 2 , 1 } u ^ { 2 } v \right ) + \frac { 1 } { 2 4 } m _ { 4 , 0 } u ^ { 4 } + O \left ( | u ^ { 5 } | + | u ^ { 3 } v | + | u | v ^ { 2 } + | v | ^ { 3 } \right ) .$$

Co is    d  e f n t oe e t steoc and S) at pz:

$$f _ { \Delta } ( u , v ) & = f _ { \sigma ^ { * } } ( u , v ) - f _ { p z } ( u , v ) \\ & = \frac { 1 } { 2 } \kappa _ { 1 } ( u ^ { 2 } + v ^ { 2 } ) + \frac { 1 } { 8 } \kappa _ { 1 } ^ { 3 } ( u ^ { 2 } + v ^ { 2 } ) ^ { 2 } + O \left ( \left ( u ^ { 2 } + v ^ { 2 } \right ) ^ { 3 } \right ) \\ & - \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } v ^ { 2 } + \frac { 1 } { 6 } \left ( m _ { 3 , 0 } u ^ { 3 } + 3 m _ { 2 , 1 } u ^ { 2 } v \right ) + \frac { 1 } { 2 4 } m _ { 4 , 0 } u ^ { 4 } \right ) + O \left ( | u ^ { 5 } | + | u ^ { 3 } v | + | u | v ^ { 2 } + | v | ^ { 3 } \right ) \\ & = \frac { 1 } { 2 } \left ( \kappa _ { 1 } - \kappa _ { 2 } \right ) v ^ { 2 } - \frac { 1 } { 6 } m _ { 3 , 0 } u ^ { 3 } - \frac { 1 } { 2 } m _ { 2 , 1 } u ^ { 2 } v + \frac { 1 } { 2 4 } ( 3 \kappa _ { 1 } ^ { 3 } - m _ { 4 , 0 } ) \, u ^ { 4 } + O \left ( | u ^ { 5 } | + | u ^ { 3 } v | + | u | v ^ { 2 } + | v | ^ { 3 } \right ) . \\ \intertext { B y d f i n t i o n f t h e m d i s e r p h e r s . h i n t h a q u n t i y s o t a i t i v e a r o w d o n ( 0 , 0 ) . }$$

By definition of the medial sphere, this quantity is 0 at (0, 0), and positive around (0, 0). Along the line u = 0, we have:

$$f _ { \Delta } ( 0 , v ) = \frac { 1 } { 2 } ( \kappa _ { 1 } - \kappa _ { 2 } ) v ^ { 2 } + O ( v ^ { 3 } ) .$$

As we said in Part I, Chapter 1, generically no umbilical points lie on Z. Thus the quantity κ1 − κ2 is strictly positive on Z. We denote by μz the minimum of κ1 − κ2 on Z:

$$\mu _ { Z } \colon = \min _ { p \in Z \cup Z ^ { \prime } } \{ \kappa _ { 1 } ( p ) - \kappa _ { 2 } ( p ) \} .$$

We consider the new condition on δz:

$$\text {For any } p \in Z ^ { + } , \kappa _ { 1 } ( p ) - \kappa _ { 2 } ( p ) \geq \frac { 1 } { 2 } \mu _ { Z } .$$

Thus, no umbilical points lie in Z+ neither.

Along the line v = 0, we have

$$f _ { \Delta } ( u , 0 ) = - \frac { 1 } { 6 } m _ { 3 , 0 } u ^ { 3 } + O ( u ^ { 4 } ) .$$


<!-- p:190 -->


It is therefore necessary that m3,0 = 0. That condition reflects that at Z, the surface reaches an extremum of curvature along the maximal direction.

We can go further by considering the curve v = φ(u) for φ(u) = m2,1 u2, that approximates the 2(κ1−κ2) curvature line at p:

$$\text {curvature line at $p$} \colon & \\ f _ { \Delta } ( u , \phi ( u ) ) = \frac { 1 } { 2 } ( \kappa _ { 1 } - \kappa _ { 2 } ) \phi ( u ) ^ { 2 } - \frac { 1 } { 2 } m _ { 2 , 1 } u ^ { 2 } \phi ( u ) + \frac { 1 } { 2 4 } \left ( 3 \kappa _ { 1 } ^ { 3 } - m _ { 4 , 0 } \right ) u ^ { 4 } + O ( u ^ { 5 } ) \\ = \frac { 1 } { 2 } ( \kappa _ { 1 } - \kappa _ { 2 } ) \left ( \frac { m _ { 2 , 1 } } { 2 ( \kappa _ { 1 } - \kappa _ { 2 } ) } u ^ { 2 } \right ) ^ { 2 } - \frac { 1 } { 2 } m _ { 2 , 1 } \frac { m _ { 2 , 1 } } { 2 ( \kappa _ { 1 } - \kappa _ { 2 } ) } u ^ { 4 } + \frac { 1 } { 2 4 } \left ( 3 \kappa _ { 1 } ^ { 3 } - m _ { 4 , 0 } \right ) u ^ { 4 } + O ( u ^ { 5 } ) \\ = \frac { 1 } { 2 4 } \left ( 3 \kappa _ { 1 } ^ { 3 } - m _ { 4 , 0 } - \frac { 3 m _ { 2 , 1 } } { \kappa _ { 1 } - \kappa _ { 2 } } \right ) u ^ { 4 } + O ( u ^ { 5 } ) .$$

That proves that the quantity 3κ3 − m4,0 − is non negative on Z. As it is done in [ABL03], we κ1−κ2 denote this quantity by α(p):

$$\alpha ( p ) \colon = 3 \kappa _ { 1 } ( p ) ^ { 3 } - m _ { 4 , 0 } ( p ) - \frac { 3 m _ { 2 , 1 } ( p ) ^ { 2 } } { \kappa _ { 1 } ( p ) - \kappa _ { 2 } ( p ) } .$$

Since a non negative function does not reach 0 generically, then we can say that there exists α0 &gt; 0 such that 3κ1(p)3 − m4,0(p) − 3m2,1(p)2 ≥ α0 for any p ∈ Z. κ1(p)−κ2(p)

We can add a new condition on δz:

$$\text {For any } p \in Z ^ { + } , \alpha ( p ) > \frac { 1 } { 2 } \alpha _ { 0 } . \\$$

The new quantity α0 will play the role of 1 − κ1r* in the previous chapter, i.e. it will give, up to a constant factor, a bound on the neighborhood in which we apply the next super-graph. The difference is that α0 is a constant of the surface, like κsup, and does not depend on p.

They computed the position of p.

When p is close to Z, the points p and p are locally related. We reuse here the geometric results presented by Attali et al. [ABL03]. We consider now that pz is the closest point on Z from p, and consider the Monge coordinate system at pz. In this frame the coordinates of p are denoted by (up, vp, wp) and the coordinate p by (up, vp, wp).

Proposition 16.6 (Attali et al.).

$$\begin{array} { r l r } { u _ { \overline { p } } } & = } & { - u _ { p } + O ( u _ { p } ^ { 2 } ) , } \\ { v _ { \overline { p } } } & = } & { O ( u _ { p } ^ { 3 } ) . } \end{array}$$

and the curvatures and medial radius of p:

Proposition 16.7 (Attali et al.).

$$\begin{array} { r l r } { \frac { 1 } { r ^ { * } ( p ) } } & { = } & { \kappa _ { 1 } - \frac { 1 } { 2 } \left ( \frac { 1 } { 3 } \alpha + \frac { m _ { 2 , 1 } ^ { 2 } } { \kappa _ { 1 } - \kappa _ { 2 } } \right ) u _ { p } ^ { 2 } + O ( u _ { p } ^ { 3 } ) , } \\ { \kappa _ { 1 } ( p ) } & { = } & { \kappa _ { 1 } - \frac { 1 } { 2 } \left ( \alpha + \frac { m _ { 2 , 1 } ^ { 2 } } { \kappa _ { 1 } - \kappa _ { 2 } } \right ) u _ { p } ^ { 2 } + O ( u _ { p } ^ { 3 } ) , } \\ { \kappa _ { 2 } ( p ) } & { = } & { \kappa _ { 2 } + O ( u _ { p } ) . } \end{array}$$

where the constants κ1, κ2, m2,1, and α, depends on pz.

Since the distance hp of p from Z corresponds asymptotically to up, we obtain:

$$h _ { p } \text { or } p \text { in } 2 \text { corresponds as } & \alpha h \text { in } 0 \text { (with } 0 \text { in } 0 \text { (with } 0 \text { in } 0 \text { )} \\ & 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) = r ^ { * } ( p ) \left ( \frac { 1 } { r ^ { * } ( p ) } - \kappa _ { 1 } ( p ) \right ) \\ & = r ^ { * } ( p ) \left ( \frac { 1 } { 3 } \alpha h _ { p } ^ { 2 } + O ( h _ { p } ^ { 3 } ) \right ) \\ & = \frac { 1 } { 3 } \frac { \alpha } { \kappa _ { 1 } ( p ) } h _ { p } ^ { 2 } + O ( h _ { p } ^ { 3 } ) , \\ \text {and } 1 - \overline { \kappa } _ { 1 } ( p ) r ^ { * } ( p ) = 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) + O ( h _ { p } ^ { 3 } ) .$$


<!-- p:191 -->


##### 16.3.2 Local degree of a point at distance hp from Z

We apply the approximations described above, in the computations already done at Section 16.2.3. Recall that we had:

$$\mathbb { E } \left [ \deg _ { | L o c } ( p , D e l ) \right ] = O \left ( \ln \frac { 1 } { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } + \frac { 1 } { K _ { S y m } ^ { 2 } } \ln \frac { 1 } { 1 - \overline { \kappa } _ { 1 } ( p ) r ^ { * } ( p ) } \right ) .$$

By adapting the values to the case of a point p close to Z, and assuming that δz is small enough so that:

$$\text {For any } p \in Z ^ { + } , \, \frac { 1 } { 2 } \left ( 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) \right ) \leq 1 - \kappa _ { 1 } ( \overline { p } ) r ^ { * } ( p ) \leq 2 \left ( 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) \right ) . \quad \text {(C)} _ { \overline { p } }$$

We deduce the local expected degree of a point p close to Z:

Lemma 16.8. Let p in Z+, at distance hp from Z, the expected number E [deg|Loc (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Loc(p) is:

$$\mathbb { E } \left [ \deg _ { | L o c } \left ( p , D e l \right ) \right ] = O \left ( \ln \frac { 1 } { h _ { p } } \right ) .$$

Proof. We start by adapting Lemma 16.3, that bounds the distance |pωp(q)| with respect to |pq|. Far from Z, we had |pωp(q)| ≈ Ksym|pq|. When p is close to Z, the surface gets back to an almost symmetrical structure and we actually have |pωp(q)| ≈ |pq|. This provides an expected degree that is:

$$\mathbb { E } \left [ \deg _ { | L o c } ( p , D e l ) \right ] = O \left ( \ln \frac { 1 } { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } + \ln \frac { 1 } { 1 - \overline { \kappa } _ { 1 } ( p ) r ^ { * } ( p ) } \right ) .$$

By the approximations we also have that κ1(p) ≈ κ1(p), so we deduce:

$$\mathbb { E } \left [ \deg _ { | L o c } ( p , D e l ) \right ] = O \left ( \ln \frac { 1 } { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } \right ) .$$

And finally, since: 1 − κ1(p)r*(p) ≈ 3 κ1 α we have:

$$\mathbb { E } \left [ \deg _ { | L o c } ( p , D e l ) \right ] = O \left ( \ln \frac { 1 } { h _ { p } } \right ) .$$

□

An important difference between points in Z+ and the others, is the size of their local neighborhood Loc(p): it decreases to 0 when p tends to Z. Indeed, close to Z the size of Loc(p) is determined by the size of those two neighborhoods:

$$\bullet \ V _ { M e d } ( p ) = \left \{ \max ( | x _ { q } | , | y _ { q } | ) \leq \frac { 1 } { 1 6 \kappa _ { \sup } } \min \left ( 4 \sqrt { 2 \left ( 1 - \kappa _ { 1 } r ^ { * } \right ) } , \frac { ( 1 - \kappa _ { 1 } r ^ { * } ) \kappa _ { \sup } } { r ^ { * } M _ { 3 } } , \frac { | z _ { \frac { p } { x _ { p } } } | } { | x _ { \frac { p } { x _ { p } } } | } , \frac { 1 - \kappa _ { 1 } r ^ { * } } { 1 - \kappa _ { 2 } r ^ { * } } \frac { | z _ { \frac { p } { y _ { p } } } | } { | y _ { \frac { p } { y _ { p } } } | } \right ) \right \} , \text { and }$$

$$\bullet \ V ^ { \infty } ( p ) \colon = \left \{ | x _ { q } | \leq \frac { ( 1 - \kappa _ { 1 } r ^ { * } ) z _ { \overline { p } } } { 1 2 8 \kappa _ { \s u p } y _ { \overline { p } } } , | y _ { q } | \leq \frac { ( 1 - \kappa _ { 1 } r ^ { * } ) z _ { \overline { p } } } { 1 2 8 \kappa _ { \s u p } x _ { \overline { p } } } \right \} .$$

The other neighborhoods remain bounded from below.

If we analyze those quantities around Z, we obtain that they contain a disk around p with radius Ω(h3). Since it goes to zero, we need to know what is the probability, for such a point p to have a neighbor at distance Ω(h3). We will do the computation in Chapter 18, and show that, as for the spheroid case, we cannot count them directly, and we need to consider a middle-range neighborhood.


<!-- p:192 -->


##### 16.3.3 Local degree of a point close to Y

Let p ∈ Y+. We could have used a method related with the symmetrical p of p, but the value 1 − κ1r* is close to 0, and we might have problem. Nevertheless, the medial sphere at p is not osculating at all, and for q close to p, we can consider a slightly different partition of PBis(p, q) than usual.

Usually, we considered also the sphere σMed(p, q) whose intersection with S contained an ellipse on the side of p and another ellipse on the side of p. The problem is that, on the side of p, the aspect ratio of the region σMed(p, q) ∩S can be small, and we need an alternative sphere that plays the role of σMed(p, q). We use the sphere σγ (p, q) instead. It is defined as follows:

Let q be close p and consider the five spheres passing through p and q, that we already used: σLow(p, q), σe(p, q), σr(p, q), σ (p, q), σr (p, q). We recall briefly which spheres are these spheres. σLow(p, q) is not so far from the sphere centered on the middle of [pq]. σe(p, q) and σr(p, q) correspond to both sides of the plane passing through p and q and that is orthogonal to Ts(p). σ) (p, q) and σ (p, q) correspond to both sides of the plane passing through p and q and p.

####### Sphere σY:

We denote by βγ the ratio:

$$\beta _ { Y } \coloneqq \sqrt { \frac { 1 - \kappa _ { 1 } \left ( \frac { 1 } { 2 } \left ( \frac { 1 } { \kappa _ { 1 } } + r ^ { * } \right ) \right ) } { 1 - \kappa _ { 2 } \left ( \frac { 1 } { 2 } \left ( \frac { 1 } { \kappa _ { 1 } } + r ^ { * } \right ) \right ) } } = \sqrt { \frac { 1 - \kappa _ { 1 } r ^ { * } } { 2 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } - \kappa _ { 2 } r ^ { * } } } .$$

The idea is that this sphere is slightly higher than the medial sphere, and for q close enough to p, it contains a non negligible part of the surface that we denote Āy (p, q) on the side of p. On the other hand, it is slightly lower than the osculating sphere, and then it contains an ellipse on the side of p for which we can compute the ratio.

Using similar computations than before, we can show:

Claim y. There exists a neighborhood Vγ (p) of p in Ts(p) with radius Ω(1), such that if q ∈ π−1 (Vr (p)), then πp (rY) contains ellβY (p, q) and A(p, q).

Then we define Loc(p, q) as the intersection of the neighborhoods associated with each spheres. We denote by Ar(p, q) := Ā(p, q) ∩ B(σr), and by Ae(p, q) := A(p, q) ∩ B(σe). Those two regions have both an area greater than a positive constant, since when q = p, the sphere is higher σy(p, q) is bigger than the medial sphere.

Thus we deduce can deduce that:

Lemma 16.9. Let p in Y+, the expected number E [deg|Loc (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Loc(p) is:

$$\mathbb { E } \left [ \deg _ { | L o c } \left ( p , \text {Del} \right ) \right ] = O \left ( 1 \right ) .$$

The sphere σY is the sphere passing through p and q, whose center c = (xc, yc, zc) verifies also:

$$\left \{ \begin{array} { l l l } { 0 } & { = } & { ( 1 - \kappa _ { 1 } z _ { c } ) \, x _ { q } y _ { c } - ( 1 - \kappa _ { 2 } z _ { c } ) \, y _ { q } x _ { c } , } \\ { z _ { c } } & { = } & { \frac { 1 } { 2 } \left ( \frac { 1 } { \kappa _ { 1 } } + r ^ { * } \right ) . } \end{array}$$


<!-- p:193 -->


186 Chapter 16. Expected local degree of a point


<!-- p:194 -->


## Chapter 17

### Expected remote degree of a point

In this section, we count the remote Delaunay neighbors of the points of S. The remote Delaunay neighbors of p are the points q such that (p, q) is a Delaunay edge joining two sample points on distant part of the surface, but necessarily, q is close to a symmetrical point of p.

We will consider a second neighborhood, the remote neighborhood denoted by Rem(p) of possible Delaunay neighbors around the symmetrical points of p. We will show that the sizes of Rem(p) and Loc(p) are linked.

We briefly recall that:

- S' is a set of curves on S. A point on S' has two symmetrical points.
- An S" point is at the concurrency of three S' curves.
- An H" point is at the concurrency of two H' curves and an S' curve.
- A Z' point is at the concurrency of two S' curves and a Z curve.
- A Y point is at the end of an S' curve, and is the symmetrical point of a Z' point.

#### 17.1 Far from the convex hull and with one symmetrical point

We start by counting the number of remote neighbors of a point p ∈ S\ (H ∪ H+ ∪ S'+). Thus p has exactly 1 symmetrical point p, the medial radius r* of p is finite, the quantities 1 − κ1r* and 1 − κ1r* are bounded from below by a positive constant, and p and p are far from a point with multiple symmetrical points. We recall that Z′ and Y are included in S'+.

When there is a single symmetrical point, we denote by Rem(p) := Loc(p), i.e. the local neighborhood of the symmetrical point p, defined in the previous chapter. We consider a point q in Rem(p). Consider the circle passing through p, p and q. It passes through another point of S close to p, we denote this point by ωp(q). Now (p, ωp(q), q, p) forms a quadrilateral for which [pq] is a diagonal (see Figure 17.1). Thus any sphere passing through p and q, contains either a sphere passing though p and ωp(q) or a sphere

passing through p and q, and we can decompose the cases.

Let σ be sphere passing through p and q, three cases arise:

Case (A): σ contains ωp(q)

In this case, σ contains one of the two regions of FLoc(p, ωp(q)) that are centered below PMed.

Case (B): σ contains p and the center c of σ has a positive z coordinate in the Monge coordinate system of p

In this case, σ contains one of the two regions of FLoc(p, q) that are centered below PMed in the coordinate system of p.


<!-- p:195 -->


e   re   sr ss y  o s     : ωp(q).

q

SP

pωp(q)

Case (C): σ contains p and the center c of σ has a negative z coordinate in the Monge coordinate system of p

Finally, in this case, the spheres are actually quite large and it is almost impossible that they are Delaunay spheres. We denote by Tc the set of centers of such spheres in PBis(p, q). This case corresponds to spheres that are centered beyond the tangent plane of p. To illustrate that such spheres are large, o   (    se ( s ta tr     t x  t sse does not even arise. Thus we treat this case only for the points of Z+ that have their symmetrical point locally close. In that case, the sector Tc of PBis(p, q) in which c lies, is a thin cone whose vertex is at the intersection cC := PBis (p, q) ∩ Ts(p) ∩ Ts(p). We denote by σc its corresponding sphere. We denote by c∞ and cx the infinite center in the respective directions PBis (p, q) ∩ Ts(p) and PBis(p, q) ∩ Ts(p). Since p ∈ Z+ the normals at p and of p have a close direction. Thus the degenerate spheres σp and σp centered could have said that a sphere centered in Tc almost contains one half of σc. But it is not necessary the case.

Instead, we consider two intermediate spheres. The first one, σp that is centered on cp := PBis(p, q) ∩ əs {0 = } ∪ (d)L ∪ ( 'dsid =:    s te, d əds  s  {0 = } ∪ (drL (x, y, z) denotes the Monge coordinates of p. Thus the part Tc can be partitioned into the triangle Crad s oird  o  '(   ) ood n   (  n) sphere centered in Tc, contains one of this intersections:

- I1 := S ∩ B (σc) ∩ B (σp) ∩ B (σp), or
- I2 := S ∩B (σp) ∩ B (σp) ∩ B (σp) ∩ B (σx).

For a point p from which p is far, and for a point q ∈ Rem(p), these intersection are clearly Ω(1) in area. If p and p are close, in particluar if p ∈ Z+, and if q ∈ Rem(p) then q is at distance O(h3) from p, while p and p are at distance Θ(hp). Since all the spheres involved are centered in a tangent plane (either Ts(p) or Ts(p)), their global shape is circular on S (as the sphere σLow for instance). Since p and p are close, the y-axis and  ̄-axis are almost parallel. Thus, S ∩ B(σc) approaches a circle passing through p, q and p. Both the spheres σp and σp approaches the Gabriel sphere of p and p. And both the planes σp and σx contains the same half of the Gabriel sphere of p and p. Consequently, the intersection I1 and I2 have area Ω(h2). But since |pq| is O(h3), then I1 and I2 have area Ω(|pq|j). Thus the contribution, in the expected degree of p, of the spheres centered in Tc is negligible , since it is roughly:

$$\lambda \int _ { \mathbb { R } ^ { 2 } } e ^ { - \lambda ( x ^ { 2 } + y ^ { 2 } ) ^ { \frac { 1 } { 3 } } d x d y } = O \left ( \frac { 1 } { \lambda ^ { 5 } } \right ) .$$

We deduce, for points p ∈ S \ (H+ ∪ S'+), and for points q ∈ Rem(p), a super graph of the 3D- Delaunay triangulation: Let FRem(p, q) be the family of regions on S:


<!-- p:196 -->


$$\begin{array} { r } { y \, \text {triangulation: Let } \mathcal { F } _ { R e m } ( p , q ) \, \text { be the family of regions on } \mathcal { S } \colon } \\ { \mathcal { F } _ { R e m } ( p , q ) \colon = \left \{ \begin{array} { l l } { \pi _ { p } ^ { - 1 } \left ( \tilde { r } _ { r } ^ { \beta _ { r ^ { * } } } ( p , \omega _ { p } ( q ) ) \right ) , \pi _ { p } ^ { - 1 } \left ( \tilde { r } _ { \ell } ^ { \beta _ { \ell ^ { * } } } ( p , \omega _ { p } ( q ) ) \right ) } \\ { \pi _ { \overline { p } } ^ { - 1 } \left ( \tilde { r } _ { r } ^ { \overline { \beta _ { r } } } ( \overline { p } , q ) \right ) , \pi _ { \overline { p } } ^ { - 1 } \left ( \tilde { r } _ { \ell } ^ { \overline { \beta _ { \ell } } } ( \overline { p } , q ) \right ) } \\ { I _ { 1 } ( p , q ) , I _ { 2 } ( p , q ) } \end{array} \right \} , } \end{array}$$

FRem

Then we can bound the expected remote degree of a point p ∈ S \ (H′+ ∪ S'+).

Lemma 17.1. Let p ∈ S\ (H′+ ∪ S′+ ∪ Z+), the expected number E [deg|Rem (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Rem(p) is:

$$\mathbb { E } \left [ d e g _ { | R e m } \left ( p , D e l \right ) \right ] = O ( 1 ) .$$

Proof. For spheres passing through p and ωp(q), we apply Lemma 16.5. Since |pωp(q)| ≤ Ksym|pq| the expected degree remains constant. For spheres passing through p and q, since p ∈ Š \ (H'+ ∪ Š'+ ∪ Z+), then dist(Z) is greater than constant and we can apply Lemma 16.5 to p.

□

We finish this section by counting the remote Delaunay neighbors of a point close to Z. Since Z+∩S'+ is not empty, some points of Z+ have multiple symmetrical points: they are close to Z'. Thus we choose δz consequently:

$$Z ^ { \prime + } \text { contains } S ^ { \prime + } \cap Z ^ { + } .$$

We can see the condition (Cz') as a refinement on the bounds on δz and δs'.

The points around Z' will be treated in 17.4.

Lemma 17.2. Let p ∈ Z+\Z′+, the expected number E [deg|Rem (p, Del)] of neighbors of p in Del(X∪{p}) that are in Rem(p) is: E [deg|Rem (p, Del)] = 0 (ln 1 hp

Proof. We apply Lemma 16.8, for p and p. If p is beyond Z+δ, its contribution to the degree is O(1). □

Note that we might have been tempted to extend this counting in S∩H+, where points p approaches o  d r , o   d  o o o  ond   os   d  n another solution to bound efficiently the number of remote neighbors. We will do this in Section 17.3. For now we deal with the points of S'+ \ Z+, points close to those that have 2 or 3 symmetrical points but far from Z.

#### 17.2 Close to points with multiple symmetrical points

We count in this section the number of remote neighbors of points that have multiple symmetrical points, and of points that are close to points with multiple symmetrical points. It corresponds to the points of S'+. If a point p has only one symmetrical point p, it is likely to have Delaunay neighbors close p and p but not only: if p is close to a point p′ ∈ S', then p can have neighbors close to the symmetrical point p' of p' (see Figure 17.2).

To take this into account, we consider the notion of supplementary symmetrical point.


<!-- p:197 -->


Figure 17.2: A point p can have Delaunay neighbors far from {p, p}. The big points are the data sample, including p. They are triangulated. p and p are in green. p is close to a point (in red) with two symmetrical point. It has two Delaunay neighbors in its neighborhood, one in the neighborhood of p that is close to a red point, and one in the neighborhood of the third red point.

##### 17.2.1 Supplementary symmetrical points

In this section, we assume that p ∈ S, the set of points with a finite symmetrical point. We say that p is a supplementary symmetrical point of p if there exists a sphere, called supplementary medial sphere whose intersection with S contains only p, p, and a topological disk around the other symmetrical points. Such a sphere is then bitangent to S at p and p (see Figure 17.3).

We can order the symmetrical points (supplementary or not). For two symmetrical points on the same medial sphere, we order the points according to their distance with p. For two points on different medial spheres, we order the points according to the inclusion-order of the medial spheres on which they lie. Thus, if p ∈ S ∉ S' ∪ S" ∪ H' ∪ H′′ ∪ Z′, we will denote them by σi, pi, and ri the respective i-th supplementary medial sphere, symmetrical point, and medial radius. We this notation, we assume that σ0 is σ*, P0 is p, and r0 is r*, the natural medial sphere, symmetrical point, and medial radius.

If p ∈ S' ∪ S" ∪ H'∪ H" ∪ Z′, the initial medial sphere has multiple symmetrical points on it, in that case we consider that σ1 = σ0, r1 = r0 and so on, if necessary.

These supplementary symmetrical points must keep a good behavior. Indeed, the supplementary medial radius ri of p must not be larger than In other words, for points in S'+ \ Z+, 1 − κ1(p)r1(p) κ1(p) must be positive.

We refine the bounds on δs, and δs′. We denote by b(δz), the minimum of 1 − κ1(p)r*(p) for points of S \ Z+:

$$b ( \delta _ { Z } ) \colon = \inf _ { p \notin Z ^ { + } } \{ 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) \} .$$

Then we want the strip S'+ to verify:

$$\text {For any } p \in S ^ { \prime + } \ \ & \ Z ^ { + } , \ 1 - \kappa _ { 1 } ( p ) r _ { 1 } ^ { * } ( p ) > \frac { 1 } { 2 } b ( \delta _ { Z } ) . \\ \text {For any } p \in S ^ { \prime + } \ \ & \ Z ^ { + } , \ 1 - \kappa _ { 1 } ( \overline { p } _ { 1 } ) r _ { 1 } ^ { * } ( p ) > \frac { 1 } { 2 } b ( \delta _ { Z } ) .$$

A convenient value for δs, can be found since for p ∈ S' r*(p) = r1 (p) and r*(p) ≤ 1 One may κ1(p1) pay attention that this bound depends on δz.

We denote by bs the minimum of 1−κ1r* of the point of S": 1−κ2r*

$$b _ { S ^ { \prime \prime } } \colon = \min _ { p \in S ^ { \prime \prime } } \{ \frac { 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) } { 1 - \kappa _ { 2 } ( p ) r ^ { * } ( p ) } \} .$$

Then we want S"+ to verify:


<!-- p:198 -->


$$& \text {For any } p \in S ^ { \prime \prime + } , \ \frac { 1 - \kappa _ { 1 } ( p ) r _ { 2 } ^ { ( p ) } ( p ) } { 1 - \kappa _ { 2 } ( p ) r _ { ^ { * } } ( p ) } > \frac { 1 } { 2 } b _ { S ^ { \prime \prime } } . \\ & \text {For any } p \in S ^ { \prime \prime + } , \text { for } i \in \{ 1 , 2 \} , \ \frac { 1 - \kappa _ { ( \bar { 1 } , \bar { 2 } ) r _ { 2 } ^ { ( p ) } ( p ) } } { 1 - \kappa _ { ( \bar { 2 } , \bar { 1 } ) r _ { ^ { * } } ( p ) } } > \frac { 1 } { 2 } b _ { S ^ { \prime \prime } } . \\$$

A convenient value for δs can be found since S" and Z are at a positive distance form each other by genericity.

Thus we can consider that any point close to S' has at least two symmetrical points (supplementary or not) and any point close to S" has three symmetrical points.

Figure 17.3: The blue part is the surface. A point p close enough to S' (in red) has a supplementary symmetrical point p1 close to S'.

p

σ*1

p

For a point p in S'+, we will count the remote neighbors close to supplementary symmetrical point as if they were not supplementary, i.e. without taking into account the intersection part close to other symmetrical points. Thus we clearly obtain an upper bound on the expected number.

##### 17.2.2 Counting of the remote Delaunay neighbors

For each p in S ∩ S'+ \ (S"+ ∪ Z+ ∪ Y+), we define Rem(p) as the reunion of the local neighborhoods of the first and second symmetrical points (supplementary or not) as they are defined in the previous section. For each p in S"+, we add also the local neighborhood of the third symmetrical point to Rem(p). Note that we don't need to precise S∩ S"+, since S" is included in S by genericity and by the choice of δg".

We deduce:

Lemma 17.3. Let p ∈ (S′+ \ (H′+ ∪ Z+ ∪ Y+)) ∪ S"+, the expected number E [deg|Rem (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Rem(p) is:

$$\mathbb { E } \left [ \deg _ { | R e m } ( p , D e l ) \right ] = O ( 1 ) .$$

Proof. This is clear since the number of symmetrical points of p (supplementary or not) we consider is smaller than 4, since the quantities 1 − κ1(p)ri(p) and 1 − κ1(pi)ri(p) are greater than −b(δ) by condition (Cs') and (Cs′), and since the medial radii are ri (p) are finite. □

We consider now the case of points close to the boundary of the convex part in the next section.


<!-- p:199 -->


#### 17.3 Close to the boundary of the convex hull

For points around the boundary H' of the convex part, we have to consider two cases depending on if they are in H or in S. Points in S∩ H'+ have a natural symmetrical point in or close to S ∩ H'+, and sometimes two, when they lie on S'. Conversely, points in H ∩ H'+ have no finite symmetrical points and we will have to consider a supplementary one, since, if they are very close to H'+, they may have remote Delaunay neighbors.

##### 17.3.1 Points close to the boundary of the convex hull, and inside S

Let p ∈ S ∩ H′+. If p ∉ H"+, it has one natural symmetrical point p, and two otherwise (the second one is the supplementary symmetrical point p1). By smoothness of the surface, p is close to H'. Since we are going to apply our previous results on p, we have to consider that δH' verifies:

$$\text {For any } p \in S \cap H ^ { \prime + } , \, \kappa _ { 1 } ( \bar { p } ) \leq \frac { 1 } { 2 } \kappa _ { H } . & & ( \overline { C } _ { H ^ { \prime } } )$$

We recall that κH denotes the supremum of the principal curvature of points of H. It is a negative constant.

We also consider that δH" verifies:

$$\text {For any } p \in S \cap H ^ { \prime \prime + } , \, \kappa _ { 1 } ( \overline { p } ) \leq \frac { 1 } { 2 } \kappa _ { H } \text { and } \kappa _ { 1 } ( \overline { p } _ { 1 } ) \leq \frac { 1 } { 2 } \kappa _ { H } . \\$$

Then we count the number of possible Delaunay neighbors q of p close to p. As usual, we consider the point ωp(q), close to p as the fourth intersection of the circle passing through p, p and q with S. We define Rem(p) as being Loc(p). Whether p belongs to H+δ or to S \ H+δ, its local neighborhood is never reduced to p. Thus Rem(p) is a neighborhood of size strictly positive around p, in which we can apply an empty rhombus graph to obtain:

Lemma 17.4. Let p ∈ S∩ (H'+ ∪ H′+), the expected number E [deg|Rem (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Rem(p) is:

$$\mathbb { E } \left [ d e g _ { | R e m } \left ( p , D e l \right ) \right ] = O ( 1 ) .$$

Proof. For symmetrical points in S\ H'+, we apply Lemma 16.5, that counts the expected local degree of a point with a finite medial radius. Otherwise, for symmetrical points in S ∩ H+, we apply Lemma 16.2 that counts the expected local degree of a point in H'+. □

##### 17.3.2 Points close to the convex hull, inside H

If p ∈ H ∩ (H'+ ∪ H′′+), it is more complicated. Indeed consider p' the closest point of p on H' ∪ H". It is clear that p can have Delaunay neighbors close to p', but this happens with a probability decreasing with its distance to H'. Instead of computing this probability, if p ∈ H ∩ H'+, we consider again a supplementary symmetrical point, still denoted p1 and count the number of neighbors of p around p1 as if it was a real symmetrical point, i.e. as if their was an empty sphere passing through p and p1. This provides clearly an upper bound on the degree since we count more neighbors while neglecting some nnd eres ns  e o  +       s ns o ns rent.

We define the points  ̄i. By definition, the tangent plane at p touches S only at p. By analogy with the previous examples, we would like to make the medial sphere growing but it is already an plane (corresponding to the tangent plane). What we do instead, is that we turn out the medial plane so it becomes a big sphere tangent at p and containing the surface. Then we reduce it, maintaining the tangent contact until it touches the surface in another point. This point is p1. If p ∈ H ∩ H"+, we can continue the procedure, neglecting the place where the supplementary medial sphere already touches S, to obtain a second supplementary symmetrical point. The points pi belong to H.

We consider the neighborhood Rem(p) around p defined by the reunion of the neighborhoods Loc(p). We deduce the following theorem:


<!-- p:200 -->


Lemma 17.5. Let p ∈ H ∩ (H'+ ∪ H′′+), the expected number E [deg|Rem (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Rem(p) is:

$$\mathbb { E } \left [ \deg _ { | R e m } ( p , D e l ) \right ] = O ( 1 ) .$$

Proof. By Lemma 16.2 which counts the expected local degree of a point in H.

□

#### 17.4 Remote neighbors of points close to Z' or to Y

The points in Y and Z′ are natural symmetrical points, thus if there is a Delaunay edge (p, q) with p in Z'+ and q in Y+, we can choose to count an edge only as it is issue either from p or from q, depending on which one is the more convenient to compute. We choose to compute edges issue from Z'+. In other words, we do not count the remote Delaunay neighbors of a point p in Y+.

We recall the generic configuration of the sets Z, Z′, S' and S". A Z' point is the endpoint of a curve in Z and two curves in S'. At a Z' point, the medial sphere has another contact point, it is a Y point. A Y point is the endpoint of a third S' curve.

We bring some more information about the geometry of S around Z'+: we can also see a Z′ point as the intersection of an S' curve and a curve of maximum of curvature. With that point of view, we have more information for the surface for any point of Z′+. In the continuation of Z, beyond Z′, the surface is still a maximum of curvature, and has this ridge geometry, but unlike on Z, the radius of curvature is greater then the medial radius. We denote by W such curves.

Consider p ∈ Z'+. Depending on its position, p has either a symmetrical point close to Z and a supplementary symmetrical point close to Y, or the opposite. This depends on where p is placed with respect to the curve S'. Topologically, S', Z and W meet into Z' to form a cross shape in Z'+ (see Figure 17.4). We distinguish two parts in Z+. the part of Z'+ delimited by S' and that contain W, that we denote by Z′, and the part delimited by S' and that contain Z, that we denote by Z′z+.

Figure 17.4: The curves S′, Z and W in Z'+. On this figure, Z′z is the pink part of Z′+, and Z' is the blue part.

S'

Zw

Z'z

Z'

Z

M

S'

If a point p belongs to Z'+, its initial symmetrical point po is close to Y+ and its first supplementary symmetrical point p1 is in Z′ but on the other side of W. In that case, the value 1 − κ1(p)ri(p) is strictly positive, and whether a point q is close to  ̄0 or p1, we can apply the usual method.

If p belongs to Z′z+ , the initial symmetrical point p of p is also in Zt+, but on the other side of Z, and the first supplementary symmetrical point p1 is close to Y+. In that case, we can no longer ensure that p verifies 1 − κ1(p)r1 (p) &gt; 0. Indeed, if p belongs to Z, its first supplementary medial radius grows linearly with the its distance to Z'+, thus the quantity 1 − κ1(p)ri(p) goes below 0. Nevertheless, as we saw in Section 16.3.3, the supplementary medial sphere of p is far from being osculating at p1. Thus their exists a constant αY such that 1 − κ1(p)r1(p) &gt; αγ by smoothness from Y. This suggests a condition for δγ. We define αγ as the minimum of 1 − κ1(p)r1(p) for p ∈ Y:

$$\alpha _ { Y } \colon = \min _ { p \in Y } \{ 1 - \kappa _ { 1 } ( p ) r ^ { * } ( p ) \} .$$


<!-- p:201 -->


$$\text {For any } p \in Y ^ { + } , \, 1 - \kappa _ { 1 } ( \overline { p } _ { 1 } ) r _ { 1 } ^ { * } ( p ) \geq \frac { 1 } { 2 } \alpha _ { Y } .$$

Thus, if q is close to p, we can apply Lemma 17.2 to bound the expected of such neighbors. And if q is close to p1, i.e. close to Y', we use the partition of PBis(p, q) similar to the one used in Section 16.3.3. We deduce that:

Lemma 17.6. Let p ∈ Z'+ at distance hp from Z ∪ W, the expected number E [deg|Rem (p, Del)] of neighbors of p in Del(X ∪ {p}) that are in Rem(p) is:

$$\mathbb { E } \left [ \deg _ { | R e m } \left ( p , D e l \right ) \right ] = O \left ( \ln \frac { 1 } { h _ { p } } \right ) .$$


<!-- p:202 -->


## Chapter 18

### Remaining neighbors

In this chapter, we count the remaining Delaunay neighbors of p: those that are not in Loc(p) neither in Rem(p), also called far neighbors. For the points p ∈ S \ Z+, we will use a simple packing argument to show that they are all in a negligible quantity. This is possible since for such points, Loc(p) and Rem(p) are large enough.

For points p ∈ Z+, we cannot do this because the size of the neighborhood Loc(p) tends to 0. Thus we will decompose the far neighbors of p into, as in Chapter 13, Section 13.5, middle-range and very far neighbors, to apply an additional analysis. For very far neighbors, we will reuse the same packing argument. For middle-range neighbors, we will use an empty region graph similar to the empty axisaligned right triangle graph. Such a graph will be used to prove that the number of middle-range edges (linking a point to a middle-range neighbor) is o(λ).

#### 18.1 On the probability that p has a Delaunay neighbor outside Loc(p) ∪ Rem(p)

We consider a point p ∈ Z+, and denote by p the symmetrical point of p that is in Z+2δ, and by θp the angle between Ts(p) and PBis(p, p). We show that, if a point q is at distance τ from σ*(p), then any sphere passing through p and q contains a region either around p or p whose area depends on both τ and the distance hp from p to Z. This region is not precise enough to obtain directly a bound on the degree, but it will be used to show that there are not so much middle-range neighbors.

We prove the following lemma:

Lemma 18.1. Let p ∈ Z+, let 0 ≤ τ ≤ rch and let q ∈ S at distance greater than τ from σ*. If a sphere σ passes through p and q then B(σ) ∩S contains either a region whose projection on Tε(p) is a disk with radius 41+2κsupr* 1 cos (θp) and with p on its boundary, or a region whose projection on Tε(p) is a disk with radius 41+2κsupr* 1 T cos (θp) and with p on its boundary.

It corresponds to Lemma 13.6 from Chapter 13 adapted to the generic case, and points p only close to Z.

Proof. The proof is similar to the proof Lemma 13.6, but we consider cones instead of cylinders. Indeed for the spheroid case, both the principal curvatures were positive, but in the general case, if κ1(p) remains positive around Z, it is not anymore the case for κ2(p) in general. On the other hand, while Lemma 13.6 considered various cases, in this lemma, we assume that zc is positive and p is close to p.

We consider a point q at distance τ from σ*. We denote by c* the center of σ*. We consider a sphere σ passing through p and q, and such that its center c = (xc, yc, zc) verifies zc &gt; 0 in the Monge coordinate system of p. We denote by B+τ(σ*) the ball centered on c* and with radius r* + τ. Then we shrink σ toward p, until it is tangent to the boundary of B+τ(σ*). We call σ' this new sphere and c' = (xc′ , yc′, zc') its center. This sphere still passes through p, and is included in σ but does not pass through q anymore.


<!-- p:203 -->


As explained in Lemma 13.6, the center of σ' lies on the prolate spheroid Prτ with focuses p and c*, and great axis r* + τ.

The projection of the intersection B(σ') ∩ S on Ts(p) is given by:

$$E _ { c ^ { \prime } } ( x , y ) \leq 0 ,$$

where

$$E _ { c ^ { \prime } } ( x , y ) & = x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + ( f _ { p } ( x , y ) ) ^ { 2 } - 2 f _ { p } ( x , y ) z _ { c ^ { \prime } } \\ & \leq x ^ { 2 } - 2 x x _ { c ^ { \prime } } + y ^ { 2 } - 2 y y _ { c ^ { \prime } } + x ^ { 2 } + y ^ { 2 } + 2 \kappa _ { \sup } \left ( x ^ { 2 } + y ^ { 2 } \right ) z _ { c ^ { \prime } } \\ & \leq 2 ( 1 + \kappa _ { \sup } z _ { c ^ { \prime } } ) x ^ { 2 } - 2 x x _ { c ^ { \prime } } + 2 ( 1 + \kappa _ { \sup } z _ { c ^ { \prime } } ) y ^ { 2 } - 2 y y _ { c ^ { \prime } } \\ & \leq 2 ( 1 + 2 \kappa _ { \sup } r ^ { * } ) x ^ { 2 } - 2 x x _ { c ^ { \prime } } + 2 ( 1 + 2 \kappa _ { \sup } r ^ { * } ) y ^ { 2 } - 2 y y _ { c ^ { \prime } } , \text { since } \tau \leq r h \leq r ^ { * } , \text { and } z _ { c ^ { \prime } } \leq r ^ { * } + \tau . \\$$

But

$$0 = ( 1 + 2 \kappa _ { \sup } r ^ { * } ) x ^ { 2 } - x x _ { c } + ( 1 + 2 \kappa _ { \sup } r ^ { * } ) y ^ { 2 } - y y _ { c ^ { \prime } } ,$$

is the equation of a circle passing through p and centered on (2 1+2κsupr* , 2 1+2κsupr* 1 xc′ 1 yc′ ), i.e. of radius 1 √x21 +y2, 2 1+2κsupr*

Then we adapt the second case of Lemma 13.6 to this radius. We consider two cylinders Cylt and Cylt of radius t, respectively around (pc*) and (pc*). We show that we can choose t small enough such that their intersection lies inside the prolate ellipsoid Prτ. We recall that θp denotes the angle between the tangent plane of p and the bisector plane of p and p. By construction, the furthest point of the intersection of the two cylinders from c* is at distance cos(θp) Since we want t small enough so that Cylt ∩ Cylt lies inside Prτ, we need to have cos(θp) t &lt; τ, so we choose t = cos (θp). Then since σ′ is centered on Prs, its center is either outside Cylt, or outside Cylt. Thus we have:

- either c' is outside Cylt, then the projection of B(σ) ∩ ε on Tε(p) contains a disk passing through p with radius 2 1+2κsupr* 1 t 41+2ksupr* T cos (θp),
- or c' is inside Cylt, or more precisely in Cylt ∩ Prτ that is above the medial plane so σ′ can be shrank from c' until it passes through p, while its center is still outside Cylt. Then the projection of B(σ) ∩ ε on Tε(p) contains a disk passing through p with radius T cos (θp). 41+2κsupr*

□

Then we consider a point q ∈ S outside Loc(p) ∪ Rem(p). We recall, from Section 16.3.1, that on Z, the quantity m3,0 is 0, and the quantity α(p) := 3κ1(p)3 − m4,0(p) − 3m2,1(p)2 reaches a strictly positive κ1(p)−κ2(p) minimum α0. By condition (Cz), for any p ∈ Z+δ, we have α(p) &gt; 2α0. But as we saw in Section 16.3.1, α(p)h4 corresponds to a lower bound on the vertical distance between the surface around pz ∈ Z and 24 the medial sphere of pz. So αo|pq|4 corresponds to a lower bound on the distance form q to the medial 48 sphere of p for p close to Z and q not farther than O(α0), from p. In order words we can say that for any p ∈ Z+δ, and for any q ∈ S \ Loc(p) ∪ Rem(p), we have

$$d i s t ( q , \sigma ^ { * } ( p ) ) > \frac { 1 } { 4 8 } \alpha _ { 0 } | p q | ^ { 4 } .$$

Since Loc(p) and Rem(p) contain disk of radius Ω (h3) around p or p, we can say that if q is not in Loc(p) and Rem(p), then it is at distance Ω (h12) from the medial sphere. We reintroduce the empty region graph from Part II, Chapter 9, that we used to quantify the probability that there exist some neighbors at a given distance: For a given t &gt; 0, we consider the isosceles triangle in Tε(p) with vertices p, (√2t, 0) and (t, t), its seven copies around p such that they cover an octagon, and their symmetrical triangles on Tε(p) with respect to PMed. That makes a total of 16 triangles around p or p. We denote by Ft(p) the family of fundamental regions made of their reciprocal projections on ε by π−1 for the triangles on Tε(p), and by π−1 for the triangles on Tε(p). Note that the area of each region is greater than t2. 2 We can deduce the following lemma:


<!-- p:204 -->


S   ft t s    xt   Z if      +Z f d  q d    n Consequently, F0

the probability that p has some Delaunay neighbors outside Loc(p) and Rem(p) is 16e−λΩ(h26).

Proof. We apply Lemma 18.1 with τ = Ω(h12) that corresponds to the distance from a point q outside Loc(p) and Rem(p), to σ*(p). We obtain that if a sphere passes through p and q, the projection of its intersection with S contains a disk of radius Ω (h12cos θp) passing through p or p. But around Z, θp is close to 2, , so cos θp ≈ cot θp that is √x+y zp in the Monge coordinate of p. And as we saw in Section 16.3.1, yp is negligible compared to xp, and then cos θp ≈ zp that is Θ(hp). In other words, any |xp| sphere passing through p and q contains a disk of radius Ω(h13). We denote by γ the constant such that, any sphere passing through p and q contains a disk of radius γh13. Consequently, any sphere contains one the 16 triangles of F0 □

Note that the bound obtained is far from being tight, but it will be sufficient for our needs.

#### 18.2 Middle-range neighbors of a point in Z+

Our goal in this section, is to show that, for any point p ∈ Z+, we can find a neighborhood, that we call MRN(p), of radius Ω(1) around p such that for any q ∈ MRN(p), any sphere passing through p and q has an intersection with S that contains an axis-aligned right rectangle depending on p and q. That will induces that any point in p ∈ Z+ has an expected degree O(ln λ). Used conjointly with the previous section, we will show that we can obtain a sub-linear number of edges with an endpoint in Z+.

Rather than delving into a very analytic approach, we show how we can go from the expression of the intersection sphere/surface to an approximation that is convenient for us, while making approximations that all involve a constant factor. For instance, the coefficient 1 - κ1r* will not be involved anymore.

We consider two points p and q in Z+. We denote by pz the closest point on Z to p, we place the surface in the Monge coordinate system of pz. We use (u, v, w) to denote these coordinates (to differentiate from the Monge coordinates in p). By construction we have vp = 0.

We use a partition of PBis(p, q) very similar than the one used in the last section of the oblate spheroid case, Part III, Chapter 13, Section 13.5, up to some adaptations, mostly because κ2(pz) is not necessarily positive.

##### 18.2.1 Choice of the specific spheres when q is on the side of p

We present the specific chosen spheres whose center will partition the bisector plane PBis(p, q) when q is on the side of p with respect to PBis(p, p). Those sphere are chosen to obtain a super-graph of the Delaunay triangulation in which a point has a logarithmic expected degree.

####### Spheres σLow, σ1, and σ2

The triangle ∆1 is the one whose side parallel to Ts(p) ∩ PBis(p, p) is the closest to p. Simply put, its the triangle close to Z. ∆2 is the other triangle (see Figure 18.1).

We still use the same sphere σLow, that is centered in the tangent plane of p and is close to the Gabriel sphere of (p, q). As we already saw, its intersection with S approximates a disk with [pq] for diameter. The sphere contains two axis-aligned right triangles ∆1 and ∆2 on S. By "axis-aligned right triangles on S", we mean that their projection on Ts(p) are right triangles whose sides are aligned with the perpendicular Ino s   e   od nd s ne (  sd o s  ooas (  oal to Ts(p).

re   ssd rnd  n one tan e e  ss a  s q, and that is orthogonal to Ts(p). We rename them σ1 and σ2 where σ1 is the sphere containing ∆1 and σ2 the sphere containing ∆2.


<!-- p:205 -->


We obtain:

q

Figure 18.1: The intersection of σLow is almost a Gabriel circle.

Z


q

∆1

∆2


∆1

v


pz

u

p

pz

u

p

Sphere σOsc

While the sphere σMed was defined to identify an ellipse inside the intersection, the new sphere σosc is defined to contain a rectangle. As a consequence, we don't limit the intersection with S to an order 2 region.

Instead of describing precisely the center of this sphere, we describe how we choose it, through some rewriting of the expression of its intersection with S. For now, we just assume that the center of σosc is on the bisector plane PBis(p, q) of p and q, and on the bisector plane PBis(p, p) of p and p.

In the Monge system coordinates (u, v, w) of pz, p has coordinates (up, 0, wp) and q has coordinates (uq, vq, wq). Note that PBis(p, p) is close to the plane defined by u = 0.

Any sphere centered on c and passing through p has equation:

$$\sigma _ { O s c } \colon ( u - u _ { c } ) ^ { 2 } + ( v - v _ { c } ) ^ { 2 } + ( w - w _ { c } ) ^ { 2 } = ( u _ { p } - u _ { c } ) ^ { 2 } + ( v _ { p } - v _ { c } ) ^ { 2 } + ( w _ { p } - w _ { c } ) ^ { 2 }$$

that we can rewrite:

$$\sigma _ { O s c } & \colon ( u - u _ { c } ) ^ { 2 } - ( u _ { p } - u _ { c } ) ^ { 2 } + ( v - v _ { c } ) ^ { 2 } - ( v _ { p } - v _ { c } ) ^ { 2 } + ( w - w _ { c } ) ^ { 2 } - ( w _ { p } - w _ { c } ) ^ { 2 } = 0 \text { or } \\ \sigma _ { O s c } & \colon ( u - u _ { p } ) ( u + u _ { p } - 2 u _ { c } ) + ( v - v _ { p } ) ( v + v _ { p } - 2 v _ { c } ) + ( w - w _ { p } ) ( w + w _ { p } - 2 w _ { c } ) = 0 .$$

Then we substitute vp = 0 and approximate uc by 0:

$$\sigma _ { O s c } \colon ( u - u _ { p } ) ( u + u _ { p } ) + v ( v - 2 v _ { c } ) + ( w - w _ { p } ) ( w + w _ { p } - 2 w _ { c } ) \simeq 0 \text { or,} \\ \sigma _ { O s c } \colon u ^ { 2 } - u _ { p } ^ { 2 } + v ( v - 2 v _ { c } ) + ( w - w _ { p } ) ( w + w _ { p } - 2 w _ { c } ) \simeq 0 .$$

We have then to identify a convenient value for vc. Since q belongs to σosc, we have:

$$u _ { q } ^ { 2 } - u _ { p } ^ { 2 } + v _ { q } ( v _ { q } - 2 v _ { c } ) + ( w _ { q } - w _ { p } ) ( w _ { q } + w _ { p } - 2 w _ { c } ) \simeq 0 .$$

We can substitute in this expression the second order approximations of wp and wq:

$$w _ { p } & \simeq \frac { 1 } { 2 } \kappa _ { 1 } u _ { p } ^ { 2 } \, \sinc e \ v _ { p } = 0 , \, \text {and} \\ w _ { q } & \simeq \frac { 1 } { 2 } \kappa _ { 1 } u _ { q } ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } v _ { q } ^ { 2 } .$$

$$u _ { q } ^ { 2 } - u _ { p } ^ { 2 } + v _ { q } ( v _ { q } - 2 v _ { c } ) + \frac { 1 } { 2 } ( \kappa _ { 1 } u _ { q } ^ { 2 } + \kappa _ { 2 } v _ { q } ^ { 2 } - \kappa _ { 1 } u _ { p } ^ { 2 } ) ( w _ { q } + w _ { p } - 2 w _ { c } ) \simeq 0 .$$


<!-- p:206 -->


In that expression, we want to choose ve so that κ1u2 + κ2v2 ,2 is a factor of the expression. q Thus we choose vc ≈ (1 − K2 vq to obtain: κ1

$$( \begin{matrix} u _ { q } ^ { 2 } - u _ { p } ^ { 2 } + v _ { q } ( v _ { q } - 2 v _ { c } ) \simeq u _ { q } ^ { 2 } - u _ { p } ^ { 2 } + v _ { q } \left ( v _ { q } - \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v _ { q } \right ) \\ \\ = u _ { q } ^ { 2 } - u _ { p } ^ { 2 } + \frac { \kappa _ { 2 } } { \kappa _ { 1 } } v _ { q } ^ { 2 } \\ \\ = \frac { 1 } { \kappa _ { 1 } } \left ( \kappa _ { 1 } u _ { q } ^ { 2 } + \kappa _ { 2 } v _ { q } ^ { 2 } - \kappa _ { 1 } u _ { p } ^ { 2 } \right ) .$$

And finally wc verifies:

$$\frac { 1 } { \kappa _ { 1 } } \left ( \kappa _ { 1 } u _ { q } ^ { 2 } + \kappa _ { 2 } v _ { q } ^ { 2 } - \kappa _ { 1 } u _ { p } ^ { 2 } \right ) + \frac { 1 } { 2 } ( \kappa _ { 1 } u _ { q } ^ { 2 } + \kappa _ { 2 } v _ { q } ^ { 2 } - \kappa _ { 1 } u _ { p } ^ { 2 } ) ( w _ { q } + w _ { p } - 2 w _ { c } ) \simeq 0 ,$$

in which we can factorize and simplify by κ1u2 + κ2v 2 − κ1u2 to obtain: q p

1 - 1(wq + wp − 2wc) ∼ 0, and then: 十 κ1

$$w _ { c } \simeq \frac { 1 } { \kappa _ { 1 } } + \frac { 1 } { 2 } ( w _ { q } + w _ { p } ) .$$

We go back to the expression of the sphere σOsc, and substitute the coordinates of c:

$$\sigma _ { O s c } \colon u ^ { 2 } - u _ { p } ^ { 2 } + v \left ( v - \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v _ { q } \right ) + ( w - w _ { p } ) \left ( w + w _ { p } - \frac { 2 } { \kappa _ { 1 } } - ( w _ { q } + w _ { p } ) \right ) \simeq 0 ,$$

simplified into:

$$\sigma _ { O s c } \colon u ^ { 2 } - u _ { p } ^ { 2 } + v \left ( v - \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v _ { q } \right ) + ( w - w _ { p } ) ( w - w _ { q } ) - \frac { 2 } { \kappa _ { 1 } } ( w - w _ { p } ) \simeq 0 .$$

We obtain an approximation of the projection of the intersection rOsc := B (σosc) ∩S, by substituting w by 2 (w − wp) or simply by 1k1u2 in (w − wp)(w − wq) where it has a κ1 higher multiplicity. This intersection is then expressed by Eosc(u, v) &lt; 0 with:

$$E _ { O s c } ( u , v ) \simeq u ^ { 2 } - u _ { p } ^ { 2 } + v \left ( v - \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v _ { q } \right ) + \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - w _ { p } \right ) \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - w _ { q } \right ) - \frac { 2 } { \kappa _ { 1 } } \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } + \frac { 1 } { 2 } \kappa _ { 2 } v ^ { 2 } - w _ { p } \right ) .$$

But 2 112 1κ1u2 + 2κ2v2 − wp) ∼ u2 + 52v2 一 SO: κ1 κ1

$$E _ { O s c } ( u , v ) & \simeq \frac { \kappa _ { 2 } } { \kappa _ { 1 } } v ^ { 2 } + v \left ( v - \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v _ { q } \right ) + \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - w _ { p } \right ) \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - w _ { q } \right ) \\ & = \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v \left ( v - v _ { q } \right ) + \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - w _ { p } \right ) \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - w _ { q } \right ) .$$

Finally we substitute in this expression, the approximations wp ≈ and wq ≈ 1κ1u2 2 (here again, we can the term in vq since it appears in a multiplication of terms). We obtain:

$$E _ { O s c } ( u , v ) & \simeq \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v \left ( v - v _ { q } \right ) + \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - \frac { 1 } { 2 } \kappa _ { 1 } u _ { p } ^ { 2 } \right ) \left ( \frac { 1 } { 2 } \kappa _ { 1 } u ^ { 2 } - \frac { 1 } { 2 } \kappa _ { 1 } u _ { q } ^ { 2 } \right ) \\ & = \left ( 1 - \frac { \kappa _ { 2 } } { \kappa _ { 1 } } \right ) v \left ( v - v _ { q } \right ) + \frac { \kappa _ { 1 } ^ { 2 } } { 4 } \left ( u ^ { 2 } - u _ { p } ^ { 2 } \right ) \left ( u ^ { 2 } - u _ { q } ^ { 2 } \right ) .$$

This approximation of curve is valid for a point q on the same side of p with respect to PBis(p, p), since the position of p needs all the terms of the surface to be determined. In some sense, since up ~ —up, we can see u2 − u2 as a good approximation of (u − up)(u − u−). In practice, the choice that cOsc belongs to PBis (p, p) makes σOsc passing exactly through p.


<!-- p:207 -->


Figure 18.2: When q is on the side of p with respect to PBis(p, p), the intersection of σosc with S has globally one of those two shapes. Both of them contain 4 axis-aligned right triangles.

Z

q

∆2

∆1

v

pz

u

p

Z|

q

∆2


∆1

v

pz

u

p

2 The curve defined by 0 = (1 − K2 v (v − vq) + (u2 − u2) (u2 − u2) can have various shapes but κ1 4 essentially two different topologies (see Figure 18.2). In both cases, it contains the two axis-aligned right triangles ∆1 and ∆2. This is clear, given the expression of the curve in which 1 − K2 and 2 are strictly κ1 4 positive by genericity on Z.

By symmetry, this intersection contains similar triangles on the side p. We denote them by ∆1 and 2.

The missing terms in the approximation make the real curve to be slightly curved. Actually the m2,1 u2 which approximates the curvature line. But this curvature does not impact the global area of the rectangles. Note that the curve obtained is an approximation of qe si toa   pd   e   o d s  ts  ( o od oy) a constant factor.

Then we consider the remaining spheres.

####### Sphere σSy Sym

The sphere σ 0 is the sphere centered on Ts(p) and passing through p, q, and p. As a sphere centered Sym in Ts(p), its intersection with S approximate a disk, the one passing though p, q, and p.

into account the spheres centered above the tangent plane of p. This sphere contains ∆1 and ∆1.

####### Sphere σNorm

This sphere is chosen depending on the relative position of p and q. In the spheroid case, the choice to orient the edges toward the closest point to Z, allowed to avoid this choice.

We describe how to obtain it: Consider the sphere σosc and makes its center moves upward (in the z coordinate, so farther from Ts(p)), but maintaining contact with p, q and p. At some point, the sphere has an intersection with S whose tangent at p or q is parallel with PBis(p, p). This is the sphere σNorm.

This sphere is a particular case of a sphere σosc (p, q′) for a q′ such that vq′ = 0. Thus it contains the triangles ∆2 and ∆2. But by symmetry with v = 0, it contains two other triangles, that we denote ∆3


<!-- p:208 -->


Figure 18.3: Intersection of σ0 Sym with S.

Z

q

∆1

v

pz

u

p

and ∆3 (see Figure 18.4). Note that ∆3 and ∆3 depends on the relative position of p and q.

Figure 18.4: The intersection of σNorm with S is almost symmetrical with respect to u = 0 and v = 0.

Z

q

v

∆2

pz

u

p

∆3

Z

∆3

△2

b

∆2

pz

u

p

####### Degenerate sphere σSv Sym

This degenerate sphere corresponds to the plane Psym(p, q) passing through p, q and p. What is important here, is Psym(p, q) cuts S in a shape of order 2 symmetrical with respect to u = 0. It is an ellipse if κ2 &gt; 0, a parabola if κ2 &gt; 0, or an hyperbola if κ2 &lt; 0. In both cases, since the half-plane is clear the sphere contains ∆3 and ∆3(see Figure 18.5).

Finally it remains to find a degenerate sphere that contains both ∆2 and ∆3, and another one that contains both ∆1, ∆2 and ∆3. But this is achieved by both σ2 and σ1 (see Figure 18.6).

On all figures above, we illustrated the intersection by triangles whose diameter have size |pq|. In order to fit with approximations, the actual triangles we consider are reductions of the triangles of the figures by a factor that depends on the surface. In any case, we assume that the reduction is at least 2. Such approximations can be made in a neighborhood of size Ω(1) around p, since all coefficients (κ1, 1 − κ2, α) involved in the expressions of the curves are strictly greater than a positive constant in Z+.


<!-- p:209 -->


Figure 18.5: The intersection of σSvn with S in the parabolic case. Sym

Z

v

pz

u

p

●

∆3

Figure 18.6: The sphere σ2 contains ∆2 and ∆3. The sphere σ1 contains the 3 triangles close to p.

Z

q

∆1

∆2

v

pz

u

p

∆3

$$\mathcal { F } _ { Z } ( p , q ) \colon = \{ \Delta _ { 1 } ( p , q ) , \overline { \Delta } _ { 1 } ( p , q ) , \Delta _ { 2 } ( p , q ) , \overline { \Delta } _ { 2 } ( p , q ) , \Delta _ { 3 } ( p , q ) , \overline { \Delta } _ { 3 } ( p , q ) \} .$$

κ1 Finally, for a point q on the side of p, we denote by Fz(p, q), the family on S of 6 projected reduced triangles:

All of them have area Θ(|up − uq||vp − vq|).

Let σ be a sphere passing by p and q, and centered on c. By Combination lemma, we have (see Figure 18.7):

- If c ∈ (csym, COsc, CLow), then σ contains ∆1,
- if c ∈ (c2, CLow, cOsc, CNorm, c2), then then σ contains ∆2,
- if c ∈ (c2, CNorm, cCSym), then σ contains ∆3,
- if c ∈ (c1, cSym, cOsc, c1), then then σ contains ∆1,
- if c ∈ (c1, cOsc, cNorm, c1), then σ contains ∆2, and
- if c ∈ (c1, CNorm, cSym), then σ contains ∆3.

##### 18.2.2 If q is on the side of p with respect to PBis(p, p)

For points q that is on the p with respect to PBis(p, p), We define ∆i(p, q) as ∆i(p, q), and ∆i(p, q) as ∆i(p, q). Note that ∆i(p, q) and ∆i(p, q) are well defined since q that is on the p (see Figure 18.9).

Then we consider a sphere σ passing through p and q, and consider that:


<!-- p:210 -->


Figure 18.7: The partition of PBis(p, q) for p ∈ Z+ and q ∈ MRN(p). A sphere centered in a given polygon of the partition contains the corresponding triangle.

Δ

3

∆2, ∆3, ∆2, ∆3

C1

4

2

cNorm

cOsc

∆2, ∆3

∆1, ∆2, ∆1, ∆2

∆1

∆2

[△1, ∆1]

∆1, ∆2

c1

cSym

cLow

z = 0

c2

Figure 18.8: And the corresponding regions. A regions is linked to its corresponding parameter by their color.

△1

∆1

∆2


∆3


- If σ does not contains p, then σ contains one of the 3 triangles ∆1(p, q), ∆2(p, q), or ∆3(p, q).
- If σ contains p and the center c of σ has a positive z coordinate in the Monge coordinate system of p, then σ contains one of the 3 triangles ∆1 (p, q), ∆2(p, q), or ∆3(p, q).
- Otherwise σ contains p and the center c of σ has a negative z coordinate in the Monge coordinate system of p. But in that case, the sphere σ contains either ∆1(p, q) or ∆2(p, q).

Thus we can extend the definition of Fz(p, q) for points q on the side of p. That provides the neighborhood MRN(p) around p and p.

Finally, by Partition lemma, this proves that:

Lemma 18.3. Let p ∈ Z+ and q ∈ MRN(p).

If (p, q) is an edge of Del(X ∩ {p}) then it is an edge of GFz(X ∩ {p}).

##### 18.2.3 Computation of the expected degree

We compute the expected middle-range degree of a point p ∈ Z+.

We will reuse the computation made in Part III, Chapter 13, Section 13.5, and combine the results of the previous sections. We recall that, for this computation, we use the fact that we found two supergraphs of the Delaunay triangulation. One is given by F0 γh13 (p), since q ∉ Loc(p) ∪ Rem(p). The other is given by Fz(p, q)


<!-- p:211 -->


Figure 18.9: When q is on the side of p we can consider the symmetrical triangles.

Z

q

∆1

∆2

v

∆3

pz

u

p

To apply our computation, we need that both family of regions are disjoint. All regions of Fγ (q) around p. Concerning the triangles of Fz(p, q), since they are reduces triangles, they are at distance greater than |pq| from p, that is itself Ω(h3). So we can find a maximal distance before which both families of regions are distinct. This gives a last condition on δz:

$$\text {For any } p \text { and } q \text { in } Z ^ { + } , \mathcal { F } _ { 0 } ^ { h _ { p } ^ { 1 3 } } ( q ) \text { and } \mathcal { F } _ { Z } ( p , q ) \text { are disjoint.} \\$$

Thus we can prove the following lemma:

Lemma 18.4. Let p be a point of Z+, and X a Poisson point process distributed on S with intensity λ. The expected number of middle-range neighbors of p in Del(X ∪ {p}) is:

$$\mathbb { E } \left [ \deg _ { | M R N } ( p , D e l ) \right ] = O ( \ln \lambda ) e ^ { - h _ { P } ^ { 2 6 } \Omega ( \lambda ) } .$$

Proof. Without entering into the details, we have:

$$\mathbb { E } \left [ \deg _ { | M R N } \left ( p , D e l \right ) \right ] \leq \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ ( p , q ) \in \overrightarrow { \mathcal { G } } _ { \mathcal { F } _ { Z } } ^ { 0 } ( X ) \cap \overrightarrow { \mathcal { G } } _ { \mathcal { F } _ { 0 } ^ { \gamma , \frac { 1 3 } { p } } } ( X ) \right ] d q ,$$

since both are super-graph of Del in MRN(p),

$$\mathbb { E } \left [ \deg _ { | M R N } \left ( p , \text {Del} \right ) \right ] & \leq \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { z } } ^ { 0 } ( X ) \left ( | p , q \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { z } ^ { k + 1 } } ^ { 0 } ( X ) \right ) \mathbb { P } \left [ ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { z } ^ { 1 + 1 } } ^ { 0 } ( X ) \right ] d q \\ & \leq \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left [ ( p , q ) \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { z } } ^ { 0 } ( X ) \left ( | p , q \in \widehat { \mathcal { G } } _ { \mathcal { F } _ { z } ^ { k + 1 } } ^ { 0 } ( X ) \right ) e ^ { - h ^ { 2 } \Omega _ { p } ( \lambda ) } d q \text { by Lemma 18.2.}$$

Since the regions of Fz(p, q) and F) γh13 (p) are disjoint, the event "(p, q) ∈ GFz|(p, q) ∈ G0 is less p

Then we obtain:

Fz

$$\mathbb { E } \left [ \deg _ { | M R N } \left ( p , \text {Del} \right ) \right ] & \leq e ^ { - h _ { p } ^ { 2 6 } \Omega ( \lambda ) } \lambda \int _ { q \in M R N ( p ) } \mathbb { P } \left ( ( p , q ) \in \mathcal { G } _ { \mathcal { F } _ { Z } } ^ { 0 } ( X ) \right ] \text {d} q \\ & = O ( \ln \lambda ) e ^ { - h _ { p } ^ { 2 6 } \Omega ( \lambda ) } ,$$

since all regions of Fz are axis-aligned right triangles.


<!-- p:212 -->


##### 18.2.4 Unlikely neighbors

In order to take into account all possible pairs of points (p, q), it remains to consider to count the far neighbors of the points p outside Z+, and of very far neighbors of the points p in Z+. But as we saw, in both cases, those neighbors are points q such that dist(σ(p), q) is greater than a positive constant (depending on the surface). Thus, a packing argument similar to the one used in Part III, Chapter 13, Section 13.5.5 implies directly the following lemma:

Lemma 18.5. Let p ∈ S\ Z+, the expected number of far neighbors of p in Del(X ∪ {p}) is:

$$\mathbb { E } \left [ \deg _ { | F N } ( p , D e l ) \right ] = o ( 1 ) .$$

Let p ∈ Z+, the expected number of very far neighbors of p in Del(X ∪ {p}) is:

$$\mathbb { E } \left [ \deg _ { | V F N } ( p , D e l ) \right ] = o ( 1 ) .$$

##### 18.2.5 Expected size of the Delaunay triangulation

We finish this part by wrapping up all results above to prove the theorem:

Theorem 18.6. The expected combinatorial complexity of the 3D-Delaunay triangulation of a Poisson process distributed with intensity λ on a smooth generic closed oriented surface is Θ(λ).

Proof. An upper bound on the expected degree of a point in the Delaunay triangulation is given by the sum of its different restricted expected degrees by neighborhood.

As we saw, a point p ∈ S \ Z+ has expected degree O(1). On the other hand, a point p ∈ Z+ has expected degree O (ln + O(ln λ)e−h26Ω(λ). hp

Thus, an upper bound on the total number of edges E of the Delaunay triangulation is given by:

$$\mathbb { E } \left [ N \right ] & = \frac { 1 } { 2 } \, \mathbb { E } \left [ \sum _ { p \in X } \deg ( p ) \right ] \\ & = \frac { \lambda } { 2 } \int _ { p \in \mathcal { S } } \mathbb { E } \left [ \deg ( p ) \right ] d p \, \text { by Slivynyak-Mecke Theorem,} \\ & = \frac { \lambda } { 2 } \int _ { p \in \mathcal { S } \nearrow Z ^ { + } } \mathbb { E } \left [ \deg ( p ) \right ] d p + \frac { \lambda } { 2 } \int _ { p \in Z ^ { + } } \mathbb { E } \left [ \deg ( p ) \right ] d p \\ & = O ( \lambda ) + \frac { \lambda } { 2 } \int _ { p \in Z ^ { + } } O \left ( \ln \frac { 1 } { h _ { p } } \right ) d p + \frac { \lambda } { 2 } \int _ { p \in Z ^ { + } } O ( \ln \lambda ) e ^ { - h _ { p } ^ { 2 } \Omega ( \lambda ) } d p . \\ \text {With a variable substitution, we can switch from the integral on $p \in Z^{+}$ to an integral on $h_{p}\in [0,1] $} .$$

With a variable substitution, we can switch from the integral on p ∈ Z+ to an integral on hp ∈ [0, δz] multiplied by the length of Z (that is finite by genericity). Since δz is small enough, this variable substitution has a bounded Jacobian.

dh = 1 and since ∞+J e−λh26 dh = O(λ−  ), we have: J0

$$\mathbb { E } \left [ N \right ] & = O \left ( \lambda + \lambda ^ { \frac { 2 5 } { 2 6 } } \ln \lambda \right ) \\ & = O ( \lambda ) .$$

Since the number of edges is an asymptotic upper bound on the combinatorial complexity of the Delaunay triangulation, we deduce that the latter is also O(λ). □


<!-- p:213 -->


206 Chapter 18. Remaining neighbors


<!-- p:214 -->


## Conclusion

In this thesis, we have shown that the expected size of the Delaunay triangulation of a Poisson point process distributed on a generic surface is linear with the number of points. To this aim, we have developed a method to compute the expected size of some empty region graphs, including the 3DDelaunay triangulation. Through this method, we explained, maybe a little bit more, how behaves the Delaunay triangulation of points on a surface. In this conclusion, we briefly present other similar problems where we could use our method, then we point out the weaknesses and possible improvements of our approach.

As it is usually done, we can have a look on the same problem for different dimensions. For instance, in R3, we can find a curve on which points have a quadratic Delaunay triangulation, the moment curve. But this curve is chosen to make the triangulation quadratic, and a natural question arises: What is the size of the Delaunay triangulation of a Poisson point process on a generic curve? Is it asymptotically unique? Can we find a class of curves for which it is linear?

We can also extend the problem to higher dimensions, and question what is the size of the Delaunay triangulation of random points distributed on a variety of dimension 1, 2 or 3 in R4. One can possibly find a pathological hyper-surface for the 4D-Delaunay triangulation, like the cylinder is in R3.

Rather than applying the empty region graph method to extended dimensions, it could be interesting, first and foremost, to improve our approach of the problem. For instance, it seems very doable to reformulate and extend a little our main result. Indeed, the notion of genericity was convenient for us to find good properties on a surface, but it is a strong condition: for example, we cannot really say that an oblate spheroid is a generic surface, nevertheless if points are distributed on this surface, they have a linear Delaunay triangulation. We can only say that an oblate spheroid has some generic properties, good for the Delaunay triangulation. But it is not necessary to have such properties: consider that the surface is a sphere, and thus that there is no unicity of the Delaunay triangulation. It is not a generic surface neither but, if a random sample is distributed on a sphere, one can find almost surely a linear triangulation [Yvi88], that is therefore a Delaunay triangulation. Thus if the surface on which the points are distributed contains a part of a sphere, we can still find a linear Delaunay triangulation. Furthermore, if a surface contains cylindrical parts, the Delaunay triangulation can remain linear, as long as the medial spheres are not osculating. The problem is not so much on surfaces but rather on their medial axis.

A more precise distinction than generic or not, can be the following: we distinct the centers of the medial axis between good and bad centers. The good centers are those for which the medial sphere has an intersection with the surface that is made of isolated points. Conversely the bad centers have a medial sphere whose intersection with the surface is 1 or 2 dimensional. In the medial axis of the surface, the bad centers are either 0 or 1 dimensional. If they are one dimensional, like on canal surface, our conjecture is that the triangulation has an expected size that is Θ(λ ln λ). But if they are 0 dimensional, i.e. isolated points on the medial axis, their contribution to the total expected size should either be negligible, or linear in the case of a spherical part. This distinction suggests a more precise conjecture: the expected size of the Delaunay triangulation of points on a surface is O (λ(1 + lbad ln λ)) where lbad denotes the length of the medial axis part that is made of bad centers. This formulation has also the advantage to exclude from the conditions the notions of smoothness, closeness and orientability.

We finish that conclusion by pointing out why we think that our method has relevant properties. On some specific surfaces, like cylinders, we explained why the Delaunay triangulation has a O(λ ln λ) expected complexity. Our computation proposes an explanation on how the Delaunay triangulation switches from super-linear to linear after perturbation of a specific surface. We refer to the proof of Theorem 18.6. In the computation of the degree of points in Z+, it appears a complexity O (λ2% ln λ) that is sub-linear. We know that this quantity is not tight, but nonetheless, it witnesses something. The value in the exponent comes from the approximation of the surface. Around Z we extended the approximation to its fourth order, for our surface to be "far enough from its first osculating sphere". In the case where the surface is closer, in term of order of approximation, to its first osculating sphere at Z, we would need to extend our approximation of the surface to an even higher degree. This would give a complexity O (λk+ī ln λ), for an higher k. This quantity remains sub-linear for any k, but is O (λ ln λ) for k = ∞. This can explain how even a very subtle perturbation on the surface can radically change the size of the Delaunay triangulation. Moreover, the fact that we linked empty axis-aligned ellipse graph and Delaunay triangulation of points on a surface made it possible to find the integrable upper bound O( (ln 1 on the expected degree of a point p. A question that remains open is: what is the expected hp degree of a point on Z? We showed that it was O(ln λ), but we did not show that it was Ω(ln λ), so it is not excluded that it is O(1), or something in between.


<!-- p:215 -->


Concerning more specific details, it might be possible to get a better constant in the big O we obtained. Indeed, we considered "reduced shapes" to fit with approximations, but when the intensity of the Poisson point process grows, this reduction is to be less and less necessary. As an illustration, consider the convex hull of a 3 dimensional set of points. It is known that the expected degree of a point on the convex hull is 6. The convex hull can be seen as the empty region graph where the region are half-spaces. Consider now that the set of points is distributed on a surface. Our approach of the problem would led us to analyze the intersections plane/surface. As a first approximation, they correspond approximately to axis-aligned ellipses with a single aspect ratio given by the local curvatures. In other words, around a given point of the surface, the convex hull corresponds to an empty axis-aligned graph with a single aspect ratio. But we proved that the degree of a point in an empty axis-aligned graph with a single aspect ratio was also 6. In other words, this example illustrates that the approach has good chance to be practically tight and shows that the approximations we made, were much too brutal, and increased too much the upper bound on the expected degree. Probably, a more elegant and less calculative approach, could have given better results.


<!-- p:216 -->


### Appendix A

### A.1 Jacobian of the Blaschke-Petkantschin variables substitution

The Jacobian matrix J of the Blaschke-Petkantschin variables substitution is:

$$J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) = \begin{pmatrix} \cos \varphi + \cos \theta _ { q } & - \rho \sin \varphi & - \rho \sin \theta _ { q } & 0 \\ \sin \varphi + \sin \theta _ { q } & \rho \cos \varphi & \rho \cos \theta _ { q } & 0 \\ \cos \varphi + \cos \theta _ { r } & - \rho \sin \varphi & 0 & - \rho \sin \theta _ { r } \\ \sin \varphi + \sin \theta _ { r } & \rho \cos \varphi & 0 & \rho \cos \theta _ { r } \end{pmatrix} ,$$

We describe here the computation of its determinant:

```
We describe here the computation of its determinant:

                                            |cos \varphi + cos \theta q      - \rho \sin \varphi      - \rho \sin \theta _ { q }          0
    det ( J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) ) = \begin{array} { c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c c
```

We develop from the coefficient that is the only not zero in a column,

```
We develop from the coefficient that is the only not zero in a column,

                    det ( J ( \rho , \varphi , \theta _ { q } ) ) =      ( \cos \varphi + \cos \theta _ { q } ) ( - \rho \cos \theta _ { q } ) + \rho ^ { 2 } \cos \varphi \sin \theta _ { r } )
                                                            - ( \sin \varphi + \sin \theta _ { q } ) ( - \rho ^ { 2 } \sin \varphi \cos \theta _ { r } + \rho ^ { 2 } \cos \varphi \sin \theta _ { r } )
                                                            + ( \cos \varphi + \cos \theta _ { r } ) ( - \rho ^ { 2 } \sin \varphi \cos \theta _ { q } + \rho ^ { 2 } \cos \varphi \sin \theta _ { q } )
                                                            - ( \sin \varphi + \sin \theta _ { r } ) ( - \rho \sin \theta _ { r } ) ( - \rho ^ { 2 } \sin \varphi \cos \theta _ { q } + \rho ^ { 2 } \cos \varphi \sin \theta _ { q } )
                                                            = \rho ^ { 3 } ( ( - \cos \varphi \cos \theta _ { q } ) - \cos ^ { 2 } \theta _ { q } ) ( - \sin \varphi \cos \theta _ { r } + \cos \varphi \sin \theta _ { r } )
                                                            - ( \sin \varphi \sin \theta _ { q } + \sin ^ { 2 } \theta _ { q } ) ( - \sin \varphi \cos \theta _ { r } + \cos \varphi \sin \theta _ { r } )
                                                            + ( \cos \varphi \cos \theta _ { r } + \cos ^ { 2 } \theta _ { r } ) ( - \sin \varphi \cos \theta _ { q } + \cos \varphi \sin \theta _ { q } )
                                                            - ( - \sin \varphi \sin \theta _ { r } - \sin ^ { 2 } \theta _ { r } ) ( - \sin \varphi \cos \theta _ { q } + \cos \varphi \sin \theta _ { q } ) ) .
                                                            2009

```


<!-- p:217 -->


We factorize by the right factor,

det (J(ρ, φ, θq, θr)) = ρ3 ((− cos φ cos θq − cos2 θq − sin φ sin θq − sin2 θq) (− sin φ cos θr + cos φ sin θr) + (cos φ cos θr + cos2 θr + sin φ sin θr + sin2 θr) (− sin φ cos θq + cos φ sin θq) ) = ρ3((−cosφ cosθq − sinφ sinθq −1) (−sinφ cosθr + cosφ sinθr) + (cosφ cosθr +sinφ sinθr + 1) (−sinφ cosθq + cosφ sinθq)) .

We distribute the 1,

$$\det \left ( J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) \right ) & = \rho ^ { 3 } \left ( ( - \cos \varphi \cos \theta _ { q } - \sin \varphi \sin \theta _ { q } ) \left ( - \sin \varphi \cos \theta _ { r } + \cos \varphi \sin \theta _ { r } \right ) \\ & + ( \cos \varphi \cos \theta _ { r } + \sin \varphi \sin \theta _ { r } ) \left ( - \sin \varphi \cos \theta _ { q } + \cos \varphi \sin \theta _ { q } \right ) \\ & + ( \sin \varphi \cos \theta _ { r } - \cos \varphi \sin \theta _ { r } ) + ( - \sin \varphi \cos \theta _ { q } + \cos \varphi \sin \theta _ { q } ) \right ) ,$$

then we develop. Many terms cancel each other to obtain:

$$\det \left ( J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) \right ) = \rho ^ { 3 } \left ( \sin \theta _ { q } \cos \theta _ { r } - \cos \theta _ { q } \sin \theta _ { r } + \sin \varphi \cos \theta _ { r } \\ - \cos \varphi \sin \theta _ { r } - \sin \varphi \cos \theta _ { q } + \cos \varphi \sin \theta _ { q } \right ) .$$

Finally we apply the formulae: cos a sin b − cos b sin a = sin(a − b), on the three well-chosen pairs of terms,

$$\det \left ( J ( \rho , \varphi , \theta _ { q } , \theta _ { r } ) \right ) & = \rho ^ { 3 } ( \sin ( \theta _ { q } - \theta _ { r } ) + \sin ( \theta _ { q } - \varphi ) + \sin ( \varphi - \theta _ { r } ) ) \\ & = \rho ^ { 3 } \left ( \sin ( \pi - ( \theta _ { q } - \theta _ { r } ) ) + \sin ( \theta _ { q } - \varphi ) + \sin ( \varphi - \theta _ { r } ) \right ) \\ & = 4 \rho ^ { 3 } \sin \left ( \frac { \pi - ( \theta _ { q } - \theta _ { r } ) } { 2 } \right ) \sin \left ( \frac { \theta _ { q } - \varphi } { 2 } \right ) \sin \left ( \frac { \varphi - \theta _ { r } } { 2 } \right ) ,$$

where the last line derives from the formula: sin a + sin b + sin c = 4 sin a|2 sin b|2 sin c|2 when a + b + c = π.

#### A.2 Some integrals

We recall that, for the positive numbers L, l, and t, we defined:

$$I _ { L , l } ( t ) = \int _ { 0 } ^ { L } \int _ { 0 } ^ { l } e ^ { - t x y } d y d x .$$

We prove the following lemma:

Lemma 8.5. Let L, l, and t be 3 positive numbers. If tLl &gt; 1 then:

$$\frac { \ln ( t L l ) } { t } < I _ { L , l } ( t ) \leq \frac { \ln ( t L l ) } { t } + \frac { 1 } { t } .$$

Proof. Let t be a positive number such that tLl ≥ 1, we start to rewrite the integral: by bounding from above the following integral:

$$f \text { following integral} & \colon \\ I _ { L , l } ( t ) & = \int _ { 0 } ^ { L } \int _ { 0 } ^ { l } e ^ { - t x } d y d x \\ & = \int _ { 0 } ^ { L } \int _ { 0 } ^ { l x } \frac { e ^ { - t u } } { x } d u d x \\ & = \int _ { 0 } ^ { L } \frac { 1 - e ^ { - t l x } } { t x } d x \\ & = \frac { 1 } { t } \int _ { 0 } ^ { t L l } \frac { 1 - e ^ { - v } } { v } d v \\$$


<!-- p:218 -->


Then we bound IL,l(t) from above:

$$T h e w \, b o und \, I _ { L , l } ( t ) \, f o r \, a b o v e: \\ I _ { L , l } ( t ) & = \frac { 1 } { t } \int _ { 0 } ^ { t L l } \frac { 1 - e ^ { - v } } { v } d v \, b u t \, 1 - e ^ { - v } \leq \min ( 1 , v ) \, \text {so} \\ & \leq \frac { 1 } { t } \int _ { 0 } ^ { t L l } \frac { \min ( 1 , v ) } { v } d v \\ & = \frac { 1 } { t } \left ( \int _ { 0 } ^ { 1 } \frac { v } { v } d v + \int _ { 1 } ^ { t L l } \frac { 1 } { v } d v \right ) \\ & = \frac { 1 } { t } \left ( \int _ { 0 } ^ { 1 } d v + \int _ { 1 } ^ { t L l } \frac { 1 } { v } d v \right ) \\ & = \frac { 1 } { t } \left ( 1 + \ln ( t L l ) \right ) . \\ \text {And we bound } I _ { L , l } ( t ) \, f o r \, b o u n d \colon$$

And we bound IL,l(t) from below:

$$I _ { L , l } ( t ) = \frac { 1 } { t } \int _ { 0 } ^ { t L l } \frac { 1 - \frac { } { } \int _ { 0 } ^ { t L l } \frac { 1 - } { } \int _ { 0 } ^ { t L l }$$

$$w \text { bound } I _ { L , l } ( t ) & \text { from below: } \\ I _ { L , l } ( t ) & = \frac { 1 } { t } \int _ { 0 } ^ { t L l } \frac { 1 - e ^ { - v } } { v } d v \\ & \geq \frac { 1 } { t } \int _ { 0 } ^ { t L l } \frac { 1 } { v + 1 } d v \quad \text { since } \frac { 1 - e ^ { - v } } { v } \geq \frac { 1 } { v + 1 } \text { for } v \geq 0 , \\ & = \frac { 1 } { t } \left ( \ln ( t L l + 1 ) \right ) \\ & > \frac { \ln ( t L l ) } { t } .$$

We also prove here the lemma involving the area of the rhombuses.

$$\L L e m { a } \, 8 . 1 0 . \ L e t \, t > 0 , \, \beta \in ] 0 , 1 [ , \, \text {and} \, I _ { \beta } ( t ) = \int _ { \mathbb { R } } \int _ { \mathbb { R } } e ^ { - t \sqrt { ( x ^ { 2 } + y ^ { 2 } ) ( \beta ^ { 2 } x ^ { 2 } + y ^ { 2 } ) } } d y d x , \\ I _ { \beta } ( t ) = \frac { 1 } { t } I _ { \beta } ( 1 ) \leq \frac { \pi } { t } \left ( 1 + \ln ( \frac { 1 } { \beta } ) \right ) .$$

Proof. We apply, in the integral, the variables substitution: (x, y) = ( Y) with Jacobian determinant 1 .7

$$I _ { \beta } ( t ) & = \int _ { \mathbb { R } } \int _ { \mathbb { R } } e ^ { - t \sqrt { ( x ^ { 2 } + y ^ { 2 } ) ( \beta ^ { 2 } x ^ { 2 } + y ^ { 2 } ) } } d y d x \\ & = \int _ { \mathbb { R } } \int _ { \mathbb { R } } \frac { 1 } { t } e ^ { - \sqrt { ( X ^ { 2 } + Y ^ { 2 } ) ( \beta ^ { 2 } X ^ { 2 } + Y ^ { 2 } ) } } d Y d X \\ & = \frac { 1 } { t } I _ { \beta } ( 1 ) .$$

Then we compute an upper bound:

$$\text {upper bound} & \quad \\ I _ { \beta } ( 1 ) & = \int _ { \mathbb { R } } \int _ { \mathbb { R } } e ^ { - \sqrt { ( x ^ { 2 } + y ^ { 2 } ) ( \beta ^ { 2 } x ^ { 2 } + y ^ { 2 } ) } } d y d x \\ & = 4 \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } e ^ { - \sqrt { ( x ^ { 2 } + y ^ { 2 } ) ( \beta ^ { 2 } x ^ { 2 } + y ^ { 2 } ) } } d y d x \\ & = 4 \int _ { 0 } ^ { \frac { \pi } { 2 } } \int _ { 0 } ^ { \infty } r e ^ { - r ^ { 2 } \sqrt { \beta ^ { 2 } \cos ^ { 2 } \theta + \sin ^ { 2 } \theta } } d r d \theta \\ & = 2 \int _ { 0 } ^ { \frac { \pi } { 2 } } \left ( \beta ^ { 2 } \cos ^ { 2 } \theta + \sin ^ { 2 } \theta \right ) ^ { - \frac { 1 } { 2 } } d \theta .$$

□


<!-- p:219 -->


On [0, x], (β2 cos2 θ + sin2 θ) is smaller than both and π ; on the one hand, because (β2 cos2 θ + sin2 θ) 1|2 decreases from 2 θ, so that: π

$$I _ { \beta } ( 1 ) & \leq 2 \int _ { 0 } ^ { \frac { \pi } { 2 } } \min \left ( \frac { 1 } { \beta } , \frac { \pi } { 2 \theta } \right ) \, d \theta \\ & = 2 \left ( \int _ { 0 } ^ { \beta \frac { \pi } { 2 } } \frac { 1 } { \beta } d \theta + \int _ { \beta } ^ { \frac { \pi } { 2 } } \frac { \pi } { 2 \theta } d \theta \right ) \\ & = \pi \left ( 1 - \ln ( \beta ) \right ) .$$

#### A.3 The set of 4/2-balls passing through two points is a good pencil

In order to prove Lemma 10.2, we must prove that, for any 3 points p, q and r of R2, there exists a single 4/2-ball whose boundary passes through p, q and r. If the existence of such a sphere is trivial, its uniqueness is more complicated to prove. We prove the equivalent property that claims that two different 4/2-balls intersect in at most two points.

Thus we actually prove the stronger property: the boundaries of any two different 4/2-balls (not only in B4/2(p, q)) intersect in at most 2 points.

First, note that any two different concentric 4/2-balls have disjoint boundary. Thus we can order the concentric 4/2-balls by inclusion. Subsequently, we can order any two 4/2-balls, up to a concentric translation. We show that, if two 4/2-balls are tangent at (0, 0), then the smaller has a larger curvature at (0, 0).

The equation of a 4/2-ball bc passing through (0, 0) and centered on c is given by :

$$b _ { c } & \colon ( x - x _ { c } ) ^ { 4 } + ( y - y _ { c } ) ^ { 2 } \leq x _ { c } ^ { 4 } + y _ { c } ^ { 2 } , & \text {that we can rewrite} \\ b _ { c } & \colon x ^ { 4 } - 4 x ^ { 3 } x _ { c } + 6 x ^ { 2 } x _ { c } ^ { 2 } - 4 x x _ { c } ^ { 3 } + y ^ { 2 } - 2 y y _ { c } \leq 0 .$$

The equation of the tangent at (0, 0) is thus:

$$2 x x _ { c } ^ { 3 } + y y _ { c } = 0$$

In other words, all spheres centered on (xc, yc) such that is constant are tangent at (0, 0). We compute the curvature of bc at (0, 0). Without loss of generality we assume that xc and yc are positive, and write the lower part of the 4/2-ball as the graph y = fc(x), where:

$$f _ { c } ( x ) = y _ { c } - \sqrt { x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } } .$$

We compute the first and second derivative of fc:

$$We compute the first and second derivative of f _ { c } \colon \\ f _ { c } ^ { \prime } ( x ) = \frac { 4 ( x - x _ { c } ) ^ { 3 } } { 2 \sqrt { x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } } } \\ f _ { c } ^ { \prime \prime } ( x ) = \frac { 1 2 ( x - x _ { c } ) ^ { 2 } \times 2 \sqrt { x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } } + 4 ( x - x _ { c } ) ^ { 3 } \times 2 \frac { 4 ( x - x _ { c } ) ^ { 3 } } { 2 \sqrt { x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } } } } { 4 \left ( x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } \right ) } \\ = \frac { 1 2 ( x - x _ { c } ) ^ { 2 } \times 4 \left ( x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } \right ) + 4 ( x - x _ { c } ) ^ { 3 } \times 8 ( x - x _ { c } ) ^ { 3 } } { 8 \left ( x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } \right ) ^ { \frac { 3 } { 2 } } } \\ = \frac { 6 ( x - x _ { c } ) ^ { 2 } \left ( x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } \right ) + 4 ( x - x _ { c } ) ^ { 6 } } { ( x _ { c } ^ { 4 } - ( x - x _ { c } ) ^ { 4 } + y _ { c } ^ { 2 } ) ^ { \frac { 3 } { 2 } } }$$


<!-- p:220 -->


The curvature is given by f" (0) 2 We want to know how it evolves when xc grows. Since they are (1+(f(0))2) tangent, it is clear that f'(0) is constant with xc, and so, we are only interested in the variation of f'(0) with xc.

$$f _ { c } ^ { \prime \prime } ( 0 ) & = \frac { 6 x _ { c } ^ { 2 } y _ { c } ^ { 2 } + 4 x _ { c } ^ { 6 } } { y _ { c } ^ { 3 } } \\ & = \frac { 6 x _ { c } ^ { 2 } y _ { c } ^ { 2 } } { y _ { c } ^ { 3 } } + \frac { 4 x _ { c } ^ { 6 } } { y _ { c } ^ { 3 } } \\ & = \frac { 6 x _ { c } ^ { 2 } } { y _ { c } } + \frac { 4 x _ { c } ^ { 6 } } { y _ { c } ^ { 3 } } \\ & = \frac { x _ { c } ^ { 3 } } { y _ { c } } \frac { 6 } { x _ { c } } + \left ( \frac { x _ { c } ^ { 3 } } { y _ { c } } \right ) ^ { 3 } \frac { 4 } { x _ { c } ^ { 3 } } . \\$$

x Since is constant for tangent 4/2-balls, the curvature is clearly decreasing with xc. In other words, a yc smaller 4/2-ball has larger curvature, whatever is the tangency point. As a consequence, if two different 4/2-balls are tangent, then the tangent point is their unique intersection.

Consider now two 4/2-balls b1 &lt; b2, and assume by the absurd that they intersect at 3 points (or more). Consider the translation of b1 from the center of b1 to the center of b2. During the translation, two of the intersection points move until they meet in a tangent contact. But by the curvature property described above, there cannot be a tangent contact and another intersecting point. So it not possible that there was three intersection points initially.

This proves that the boundary of two different 4/2-balls intersect in at most 2 points, and so, that the pencil of 4/2-balls whose boundary passes through two given points is a good pencil.


<!-- p:221 -->
