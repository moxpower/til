# Install Jupyterhub on CentOS

First, install [miniconda](../conda/install-miniconda.md) and create a `python3` conda environment named `py3`.

```bash
conda create --name py3 python=3 jupyter notebook matplotlib seaborn pandas numpy scipy scikit-learn
```



```bash
# This relies on creating a conda environment called py3 first
source activate py3
sudo yum install epel-release
sudo yum install nodejs npm
sudo npm install -g configurable-http-proxy
pip install jupyterhub
jupyterhub --generate-config
```
