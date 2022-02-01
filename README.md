# Policy Analysis of Rooftop Solar Incentives in MA  

Code written for CAS EE 508: Data Science for Conservation Decisions, Boston University fall 2021.

## Background

This analysis attempts to determine which incentives are more effective in encouraging the adoption of rooftop solar PV systems in Massachusetts, and specifically 4 study locations: Newton, West Roxbury, Hyde Park, and Milton. 

## Data  

- Existing PV installations in MA, provided by the [Massachusetts Clean Energy Center](https://www.masscec.com/public-records-requests), which includes all solar PV systems fully registered in the Production Tracking System (PTS), current as of May 2021. From these data, I extracted the PV systems that were listed as: residential; multi-family residential; mixed-use (commercial & residential); and that were not third-party owned in the study locations: “PV in PTS Public Records Request.” Massachusetts Clean Energy Center, May 2021. https://www.masscec.com/public-records-requests.

- Boundaries of MA by town and zipcode, provided by [MassGIS](https://www.mass.gov/info-details/massgis-data-zip-codes-5-digit-from-here-navteq). From these, I extracted the zipcodes included in the study locations: MassGIS (Bureau of Geographic Information), Commonwealth of Massachusetts EOTSS, accessed 12/09/2021.

- Roofprints of MA buildings larger than 150 sq ft, provided by [MassGIS](https://www.mass.gov/info-details/massgis-data-building-structures-2-d): MassGIS (Bureau of Geographic Information), Commonwealth of Massachusetts EOTSS, accessed 12/09/2021.  

- Photovoltaic Electricity Potential data for the USA, provided by [SolarGIS](https://solargis.com/maps-and-gis-data/download/usa) (PVOUT, map 1): © 2020 The World Bank, Source: Global Solar Atlas 2.0, Solar resource data: Solargis.

- ShopSolarKits. “300-Watt Solar Panels: Everything You Need to Know,” December 14, 2021. https://shopsolarkits.com/blogs/learning-center/300-watt-solar-panels.

- climatemps. “Sunshine & Daylight Hours in Boston, Massachusetts, USA.” Accessed January 8, 2022. https://www.boston.climatemps.com/sunlight.php.

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

-  Borenstein, Lucas, and Lucas Davis W. “The Distributional Effects of US Clean Energy Tax Credits.” Tax Policy and the Economy 30, no. 1 (2016). https://www.journals.uchicago.edu/doi/full/10.1086/685597.

- Barbose, Galen, L., Naim Darghouth R., Hoen Ben, and Ryan Wiser H. “Income Trends of Residential PV Adopters: An Analysis of Household-Level Income Estimates.” Electricity Markets & Policy. Berkeley Lab, April 2018. https://emp.lbl.gov/publications/income-trends-residential-pv-adopters

- Tong, James, and Alison Mickey. “How to Turn Solar ‘Considerers’ Into Solar Adopters.” GreenTech Media (blog), June 20, 2016. https://www.greentechmedia.com/articles/read/How-to-Turn-Solar-Considerers-Into-Solar-Adopters.

- Initiative for Energy Justice. “Section 1: Defining Energy Justice: Connections to Environmental Justice, Climate Justice, and the Just Transition,” December 2019. https://iejusa.org/section-1-defining-energy-justice/.

- Katie Luu, Scott Burger. “The Economics of Rooftop Solar.” MIT Energy Initiatve. Accessed January 30, 2022. https://energy.mit.edu/podcast/the-economics-of-rooftop-solar/.

- Smith, Aidan, Danilo Morales, and Jen Stevenson Zepeda. Exploring Environmental Justice: Energy Justice in the Boston Area. Interview by Gabriela Boscio Santos and Neha Chinwalla. Zoom, April 21, 2021. https://www.youtube.com/watch?v=prKBKUhYcoA.

- Sommer, Lauren. “What Losing Build Back Better Means for Climate Change.” NPR, December 20, 2021. https://www.npr.org/2021/12/20/1065695953/build-back-better-climate-change.

- Baker, Charles, D., Karyn Polito E., Kathleen Theoharides A., and Martin Suuberg. “Statewide Greenhouse Gas Emissions Level: 1990 Baseline Update.” MGL Chapter 21N, Section 3. Commonwealth of Massachusetts Executive Ofice of Energy & Environmental Affairs, Department of Environmental Protection, May 2021. https://www.mass.gov/doc/statewide-greenhouse-gas-emissions-level-proposed-1990-baseline-update-including-appendices-a-b/download.

- United States Environmental Protection Agency. “Greenhouse Gas Emissions from a Typical Passenger Vehicle,” March 2018. https://www.epa.gov/greenvehicles/greenhouse-gas-emissions-typical-passenger-vehicle#:~:text=typical%20passenger%20vehicle%3F-,A%20typical%20passenger%20vehicle%20emits%20about%204.6%20metric%20tons%20of,8%2C887%20grams%20of%20CO2.

- AN ACT RELATIVE TO GREEN COMMUNITIES, Pub. L. No. Chapter 169, § 138. Accessed January 31, 2022. https://malegislature.gov/laws/sessionlaws/acts/2008/chapter169.

- EnergySage Local Data. “Community Solar in Massachusetts.” Accessed January 31, 2022. https://www.energysage.com/local-data/community-solar/ma/.

- Dong, Changgui, and Benjamin Sigrin. “Using Willingness to Pay to Forecast the Adoption of Solar Photovoltaics: A ‘Parameterization + Calibration’ Approach.” Energy Policy 129, no. June 2019: 100–110. Accessed January 29, 2022. https://doi.org/10.1016/j.enpol.2019.02.017. 


## Use Instructions  

To replicate this project on your local machine with anaconda, enter the following command in a terminal window:  

`conda create --name myenv --file requirements.txt`  

Where `myenv` is the name of your local environment. Then clone this repository to edit and run the code. 
