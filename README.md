Mixed Beverage Receipts
=============================

This was born from the public [UT Data](https://github.com/utdata/mixbev-receipts/) team, but that one is more geared toward a step by step on using agate, etc.

This repo deals with Mixed Beverage Receipts from the Texas Comptroller. In November 2017, these source data was moved from the comptroller's own data site to [data.texas.gov](https://data.texas.gov/Government-and-Taxes/Mixed-Beverage-Gross-Receipts/naix-2893), which is a Socrata portal.

This new data set is cleaner than previous, and has more data points to play with.

## Reconfiguration

I'll reconfigure this repo to use the new data source, but will do so in phases.
- First I'll make an analysis possible through downloading from the new source. I actually worked this out in the utdata repo, but will transfer here.
- Then we need to figure out how to use the Socrata API to pull the data.

There will be quite a bit of rearranging and deleting of files and such, since the data is more accessible now.

## Setup

I use the `conda` virtual environment. (Note: If you are using a different virtual environment, you can use mixbev-pip.txt  as a requirements file.)

This should only have to be done once on your machine. Assumes you are on Mac, but this should work with Windows.

### Install conda
- install [conda](https://conda.io/docs/download.html) or [miniconda](https://conda.io/miniconda.html) for Python 3.x
- run `conda update conda` to make sure it is up-to-date

### Create and configure the environment
- run `conda create -n mixbev --file mixbev-env.txt` to create the mixbev environment that has the pyton packages you need
- run `source activate mixbev` to load the environment so we can add the `agate` package that is not in conda.
- run `pip install agate` to install the [agate](http://agate.readthedocs.io/) package

## Updating monthly numbers

- `cd` into the `mixbev-receipts`
- run `source activate mixbev` to enter the virtual environment
- run `jupyter notebook` to start the notebook
- Your browser will open[jupyter](http://localhost:8888/tree)
- Go inside the `notebooks` directory and choose `Mixed-beverages-agate.ipynb` 

The rest of the directions are in the **Mixed beverages monthly update** notebook.
