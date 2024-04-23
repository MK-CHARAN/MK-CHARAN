Open Source Geoprocessing Tutorial
==================================

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">
<img
    alt="Creative Commons License"
    style="border-width:0"
    src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" />
</a><br />
<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title"></a>

Tutorial of basic remote sensing and GIS methodologies using modern open source
software in Python (`rasterio`, `shapely`, `geopandas`, `folium`, etc). Notebooks cover raster processing, vector analysis, cloud-based tools like Google Earth Engine, a workflow to perform image classification using machine learning classifiers in `scikit-learn`, and an introduction to handling large array datasets with `xarray`:

# Repo Structure 

All chapters are available as jupyter notebooks in the `notebooks/` directory or viewable via a normal web browser in HTML:

0. Introduction
   [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_0_introduction.html)]
1. The GDAL datatypes and objects
   [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_1_rasterio.html)]
2. Your first vegetation index
   [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_2_indices.html)]
3. Visualizing data
   [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_3_visualization.html)]
4. Vector data - the OGR library
   [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_4_vector.html)]
5. Land cover classification
   [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_5_classification.html)]
6. Deep Learning for land cover classification [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_6_neural_networks.html)] built to run in [Google Colab](https://colab.research.google.com/github/patrickcgray/open-geo-tutorial/blob/master/notebooks/chapter_6_neural_networks.ipynb).

7. Earth Engine for Oceanographic Time Series Analysis [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_7_earth_engine_oceanography.html)]
8. Xarray for handling N-dimensional arrays and advanced visualization with hvplot  [[HTML](http://patrickgray.me/open-geo-tutorial/chapter_8_xarray_netcdfs.html)]

### Some of the things you'll learn:

#### Raster Operations, Processing, and Visualization
<img src="data/raster_viz.png" width="500">

#### Interactive Shapefile and Raster Visualization
 <img src="data/folium_exp.png" width="500">

#### Machine Learning based Satellite Image Classification
<img src="data/ml_exp.png" width="750">

#### Dealing with large datasets and interactive analysis
<img src="data/chla_xarray.png" width="650">

# Setup

## Locally

### Download

Materials for these lessons are included inside this repository under
the `notebooks/` directory. If you're not running in Binder I would recommend downloading all of the lesson material
at once, instead of downloading individual files.

* Use `git clone https://github.com/patrickcgray/open-geo-tutorial.git` to clone the repository
    * [More Instructions](https://help.github.com/articles/cloning-a-repository/)

### Python Installation

To run the Jupyter Notebooks (formerly known as IPython Notebooks) and follow the tutorial locally, you will need to install Python and the libraries used in the tutorials. This installation can be accomplished in many ways, but I recommend Docker:

#### Docker

I highly recommend trying out [Docker](https://docs.docker.com/get-started/) if you're not familiar with it. There is a bit of a startup time just for getting up to speed but it is the way to go for reproducible work and cloud deployable workflows. Docker provides operating-system-level virtualization, also known as "containerization" and thus you can be sure that your setup precisely replicates the one used here and will easily run everything. Once you've downloaded Docker you can simply cd into the cloned git repo and run: 

`docker run -it --rm -p 8888:8888 -v <path to repo>:/home/jovyan/repo/ pangeo/pangeo-notebook:2021.05.15 jupyter lab --ip 0.0.0.0`

This will download the Docker image that is needed to run this whole repo and then it will start up a Jupyter Lab instance that you can access by clicking the link in the terminal. Just change `<path to repo>` to the appropriate path and you'll be good to go!

# Thanks

patrick gray for the source material: https://github.com/patrickcgray
