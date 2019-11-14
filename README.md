# Bony Fish Phylogeny in anvi'o

In this repo we provide the files needed to **visualize and explore** the bony fish phylogeny from [Betancur-R et. al (2017)](https://link.springer.com/article/10.1186/s12862-017-0958-3){target="_blank"} in [anvi'o](http://merenlab.org/software/anvio/).

**The bony fish phylogeny** contains 1990 species encompassing 72 orders and 410 families. At the time of publication this represented roughly 80% of recognized bony fish families. The study uses molecular and genomic data to base classification on inferred phylogenies. From the abstract the author state:

"*The first explicit phylogenetic classification of bony fishes was published in 2013, based on a comprehensive molecular phylogeny [(www.deepfin.org)](www.deepfin.org). We here update the first version of that classification by incorporating the most recent phylogenetic results.*"

The authors provide many files but for our purposes we used two files from the [Supplementary material](https://link.springer.com/article/10.1186/s12862-017-0958-3#SupplementaryMaterial), specifically Additional file 2 (Complete tree in newick format) and Additional file 4 (Table S1. Spreadsheet with the complete classification). We modified the tree file slightly---in the original file, the Family name was used as a prefix for each species. We removed the Family names from all leaves. Additional file 4 was slightly reformatted to make it compatible with anvi'o. Beyond this, the original files were not altered.

 **Anvi'o** "*is an open-source, community-driven analysis and visualization platform for ‘omics data.*" One of the best aspects of anvi'o is it's interactive interface, which is amazing for data exploration---especially phylogenetic trees. Anvi'o is really easy to install using conda in the [Miniconda](https://docs.conda.io/en/latest/miniconda.html) environment. See the installation instructions [here](http://merenlab.org/2016/06/26/installation-v2/).


There are **two ways** you can visualize Betancur-R tree in anvi'o using the files we provided here. Both assume you have anvi'o installed.

**Method 1**

Start anvi'o and generate a *ad hoc* database using the `fish_tree.tre` and `additonal_data.txt` files. The tree file is simply our modified version of Additional file 2 and other file contains the taxonomic data for each species from Additional file 4. The only other thing you need is a dummy database file (note: this file **does not** need to exist the first time you run the command).  

Then run this command...

`anvi-interactive -p dummy.db --tree fish_tree.tre  --additional-layers additonal_data.txt --manual`

 If everything works a new interface will open in your browser window. Hit the `Draw` button and the tree will render. At this point you can modify the look of the tree, export an SVG image, etc.

 **Method 2**

The other thing you can do is use our database (`profile.db`) as a starting point. The principle is the same as the other method except that here we have done some beautification already. This database contains the information in the `additonal_data.txt` and the `fish_tree.tre`. It also contains an additional tree representation where we collapsed leaves by Family.

To use this database run this command:

`anvi-interactive -p profile.db  --manual`
