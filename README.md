# Senegal Locust Damage Analysis

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17547461.svg)](https://doi.org/10.5281/zenodo.17547461)

This repository contains data and code for the manuscript "Evidence that community-based soil amendments suppress migratory pests and increase yield". The workflows here support the analyses and figures presented in the paper and provide reproducibility for other interested researchers.

## Authors

Mamour Toure<sup>1*</sup>, Amadou Fall<sup>2</sup>, Alana Burnham<sup>3</sup>, Alioune Beye<sup>4</sup>,  
Fatou Bintou Sarr<sup>5</sup>, Douglas Lawton<sup>6</sup>, Arianne Cease<sup>7,8*</sup>  

<sup>1</sup> UFR EFSS, Gaston Berger University, Saint Louis, Senegal  
<sup>2</sup> Biology Animal Department, FST, UCAD, Dakar, Senegal  
<sup>3</sup> Arizona State University, Tempe, AZ, USA  
<sup>4</sup> Retired, Direction de la Protection des Végétaux, Nganda, Senegal  
<sup>5</sup> Institute of Environmental Science, UCAD, Dakar, Senegal  
<sup>6</sup> Syngenta Seeds, Research Triangle Park, NC, USA  
<sup>7</sup> School of Sustainability, Arizona State University, Tempe, AZ, USA  
<sup>8</sup> School of Life Sciences, Arizona State University, Tempe, AZ, USA  

**Corresponding authors**: mamour.toure@ugb.edu.sn, acease@asu.edu 

## Repository Structure

This repo is divided as follows:

- `data/`: Raw and processed experimental data
    - `alldata_v17.xlsx`, `alldata_v19.xlsx`: Original field data
    - `analysis_ready_data.csv`: Cleaned data after manipulation
    - `processed/`: Output from modeling scripts, ready for further analysis or figure generation
- `output/`: Results from analysis scripts (plots, tables, and model summaries)
    - `raw_yield_plots/`: Basic yield visualizations
    - `ose_treatment_plots/`: Exploratory and modeled locust abundance/damage plots
    - `modeled_yield_plots/`: Model-derived yield comparisons
    - `model_summary_files/`: Tables summarizing statistical models
    - `locust_yield_plots/`, `raw_visualization/`, `raw_yield_plots/`, etc.: Supporting output files and figures used in manuscript
    - PDFs and PNGs: Manuscript-ready figures
- `scripts/`: Analysis scripts (organized numerically by workflow step)
    - `01_data_management_and_quick_viz.qmd`: Reads, cleans, and formats field data
    - `02_fertilization_millet_yield.qmd`: Main yield analysis and modeling
    - `03_fertilization_locust_abundance_attack.qmd`: Locust abundance and crop damage modeling
    - `04_additional_correlations.qmd`: Additional correlation analyses (temperature, humidity, ground cover)
    - `05_manuscript_figure_and_table_construction.qmd`: Figure/table generation for final publication
    - `06_weather_data_extraction.ipynb`: Extracts ERA5 weather data for site regions (not implemented in main analyses, but included for completeness)
- `renv/`, `renv.lock`: R environment version control. Use these files to ensure reproducibility (see below).

Other files:
- `LICENSE`: Licensing and use requirements.
- `.gitignore`: Version control housekeeping.

## Software Versions

The analyses were run in R version 4.4.1.  

All packages are version-locked via `renv.lock` for reproducibility. This includes packages like tidyverse, ggplot2, mgcv, gratia, emmeans, janitor, MetBrewer, patchwork, sf, rnaturalearth, rnaturalearthdata, and others listed in `renv.lock`.  

There is one Jupyter notebook for external data, written in Python 3.13. This was used solely for weather data extraction and is not required for the main analyses. 

## How to Reproduce Analyses

1. Clone or download the repository.
2. Restore package environment:
    ```r
    # In R
    install.packages("renv")
    renv::restore()
    ```
3. Begin with `01_data_management_and_quick_viz.qmd` to generate analysis-ready data (`analysis_ready_data.csv`).
4. Run scripts `02_...qmd` through `05_...qmd` in order. These scripts depend on outputs from preceding scripts. Figures and tables for the manuscript will appear in the `output/` folder.
5. The weather extraction notebook (`06_weather_data_extraction.ipynb`) is not required for the main paper, but is included for completeness. It uses Google Earth Engine and ERA5 and may require special authentication.

## Data & Manuscript Overview

The experiments involve field trials measuring the effects of soil amendments on locust abundance/damage and millet yield across two villages (Gniby, Gossas), with multi-timepoint survey data.  

Scripts handle cleaning, adjusting locust metrics per village, fitting models for treatment effects, and building figures/tables for publication.

## Questions

For scientific or technical questions, reach out to the corresponding authors listed above. If you have questions about the code and statistical workflow, please contact the repo owner.


If you use this code or data in research, please cite the manuscript and data.
