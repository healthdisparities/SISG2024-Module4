## Computational prerequisites for Module 4
We expect attendes to have a Linux, Mac, or Windows based systems. The datasets used (present in the Data/ path) in the course will be small enough so that students can complete all analyses on their laptops.

### 1. Platform requirements
All of the quantitative and statistical analyses for SISG2024-Module4 will be performed in R coding language powered by [Jupyter Lab](https://jupyter.org/) (a web-based interactive development environment for notebooks, code, and data). 


### 2. Installing Jupyter Lab
 Use either 2.1 or 2.2 to get set up with Jupyter Lab. Once that is set up, go to 2.3 and get set up with IRKernel in your Jupyter Lab.
 
 2.1 **Approach 1** Direct installation instructions can be found on the [Jupyter Lab website](https://jupyter.org/install)
   + Mac or Linux systems:
      + pip based installation might be the easiest using `pip install jupyterlab`
      + If on Mac, homebrew solution also works well `brew install jupyterlab`
   + Windows system
     + Windows x64 installer file can be obtained from [here](https://github.com/jupyterlab/jupyterlab-desktop?tab=readme-ov-file#installation)
     + Windows system might run into unexpected errors; [this website](https://crib.utwente.nl/manual/pages/jupyterlab-install-guide/index.html) offers a nice & guided step-by-step process for installation.
  + If you have Jupyter Lab running, please got to step 2.3 to get IRKernel set up. 

 2.2 **Approach 2** Conda is another friendly way of getting things up and running
   The easiest way to get *Conda* set up on your systems is by getting [Miniconda]() set up on your systems. Installations will differ depending on your systems. 
   
   + <img width="500" alt="Screenshot 2024-05-29 at 1 43 47 PM" src="https://github.com/healthdisparities/SISG2024-Module4/assets/14136915/8c569b90-bbf4-430b-a900-0d5abcae3f0c">

   + Using the following commands on terminal (Mac/Windows/Linux), you should be able to install Miniconda on your system.
     ```
     curl -o Miniconda3-latest-MacOSX-arm64.sh 'https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh'
     bash Miniconda3-latest-MacOSX-arm64.sh
     ```
     Follow along with the process, and feel free to ask a TA for any help. Once you have conda set up, you can duplicate the following environment to get set up.


   + Please look at the [Conda Specification File](CondaEnvironment.txt) and use the command `conda create --name sisg-module4 --file CondaEnvironment.txt` followed by `conda activate sisg-module4`
      + From here, you can run Jupyter Lab using the command `jupyter lab` in your terminal.
        
 2.3 Getting R kernel set up
   + By default, jupyter lab comes with a Python kernel and not the R kernel. We need to get an R kernel set up in our Jupyter Lab
   + Open R session inside the conda environment. You can open a terminal in Jupyter Lab and type `R` there.
   + Run the following commands to get IRKernel set up:
     ```
      install.packages("devtools")
      devtools::install_github("IRkernel/IRkernel")
      IRkernel::installspec()
     ```
 

### 3. R studio packages
   + Devtools will be needed down the lane, so please install that first: `install.packages("devtools")`
   + Core packages can be installed using the following block:
        ```
        install.packages("data.table")
        install.packages("dplyr")
        install.packages('stringr')
        install.packages('ggplot2')
        install.packages("tidyverse")
        install.packages("mediation")
        ```
   + We also plan on using some non-CRAN packages. Please install these as well:
        ```
        devtools::install_github("rdboyes/forester")
        ```

## Additional resources

### 1. Running code in RStudio
We strongly recommend working on Jupyter based engine, nevertheless, the scripts and code will work fine on RStudio IDE
+ R version 4.4 (or higher)<br>
   + Windows installation - https://cran.r-project.org/bin/windows/base/<br>
   + Mac installation - https://cran.r-project.org/bin/macosx/<br>


### 2. Helpful tutorials
+ Installing R kernel on Jupyter Notebooks - https://docs.anaconda.com/free/navigator/tutorials/r-lang/
+ NASA has a nice tutorial for getting R kernel set up in Jupyter Lab - https://www.nas.nasa.gov/hecc/support/kb/how-to-set-up-r-kernel-in-jupyter-lab_685.html

### 3. Troubleshooting
There is a possibility that commands and tutorials might not work successfully on your laptop. In this case, please look around for a TA in the classroom and they would be happy to help you.
