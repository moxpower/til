# Turn off Notebook caching

If the output of some cells is large, it can help clear up some memory if the results aren't cached. This sets the `cache_size` to zero. 

```bash
ipython profile create default
```

Next, edit: `~/.ipython/profile_default/ipython_config.py`

change this line:

    # c.InteractiveShell.cache_size = 1000

to:

    c.InteractiveShell.cache_size = 0
