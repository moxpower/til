# Install Miniconda

Your first stop should obviously be: http://conda.pydata.org/miniconda.html. 

## OS X

```bash
cd ~/Downloads
wget https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh

# Lots of license agreements to read and agree to

#Update your .bashrc
source ~/.bashrc

conda update conda -y
```

## Create new conda environment

```bash
# choose a python version and descriptive name
conda create --name descriptive_name3 python=3 jupyter matplotlib pandas 

source activate descriptive_name3

# Do things with this environment

# End it with
source deactivate
```
