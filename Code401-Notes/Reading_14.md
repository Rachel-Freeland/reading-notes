# Data Visualization

## Reading

- [Matplotlib Tutorial](https://github.com/rougier/matplotlib-tutorial)

- Probably the most used package in Python for 2D graphics
- Of note: Pyplot which we have been working with has a PyPlot tutorial [here](https://matplotlib.org/2.0.2/users/pyplot_tutorial.html)

- Forked from GitHub

## Bookmark & Review

- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)
- [Bokeh Tutorial](https://notebooks.gesis.org/binder/jupyter/user/bokeh-bokeh-notebooks-yllsdysh/notebooks/tutorial/00%20-%20Introduction%20and%20Setup.ipynb)

- Seaborn is good for plotting functions
  - Figure-level vs Axes-level Functions:
        - Figure-level plotting puts the legend is placed outside of the plot
        - Figure-level functions wrap their axes-level counterparts and pass the kind-specific arguments down to the underlying function
            - Figure-level function Pros:
                1. Easy faceting by data variables
                2. Legend is outside the plot
                3. Easy figure-level customization
                4. Different figure size paramaterization
            - Figure-level function Cons:
                1. Many parameters not in the function signature
                2. Cannot be part of a larger matplotlib figure
                3. Different API from matplotlib
                4. Different figure size parameterization
        - Axes-level functions act like drop-in replacements for matplotlib functions
        - Axes-level functions call the matplotlib function internally. This hooks into the matplotlib state-machine so that the plots are drawn on their "currently-active" axis.

- Bokeh is an interactive visualiztion library. It is good for things like;
  - Interactive visualization in today's browsers
  - Standalone HTML docs or server-backed apps
  - Expressive and versatile graphics
  - Large, dynamic, or streaming data
  - Works easily with Python

### Cheat Sheet

- [Seaborn Cheat Sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf)
