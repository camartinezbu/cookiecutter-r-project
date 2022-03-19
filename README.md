# cookiecutter-r-template

A template for R projects made using cookiecutter.

## Structure

    .
    ├── LICENSE
    ├── .Rprofile
    ├── .gitignore
    ├── README.md
    ├── analysis
    │   └── notebooks
    ├── data
    │   ├── external
    │   ├── interim
    │   ├── processed
    │   └── raw
    ├── etl
    ├── reports
    ├── references
    ├── viz
    │   └── figures
    └── {{cookiecutter.project_slug}}.Rproj

- `LICENSE`
  - License file for the project.
  - Availiable options include MIT and BSD-3-Clause.
- `.Rprofile`
  - Stores environment variables for local R projects.
- `.gitignore`
  - Ignores R user profile temporary files.
- `README.md`
  - Project specific readme.
- `analysis`
  - R code that involves analysis on already-cleaned data. Code for cleaning data should go in `etl`.
  - Multiple analysis files are numbered sequentially.
    - `analysis/notebooks`
      - Any R Markdown files go here.
- `data`
  - This is the directory used to store all of the project's data. All files should go into one of the following folders.
  - `data/external`
    - Data from third party sources.
  - `data/interim`
    - Intermediate data that has been transformed.
  - `data/processed`
    - The final, canonical data sets for analysis.
  - `data/raw`
    - The original, inmutable data dump.
- `etl`
  - ETL (extract, transform, load) scripts for reading in source data, cleaning and standardizing it to prepare for analysis go here.
    - Multiple ETL files are numbered sequentially.
    - Joins are included in ETL process.
- `reports`
  - Generated analysis as HTML, PDF, LaTeX, etc.
- `references`
  - Data dictionaries, manuals, and all other exploratory materials.
- `viz`
  - Graphics and visualization development specific work should go here.
    - Multiple viz files are numbered sequentially.
  - `viz/figures`
    - Generated graphics and figures to be used in reporting.
- `{{cookiecutter.project_slug}}.Rproj`
  - This is the .Rproj file that can be used with RStudio to work within the project.

## Installation

In the folder where you want to generate the project, run:

```shell
cookiecutter https://github.com/camartinezbu/cookiecutter-r-project
```

## Credits

This template was designed based on [jvelesmagic's Cookiecutter Conda Data Science](https://github.com/jvelezmagic/cookiecutter-conda-data-science) and [AP's R Cookicutter](https://github.com/associatedpress/cookiecutter-r-project).

## Extra

Check out a similar template for python [here](https://github.com/camartinezbu/cookiecutter-python-project).