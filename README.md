# Data access and time-series statistics cyberseminar

Repo for "Data access and time-series statistics" [WaterHackWeek](https://waterhackweek.github.io) cyberseminar. This seminar took place on February 7, 2019. The seminar series, including abstracts and links to seminar recordings, is available at https://www.cuahsi.org/education/cyberseminars/waterhackweek-cyberseminar-series/

Launch on [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/waterhackweek/tsdata_access/master) to run and explore the Jupyter notebooks.

## Conda environment and Jupyter

First make sure the `miniconda` or `anaconda` [conda](https://docs.conda.io/projects/conda/en/latest/) version is installed. See instructions below for [miniconda](https://docs.conda.io/en/latest/miniconda.html). See below for installation instructions.

To install the conda environment used for running the Jupyter notebooks in this seminar, change to the directory where the [environment.yml](environment.yml) file is found, downloaded from this GitHub repository (or based on a git clone). Then, at the terminal, run:
```bash
conda env create -f environment.yml
```
An environment called `whwtimeseries` will be created. Note that this environment doesn't include Jupyter. It assumes you are running Jupyterlab (or jupyter notebook) using a different conda environment where Jupyterlab is installed.

### Install miniconda and setup jupyter lab

Steps taken from https://geohackweek.github.io/preliminary/01-conda-tutorial/
Instructions for MacOSX and Windows are also available there.

**On linux:**
```bash
# Install miniconda
url=https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
wget $url -O miniconda.sh
bash miniconda.sh -b -p $HOME/miniconda
export PATH="$HOME/miniconda/bin:$PATH"
conda update conda --yes

# Create a conda environment with jupyterlab
conda create -n jupyterlab -c conda-forge python=3.6 jupyterlab nb_conda_kernels

# Starting jupyter lab
source activate jupyterlab
# Then run jupyter lab
jupyter lab
```
