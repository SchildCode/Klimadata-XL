# Klimadata-XL
Klimadata-XL is a macro-enabled Microsoft Excel workbook.
It enables simple and fast downloading of hourly weather data direct to Excel from met.no (Frost API) and NIBIO (AgroMetBase). Advanced quality-checking and gap-filling.

### Features:
- Dynamic menu, search for available parameters for a given station and/or dates, or search for available stations for a given parameter
- Lists the nearest stations for a given latitude & longitude, municipality, or for a given meteo station
- Practically unlimited number of observations can be downloaded from the Frost-API/AgroMetBase web services, i.e. many years and parameters
- You can paste in data from your own sources, to use the quality-checking and gap-filling features
- Downloads quality flags from Met.no, which indicate the quality of data for each hour
- Vets data for jumps, extreme values, and static values (dead sensor); calculates sigma value for these errors (threshold sigma can be changed)
- Finds outliers (calculates sigma value) by comparing observations with multiple nearby stations
- Hotkey CTRL+N jumps to the next period containing outlier values
- Parameter-specific code for checking quality, e.g. checks relative humidity, dew-point and dry-bulb temperatures for equivalence
- Special code for solar radiation (global, direct, or diffuse) including checking for incorrect time-stamp, correction for night-time calibration offset, automatic detection of obscuring features such as trees or masts that shade the pyranometer, and comparison with clear-sky irradiance (REST2-model)
- Visualizes the data (scatter-plot comparing with nearby stations) and carpet plot
- Parameter-specific gap-filling, which prioritizes moving observations from best-fit nearby stations (kriging by regression), and if such data is unavailable then the gaps are filled by interpolation using a method similar to Kalman filter, which faithfully reproduces the diurnal profile.

### Licences:
- The Klimadata-XL workbook and source code is free closed-source (Lisence CC BY-ND 4.0): https://creativecommons.org/licenses/by-nd/4.0/
- Data from Frost API can have different licenses depending on source. Most data is licensed under 'Norwegian license for public data' (NLOD) and Creative Commons 4.0 BY International: http://creativecommons.org/licenses/by/4.0/
- Data from NIBIO Landbruksmeteorologisk tjeneste (LMT) AgroMetBase is lisenced under 'Norwegian license for public data' (NLOD): http://data.norge.no/nlod/

### Author:
Klimadata-XL written by Peter G. Schild, Oslo Metropitan University & SINTEF Byggforsk in the period 2008-2019.
