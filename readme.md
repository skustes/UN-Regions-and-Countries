# Wrangling UN Regions & Countries
## By: Scott Kustes

## Objective
Wrangle Geographic Regions from United Nations Statistics Division and associated countries into rationalized format for database storage. This data will be used for a future website.

## Dataset
The CSV was downloaded from the UN Statistics Division website at https://unstats.un.org/unsd/methodology/m49/overview/

It consists of a file with 249 rows and 15 columns. Each row contains information on a country or area with associated Region, Sub-region, and Intermediate Region information, along with M49 codes, ISO Alpha3 codes, and a several "Other Groupings" such as Least Developed Countries, Landlocked Developing Countries, Developed Countries, Developing Countries, and Small Island Developing States.

To this file, I manually added the official name of the country, the common name of the country, and the capital city. Example:
- Common: Ireland
- Official: Republic of Ireland
- Capital: Dublin

## Output
The data was cleaned and wrangled to create the following dataframes:
- UN Regions: Master table with hierarchy of UN Geoscheme Regions
- UN Groupings: Master table with the "Other Groupings" to which countries can be assigned
- Countries to Groups: Junction table to associate Countries to UN Groupings
- Countries: Master table of UN-recognized countries and areas of the world (utf-16 encoding to preserve unique characters in a few country names)

These were exported to csv and inserted into a relational database.