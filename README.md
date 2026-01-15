# TraitTimeLagsMarine

This repository contains the data, scripts, and outputs used to analyse time-lagged biodiversity responses (extinction debt and immigration credit) in benthic megafaunal communities of the Dogger Bank (North Sea), using suitability estimates from observed and dark diversity.

The repository is organised to allow full reproducibility of the analyses and figures presented in the associated manuscript.


## Reproducibility

This project uses renv to manage R package dependencies.

To reproduce the analyses:

```{r}

# install renv if needed
install.packages("renv")

# restore the project environment
renv::restore()

# Then open and render:

scripts/script_GCB_MarineDD.qmd

```

## Repository structure

```text

├── data/
├── figs/
│   ├── MainFigs/
│   ├── SuppFigs/
│   └── silhouettes/
├── rdsFiles/
├── renv/
├── scripts/
└── README.md

```

## Folder descriptions


- `data/`

```text

Input datasets used in the analyses.

`coordinates.csv`
Geographic coordinates of sampling stations.

`comm_data.csv`
Community data including species occurrences by station and year.

`trait_df.csv`
Species trait data, including body size and motility.
```

- `figs/`

```text

Figures generated for the manuscript.

  `MainFigs/`
Final versions of figures included in the main text (except Figure 1, which was created using Inkscape).

  `SuppFigs/`
Supplementary figures.

  `silhouettes/`
SVG silhouette files used for species illustrations (e.g. Figure 5).
```

- `rdsFiles/`

```text

Intermediate .rds objects used in the analyses to avoid repeated data processing.

Examples include:

GBIF-derived taxonomic information (e.g. phylum assignment)

Processed temperature data
```
- `scripts/`

```text


Scripts used to run all analyses and generate figures.

 `script_GCB_MarineDD.qmd`


Quarto document containing the full analysis workflow, including:

data processing; 
suitability and dark diversity estimation; 
trait-based analyses; 
statistical models; 
figures
```

`renv/`

Project-specific R environment managed with renv.
This ensures package versions are fixed and analyses remain reproducible.


## Data sources and notes

Analyses were developed and run using R version 4.4.0. Make sure you are not using an older version.

Temperature data were obtained from the Copernicus Marine Environment Monitoring Service (CMEMS).

Trait information was compiled from published sources and the WoRMS database.

Some intermediate .rds files are included to improve computational efficiency and future reproducibility.

## Citation

If you use data, code, or ideas from this repository, please cite the associated manuscript:

[Citation will be added upon publication]

## License

Code and data in this repository are shared for reuse with attribution.
Please cite this repository and the associated paper when using any part of the material.