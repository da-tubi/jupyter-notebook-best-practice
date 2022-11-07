# Launching Jupyter Notebooks in an easy way
## Usage
``` shell
bin/lab
```

## Three Highlights
+ **Free** yourself of **Python virtual environment**
+ **Reproducible** because of  the dependencies lock mechanism
+ As **Easy** as `bin/lab` to launch a JupyterLab

## How to change the dependencies
Just change the requirements in [notebooks/BUILD.pants](notebooks/BUILD.pants). 

**Notice** that you have to quit (Ctrl+C) `bin/lab` and generate lockfiles using

```
# just like pip install, it will download the python packages for you
# the difference is that you do not need to manage the python virtual environments

./pants generate-lockfiles
```

and then launch the JupyterLab by `bin/lab` again.


If you want to manage the different set of dependencies and launch different JupyterLab instances in one Git repo, see [jupyterlab-best-practice](https://github.com/da-tubi/jupyterlab-best-practice).
