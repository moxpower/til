# Using seaborn color palettes

The fantastic [`seaborn`](https://stanford.edu/~mwaskom/software/seaborn) wrapper around `matplotlib` has great documentation.

The color palette functionality is described [here](https://stanford.edu/~mwaskom/software/seaborn/tutorial/aesthetics.html), and it doesn't tell you how to actually go from palette to color (on a 0-1 scale, for example). 

```python
import seaborn as sns

cmap = sns.light_palette('navy', as_cmap=True)
```

When doing some plot: 

```python
fig, ax = plt.subplots()
for threshold in np.linspace(0.3, .9):
    plt.plot(x, y, c=cmap(threshold))
ax.legend(loc='best')    
fig.tight_layout()
```


https://stanford.edu/~mwaskom/software/seaborn
