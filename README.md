# ATMS 523 Module-4

Time Series and Empirical Orthogonal Function (EOF) analysis was completed in this project. The main goal in this exercise was to get more experience with time series data and to make different visualizations to complete EOF analysis.

## Setting Up
In order to complete the EOF Analysis in Python, the eofs package (available on Github [here](https://github.com/ajdawson/eofs)) will be used. 

The package can be installed using [conda](https://docs.conda.io/projects/conda/en/latest/)
```conda install -c conda-forge eofs```

## Demo the code
Run the ```Module4.ipynb``` file. The necessary datasets are already provided and do not need to be generated again. Feel free to comment those lines out to avoid errors.

## Data
The ERA-5 data for this module was accessed through NCAR's RDA via the THREDDS server which is cited below.

Sea Surface Temperature (SST) and Total Column Water Vapor (WV) variables over the Pacific Basin (65°N to 65°S, 120°E to 60°W) were accessed for the time period of 1979 to 2021. For Problem 1 of the assignment, the data was masked out over land using the [ERA-5 land sea mask](https://rda.ucar.edu/thredds/dodsC/files/g/ds633.0/e5.oper.invariant/197901/e5.oper.invariant.128_172_lsm.ll025sc.1979010100_1979010100.nc).

### NCAR RDA ERA-5 Reanalysis Data
European Centre for Medium-Range Weather Forecasts, 2019: ERA5 Reanalysis (Monthly Mean 0.25 Degree Latitude-Longitude Grid). Research Data Archive at the National Center for Atmospheric Research, Computational and Information Systems Laboratory. Accessed 04 March 2024, https://doi.org/10.5065/P8GT-0R61.

## Key functionalities
- Calculate SST and Total Column WV monthly mean anomalies
- Use of a land sea mask
- Deseasonalize, detrend, and standardize data
- Perform EOF Analysis
- Plot Percent Variance using EOFs
- Reconstruct SST field with EOFs
- Plot [Pearson's correlation coefficient](https://docs.xarray.dev/en/stable/generated/xarray.corr.html)

## References and Acknowledgements
The  [Computations and Masks with Xarray](https://foundations.projectpythia.org/core/xarray/computation-masking.html#overview) was used to mask out the data over land.

For detrending the data, the detrend function from the PyCLIM documentation was used and can be found [here](https://climate.usu.edu/people/yoshi/pyclm101/monthly.html).