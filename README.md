# dtsa5301-nypd
CU Boulder MSDS Data Science as a Field (DTSA 5301) NYPD Shooting Incidents Project

## Assignment Information

This repository contains my (Trey Hendrix's) DTSA 5301 module 3 and 5 assignments related to the NYPD shootings dataset. The knit `NYPD_Shooting_Report_v01_260307.html` file is for module 3's "Peer-graded Assignment: NYPD Shooting Incident Data Report", and the reproducible `NYPD_Shooting_Report_v01_260307.Rmd` file is for module 5's "Peer-graded Assignment: DTSA 5301: Data Science as a Field Final Projects" part 1. 

## Reproducibility and Environment Setup

As Dr. Wall suggested, I include a list of all R packages used as the second cell of my `NYPD_Shooting_Report_v01_260307.Rmd` file. Additionally, the last cell of the document calls `sessionInfo()`, which lists the exact versions of all packages used. 

As an alternative to this approach, I also use [`renv`](https://rstudio.github.io/renv/articles/renv.html) to ensure package version consistency and create a reproducible R environment. While `sessionInfo()` is passive (it tells you whan packages you need and leaves it up to you to install them), `renv` is active and will set up an isolated, exact reproduction of my R environment on your machine. Specifically, `renv` will install packages into a project-specific library and, thus, will not interfere with your global R library or other R projects. To set up the environment locally:

### 1. Clone the Repository

Open your terminal and run to clone this repository to your current working directory:

```bash
git clone https://github.com/treyhendrix/dtsa5301-nypd.git
```

Alternatively, you can clone the repo to a specific location (e.g., your Downloads folder where it will be easy to delete later).

```bash
# Replace <target-folder-name> with an actual filepath, e.g., ~/Downloads/temp_nypd_repo
git clone https://github.com/treyhendrix/dtsa5301-nypd.git <target-folder-name>
```

### 2. Open the Project 

Open the `dtsa5301-nypd.Rproj` file in RStudio. This will automatically trigger `renv` to bootstrap itself using the included `renv/activate.R` script.

### 3. Restore the Library

In the R console, run the following command to download and install all required packages as specified in the `renv.lock` file:

```r
renv::restore()
```

### 4. Run the Analysis 

You can now knit the `NYPD_Shooting_Report_v01_260307.Rmd` file with the confidence that you are using the exact package versions used during development and that no environment-setup-related errors will occur.