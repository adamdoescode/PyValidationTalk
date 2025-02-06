# pd.read_csv is NOT all you need: DataFrame validation in Python

Notes and code for my Python DataFrame Validation talk.

## Outline

This talk aims to describe:
- That you need to be dealing with your messy inconsistent data
- You should use data validation to handle your data
- And validation should occur before you do any processing + analysis
- We focus on validation of *dataframes* i.e. table objects in `Python`
- We present several approaches of varying quality and effectiveness

The talk is composed of two parts:
- A slide deck of introductions and concepts (see: `reports/slides.md`)
- And a demonstration notebook of various strategies (see: `notebooks/demo.ipynb`)

## Getting Started

To follow along with this on your own machine:
1. `git clone` the entire repo:
```
git clone https://github.com/adamdoescode/PyValidationTalk
```
2. make the conda environment from the `environment.yml`:
```
cd PyValidationTalk/
make create_environment
```
3. activate the environment:
```
conda activate PyValidationTalk
```

You should now be able to run the demo.ipynb notebook!


## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   └── generated      <- Data generated as part of this talk
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── notebooks          <- Jupyter notebooks.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         PyVal and configuration for tools like black
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── environment.yml    <- The requirements file for reproducing the analysis environment, e.g.
│
├── setup.cfg          <- Configuration file for flake8
│
└── PyVal   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes PyVal a Python module
    │
    └── config.py               <- Store useful variables and configuration
```

--------

