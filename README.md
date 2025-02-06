# pd.read_csv is NOT all you need: DataFrame validation in Python

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

Notes and code for my Python DataFrame Validation talk.

## Outline

It is a little tricky thinking about how to go about the order of attack...

Goals:
- Convey importance of the problem
- Indicate that this often a *design* problem:
  - you need to have strong assumptions about your data before you write your code
  - otherwise your code becomes unmaintainable
- 


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

