# tsdata_access
Repo for "Data access and time-series statistics" waterhackweek tutorial

## conda environment and jupyter

- The conda environment file `environment.yml` doesn't install jupyter. It assumes you are running jupyterlab using a different conda environment where jupyterlab is installed. We can change this (add jupyter to this conda env) later if we think it'll cause less confusion. To create a conda environment named `whw_tsdata` from this file: `conda env create -n whw_tsdata -f environment.yml`
- We may want to add a couple of packages from Emilio's [geohackweek vector tutorial conda environment file](https://github.com/geohackweek/tutorial_contents/blob/master/vector/environment.yml). Also note that in that file, `jupyter` *is* installed.

### Install miniconda and setup jupyter lab
Steps taken from https://geohackweek.github.io/preliminary/01-conda-tutorial/
Instructions for MacOSX (and Windows?) are also available there.

**On linux:**
```bash
# Install miniconda
url=https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
wget $url -O miniconda.sh
bash miniconda.sh -b -p $HOME/miniconda3
export PATH="$HOME/miniconda3/bin:$PATH"
conda update conda --yes

# Create a conda environment with jupyterlab
conda create -n jupyterlab -c conda-forge python=3.6 jupyterlab nb_conda_kernels

# Starting jupyter lab
conda activate jupyterlab
# If that doesn't work, try source activate jupyterlab
jupyter lab
```


## Other WaterHackWeek resources
- https://waterhackweek.github.io/
- https://www.cuahsi.org/education/cyberseminars/waterhackweek-cyberseminar-series/
