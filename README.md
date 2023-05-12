# wur_mumm_campaign_2021
Vertical Profiles of NO2 over the North Sea in summer 2021 as measured by an aircraft and co-sampled from TM5.  


============================================================================================================
START readme
============================================================================================================


============================================================================================================
## General
============================================================================================================

+ Author(s): T. Christoph V. W. Riess, Jasper van Vliet, Ward Van Roy, Jos de Laat,
Enrico Dammers, and K.Folkert Boersma
+ Contact: christoph.riess@wur.nl


============================================================================================================
## Title
============================================================================================================

Aircraft and TM5 NO2 profiles underlying publication "doi"


============================================================================================================
## Methods
============================================================================================================

# Introduction

Aicraft measured vertical profiles of NO2 over the North Sea during summer 2021, as well as coinciding TM5 profiles.



============================================================================================================
## FolderStructure
============================================================================================================

There is only one parent directory present containing all files.



============================================================================================================
## FolderContents
============================================================================================================

- parent_folder/
- 
"{profilenumber}".csv 
	-One .csv-file for each of the vertical profiles.
	
mean_profile.csv 
	-This is the mean of the campaign, representing a summerday North Sea profile over a busy ship track
	
TM5_"{profilenumber}".csv 
	- One .csv file for each TM5 profile coinciding with the measured profiles

============================================================================================================
## FileFormats
============================================================================================================

The "{profilenumber}".csv -files for the single profiles have the following columns:
"profile": name of the profile
"mid_layer_altitude [m]": center altitude of the layer in meters
"Lat": mean latitude (in Degreees North) 
"Lon": mean longitude (in degrees East)
"NO2 [molec/m^3]": mean corrected number density of NO2 in the layer (in molec/m^3). if multiplied with layer thickness (50m), this yields the sub-columns
"w_n [m/s]": mean northward wind in the layer (in m/s)
"w_e [m/s]": mean eastward wind in the layer (in m/s)
"start [UTC]": starting time of the profile flight (dd.mm.yyyy hh:mm:ss in UTC)
"end [UTC]": end time of the profile flights (dd.mm.yyyy hh:mm:ss in UTC)

The mean_profile.csv has the following columns:
"profile": name of the profile
"mid_layer_altitude [m]": center altitude of the layer in meters
"NO2 [molec/m^3]": mean corrected number density of NO2 in the layer (in molec/m^3) of all ten profiles. if multiplied with layer thickness (50m), this yields the sub-columns
"NO2_sem [molec/m^3]": standard error of NO2 in the layer (in molec/m^3) of all ten profiles

The TM5_"{profilenumber}".csv have the following format:
Alt_int: Altitude of the upper layer interface in [m]. Calculated from the TM5 pressure levels using ERA pressure profiles.
Alt_mid: Altitude of the middle of the layer in [m]. Calculated from the TM5 pressure levels using ERA pressure profiles.
NO2: TM5 NO2 in [molec/m^3] for the given layer. Calculated as the distance weighted mean from TM5 files at https://scihub.copernicus.eu
p: mid-level pressure of the layer and using ERA5 to translete from mixing ratio	
NO2_mr: NO2 as mixing ratio for each layer
AK: Averaging Kernel for each layer as provided in the TM5 files
AK_trop: tropospheric Averaging Kernel for each layer as provided in the TM5 files
T: temperature of each layer from ERA5 data

============================================================================================================
END readme
============================================================================================================
