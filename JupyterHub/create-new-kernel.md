# Add kernel available to all JupyterHub users

Example w/ an environment `harrison`


```bash
# might have to do from root?

conda create -n harrison python=2 jupyter notebook 
source activate harrison
ipython kernel install --display-name harrison --name harrison

# untested
# if you only want the kernel for yourself
ipython kernel install --display-name harrison --name harrison --self
```


