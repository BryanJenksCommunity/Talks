# Data Driven CV

## Required Tech

- [RStudio](https://www.rstudio.com/products/rstudio/download/#download)
- The packages needed by running this command:

```r
install.packages('xfun')
pkgs <- c('vitae' ,'here' ,'tinytex' ,'tibble' ,'glue' ,'rmarkdown' ,'dplyr', 'readr' ,'yaml')
xfun::pkg_attach2(pkgs)
```

- The template repository [HERE](https://github.com/BryanJenksCommunity/Talks)
    - you're looking to get the `CV` directory and files in the `2021-04-17-FCC-CV-Workshop` directory

## Technology used in this project

- LaTeX
- R
- YAML
- Markdown
- csv

## The goal

> The goal of this project is to have a data driven CV i.e. a resume that can have data added and requires no formatting work. Just add new data and the resume is re-rendered.

## Concepts covered

- YAML metadata
- Template Literals
- Row Wise data frames
- VERY basic LaTeX commands and what a `.cls` file is and what even in LaTeX
- RMarkdown / RStudio / Pandoc

