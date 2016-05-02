# Jupyter Profiles

If you want to have different IPython (Jupyter) behavior depending on profile, create a new profile with:

```bash
JUPYTER_CONFIG_DIR=~/.jupyter-nbserver jupyter notebook --generate-config
```

Remember you are temporarily changing the `JUPYTER_CONFIG_DIR` for one command only. Now, to run w/ that profile: 

```bash
JUPYTER_CONFIG_DIR=~/.jupyter-nbserver jupyter notebook
```

And if you want this to be a bash alias add this to your `.bashrc`: 

```bash
alias jupyter-nbserver='JUPYTER_CONFIG_DIR=~/.jupyter-nbserver jupyter notebook'
```

Source: http://stackoverflow.com/questions/32320836/how-do-i-get-ipython-profile-behavior-from-jupyter-4-x
