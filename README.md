
# WildfirePrediction Project Documentation

## CSCE 5900 Special Problems Course Project

### Project Overview
The objective of this project is to analyze geospatial data, specifically temperature data, and visualize this data on maps. Using netCDF files for temperature data and shapefiles for geographical boundaries, the project consists of several stages: data loading, manipulation, visualization, and animation creation.

The project is structured around multiple Jupyter notebooks, each corresponding to a different stage of the data analysis pipeline:

1. **Loading** geospatial data from netCDF files and shapefiles.
2. **Transforming and analyzing** the data.
3. **Visualizing** the results.
4. **Saving** visualizations as images or animations.

---

### Notebook Descriptions

1. **Untitled.ipynb**
   - Loads a shapefile and a netCDF file, then plots temperature data from the netCDF file on a map with the shapefile as a boundary. 
   - Down-samples the data and plots the down-sampled temperature data.

2. **DAYMET(NA)(TMIN)(2000).ipynb**
   - Loads and visualizes Daymet data for minimum temperature, overlaying it with a shapefile grid.
   - Attempts to reproject the shapefile to match the CRS of the Daymet data.

3. **DAYMET(NA)(TMIN)(2000) (2).ipynb**
   - Similar to the previous notebook, but includes more detailed comments explaining the processing steps.

4. **dataRemix_tmin.ipynb**
   - Overlays minimum temperature data from a Daymet file on a clipped grid.
   - Demonstrates various approaches to the overlay using `rasterio` and `geopandas` for geospatial operations and `matplotlib` for visualization.

5. **Copy_of_overlay_that_keeps_skipping_every_tif_file_this_keeps_crashing_because_no_ram.ipynb**
   - Attempts to overlay multiple TIF files onto a shapefile of North America.
   - Plots the shapefile, then loops through the TIF files, plotting each one at the corresponding coordinates. This notebook can encounter memory issues due to large data size.

6. **Breaking_down_the_netCDF_file_into_daily_files.ipynb**
   - Contains a function to split a netCDF file into daily files.
   - Loops through each day in the dataset, selects data for that day, and saves it as a new netCDF file.

7. **Combining_the_images_to_create_animation.ipynb**
   - Combines multiple images into a GIF animation.
   - Loops through a range of days, generates plots for each, saves them as images, and combines all images into a single GIF.

8. **idk.ipynb**
   - Loads a shapefile and netCDF file, down-samples the netCDF data, and plots the data with a color bar.
   - Contains a loop to generate a plot for a range of days and save each plot as an image.

---

### Project Outcomes
The project provides insights into manipulating and visualizing geospatial data. The ability to overlay temperature data on a map and animate it over time offers valuable visualization of changing temperature patterns. Techniques for handling large datasets and managing memory usage were also explored.

---

### Usage Guide

To use each notebook:
1. **Ensure all required data paths** are correctly specified within each notebook.
2. **Run all cells sequentially** in the order provided to ensure that data loading, processing, and visualization steps execute correctly.

Each notebook is self-contained and does not require specific input beyond the data paths already provided.

---

### Troubleshooting

**Memory Errors**  
If you encounter `MemoryError` messages while running the notebooks, this is likely due to the large size of the data.  
Suggestions:
- **Process data in smaller chunks** using libraries like `Dask`.
- **Optimize memory usage** by adjusting code to handle data in smaller segments.

---

### Data Documentation

**Data Sources**  
- **netCDF Files**: Contain daily minimum temperature data across North America, organized by latitude and longitude. Each file represents a different day.
- **Shapefiles**: Provide geographical boundaries used in visualizations. For this project, a North America shapefile is used as a base for mapping the temperature data.

---

### Code Explanation

The code in this project is written in Python and organized across several Jupyter notebooks, each representing different stages of the analysis pipeline.

#### Key Python Libraries
- **netCDF4**: For reading netCDF files.
- **geopandas**: For working with shapefiles and other geospatial data.
- **rasterio**: For raster data processing and overlaying data on shapefiles.
- **matplotlib**: For creating static visualizations.
- **imageio**: For creating GIF animations from image sequences.

---

### Future Work

1. **Improve Data Processing Efficiency**  
   - Modify the data pipeline to reduce memory usage, either by processing in smaller chunks or by using optimized data structures.

2. **Enhance Data Analysis**  
   - Consider additional analyses, such as identifying temperature trends over time or correlating temperature changes with environmental factors.

---

This documentation provides an overview of the **WildfirePrediction** project structure, goals, and methods. It can serve as a guide for running the project notebooks and understanding the steps required to replicate the analyses and visualizations.
