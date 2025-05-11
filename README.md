# WATER BALANCE MODEL FROM COURSE APPLIED LAND SURFACE MODELING SOSE24

Final version of the Simple Waterbalance Model (SWBM) including:

* Snow implementation
* Influence of LAI and Temperature on $\beta_0$
* Running over all grid cells at the same time using xarray functionality

Have a look at the basic structure of the model [here](workflow.jpeg).

All Data has 0.5° spatial resolution and a temporal coverage between 2000 and 2023. Data can be downloaded under this [link](https://drive.google.com/drive/folders/1V765zRx40aa4dfW-wJSSS-9CB0W1tfSI?usp=sharing)

* LAI data (MOD15A2H.061) is lineary interpolated to daily resolution (origionally 8-daily)
* Temperature, Net-Radiation & Precipitation are ERA5 reanalysis Data

You can set up a Python environment using the `environment.yml` file in order to automatically install all required packages (and their correct versions) with Conda (you need to install anaconda first, if not already done). In your terminal run

```
conda env create -f environment.yml
```

to activate the environment:

```
conda activate your-env-name
```


