# Senegal locust damange analysis

This repository is partnered with a manuscript soon to be published entitled 'Evidence that community-based soil amendments suppress migratory pests and increase yield'

## Authors

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

**Corresponding authors**: [mamour.toure@ugb.edu.sn](mailto:mamour.toure@ugb.edu.sn), [acease@asu.edu](mailto:acease@asu.edu)  


## repository structure
This repo is structured as follows:

 - `/data`
  - `/data/processed`: where all post processing data is stored
 - `/output`: where all figures, tables, and potentially model objects are stored
 - `/renv`: this subdirectory is specifically for renv for version control
 - `/scripts`: where all scripts are stored (numbered in order)
  - `scripts/01_data_management_and_quick_viz.qmd`: data management step
  - `scripts/02_fertilization_millet_yield.qmd`: millet fertilization analysis
  - `scripts/03_fertilization_locust_abundance_attack.qmd`: fertilization and locust abundance/attack analysis
  - `scripts/04_additional_correlations.qmd`: temperature, yield, and locust count corrleations
  - `scripts/05_manuscript_figure_and_table_construction.qmd`: where manuscript tables and figures are constructed


## Citation

If you use this code or data in your own research, please cite the following:

Your Name, Co-Author Name, "Title of Your Scientific Article," Journal Name, Year, DOI: [link to article]