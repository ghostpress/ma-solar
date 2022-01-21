# Policy Analysis of Rooftop Solar Incentives in MA  

Code written for CAS EE 508: Data Science for Conservation Decisions, Boston University fall 2021.

## Background

This analysis attempts to determine which incentives are more effective in encouraging the adoption of rooftop solar PV systems in Massachusetts, and specifically 4 study locations: Newton, West Roxbury, Hyde Park, and Milton. 

## Data  

- Existing PV installations in MA, provided by the [Massachusetts Clean Energy Center](https://www.masscec.com/public-records-requests), which includes all solar PV systems fully registered in the Production Tracking System (PTS), current as of May 2021. From these data, I extracted the PV systems that were listed as: residential; multi-family residential; mixed-use (commercial & residential); and that were not third-party owned in the study locations.

- Boundaries of MA by town and zipcode, provided by [MassGIS](https://www.mass.gov/info-details/massgis-data-zip-codes-5-digit-from-here-navteq). From these, I extracted the zipcodes included in the study locations.

- Roofprints of MA buildings larger than 150 sq ft, provided by [MassGIS](https://www.mass.gov/info-details/massgis-data-building-structures-2-d): MassGIS (Bureau of Geographic Information), Commonwealth of Massachusetts EOTSS, accessed 12/09/2021.  

- Photovoltaic Electricity Potential data for the USA, provided by [SolarGIS](https://solargis.com/maps-and-gis-data/download/usa) (PVOUT, map 1): © 2020 The World Bank, Source: Global Solar Atlas 2.0, Solar resource data: Solargis.

- Household income data by MA block group (2015-2019), provided by [NHGIS](https://data2.nhgis.org/): Steven Manson, Jonathan Schroeder, David Van Riper, Tracy Kugler, and Steven Ruggles. IPUMS National Historical Geographic Information System: Version 16.0 [dataset]. Minneapolis, MN: IPUMS. 2021. http://doi.org/10.18128/D050.V16.0.

- 2019 federal tax brackets by annual income, provided by [CreditKarma](https://www.creditkarma.com/tax/i/2019-tax-brackets-things-to-know): Pimplaskar, Evelyn. “2019 Tax Brackets: Things to Know: Credit Karma Tax®.” Credit Karma, 7 Dec. 2020, https://www.creditkarma.com/tax/i/2019-tax-brackets-things-to-know. 

- Massachusetts income tax rate, provided by the [Tax Foundation](https://taxfoundation.org/state/massachusetts/): “Massachusetts Tax Rates & Rankings: MA State Taxes.” Tax Foundation, Tax Foundation, https://taxfoundation.org/state/massachusetts/.

- eGRID CO2-equivalent emissions estimates for MA electricity generated, provided by the [EPA](https://www.epa.gov/sites/default/files/2015-10/documents/egrid2012_summarytables_0.pdf): United States Environmental Protection Agency (EPA). 2021. “Emissions & Generation Resource Integrated Database (eGRID), 2019” Washington, DC: Office of Atmospheric Programs, Clean Air Markets Division. Available from EPA’s eGRID web site: https://www.epa.gov/egrid.

- National average cost of PV systems in $/W, provided by [EnergySage](https://news.energysage.com/how-much-does-the-average-solar-panel-installation-cost-in-the-u-s/): Marsh, Jacob. “How Much Do Solar Panels Cost in 2022?: Energysage.” How Much Do Solar Panels Cost?, EnergySage, 4 Jan. 2022, https://news.energysage.com/how-much-does-the-average-solar-panel-installation-cost-in-the-u-s/. 

- Existing incentive programs for residential rooftop PV adoption in Massachusetts, provided by [MASSCEC](https://www.masscec.com/solar-incentives-and-programs): “Incentives and Programs.” MASSCEC, Massachusetts Clean Energy Center, 14 July 2021, https://www.masscec.com/solar-incentives-and-programs.

- Solar Massachusetts Renewable Target (SMART) Program incentive details, provided by the Commonwealth of Massachusetts and Eversource:
  - “SMART Incentive Program.” Eversource, Eversource, https://www.eversource.com/content/ema-c/residential/save-money-energy/explore-alternatives/learn-about-solar-energy/smart-program.
  - “Capacity Block, Base Compensation Rate, and Compensation Rate Adder Guideline.” | Mass.gov, Commonwealth of Massachusetts, https://www.mass.gov/doc/capacity-block-base-compensation-rate-and-compensation-rate-adder-guideline-2.
  - United States, Congress, Executive Office of Energy and Environmental Affairs. Guideline Regarding Low Income Generation Units, 225 CMR 20.00, p. 2. SOLAR MASSACHUSETTS RENEWABLE TARGET PROGRAM.

## Other Sources

- Electricity use in homes, provided by the [US Energy Information Administration (EIA)](https://www.eia.gov/energyexplained/use-of-energy/electricity-use-in-homes.php): “Use of Energy Explained: Energy Use in Homes.” U.S. Energy Information Administration (EIA), EIA, 9 May 2019, https://www.eia.gov/energyexplained/use-of-energy/electricity-use-in-homes.php.

- Estimate of % energy loss (through heat, soil, shading, etc.), provided by NREL's (PVWatts Calculator)[https://pvwatts.nrel.gov/pvwatts.php]: Dobos, Aron, P. “PVWatts Version 5 Manual.” Technical Report. National Renewable Energy Laboratory, September 2014. https://www.nrel.gov/docs/fy14osti/62641.pdf.


## Use Instructions  

To replicate this project on your local machine with anaconda, enter the following command in a terminal window:  

`conda create --name myenv --file requirements.txt`  

Where `myenv` is the name of your local environment. Then clone this repository to edit and run the code. 
