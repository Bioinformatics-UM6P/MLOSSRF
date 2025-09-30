# Al Moutmir Agronomic Dataset

This directory provides schema documentation and structural details about the dataset used in the research paper _"Machine Learning-Based Optimization of Site-Specific Fertilizer Recommendation."_ The data was collected and curated by the **Al Moutmir Initiative** — a national agricultural development program launched by **OCP Group**, a global leader in the phosphate industry.


## 1. About the Al Moutmir Program

Al Moutmir is a science-based multi-service platform that supports smallholder farmers across Morocco through:

- Soil analysis and fertility diagnosis
- Personalized NPK fertilizer recommendations
- Demonstration platforms and field trials
- Capacity building for rural communities
- Promotion of sustainable agricultural practices

The dataset used in this project spans three agricultural seasons (2018–2021), covers 34 provinces across 8 regions, and includes detailed soil, crop, and management information across multiple crop types, including soft wheat, durum wheat, and barley.


## 2. Raw Dataset Schema and Column Descriptions

### Agronomic & Geographic Information
  
  | Column Name             | Description |
  |------------------------|-------------|
  | `growth_season`        | Season identifier (e.g., 2018–2019) |
  | `region`, `province`   | Administrative and geographic area |
  | `longitude`, `latitude`| Geographic coordinates of the field site |
  | `sub_program`          | Program type (e.g., GAP, farmer control) |
  | `crop`                 | Crop type (soft wheat, durum wheat, barley) |
  | `variety`              | Crop variety |
  | `sowing_date`          | Date of sowing |
  | `harvesting_date`      | Date of harvesting |
  | `sowing_rate_kg_ha`    | Seed application rate (kg/ha) |
  | `water_regime`         | Irrigation type (e.g., rainfed, irrigated) |
  | `previous_crop`        | Crop grown in previous season |


### Soil Analysis
  
  | Column Name             | Description |
  |------------------------|-------------|
  | `soil_ph`              | Soil acidity/alkalinity |
  | `organic_matter_percent` | Percentage of organic matter |
  | `caco3_t`, `caco3_ac`  | Total and active calcium carbonate |
  | `clay_percent`         | Proportion of clay in the soil |
  | `sand_percent`         | Proportion of sand in the soil |
  | `phosphorus_ppm`       | Available phosphorus (Olsen ppm) |
  | `potassium_ppm`        | Potassium in parts per million |
  | `electrical_conductivity` | Soil salinity (mS/cm) |


### Base Fertilizer Application (kg/ha)
  
  | Column Name            | Description |
  |-----------------------|-------------|
  | `npk_nitrogen`        | Nitrogen dose |
  | `npk_phosphorus_p2o5` | Phosphorus dose |
  | `npk_potassium_k2o`   | Potassium dose |
  | `npk_so3`             | Sulfur dose |
  | `npk_mgo`             | Magnesium oxide dose |
  | `npk_cao`             | Calcium oxide dose |
  | `npk_zn`, `npk_mn`    | Zinc and manganese doses |


### Topdressing Fertilizer Application (kg/ha)
  
  | Column Name            | Description |
  |-----------------------|-------------|
  | `topdress_n`, `topdress_p2o5`, `topdress_k2o` | Post-sowing nitrogen, phosphorus, potassium |
  | `topdress_so3`, `topdress_mgo`, `topdress_cao` | Sulfur, magnesium, calcium topdress doses |
  | `topdress_nbr_of_applications` | Number of topdress events |


### Plant Growth & Performance
  
  | Column Name                      | Description |
  |---------------------------------|-------------|
  | `plant_height_anthesis_cm`      | Height at flowering stage |
  | `plant_density_tillering`       | Density during tillering stage |
  | `number_of_tillers_booting`     | Tiller count at booting stage |
  | `number_of_ears_per_plant`      | Ears per plant |
  | `fresh_biomass_kg_ha`           | Fresh biomass weight per hectare |
  | `grain_yield_kg`                | Final grain yield in kg/ha |
  | `harvest_index`                 | Ratio of grain to total biomass |
  | `tsw_g`                          | Thousand seed weight (grams) |


## 3. Full Descriptive Statistics (Post Data Processing)

### Dataset Shape
- **Rows:** 7,180
- **Columns:** 46

### Crops
  
  | Crop         | Count | %     |
  |--------------|-------|-------|
  | **S. Wheat**    | 5,495 | 76.53% |
  | **D. Wheat**    | 878   | 12.23% |
  | **Barley**      | 800   | 11.14% |
  | **Oats**        | 7     | 0.10%  |

### Seasons
- **2018–2019:** 914 samples (12.73%)
- **2019–2020:** 1,736 samples (24.18%)
- **2020–2021:** 4,530 samples (63.09%)

### Growth Season × Crop Distribution (examples)
- **2018–2019:**  
  - S. Wheat: 608 (66.52%)  
  - D. Wheat: 131 (14.33%)  
  - Barley: 168 (18.38%)  
  - Oats: 7 (0.77%)  

- **2019–2020:**  
  - S. Wheat: 1,102 (63.48%)  
  - D. Wheat: 432 (24.88%)  
  - Barley: 202 (11.64%)  

- **2020–2021:**  
  - S. Wheat: 3,785 (83.55%)  
  - D. Wheat: 315 (6.95%)  
  - Barley: 430 (9.49%)  

### Descriptive Statistics of Key Variables

<div align="center">
    
  | Variable                  | Mean   | SD    | P0   | P25  | P50  | P75  | P100 |
  |---------------------------|--------|-------|------|------|------|------|------|
  | **Soil pH**                   | 7.97   | 0.41  | 7.30 | 7.60 | 8.00 | 8.30 | 8.50 |
  | **Organic Matter Percent**    | 2.41   | 0.66  | 1.60 | 1.80 | 2.30 | 3.00 | 3.50 |
  | **Electrical Conductivity**   | 0.07   | 0.38  | 0.00 | 0.00 | 0.00 | 0.00 | 8.00 |
  | **Nitrogen (N)**              | 29.60  | 6.81  | 20.00| 24.00| 30.00| 35.00| 40.00|
  | **Phosphorus (P₂O₅)**         | 47.01  | 16.33 | 24.00| 32.00| 46.00| 60.00| 70.00|
  | **Potassium (K₂O)**           | 40.03  | 17.61 | 20.00| 22.00| 39.00| 60.00| 70.00|
  | **Yield (kg/ha)**             | 3473.83| 1437.98|1400.00|2250.00|3500.00|4800.00|5500.00|

</div>

> **Note:** The dataset is confidential and **not publicly shared** due to privacy and licensing constraints. This documentation is provided for transparency and to support reproducibility for researchers working with similar datasets.
