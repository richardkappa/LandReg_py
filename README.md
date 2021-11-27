# LandReg_py

This code takes shape files and data from a number of different sources and plots it using python

## Data Sources

The data has all been downloaded to my local PC but it can be found in the locations below. It is all UK data with an open government licence, or equivalent. I've found other shapefiles online but was unsure on their licence requirements so have not used them

+ National statistics Geoportal
    + National Statistics Postcode Lookup File [NSPL](https://geoportal.statistics.gov.uk/)
    + shape files for Counties, National Parks, Countries, Local Authorities, LSOA 2011
+ Land Registry Price Paid data [PP_data](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads)
+ Ordnance Survey OpenData
    + [Boundary-Line](https://osdatahub.os.uk/downloads/open/BoundaryLine)
    + [OS Open Greenspace](https://osdatahub.os.uk/downloads/open/OpenGreenspace)
    + [OS Open Rivers](https://osdatahub.os.uk/downloads/open/OpenRivers)
    + [OS Open Roads](https://osdatahub.os.uk/downloads/open/OpenRoads)
    + [OS Open UDPRN](https://osdatahub.os.uk/downloads/open/OpenUPRN) (Not used)
    + [Strategi](https://osdatahub.os.uk/downloads/open/Strategi) (As at 2016)
        + Used for coastline, railways, ferries...
    + [OS Terrain50](https://osdatahub.os.uk/downloads/open/Terrain50)

## Processing
+ 01_GetFlatData.ipynb
    + Imports & Processes the NSPL and land registry data so it can be processed into map data in the next step
+02_MakeGeopandasDataframes.ipynb
    + Imports the various shape files and converts them into a geopandas format
    + Converts the data from 01 into geopandas format
    + Saves the Geopandas files for later use
    + Selects some key grid references and clips the geopandas data to areas around these for quicker processing later