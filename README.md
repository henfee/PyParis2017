# PyParis2017
Repo for a talk on Jupyter nbextensions at PyParis 2017

The `JupExtensions_talk.ipynb` was used during a talk at [PyParis 2017](http://pyparis.org/). In order to fully reproduce what was done there, 

1. you should have a working installation of the  [jupyter_contrib](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) notebook extensions. See [here](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) for installation instructions. Using pip, it should be as easy as
```
pip install https://github.com/ipython-contrib/jupyter_contrib_nbextensions/tarball/master
```
and then 
```
jupyter contrib nbextension install --user
``` 
(or `--system` to install system wide). The, you should enable at least `highlighter`, `latex_envs`

2. You need to have a copy of the following repo and a demo nbextension `toggleCase` installed: do this by
    - install the demo nbextension by 
    ```
    jupyter nbextension install https://rawgit.com/jfbercher/small_nbextensions/master/toggleCase.zip --user
    ```
    - download https://github.com/jfbercher/PyParis2017/raw/master/JupNbextensions.zip, unzip, change to PyParis2017 directory and \underline{run jupyter notebook from that directory} (this preserve links) -- alternatively, you can just git clone this repo.
    
3. Displaying correcly the present notebook needs the [jupyter_latex_envs](https://pypi.python.org/pypi/jupyter_latex_envs) nbextension to be installed and enabled; is it not a strong requirement though.

- Unfortunately, during the talk, the demo for `python-markdown` failed. This was due to the fact that this extension needs the notebook to be *trusted* (by pressing a menu button on the upper right)
