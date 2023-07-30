# WildfirePrediction
Project in Special Problems 
Documentation for CSCE 5900 Special Problems Course Project
Project Overview
The objective of this project is to analyze geospatial data, specifically temperature data, and visualize this data on maps. The data is sourced from netCDF files and shapefiles. The project involves several steps: data loading, data manipulation, data visualization, and the creation of animations.

The project is structured around several Jupyter notebooks, each representing a stage in the data analysis pipeline. The stages are:

Loading geospatial data from netCDF files and shapefiles.
Performing transformations and analyses on the data.
Visualizing the results.
Saving the visualizations as images or animations.
Notebook Descriptions
1. Untitled.ipynb

This notebook loads a shapefile and a netCDF file, and plots the temperature data from the netCDF file on a map using the shapefile as a boundary. It then down-samples the data and plots the down-sampled temperature data.

2. DAYMET(NA)(TMIN)(2000).ipynb

This notebook attempts to load and visualize the Daymet data for minimum temperature overlaid with a shapefile grid. It also attempts to reproject the shapefile to match the CRS of the Daymet data.

3. DAYMET(NA)(TMIN)(2000) (2).ipynb

This notebook does the same as the previous one but provides more detailed comments on the processing steps.

4. dataRemix_tmin.ipynb

This notebook overlays minimum temperature data from a Daymet file on a clipped grid. It provides multiple ways to approach this problem, including using rasterio and geopandas for geospatial operations and matplotlib for visualization.

5. Copy_of_overlay_that_keeps_skipping_every_tif_file_this_keeps_crashing_because_no_ram.ipynb

This notebook overlays multiple TIF files onto a shapefile of North America. It plots the shapefile and then loops through the TIF files, plotting each one at the corresponding longitude and latitude.

6. Breaking_down_the_netCDF_file_into_daily_files.ipynb

This notebook contains a function to split a netCDF file into daily files. The function opens the netCDF file, loops over each day in the dataset, selects the data for the current day, and saves the daily data to a new netCDF file.

7. Combining_the_images_to_create_animation.ipynb

This notebook combines multiple images into a single GIF animation. It loops through a range of days, generates a plot for each day, and saves the plot as an image. It then combines all the images into a GIF animation.

8. idk.ipynb

This notebook contains code for loading a shapefile and a netCDF file, down-sampling the netCDF data, and then plotting the data with a color bar. It also contains a loop that generates a plot for a range of days and saves each plot as an image.

Project Outcomes
This project has provided valuable insights into the manipulation and visualization of geospatial data. The ability to overlay temperature data on a map and create animations of the data over time provides a powerful tool for understanding changes in temperature patterns. The project has also explored techniques for handling large datasets and managing memory usage.

 Usage Guide
Below is a guide on how to use each notebook in the project.

1. Untitled.ipynb

This notebook is the starting point of the project. Load it and run all the cells sequentially. The notebook does not require any specific inputs, and all data paths are specified within the notebook.

2. DAYMET(NA)(TMIN)(2000).ipynb

Load and run all the cells in this notebook. Like the first notebook, it does not require any specific inputs, and all data paths are specified within the notebook.

3. DAYMET(NA)(TMIN)(2000) (2).ipynb

Load and run all the cells in this notebook. It does not require any specific inputs, and all data paths are specified within the notebook.

4. dataRemix_tmin.ipynb

Load and run all the cells in this notebook. It does not require any specific inputs, and all data paths are specified within the notebook.

5. Copy_of_overlay_that_keeps_skipping_every_tif_file_this_keeps_crashing_because_no_ram.ipynb

Load and run all the cells in this notebook. It does not require any specific inputs, and all data paths are specified within the notebook.

6. Breaking_down_the_netCDF_file_into_daily_files.ipynb

Load and run all the cells in this notebook. It does not require any specific inputs, and all data paths are specified within the notebook.

7. Combining_the_images_to_create_animation.ipynb

Load and run all the cells in this notebook. It does not require any specific inputs, and all data paths are specified within the notebook.

8. idk.ipynb

Load and run all the cells in this notebook. It does not require any specific inputs, and all data paths are specified within the notebook.

Troubleshooting
If you encounter a MemoryError while running the notebooks, it is likely due to the large size of the data being processed. If this happens, you may need to adjust the code to process the data in smaller chunks.We might get Memory Error If we want to run all the .nc file because we had low Ram so we need to chunk the Data and then process it ,For this Process we have to use Dusk library and do it . 

Data Documentation
The data used in this project is sourced from netCDF files and shapefiles. The netCDF files contain temperature data, while the shapefiles provide geographical boundaries for visualization.

1. netCDF Files

The netCDF files contain daily minimum temperature data across North America. Each file represents a different day, and the data in each file is organized into latitude and longitude coordinates. Before using this data, we first break down the original netCDF file into individual daily files for easier processing.

2. Shapefiles

The shapefiles provide the geographical boundaries used to visualize the temperature data. We use a shapefile of North America as the base for our visualizations. The shapefile data is used to create a geographical context for the temperature data, allowing us to plot the temperature data on a map.

Code Explanation
The code in this project is primarily written in Python and is organized into several Jupyter notebooks. Each notebook represents a different stage in the data analysis pipeline.

The key Python libraries used in this project are:

netCDF4: Used for reading netCDF files.
geopandas: Used for working with geospatial data, particularly shapefiles.
rasterio: Used for raster processing, particularly overlaying data onto a shapefile.
matplotlib: Used for creating visualizations.
imageio: Used for creating animations from images.
Future Work
Future iterations of this project could focus on improving the efficiency of the data processing pipeline, particularly with regard to memory usage. The current pipeline sometimes encounters MemoryErrors due to the large size of the data being processed. Processing the data in smaller chunks or using more efficient data structures could help mitigate these issues.

Additionally, future work could involve more complex analyses of the temperature data, such as identifying trends over time or correlating temperature changes with other environmental factors.








