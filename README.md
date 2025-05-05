# Study Repository 

This repository contains the data and statistical analyses of the study **Association Between COVID-19 Vaccination and Mortality in Immunocompromised Older Adults: A Population-Based Analysis**.

Check the results at [analysis.html](analysis.html).

## Files

The repository contains the following files:

- SIVEP-Gripe data: [SRAG 2024_DOWNLOAD 29_3_25 IMUNODEPRE_RT_PCR OU ANTIGENO%20POSITIVO.xlsx](SRAG%202024_DOWNLOAD%2029_3_25%20IMUNODEPRE_RT_PCR%20OU%20ANTIGENO%20POSITIVO.xlsx)
- Data dictionary (in Portuguese): [Dicionario_de_Dados_SRAG_Hospitalizado_19.09.2022.pdf](Dicionario_de_Dados_SRAG_Hospitalizado_19.09.2022.pdf)
- R notebook source: [analysis.Rmd](analysis.Rmd)
- R notebook result as HTML: [analysis.html](analysis.html)
- Table with versions of R packages for reproducibility: [installed_packages.csv](installed_packages.csv)
- Project README (this): [README.md](README.md)

## How to run

We performed the statistical analyses in R (version 4.5.0) using a single [R notebook](analysis.html). The notebook is divided into sections and produces the results we included in the study.

It is possible to run and edit the notebook source ([analysis.Rmd]) with [RStudio](https://rstudio.com/products/rstudio/) and use it to invoke `knit` to generate the results as HTML.

You may need to install some additional R libraries to run it. Use the following commands on R console:

```R
install.packages("openxlsx")
install.packages("dplyr")
install.packages("lubridate")
install.packages("purrr")
install.packages("tidyr")
install.packages("prettyR")
install.packages("scales")
install.packages("DescTools")
install.packages("ggplot2")
install.packages("pROC")
install.packages("ResourceSelection")
```

For specific versions of the libraries, check [installed_packages.csv](installed_packages.csv). This file was created using the following commands:

```R
ip = as.data.frame(installed.packages()[,c(1,3:4)])
ip = ip[is.na(ip$Priority),1:2,drop=FALSE]
write.csv(ip, "installed_packages.csv")
```

## Authors

- Rodrigo P. V. Rezende MD PhD[^1]
- João Felipe Pimentel PhD[^2],
- Bruno S. Caxias MD[^1],
- Caio M. Salgueiro MD[^1],
- Lucas T. Oliveira MD[^1],
- Luís Fernando A. Santos MD[^1],
- Caroline P. Pessanha MD[^1]
- Vitoria Xavier Tracierra MD[^1]
- Michael G. Simão MD[^1]
- Mario Gustavo A. Pacheco MD[^1]
- Vitor A. Cruz MD PhD[^3]
- Luiz Eduardo C. Oliveira MD MSc[^1]

[^1]: Faculty of Medicine, Universidade Federal Fluminense, RJ, Brazil
[^2]: Institute of Computing, Universidade Federal Fluminense, RJ, Brazil
[^3]: Faculty of Medicine, Universidade Federal de Goiás, GO, Brazil
 
