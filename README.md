Disaggregation
==============

[![Build Status](https://travis-ci.org/aknandi/disaggregation.svg)](https://travis-ci.org/aknandi/disaggregation)
[![codecov.io](https://codecov.io/github/aknandi/disaggregation/coverage.svg?branch=master)](https://codecov.io/github/aknandi/disaggregation?branch=master)

A package containing useful functions for disaggregation modelling

Installation
------------

```R
devtools::install_github('aknandi/disaggregation')
```

Inputs 
-------

Required
* A RasterStack of covariate rasters to be used in the model
* A SpatialPolygonsDataFrame containing the response count data (for binomial data it can also contain sample size) 

Optional
* Raster used to aggregate the pixel level predictions to polygon level (usually population)

Overview
--------

## Data preparation

### Extract

Functions to get covariate rasters, extract covariate data and setup polygon data to be used in model


### Matching

Function to match which pixels are contained within a given polygon


### Build mesh

Function to build INLA mesh

### Prepare data

Function takes in SpatialPolygonDataFrame (response) and RasterStack (covariates) to produce a data structure required for the disaggregation modelling. Calls functions from extract, matching and build_mesh

## Model fitting

### Fit model

Function takes data structure returned by prepare_data and fits a TMB disaggregation model

## Model prediction

### Predict model

Function takes data structure returned by prepare_data and fit_model to predict model results

## Plotting

Plotting functions for input data, model results and predictions

