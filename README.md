# Betancur-R Bony Fish Phylogeny in anvi'o

This repo contains files for using [anvi'o](http://merenlab.org/software/anvio/) to **visualize and explore** the bony fish phylogeny from [Betancur-R et. al (2017)](https://link.springer.com/article/10.1186/s12862-017-0958-3) and metadata scrapped from [FishBase](https://www.fishbase.se/). 

**The bony fish phylogeny** contains 1992 species encompassing 72 orders and 410 families. At the time of publication this represented roughly 80% of recognized bony fish families. The study uses molecular and genomic data to base classification on inferred phylogenies. From the abstract the author state:

"*The first explicit phylogenetic classification of bony fishes was published in 2013, based on a comprehensive molecular phylogeny [(www.deepfin.org)](www.deepfin.org). We here update the first version of that classification by incorporating the most recent phylogenetic results.*"

The authors provide many files, but for the purposes of this visualization, I used two files from the [Supplementary material](https://link.springer.com/article/10.1186/s12862-017-0958-3#SupplementaryMaterial), specifically **Additional file 2** (complete tree in newick format) and **Additional file 4** (Table S1. spreadsheet with full classification). 

There are two options for visualizations. You can *either* visualize the Betancur-R tree and the metadata scrapped from [FishBase](https://www.fishbase.se/) *or* visualize the Betancur-R tree where Families with more than one species are collapsed. This is nice because I collapsed almost 300 clades so you don't have to. Of course, clades can be expanded at will. That said, the collapsed data base contains only the `CLADE`, `Family`, and `Order` data. 

## Files in this repo

1) `12862_2017_958_MOESM2_ESM.tre` The original Betancur-R tree, not changed or altered.

2) `fish_metadata_complete.txt` All tree metadata, containing data from the Betancur-R **Additional file 4** plus the data scrapped from FishBase.

3) `tree_not_collapsed` Directory

- `not_collapsed_profile.db` Anvi'o profile data base.  
- `not_collapsed_fish_tree.tre` The modified  Betancur-R tree.  
- `data.txt` metadata scraped from FishBase for visualization.
- `default.json` anvi'o states file.

4) `tree_collapsed` Directory

- `collapsed_profile.db` Anvi'o profile data base for the collapsed (by Family) Betancur-R modified tree.
- `collapsed_fish_tree.tre` The collapsed and modified  Betancur-R tree.
- `data.txt` a minimal metadata set for the collapsed tree.

For instructions on how these files were created and all of the R code, please see the [project page](https://istmobiome.rbind.io/project/betancur-r-fish-tree/).

## Changes 

I made a few changes to the original data to make it more compatiable with anvi'o. First, I modified the tree file slightly---in the original file, the Family name was used as a prefix for each species. I removed the Family names from all leaves. **Additional file 4** was slightly reformatted to make it compatible with anvi'o but nothing else was changed. Otherwise the original files were not altered further. The modified files are called `fish_tree.tre` and `additonal_data.txt`, respectively.

 **Anvi'o** "*is an open-source, community-driven analysis and visualization platform for ‘omics data.*" One of the best aspects of anvi'o is it's interactive interface, which is amazing for data exploration---especially phylogenetic trees. Anvi'o is really easy to install using conda in the [Miniconda](https://docs.conda.io/en/latest/miniconda.html) environment. See the installation instructions [here](http://merenlab.org/2016/06/26/installation-v2/).

## How to visualize the trees

Once you have anvi'o installed and the data in hand, visualization is pretty easy. There are **two ways** you can visualize the Betancur-R tree in anvi'o using the files provided here. Both assume you have anvi'o installed and working correctly. If you run `anvi-self-test --suite mini` and everything works you should be good to go.

To visualize the tree with the metadata run this command. 

```
anvi-interactive --profile-db not_collapsed_profile.db \
                 --view-data data.txt \
                 --tree not_collapsed_fish_tree.tre \
                 --manual
```

Or, if you would rather use the use the tree collapsed by family, run this command. 

```
anvi-interactive --profile-db collapsed_profile.db \
                 --view-data data.txt \
                 --tree collapsed_fish_tree.tre \
                 --manual
```

And that's it for now. 
