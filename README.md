
Source Code for the Power Analysis of a Differentially Private Wilcoxon Signed-Rank Test
========================================================================================

This repository contains source code to carry out the power analysis of a differentially private Wilcoxon signed-rank test, the full version of which can be found [here](link). The organization of this repo is as follows:

-   `application`: Source code for the section "Application to Real World Data" in our paper. In this folder, we have code for plot generation as well as tidying of the data set we chose to use: a dataset of NYC taxi rides in 2013.
-   `comparison`: Source for for the section "Comparison to Previous Work," which compares our test to a prviously proposed version of a differentially private Wilcoxon signed-rank test.
-   `fxns`: This folder contains several R scripts of functions used repeatedly throughout the power analysis. (There are several other functions that are fundamental to functionalizing the power analysis process, but they vary slightly depending on the arguments being treated as variables. See the `.Rmd` files for these functions.) These functions are sourced often from the `.Rmd`s in the other folders---documentation can be found commented out within the scripts.
-   `results`: Source code for the "Experimental Results" section of our paper, which analyzes the power of our test on its own.

In general, this repository contains almost exclusively `.Rmd`, `.Rda`, and `.R` files. The `.Rmd` files are heavily annotated documents outlining our procedures and providing code to carry out the power analysis of our test. Files ending in `.Rda` will almost exclusively be suffixed with `_data`, indicating that they come from a `.Rmd` file of the same name, without the suffix. These files are the data that will be plotted in the `.Rmd` files to create *figures*. There are a couple exceptions to this rule. `.R` files are R scripts containing functions used repeatedly throughout the power analysis process, and are often sourced in the `.Rmd` files. Some of the `.Rmd` files also output `.tex` files, which are *tables* to be included in the paper. The `.tex` files are not included in this folder, but the relevant `.Rmd` files can be ran to generate them. Note that the knit directory of the `.Rmd` files must be set to "Current Working Directory" for all of the `.Rmd` files to run correctly, where the working directory is the parent `wilcoxon` folder.

We refer to *Task 2016* and *the TC test* many times throughout these analyses. This citation refers to the previous proposal of a differentially private Wilcoxon Signed-Rank Test which we improved upon. See [their paper](https://epubs.siam.org/doi/pdf/10.1137/1.9781611974348.18) for more details.

Christine Task and Chris Clifton. 2016. Differentially Private Significance Testing on Paired-Sample Data. In *Proceedings of the 2016 SIAM International Conference on Data Mining.* SIAM, 153–161.

*Simon P. Couch*
