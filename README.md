# ModernBodyForm_China
Code and models for analysing spatial variation in human body form across modern China using georeferenced anthropometric data and Bayesian GAMMs. Explores ecological, historical, and sociocultural drivers of variation in stature, body mass, and body proportions.

## 📂 Data Description
The primary dataset, `data/raw/modern_multiple_groups.csv`, contains group-level means compiled from published literature.
- **Sample Size**: 91,683 adults (46,885 males, 44,798 females) from 213 groups

- **Time Periods**:  
  - **Mid-to-late 20th century** (1949–1999): Includes individuals born during the Great Chinese Famine (1959–1961), marked by malnutrition and developmental delays.  
  - **Early 21st century** (post-2000): Represents individuals benefiting from improved healthcare, urbanization, and living standards after China's 1978 economic reforms.  
- **Anthropometric Measures**: Group mean stature, body mass, and sitting height from individuals aged 18 and above. 

### 🌍 Climate Data
Climate rasters (temperature, precipitation, elevation) are stored under `data/raw/worldclim/` and sourced from WorldClim v2.1:  
> Fick, S. E. & Hijmans, R. J. (2017). *WorldClim 2: new 1-km spatial resolution climate surfaces for global land areas.* International Journal of Climatology, 37(12), 4302–4315. DOI: 10.1002/joc.5086

---
## 🔁 Reproducibility
- All analyses are conducted in **R ≥ 4.2.0**.
- Model priors, formulas, MCMC settings, and plotting themes are specified in full within the scripts.
- No manual tweaking or GUI interactions required.

---
## 📦 Key R Packages

**Data wrangling & plotting**  
- `tidyverse` (dplyr, tidyr, ggplot2, stringr, …)  
- `here` (project-root file paths)

**Spatial data**  
- `sf` (vector GIS operations)  
- `raster` (raster I/O and processing)  
- `sp` (SpatialPoints and legacy classes)

**Modeling & posteriors**  
- `brms` (Bayesian GAMMs via Stan)  
- `bayesplot` (MCMC diagnostics & plots)  
- `tidybayes` (tidy posterior draws)

**Multi-panel & colors**  
- `patchwork` (plot_layout)  
- `RColorBrewer` (palette generation)




