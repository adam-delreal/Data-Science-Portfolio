
# Project 4 - Predicting the West Nile Virus

Members: Adam Del Real, Bing Chen, Max Reinisch, and Yuki Hadeishi

--------------

## Motivation

The motivation behind this project was to create a model that may **predict when and where different species of mosquitos will test positive with the West Nile virus.** Permitting the City of Chicago and the Chicago Department of Public Health (CPHD) to efficiently and effectively allocate their resources towards the prevention of the West Nile Virus.

----------

## Built with

This project was built with Jupyter Notebooks, using (but not limited to): Python, Pandas, Numpy, Scikit Learn, Natural Langauage Toolkits, Seaborn, Motplotlib, Keras, & Tensorflow.

-------

## Overview

This project is broken down into 4 Categories and 6 notebooks:

- Exploratory Data Analysis:
    - 01A) Data Cleansing Weather Master
    - 01B) Data Cleansing Traps Master
    - 01C) Data Visualization

- Preprocessing the Data:
    - 2) Preprocessing Master

- Kaggle Submission:
    - 3) Create Submission
    
- Predictive Models:
    - 4) Build Models

-------

## Dictionary 

Three dataframes were used for this project and an index is provided for each below.

------

### Train: 
- `ID`                       : The id of the record.
- `Date`                     : date that the WNV test is performed - YEAR/MM/DD - Between: 2007-06-29 & 2013-09-26
- `Address`                  : Approximate address of the location of trap. This is used to send to the GeoCoder. 
- `Species`                  : 7 Species of Mosquitoes:

    - `CULEX TERRITANS` 
    - `CULEX TARSALIS` 
    - `CULEX SALINARIUS`
    - `CULEX RESTUANS` : West Nile Virus is Presesnt among `0.017883` of this species.
    - `CULEX PIPIENS/RESTUANS` : West Nile Virus is Presesnt among `0.055135` of this species.
    - `CULEX PIPIENS` : West Nile Virus is Presesnt among `0.088922` of this species.
    - `CULEX ERRATICUS`
    

- `Block`                    : Block number of address
- `Street`                   : Street name
- `Trap`                     : Id of the trap
- `AddressNumberAndStreet`   : Approximate address returned from GeoCoder
- `Latitude`                 : Latitude returned from GeoCoder
- `Longitude`                : Longitude returned from GeoCoder
- `AddressAccuracy`          : Accuracy returned from GeoCoder
- `NumMosquitos`             : Number of mosquitoes caught in this trap
- `WnvPresent`               : Whether West Nile Virus was present in these mosquitos. 1 means WNV is present, and 0 means not present.


-------

### Weather: 

- `Station`        : `1` or `2`
- `Date`           : YEAR/MM/DD 
- `Tmax`           : Maximum Temperature - Values: 41 - 104
- `Tmin`           : Minimum Temperature - Values: 29 - 83
- `Tavg`           : Average Temperature - Values: 36 - 94 
- `Depart`         : Departure from normsl temperature. 
- `DewPoint`       : Average Dew Points in whole degrees Fahrenheit.
- `WetBulb`        : Average Wet Bulb.
- `Heat`           : Seasonal - Starts in July
- `Cool`           : Seasonal - Starts in January
- `Sunrise`        : Time of Sunrise - 4:17 through 6:23
- `Sunset`         : Time` of Sunset - 16:56 through 19:31
- `CodeSum`        : 

- **Tornado:**
    - `+FC TORNADO/WATERSPOUT`
    - `FC FUNNEL CLOUD`


- **Rain:**
    - `TS THUNDERSTORM` 
    - `GR HAIL`
    - `RA RAIN`
    - `DZ DRIZZLE`
    - `SH SHOWER`

    
    
- **Snow:**
    - `SN SNOW`
    - `SG SNOW GRAINS`
    - `GS SMALL HAIL &/OR SNOW PELLETS`
    - `PL ICE PELLETS`
    - `IC ICE CRYSTALS`
    - `DR LOW DRIFTING`*
    - `BC PATCHES`*
    
    
- **Fog/Mist:**
    - `FG+ HEAVY FOG (FG & LE.25 MILES VISIBILITY)`
    - `FG FOG`
    - `BR MIST`
    
    
- **Others:**
    - `UP UNKNOWN PRECIPITATION`
    - `HZ HAZE`
    - `FU SMOKE`
    - `VA VOLCANIC ASH`
    - `DU WIDESPREAD DUST`
    - `DS DUSTSTORM`
    - `PO SAND/DUST WHIRLS`
    - `SA SAND`
    - `SS SANDSTORM`
    - `FZ FREEZING`
    - `MI SHALLOW`
    - `PR PARTIAL`
    - `PY SPRAY`
    - `SQ SQUALL`
     - `BL BLOWING`
     - `VC VICINITY`
     - `- LIGHT`
     - `+ HEAVY`
     - `"NO SIGN" MODERATE`
- `Depth`          : Snoe depth in inches
- `Water1`         : WATER EQUIVALENT(INCHES & HUNDREDTHS(2400 LST)
RAINFALL & MELTED SNOW 
- `SnowFall`      : SNOWFALL (INCHES AND TENTHS)(2400 LST)*
- `PrecipTotal`    : Precipitation
- `StnPressure`    : Pressure in inches of HG
- `SeaLevel`       : Average sea level pressure
- `ResultSpeed`   : Speed of the Vector of the wind. 
- `ResultDir`      : Resultant Direction of the wind in whole degrees
- `AvgSpeed`       : Avg Wind speed


-------

### Spray:

- `Date` : The date the pesticide was sprayed in YEAR/MONTH/DAY.
- `Time` : The time sprayed.
- `Latitude` : The latitude of the location sprayed.
- `Longitude` : The longitude of the location sprayed.


-------

## Optimal Model:

**Random Forest Classifier:** Draws a sample from the training data with replacement (bootstrap sampling); meaning a sample is drawn and put back in place to randomly chose a sample again. Furtheremore, when splitting a node, the split that is picked is the best hew among a random subset of the features.

**Parameters:** 
- `N Estimators` is the number of trees in the forest, which we tuned to 100.
- `Maximum Depth` allows us to control the maximum number of depth the tree, which we set to 3.
- `Minimum Leaf Sample` is the minimum number of samples in a leaf, which we set to 3

**Score on the Training Data:** ~ 0.958

**Score on the Testing Data:** ~ 0.958

**Average X Test Prediction:** ~ 0.011

**ROC/AUC Score:** ~ 0.897

**Kaggle Score:** ~71%