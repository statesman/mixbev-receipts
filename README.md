Mixed Beverage Receipts Lesson
=============================

This is a fork from the public [UT Data](https://github.com/utdata/mixbev-receipts/) team, but that one is more geared toward a step by step on using agate, etc.

This one is configured to process and publish the updated data.

It uses a `conda` virtual environment.

(Note: If you are using a different virtual environment, you can use mixbev-pip.txt as a requirements file.)

## Setup
This should only have to be done once on your machine. Assumes you are on Mac, but this should work with Windows.

### Install conda
- install [conda](https://conda.io/docs/download.html) or [miniconda](https://conda.io/miniconda.html) for Python 3.6
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
