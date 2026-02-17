# Public Datasets

> All projects in this repo use publicly available data. This file is the master reference for data sources by domain.

---

## Groundwater & Surface Water

| Dataset | Source | Format | Use Case |
|---------|--------|--------|----------|
| [National Water Information System (NWIS)](https://waterdata.usgs.gov/nwis) | USGS | API / CSV | Groundwater levels, streamflow, water quality — ideal for time series projects |
| [Water Quality Portal](https://www.waterqualitydata.us/) | USGS / EPA / NWCMC | API / CSV | Multi-agency water quality data; great for contamination analysis |
| [Groundwater Watch](https://groundwaterwatch.usgs.gov/) | USGS | Web / CSV | Long-term groundwater level trends |
| [National Groundwater Monitoring Network](https://cida.usgs.gov/ngwmn/) | USGS | API | Standardized groundwater data across state agencies |

---

## Environmental Contamination & Compliance

| Dataset | Source | Format | Use Case |
|---------|--------|--------|----------|
| [EPA ECHO (Enforcement & Compliance)](https://echo.epa.gov/) | EPA | API / CSV | Facility compliance records, violations, inspections |
| [Superfund Site Information (CERCLIS)](https://www.epa.gov/superfund/superfund-data-and-reports) | EPA | CSV | NPL site data, remediation status, contaminants |
| [Toxics Release Inventory (TRI)](https://www.epa.gov/toxics-release-inventory-tri-program) | EPA | CSV / API | Annual facility-level toxic chemical releases |
| [Risk Management Program (RMP)](https://www.epa.gov/rmp) | EPA | CSV | Chemical accident risk data for industrial facilities |
| [EnviroFacts](https://enviro.epa.gov/) | EPA | API | Multi-program environmental data in one place |

---

## ESG & Corporate Sustainability

| Dataset | Source | Format | Use Case |
|---------|--------|--------|----------|
| [SEC EDGAR ESG Disclosures](https://www.sec.gov/cgi-bin/browse-edgar) | SEC | XBRL / Text | Public company ESG filings; great for NLP/LLM projects |
| [CDP Open Data](https://www.cdp.net/en/articles/media/cdp-datasets) | CDP | CSV | Corporate climate, water, and forest disclosures |
| [GRI Sustainability Disclosure Database](https://database.globalreporting.org/) | GRI | Web / CSV | Standardized ESG reporting data |
| [World Bank ESG Data](https://datatopics.worldbank.org/esg/) | World Bank | API / CSV | Country-level ESG indicators |

---

## Geospatial & Remote Sensing

| Dataset | Source | Format | Use Case |
|---------|--------|--------|----------|
| [Landsat (USGS/NASA)](https://earthexplorer.usgs.gov/) | USGS / NASA | GeoTIFF | Satellite imagery for land use, vegetation, site characterization |
| [National Land Cover Database (NLCD)](https://www.mrlc.gov/) | USGS | GeoTIFF | Land use / land cover classification across the US |
| [National Hydrography Dataset (NHD)](https://www.usgs.gov/national-hydrography) | USGS | Shapefile / GDB | Stream networks, watersheds, water bodies |
| [Watershed Boundary Dataset (WBD)](https://www.usgs.gov/national-hydrography/watershed-boundary-dataset) | USGS | Shapefile | HUC boundaries for watershed-scale analysis |
| [EPA GeoPlatform](https://www.epa.gov/geospatial) | EPA | Various | EPA geospatial datasets — facilities, watersheds, air quality |
| [OpenTopography](https://opentopography.org/) | NSF | LiDAR / DEM | High-resolution elevation data |

---

## Climate & Meteorology

| Dataset | Source | Format | Use Case |
|---------|--------|--------|----------|
| [NOAA Climate Data Online](https://www.ncdc.noaa.gov/cdo-web/) | NOAA | API / CSV | Historical weather, precipitation, temperature |
| [Daymet](https://daymet.ornl.gov/) | NASA / ORNL | NetCDF | Daily gridded climate data (precip, temp) across North America |
| [PRISM Climate Data](https://prism.oregonstate.edu/) | Oregon State | GeoTIFF / CSV | High-resolution gridded climate normals and recent data |

---

## Soil & Geology

| Dataset | Source | Format | Use Case |
|---------|--------|--------|----------|
| [Web Soil Survey (SSURGO)](https://websoilsurvey.nrcs.usda.gov/) | USDA NRCS | Shapefile / API | Soil properties, classifications, and mapping units |
| [National Geologic Map Database](https://ngmdb.usgs.gov/) | USGS | Various | Geologic mapping data |
| [USGS Mineral Resources Data System](https://mrdata.usgs.gov/) | USGS | CSV / API | Mine sites, mineral deposits — useful for legacy contamination work |

---

## Accessing Data Programmatically

Most USGS and EPA datasets have Python-friendly APIs. Key libraries:

```python
# USGS water data
import dataretrieval.nwis as nwis
df = nwis.get_record(sites='01646500', service='dv', start='2020-01-01')

# EPA ECHO via REST API
import requests
r = requests.get('https://echo.epa.gov/api/rest/facility/search', params={...})

# Landsat via Google Earth Engine (requires free account)
import ee
ee.Initialize()
```

---

*All data used in this repo is publicly available and used in accordance with each source's terms of use. No proprietary or client data is included.*
