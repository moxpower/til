# Set up nbextensions for single user on JupyterHub

```bash
USERNAME=username

# Switch to root

cd
git clone https://github.com/ipython-contrib/IPython-notebook-extensions.git
cd IPython-notebook-extensions
source activate py3
./setup.py install

# Switch back to user 

cp -r /root/.local/share/jupyter/templates /home/$USERNAME/.local/share/jupyter/templates
cp -r /root/.local/share/jupyter/extensions /home/$USERNAME/.local/share/jupyter/extensions
cp -r /root/.local/share/jupyter/nbextensions /home/$USERNAME/.local/share/jupyter/nbextensions
echo "from jupyter_core.paths import jupyter_config_dir, jupyter_data_dir \n import os.path \n import sys \n \n sys.path.append(os.path.join(jupyter_data_dir(), 'extensions')) \n \n c = get_config() \n \n c.NotebookApp.extra_template_paths = [os.path.join(jupyter_data_dir(), 'templates') ] \n c.NotebookApp.server_extensions = ['nbextensions'] \n" > /root/.jupyter/jupyter_notebook_config.py
cp /root/.jupyter/jupyter_notebook_config.py /home/$USERNAME/.jupyter/jupyter_notebook_config.py
```

Stop/restart server then navigate to: http://192.168.106.106:8000/user/username/nbextensions


