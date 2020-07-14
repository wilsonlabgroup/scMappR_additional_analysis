
# single-cell mapper (scMappR) figure regeneration

### Dustin Sokolowski: dustin-dot-sokolowski-at-sickkids-dot-ca

### Date: 07/02/2020


## Description

These folders contain all of the data and R scripts required to generate the main figures, tables, and supplemental figures used in the scMappR manuscript. Within each folder has it's own readme of how to regenerate the scripts.

To re-create absolutely everything it would take > 4 hours and requires internet due to pathway enrichment but the executable below will run it. The following R packages are additionally required.
To regenerate an indivudual figure. Change your working directory in R into that directory.

All original data, intermediary files for re-processing, and outputs are saved within each directory. Below describes how to re-create all of the output code. 

Also, the main figures contain R markdown directories to describe the clode a little clearer.

# Generating each figure

```{r install_developter, eval=FALSE}

# Table 1
setwd("Table 1/")
source("execute_Table1.R")
setwd("..")

# Table # Note: This requires the use of internet (gmt file)
setwd("Table 2/")
source("execute_Table1.R")
setwd("..")

# Figure 2 
setwd("Figure 2/")
source("execute_Figure2.R")
setwd("..")

# Figure 3 # Note: This requires the use of internet (pathway enrichment)
setwd("Figure 3/")
source("execute_Figure3.R")
setwd("..")

# Supplementary 

setwd("Supplemental")


setwd("Supplementary Table 1/")
source("SupplementaryTable1.R")
setwd("../")



# Supplemental 1

setwd("Supplementary1_volcanoplot/")
source("SupplementaryFigure1.R")
setwd("..")

# Supplemental 2

setwd("Supplementary2_permutation/")
source("SupplementaryFigure2.R")
setwd("..")

# Supplemental 3

setwd("Supplementary3_ranks/")
source("SupplementaryFigure3.R")
setwd("..")

# Supplemental 4

setwd("Supplementary4_pca_correlation/")
source("SupplementaryFigure4.R")
setwd("..")

# Supplementary Figure 5 is part of Figure 3

# Supplemental 6

setwd("Supplementary6_scatterplots/")
source("SupplementaryFigure6.R")
setwd("..")

# Supplemental Table 1

setwd("SupplementaryTable1/")
source("SupplementaryTable1.R")
setwd("..")

# Supplemental Table 2

setwd("SupplementaryTable2/")
source("SupplementaryTable2.R")
setwd("..")

# Supplemental Table 3

setwd("SupplementaryTable3/")

# If you want to redo the identification of all cwFold-changes, then run the scripts in 
# the "proessing" directory. This takes a while and the output is stored.
# source("preprocessing/kidney_scMappR_comparisons.R") # all cwFold-changes
# source("preprocessing/kidney_scMappR_comparisons_small.R") # 7 samples, 4 cell-types
# source("preprocessing/kidney_scMappR_comparisons_allSamples_4cells.R") # 50 samples 4 cell-types

source("SupplementalTable3.R")
setwd("../")

# Supplemental Table 4 Note: This requires the use of internet (gmt file)

setwd("SupplementaryTable4/")
source("SupplementalTable4.R")
setwd("../")

# Supplemental Table 5 Note: This requires the use of internet (gmt file)

setwd("SupplementaryTable5/")
source("SupplementalTable5.R")
setwd("../")

setwd("..")

# Supplemental 7

setwd("Supplementary7 and supplemental Table 2_subsampling/")

# This code calculates all cwFold-changes with all samples and all cell-types,
# Results are stored in /data and code takes a while to run
source("preprocessing/kidney_scMappR_comparisons.R")

# This code calculates all cwFold-changes with 7 samples and 4 cell-types
# Results are stored in /data and code takes a while to run

source("preprocessing/kidney_scMappR_comparisons_small.R")

source("SupplementaryFigure7.R")
setwd("..")

# Supplemental 8

setwd("Supplementary8_gwas/")

source("SupplementaryFigure8.R")

setwd("..")


```
