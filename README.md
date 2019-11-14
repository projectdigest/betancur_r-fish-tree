# Bony Fish Phylogeny in anvi'o

In this repo we provide the files needed to **visualize and explore** the bony fish phylogeny from [Betancur-R et. al (2017)](https://link.springer.com/article/10.1186/s12862-017-0958-3){target} in [anvi'o](http://merenlab.org/software/anvio/).

**The bony fish phylogeny** contains 1990 species encompassing 72 orders and 410 families. At the time of publication this represented roughly 80% of recognized bony fish families. The study uses molecular and genomic data to base classification on inferred phylogenies. From the abstract the author state:

"*The first explicit phylogenetic classification of bony fishes was published in 2013, based on a comprehensive molecular phylogeny [(www.deepfin.org)](www.deepfin.org). We here update the first version of that classification by incorporating the most recent phylogenetic results.*"

The authors provide many files but for our purposes we used two files from the [Supplementary material](https://link.springer.com/article/10.1186/s12862-017-0958-3#SupplementaryMaterial), specifically Additional file 2 (Complete tree in newick format) and Additional file 4 (Table S1. Spreadsheet with the complete classification). We modified the tree file slightly---in the original file, the Family name was used as a prefix for each species. We removed the Family names from all leaves. Additional file 4 was slightly reformatted to make it compatible with anvi'o. Beyond this, the original files were not altered.

 **Anvi'o** "*is an open-source, community-driven analysis and visualization platform for ‘omics data.*" One of the best aspects of anvi'o is it's interactive interface, which is amazing for data exploration---especially phylogenetic trees. Anvi'o is really easy to install using conda in the [Miniconda](https://docs.conda.io/en/latest/miniconda.html) environment. See the installation instructions [here](http://merenlab.org/2016/06/26/installation-v2/).


There are two ways you can visualize Betancur-R tree in anvi'o using the files provided



Anyway, we used the original tree from the paper to choose an out group for our analysis (Gerreidae) and for the fun of it decided to make our own representation of the Betancur-R et. al., tree. To construct the tree above we first downloaded the newick file from the paper’s supplementary material (download link), parsed out the Family data from the tree file (included in the name of each leaf), and finally visualized the tree in anvi’o. Within the anvi’o interface we collapsed any Family represented by two or more species. The size of each triangle is proportional to the number of species in that family while the colors are somewhat arbitrary. Originally we thought it would be cool to color leaves by the Order but that was too complicated. So the colors are really just for looks.

The image above is just half the tree. You can download a full SVG version of our tree by clicking the image below. In the future we would like to identify which fish families have been the subject of microbial investigations and use the phylogenetic framework to identify gaps in knowledge and patterns of associations. The families we studied in this project are in the lower left, marked by asterisks.
