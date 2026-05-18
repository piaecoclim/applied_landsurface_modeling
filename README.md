# 🌍 Simple Water Balance Model (SWBM)

Final version of the model developed during the **Applied Land Surface Modeling** course (SoSe 2025). A general workflow of the model can be found [here](workflow.jpeg).
---

### Features
- Snow dynamics based on temperature threshold and melt coefficient
- Dynamic evapotranspiration coefficient ($\beta_0$) influenced by Leaf Area Index (LAI) and temperature
- Modular and fully vectorized with `xarray` and `apply_ufunc`

---

### 🗂️ Data Overview

All input data has:
- **Spatial resolution**: 0.5°
- **Temporal range**: 2000–2023  
- Download: [Google Drive Folder](https://drive.google.com/drive/folders/1V765zRx40aa4dfW-wJSSS-9CB0W1tfSI?usp=sharing)

**Datasets used:**
- **LAI**: MOD15A2H.061 (originally 8-daily, linearly interpolated to daily)
- **ERA5**: Daily average temperature, net radiation, and total precipitation

---

### 🔧 Setup Instructions

The following steps provide an easy and user-friendly way to install the required dependencies for the model. While you can manually install missing packages using pip or conda (primarily numpy, xarray, and matplotlib), using a dedicated Conda environment is generally a more reliable approach. It helps avoid version conflicts and package clashes, especially when working across multiple projects.

#### 1. Install (Mini-)Conda (if not installed):  


#### 2. Create the environment from `.yml` file:
```bash
conda env create -f environment.yml
```

to activate the environment:

```
conda activate wbm_env
```

#### 3. Modify the <code> data_path & output_path </code> within the waterbalancemodel.py file. And then run python waterbalancemodel.py in the python environment.

#### 4. Run the model in the terminal via
```
python waterbalancemodel.py
```


# Output 
- model_output.nc: Water balance components (runoff, evapotranspiration, soil moisture, snow)
- water_balance_components.png: Time series plot for a selected location (e.g., Freiburg)


### Alternative Version for setting up the environment
```
conda create --name wbm_env

conda activate wbm_env

conda install -c conda-forge numpy xarray matplotlib netcdf4 h5netcdf dask

```

### Global runoff observation-driven dataset
```
https://essd.copernicus.org/articles/11/1655/2019/

```

### NDVI LAI 500m
```
https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD15A2H
https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MOD13A1#bands

```

### Global irrigation gridded dataset
```
https://gee-community-catalog.org/projects/global_irrigation/#citation
```

### Month and nice colorbar
```
https://colorcet.holoviz.org/user_guide/Continuous.html
<img width="237" height="88" alt="Screenshot 2026-05-18 at 12 13 50 PM" src="https://github.com/user-attachments/assets/63e70e1e-19b4-4eec-ac2c-ccb876b4cb48" />
```
### Biome
```
https://www.gloh2o.org/koppen/
```

### Google earth engine
```
https://code.earthengine.google.com/
```
