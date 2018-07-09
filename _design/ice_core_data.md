---
layout: page
uid: design-ice-core-data
title: Ice core data sources
---

# Ice core data sources

The data is mostly found on [NOAA NCDC's Paleo Data page](https://www.ncdc.noaa.gov/paleo-search/)

## Depth/Age:
  - [GISP2 Meese/Sowers Timescale](ftp://ftp.ncdc.noaa.gov/pub/data/paleo/icecore/greenland/summit/gisp2/depthage/gisp2age.txt) - official timescale for the GISP2 ice core 110K years BP - present (1988)

## Temperature:
  - [GISP2 Ice Core Temperature and Accumulation Data](ftp://ftp.ncdc.noaa.gov/pub/data/paleo/icecore/greenland/summit/gisp2/isotopes/gisp2_temp_accum_alley2000.txt) - 49K years BP - present
  - [North GRIP - MIS3 CH4, d15N, and Temperature Data](https://www1.ncdc.noaa.gov/pub/data/paleo/icecore/greenland/summit/ngrip/ngrip2006d15n-ch4-t.txt) - 80K years BP - 30K years BP

## CO2 (multiple sources needed for full temporal coverage):
  - [NOAA ESRL - Mauna Loa CO2](ftp://aftp.cmdl.noaa.gov/products/trends/co2/co2_annmean_mlo.txt) - 1958 to present
  - [Law Dome Ice Core](ftp://ftp.ncdc.noaa.gov/pub/data/paleo/icecore/antarctica/law/law2006.txt) - 0 to 2000 A.D.
  - [EPICA Dome C Ice Core High Resolution Holocene and Transition CO2 Data](ftp://ftp.ncdc.noaa.gov/pub/data/paleo/icecore/antarctica/epica_domec/edc-co2.txt) - 22K to 173 years BP
  - [Vostok Ice Core](http://cdiac.ess-dive.lbl.gov/ftp/trends/co2/vostok.icecore.co2) - 400K - 5K years BP

## Sea level:
  - [Sea-level and Deep Water Temperature 430KYr Reconstructions](https://www1.ncdc.noaa.gov/pub/data/paleo/contributions_by_author/waelbroeck2002/waelbroeck2002.txt) Waelbroeck, C., et al. 2010. - 430K years BP to present

## Population:
  - [World Population Prospects: The 2017 Revision, United Nations](https://esa.un.org/unpd/wpp/DVD/Files/1_Indicators%20(Standard)/EXCEL_FILES/1_Population/WPP2017_POP_F01_1_TOTAL_POPULATION_BOTH_SEXES.xlsx) - 1950 - present
  - [Global historical population estimates 10k BC - 2 k AD (in millions)](http://themasites.pbl.nl/tridion/en/themasites/hyde/basicdrivingfactors/population/index-2.html) - 10K years BP - present
  - [Christian, David. Maps of Time: An Introduction to Big History, University of California Press: 2011. ](../assets/population_table.png) - historical counts 100K years BP - present

## Datasets in stories:

- [GISP2 Oxygen Isotope Data](ftp://ftp.ncdc.noaa.gov/pub/data/paleo/icecore/greenland/summit/gisp2/isotopes/gispd18o.txt)
- [GISP2 Ice Core 110,000 Year Ions Data](https://www.ncdc.noaa.gov/paleo-search/study/17805):
  - `calcium` column (`Ca_ppb`) used for dust
  - `sodium` column (`Na_ppb`) used for sea salt
- [Blue Marble 3000](http://radar.zhaw.ch/bluemarble3000_en.html) - [video](https://www.youtube.com/watch?feature=player_profilepage&v=S5UuXfcDqX0) used for ice sheet story
  - Also on [Science on a Sphere](https://sos.noaa.gov/datasets/blue-marble-sea-level-ice-and-vegetation-changes-19000bc-10000ad/)

## Not used:

- [GISP2 Volcanic markers](ftp://ftp.ncdc.noaa.gov/pub/data/paleo/icecore/greenland/summit/gisp2/chem/volcano.txt)
