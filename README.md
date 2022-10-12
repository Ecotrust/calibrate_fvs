Calibrate FVS
==============================

This repo contains data processing and modeling workflows to calibrate the 
Forest Vegetation Simulator (FVS) against repeated measurements of trees in the
USFS Forest Inventory & Assessment (FIA) databases. 

The approach we take in this project is to utilize FVS keywords to modify 
predictions of tree growth and mortality by FVS at runtime to better fit the 
observations of growth and mortality recorded on repeatedly-measured FIA plots. 

This keyword calibration task treated as a black-box optimization problem. It 
does not involve re-fitting underlying equations and routines in FVS source code.
The optimization process seeks to find parameters to FVS growth- and mortality-
modifying keywords (e.g., FIXDG, MORTMULT, SDIMAX) that minimize the deviation 
of FVS predictions of growth and mortality observed on FIA plots.

Our intent is to develop this workflow using a publicly-available dataset while
enabling transferability of these tools and methods to calibrate FVS against 
other forest inventory datasets (e.g., Continuous Forest Inventory and other 
permanent plot systems).


Project Organization
------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- Finalized data sets ready for modeling.
    │   └── raw            <- Extracted data ready to be transformed.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── notebooks          <- Jupyter notebooks.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analyses.
    │   └── figures        <- Generated graphics and figures to be used in reporting.
    │
    ├── environment.yml   <- The requirements file for reproducing the analysis environment
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    │
    └── src                <- Source code for use in this project.

--------

<p><small>Repository structure based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
