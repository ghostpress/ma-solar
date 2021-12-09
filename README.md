# Policy Analysis of Rooftop Solar Incentives in MA  

Code written for CAS EE 508: Data Science for Conservation Decisions, Boston University fall 2021.  

## Data  

- Roofprints of MA buildings larger than 150 sq ft, provided by [MassGIS](https://www.mass.gov/info-details/massgis-data-building-structures-2-d): MassGIS (Bureau of Geographic Information), Commonwealth of Massachusetts EOTSS, accessed 12/09/2021.  

- Solar curve supply map, provided by [NREL](https://www.nrel.gov/gis/solar-supply-curves.html).

- Average cost of residential and commercial sollar installations in 2020 (Q1), provided by NREL: Feldman, David, Vignesh Ramasamy, Ran Fu, Ashwin Ramdas, Jal Desai, and Robert Margolis. “US Solar Photovoltaic System and Energy Storage Cost Benchmark: Q1 2020.” Technical Report. National Renewable Energy Laboratory, January 2021. https://www.nrel.gov/docs/fy21osti/77324.pdf.

- 2019 federal tax payments in MA by annual income, provided by the [IRS](https://www.irs.gov/statistics/soi-tax-stats-historic-table-2).

- Household income data by MA block group (2015-2019), provided by [NHGIS](https://data2.nhgis.org/): Steven Manson, Jonathan Schroeder, David Van Riper, Tracy Kugler, and Steven Ruggles. IPUMS National Historical Geographic Information System: Version 16.0 [dataset]. Minneapolis, MN: IPUMS. 2021. http://doi.org/10.18128/D050.V16.0.

- eGRID CO2-equivalent emissions estimates for MA electricity generated, provided by the [EPA](https://www.epa.gov/sites/default/files/2015-10/documents/egrid2012_summarytables_0.pdf): United States Environmental Protection Agency (EPA). 2021. “Emissions & Generation Resource Integrated Database (eGRID), 2019” Washington, DC: Office of Atmospheric Programs, Clean Air Markets Division. Available from EPA’s eGRID web site: https://www.epa.gov/egrid.


## Use Instructions  

To replicate this project on your local machine with anaconda, enter the following command in a terminal window:  

`conda create --name myenv --file requirements.txt`  

Where `myenv` is the name of your local environment. Then clone this repository to edit and run the code. 
