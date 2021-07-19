# fly2p

Tools for analyzing two-photon (2p) imaging data collected with [Vidrio Scanimage software](https://vidriotechnologies.com/scanimage/). Relies on [scanimageReader](https://pypi.org/project/scanimage-tiff-reader/), which can be installed via 'pip install scanimage-tiff-reader'. Other dependencies are tracked using poetry.

I'm also working on expanding this codebased to work with imaging data collected with micromanger. 

### Organization:
The fly2p package contains the following submodules:
* **preproc**: Some file-format specific functions that extract metadata and load the imaging data. imgPreproc.py defines a data object to hold metadata and imaging data as well as basic proporcessing functions.
* **viz**: A collection of utility functions related to plotting flourescence traces and images.

In addition, the **scripts** folder contains notebooks that illustrate how to use functions in this module based on example files in **sample** (sample files are not currently pushed to repo).


### Install:
I recommend using poetry to setup a custom conda environment. A helpful introduction can be found [here](https://ealizadeh.com/blog/guide-to-python-env-pkg-dependency-using-conda-poetry).

0. Clone repo, navigate into folder
1. If you don't already have poetry, [install poetry](https://python-poetry.org/docs/#installation). You may need to close command window and open a new one.
2. Create conda environment:  
 `conda create --name unityvr python=3.8`
4. Activate environment:  
 `conda activate unityvr`
6. Make sure you are in the top folder of the cloned repo, then install dependencies:  
 `poetry install`
8. Setup the new environment as an ipython kernel:  
    `conda install -c anaconda ipykernel`  
    then  
    `python -m ipykernel install --user --name=unityvr`
    
Now you should be able to run the example notebooks in the **scripts** folder without problems.
