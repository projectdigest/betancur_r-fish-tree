# Bony Fish Phylogeny

In this repo we provide the files needed to visualize the bony fish phylogeny from [Betancur-R et. al (2017)](https://link.springer.com/article/10.1186/s12862-017-0958-3) in [anvi'o](http://merenlab.org/software/anvio/).

**The bony fish phylogeny** contains 1990 species encompassing 72 orders and 410 families. At the time of publication this represented roughly 80% of bony fishes recognized. The study uses molecular and genomic data to base classification on inferred phylogenies. From the abstract the author state:

*The first explicit phylogenetic classification of bony fishes was published in 2013, based on a comprehensive molecular phylogeny [(www.deepfin.org)](www.deepfin.org). We here update the first version of that classification by incorporating the most recent phylogenetic results.*




To construct the tree we first needed an appropriate out group. Our search for an out group lead to DeepFin and the amazing paper by Betancur-R et. al., (2017) on the phylogenetic classification of bony fishes. The tree in this paper is the 4th version (the original dates back to 2013) and is based on the phylogeny of a whopping 1990 species encompassing 72 orders and 410 families. Wow. In our study, we looked at intestinal microbes from five fish species across two families.

Anyway, we used the original tree from the paper to choose an out group for our analysis (Gerreidae) and for the fun of it decided to make our own representation of the Betancur-R et. al., tree. To construct the tree above we first downloaded the newick file from the paper’s supplementary material (download link), parsed out the Family data from the tree file (included in the name of each leaf), and finally visualized the tree in anvi’o. Within the anvi’o interface we collapsed any Family represented by two or more species. The size of each triangle is proportional to the number of species in that family while the colors are somewhat arbitrary. Originally we thought it would be cool to color leaves by the Order but that was too complicated. So the colors are really just for looks.

The image above is just half the tree. You can download a full SVG version of our tree by clicking the image below. In the future we would like to identify which fish families have been the subject of microbial investigations and use the phylogenetic framework to identify gaps in knowledge and patterns of associations. The families we studied in this project are in the lower left, marked by asterisks.
