# Land Use Analysis Tool

This Python script automates a land use classification workflow using a user-provided shapefile boundary and NLCD land cover raster. It is designed to run in the ArcGIS Pro Python environment (`arcgispro-py3`) and offers optional map symbology and PNG export for visual outputs. The 2023 National Land Cover Database download link is included and a shapefile boundary of the San Francisco Bay Area are provided, but any NLCD year or alternative shapefile can be used.

## Features

- Reprojects shapefile to match raster projection
- Clips land cover raster to the input shapefile
- Converts raster to polygon
- Assigns land use class names and RGB codes
- Optionally applies symbology using a `.lyrx` file
- Optionally exports a PNG map using a layout from an ArcGIS Pro project

## Repository Structure

```
LandUseAnalysis/
├── BayArea_Boundary.shp                        # Example input shapefile (and .dbf/.shx/etc.)
├── Final Project Script_Input_Copy.py          # Main script
├── LandUse_Symbology.lyrx                      # Layer symbology file
├── MapTemplate.aprx                            # ArcGIS Pro project with a layout
├── README.md                                   # This file
```

## How to Run

1. Download the Annual NLCD from the link below. 
2. Run the script (`Final Project Script_Input_Copy.py`).
3. Provide:
   - Working directory path
   - Shapefile name
   - Optionally, a different NLCD `.tif` file
   - Whether you're running inside ArcGIS Pro
   - Whether you want a PNG map export

## Required Download

Due to GitHub file size limits, the NLCD land cover raster is not included in this repository.

[Download Annual_NLCD_LndCov_2023_CU_C1V0_2.tif from Dropbox] (https://www.dropbox.com/scl/fi/vc2helt0nn0jn7f1l97iu/Annual_NLCD_LndCov_2023_CU_C1V0_2.tif?rlkey=ar91gnp946qrc6ol7fgtsutl0&st=qlmnfnxf&dl=1)

After downloading, place the file in your project folder so it’s available to the script.

## Data Sources

- **National Land Cover Database (2023)** – 30-meter resolution raster: United States Geological Survey (USGS) and the Multi-Resolution Land Characteristics Consortium (MRLC) https://www.usgs.gov/centers/eros/science/national-land-cover-database
- **Bay Area boundary shapefile** – American Community Survey Cartographic Boundary Files (cb_2023_us_county_500k) https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html

## License

This project is licensed under the MIT License.

## Author

Catherine Campbell – GIS and environmental justice enthusiast.
