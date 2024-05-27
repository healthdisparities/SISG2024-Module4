# Computational prerequisites for Module 4
We expect attendes to have a Linux, Mac, or Windows based systems. The datasets used (present in the Data/ path) in the course will be small enough so that students can complete all analyses on their laptops.

### 1. Platform requirements
All of the quantitative and statistical analyses for SISG2024-Module4 will be performed in R coding language powered by [Jupyter Lab](https://jupyter.org/) (a web-based interactive development environment for notebooks, code, and data). 


### 2. Installing Jupyter Lab
1. Direct installation instructions can be found on the [Jupyter Lab website](https://jupyter.org/install)
   + Mac or Linux systems:
      + pip based installation might be the easiest using `pip install jupyterlab`
      + If on Mac, homebrew solution also works well `brew install jupyterlab`
   + Windows system
     + Windows x64 installer file can be obtained from [here](https://github.com/jupyterlab/jupyterlab-desktop?tab=readme-ov-file#installation)
     + Windows system might run into unexpected errors; [this website](https://crib.utwente.nl/manual/pages/jupyterlab-install-guide/index.html) offers a nice & guided step-by-step process for installation.

 2. Conda is another friendly way of getting things up and running
   + Please look at the [Conda Specification File](CondaEnvironment.txt) and use the command `conda create --name sisg-module4 --file Conda-Spec-File.txt` followed by `conda activate sisg-module4`
   + From here, you can run jupyter lab using the command `jupyter lab` in your terminal.
 

### 3. Running code in RStudio
We strongly recommend working on Jupyter based engine, nevertheless, the scripts and code will work fine on RStudio IDE
+ R version 4.4 (or higher)<br>
   + Windows installation - https://cran.r-project.org/bin/windows/base/<br>
   + Mac installation - https://cran.r-project.org/bin/macosx/<br>


### 4. R studio packages
   + Devtools will be needed down the lane, so please install that first: `install.packages("devtools")`
   + Core packages can be installed using the following block:
        ```
        install.packages("data.table")
        install.packages("dplyr")
        install.packages('stringr')
        install.packages('ggplot2')
        install.packages("tidyverse")
        ```
   + We also plan on using some non-CRAN packages. Please install these as well:
        ```
        devtools::install_github("rdboyes/forester")
        ```

### 5. Helpful tutorials
+ Installing R kernel on Jupyter Notebooks - https://docs.anaconda.com/free/navigator/tutorials/r-lang/
+ NASA has a nice tutorial for getting R kernel set up in Jupyter Lab - https://www.nas.nasa.gov/hecc/support/kb/how-to-set-up-r-kernel-in-jupyter-lab_685.html
