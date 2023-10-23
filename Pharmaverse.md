---
name: Pharmaverse
topic: Pharmaverse Packages for Clinical Reporting
maintainer: Mike Stackhouse
email: Mike.Stackhouse@atorusresearch.com
version: 2023-10-23
source: https://github.com/pharmaverse/pharmaverse_task-view
---

Analysis of pharmacokinetic (PK) data is concerned with defining the
relationship between the dosing regimen and the body's exposure to drug
as indicated by the concentration time curve to determine a dose. To
analyze PK data, there are three categories of packages within CRAN:
noncompartmental analysis (NCA), modeling (typically using compartmental
analysis), and reporting (typically for NCA).

Pharmacokinetics are often collected during clinical trials of new
drugs. For more information on R packages for clinical trials, see
`r view("ClinicalTrials")`.

# Noncompartmental Analysis (NCA)

NCA is used as method of description of PK with minimal assumptions of
the rates of distribution of the drug through the body. NCA is typically
used to describe the PK of a drug in clinical studies with many samples
per subject on the same and sequential days.

The NCA packages are:

`r pkg("ncappc")`: Performs traditional NCA and simulation-based
posterior predictive checks for a population PK model using NCA metrics.
It targets summarizing data from model-fit or simulated sources.

# Pharmacometric Modeling

Modeling of PK data typically uses compartmental methods which assume
that the drug enters the body either through an intravenous (IV) or
extravascular (often oral or subcutaneous, SC) dose. Packages listed
below are restricted to packages that have specific interest to PK
modeling and not the (many) packages that support modeling that could be
used for PK data. The PK modeling and simulation packages are:

`r pkg("bayesnec")`: A Bayesian No-Effect- Concentration (NEC) Algorithm

# Visualization

`r pkg("nlmeVPC")`: Various visual and numerical diagnosis methods for
the nonlinear mixed effect model, including visual predictive checks,
numerical predictive checks, and coverage plots.

### Links

-   [PKBugs](https://www.mrc-bsu.cam.ac.uk/software/bugs/the-bugs-project-pkbugs/)
-   [WinBUGS](http://winbugs-development.mrc-bsu.cam.ac.uk/)
-   [NONMEM](http://www.iconplc.com/innovation/nonmem/)
-   [STAN](http://mc-stan.org/)
