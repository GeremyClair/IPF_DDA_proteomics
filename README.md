# Proteome analysis of a human donor cohort to study Idiopathic Pulmonary Fibrosis
 Data analysis of the proteomics for UNAGI paper done by Geremy Clair

Please let us know if you need any assistance in executing or understanding this code.

This repository contains the details of the LC-MS/MS data analysis for the UNAGI IPF paper.

The R markdown and the knitR html report are located in the main folder of the repository

All required files for the analysis are located in the folder 01_source_files

All the files generated during the data analysis are located in the folder 03_Output_files.

Note that you can install [RomicsProcessor](https://github.com/PNNL-Comp-Mass-Spec/RomicsProcessor) from its dedicated repository.

Raw files are deposited on [MassIVE](https://massive.ucsd.edu/ProteoSAFe/static/massive.jsp)

# Code requirements

The code was run using [R](https://cloud.r-project.org) v.4.2.1 on [Rstudio](https://rstudio.com) version 2022.07.1+554 for macOS.

Running the code require:

- The installation of [Devtools](https://cran.r-project.org/web/packages/devtools/index.html)

- The package[RomicsProcessor v.1.1.0](https://github.com/PNNL-Comp-Mass-Spec/RomicsProcessor/blob/master/RomicsProcessor_1.1.0.tar.gz) (follow the package page for installation instructions). RomicsProcessor is an R package that can be used to analyze omics data. The package provides a structured R object to store the data, allowing for reproducible data analysis. The package also supports creating analytically pipelines from previously processed objects and applying these pipeline to other objects. This allows for rapid development and reuse of bioinformatics methods.

- for enrichments analyses we used a packaged named Protein-MiniOn currently only available for MAC users  [ProteinMiniOn](https://github.com/GeremyClair/Protein_MiniOn) from its dedicated repository.

- To run the code create a copy of the repository in a folder on your computer and open the file named "02 - Code.Rmd" and in the rmd file change the working directory to your local location (L17).

- The version of the different dependencies that were employed at time of analysis are contained in the "Romics_object.RData" object located in the folder ".*/03 - Output files". After loading the object in the R environment you can get the version of all packages by typing the following in the R console
```
romics_proteins$dependencies

```

# Data pre-processing

The data was pre-processed using MaxQuant (v1.16.0.1) the file [parameters.txt](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/01_source_files/parameters.txt) generated by MaxQuant is provided. The [summary.txt](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/01_source_files/summary.txt) file indicates what raw files located on MassIVE were used for the analysis. The [peptide.txt](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/01_source_files/peptides.txt) and [proteinGroups.txt](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/01_source_files/proteinGroups.txt) files are also provided along with the metainformation of associated with the samples in the file [metadata.csv](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/01_source_files/metadata.csv).
It is important to note that the [fasta](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/03_output_files/Uniprot_Homo_sapiens_proteome_UP000005640_2021_03_23.fasta) file uploaded was the one used for the search.

The [R markdown knitR report file](https://github.com/GeremyClair/IPF_DDA_proteomics/blob/main/02_IPF_LF_proteomics_code.html) final report can be seen directly without having to run the code.

All the files generated during the data analysis are located in the folder 03 - Output files.

Please let us know if you need any assistance in executing or understanding this code.

## Contacts

Written by @GeremyClair for the Department of Energy (PNNL, Richland, WA) \
E-mail: geremy.clair@pnnl.gov or proteomics@pnnl.gov \
Website: https://omics.pnl.gov/ 

## License

This code is licensed under the 2-Clause BSD License; 
you may not use this file except in compliance with the License.  You may obtain 
a copy of the License at https://opensource.org/licenses/BSD-2-Clause

Copyright 2022 Battelle Memorial Institute