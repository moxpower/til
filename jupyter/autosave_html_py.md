# Autosave .html and .py versions for Jupyter Notebook

The Jupyter config files are stored in `~/.jupyter` by default. This directory is the `JUPYTER_CONFIG_DIR` environment variable, and the config file is found at: `~/.jupyter/jupyter_notebook_config.py`

Don’t have this file? 

```bash
# Create config file
jupyter notebook --generate-config 
```

Add the following text to the top of the file:

    c = get_config()
    ### If you want to auto-save .html and .py versions of your notebook:
    # modified from: https://github.com/ipython/ipython/issues/8009
    import os
    from subprocess import check_call

    def post_save(model, os_path, contents_manager):
        """post-save hook for converting notebooks to .py scripts"""
        if model['type'] != 'notebook':
            return # only do this for notebooks
        d, fname = os.path.split(os_path)
        check_call(['jupyter', 'nbconvert', '--to', 'script', fname], cwd=d)
        check_call(['jupyter', 'nbconvert', '--to', 'html', fname], cwd=d)

Now, everytime that you hit save while working in your Jupyter notebook, it will write/overwrite an identically named .html and .py version. 

Sources: 
 - http://www.svds.com/jupyter-notebook-best-practices-for-data-science/
 - http://stackoverflow.com/a/32516200/246856
