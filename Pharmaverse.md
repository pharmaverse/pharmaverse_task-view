---
name: Pharmaverse
topic: Pharmaverse Packages for Clinical Reporting
maintainer: Mike Stackhouse
email: Mike.Stackhouse@atorusresearch.com
version: 2023-10-23
source: https://github.com/pharmaverse/pharmaverse_task-view
---

The packages included within the pharmaverse focus on a specific subset of clinical trial activities, specifically on the clinical reporting pipelines used within the pharmaceutical industry. These activities follow specific standards, such as [CDISC Data Standards](https://www.cdisc.org/) and [ICH E3](https://database.ich.org/sites/default/files/E3_Guideline.pdf). The scope of pharmaverse packages ranges from CRF (Case Report Forms - or data collection for a clinical trial) through clinical trial analysis reporting, including formatting of data to match SDTM (Study Data Tabulation Model) and ADaM (Analysis Data Model) standards, and production of TLGs (Tables, Listings, and Graphs). Furthermore, pharmaverse packages help supporting the orchestration activities of clinical trial data analysis through regulatory requirements. 

The scope of the pharmaverse is only a small subset of the larger range of clinical trial activities for with R can be applied. For more information on R packages for clinical trials, see `r view("ClinicalTrials")`.

# Study Data Tabulation Model (SDTM)

SDTM provides a standard for organizing and formatting data to streamline processes in collection, management, analysis and reporting. Implementing SDTM supports data aggregation and warehousing; fosters mining and reuse; facilitates sharing; helps perform due diligence and other important data review activities; and improves the regulatory review and approval process. SDTM is also used in non-clinical data (SEND), medical devices and pharmacogenomics/genetics studies.

SDTM is one of the required standards for data submission to FDA (U.S.) and PMDA (Japan).

The SDTM packages are:

`r pkg("datacutr")`: This package works with tabulation data following an SDTM standard. For ease of processing, the assumption is that supplemental qualifiers have been combined with their parent domain prior to the application of the cut process (sometimes labeled as SDTMv). The user has the flexibility to select the type of cut applied to each SDTM domain (either no cut, patient cut, date cut, or a special DM cut).

# Analysis Data Model (ADaM)

ADaM defines dataset and metadata standards that support:

 - efficient generation, replication, and review of clinical trial statistical analyses, and
 - traceability among analysis results, analysis data, and data represented in the Study Data Tabulation Model (SDTM).
 
ADaM is one of the required standards for data submission to FDA (U.S.) and PMDA (Japan).

The SDTM packages are:

`r pkg("admiral")`: admiral provides an open source, modularized toolbox that enables the pharmaceutical programming community to develop ADaM datasets in R. For admiral and all extension packages, the priority is to provide a simple to adopt toolkit that enables users to produce readable and easily constructable ADaM programs. the guiding principles of admiral are to that all functions should be easy to use, have a clear purpose, be easily locatable within documentation, and be readable following a high degree of consistency throughout the package. 

`r pkg("admiralonco")`: This is an extension package of admiral focusing on oncology disease area specifics.

`r pkg("admiraloptha")`: This is an extension package of admiral focusing on ophthalmology disease area datasets and endpoints.

`r pkg("admiralvaccine")`:  This is an extension package of admiral focusing on vaccine specific domains.

# TLGs

TLGs (tables, listings, and graphs - also known as TLFs/TFLs with F for figures) refer to the packages that take data, and convert then into a human intepretable insight.

There are two relevant stages of TLGs - static TLGs, which as of today are the only type of evidence submitted to regulatory bodies, and interactive TLGs, which are predominantly, but not limited to, shiny apps.

For tables, we recommend the effort from R Consortium - [Tables in Clinical Trials with R](https://rconsortium.github.io/rtrs-wg/) - as a useful read to compare examples from several of the below packages.

## Tables

`r pkg("rtables")`: The rtables R package was designed to create and display complex tables with R. The cells in an rtable may contain any high-dimensional data structure which can then be displayed with cell-specific formatting instructions. Currently, rtables can be outputted in ascii html, and pdf, as well Power Point (via conversion to flextable objects). rtf support is in development and will be in a future release.

`r pkg("Tplyr")`: Tplyr is a traceability minded grammar of data format and summary. It’s designed to simplify the creation of common clinical summaries and help you focus on how you present your data rather than redundant summaries being performed. Furthermore, for every result Tplyr produces, it also produces the metadata necessary to give you traceability from source to summary.

`r pkg("pharmaRTF")`: pharmaRTF was developed to leverage the huxtable R packages to output RTF documents and add other necessary document attributes necessary for clinical reports, including document property options, multi-page displays, and titles/footnotes within teh document headers and footers.

`r pkg("tfrmt")`: The tfrmt package provides a language for defining display-related metadata, which can then be used to automate and easily update output formats. What makes tfrmt unique is that it offers an intuitive interface for defining and layering standard or custom formats that are often specific to clinical trials. It also offers the novel ability to easily generate mock displays using metadata that will be used for the actual displays. tfrmt is built on top of the powerful gt package, which is intended to support a variety of output formats in the future.

`r pkg("tidytlg")`: The goal of tidytlg is to generate table, listings, and graphs (TLG) using Tidyverse. This can be achieved multiple ways with this package, including functional methods by building a custom script for each TLG, and metadata methods by building a generic script that utilizes column and table metadata to produce each TLG result.

## Plots

`r pkg("visR")`: The goal of visR is to enable fit-for-purpose, reusable clinical and medical research focused visualizations and tables with sensible defaults and based on sound graphical principles. By using a common package for visualising data analysis results in the clinical development process, visR wants to have a positive influence on the choice of visualisation by making it easy explore different visualisation and to use impactful visualisations fit-for-purpose,and effective visual communication by making it easy to implement best practices.

`r pkg("ggsurvfit")`: The ggsurvfit package eases the creation of time-to-event (aka survival) summary figures with ggplot2. The concise and modular code creates images that are ready for publication or sharing. Competing risks cumulative incidence is also supported via ggcuminc().

## Interactive

`r pkg("tidyCDISC")`: One of tidyCDISC’s goals is to develop clinical tables that meet table standards leveraged for submission filings, called "standard analyses". The primary purpose of the app is to provide rich exploratory capabilities for clinical studies. High-level features of the app allow users to produce customized tables using a point-and-click interface, examine trends in patient populations with dynamic figures, and supply visualizations that narrow in on a single patient profile.

`r pkg("rhino")`: Rhino allows you to apply best software engineering practices, modularize your code, test it well, make the UI beautiful, and think about user adoption from the very beginning. Rhino is an opinionated framework with a focus on software engineering practices and development tools.

## Frameworks

`r pkg("tern")`: The tern R package contains analysis functions to create tables and graphs used for clinical trial reporting. The package provides a large range of functionality, for example, data visualizations including forest plots, line plots, Kaplan-Meier plots and more. Statistical model fits, including logistic regression, Cox regression, and more. Additionally, summary tables calculating unique patients, exposure across patients, change from baseline for parements, and more. 


# eSUB (Electronic Submissions)

There are several activities required for regulatory submissions that have highly specific requirements. For example, the FDA has guidance like the [eCTD (Common Technical Document)](https://www.fda.gov/drugs/electronic-regulatory-submission-and-review/electronic-common-technical-document-ectd) and the [Study Data Technical Conformance Guide](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/study-data-technical-conformance-guide-technical-specifications-document). The following pharmaverse packages focus on easing conforming to these requirements:

`r pkg("xportr")`: xportr is designed xportr to help get your xpt files ready for transport either to a clinical data set validator application or to a regulatory agency. This package has the functionality to associate metadata information to a local R data frame, perform data set level validation checks and convert into a [transport v5 file (xpt)](https://documentation.sas.com/doc/en/pgmsascdc/9.4_3.5/movefile/n1xbwdre0giahfn11c99yjkpi2yb.htm). xportr is built on top of the haven R package to generate the version 5 transport files. 

`r pkg("pkglite")`: pkglite offers a solution for converting R package source code to a compact, text-based representation and restore the source package structure from the representation. There are three specific aims: To provide a tool for packing and restoring R packages as plain text assets that are easy to store, transfer, and review. To provide a grammar for specifying the file packing scope that is functional, precise, and extendable. To provide a standard for exchanging the packed asset that is unambiguous, human-friendly, and machine-readable.

# Metadata 

Metadata is a heavy focus of clinical reporting, as dataset documentation must provide traceability for all variables provided within a regulatory submission. Pharmaverse packages focusing on metadata include: 

`r pkg("metacore")`: The purpose of metacore is to establish a common foundation for the use of metadata within an R session. This is done by creating an R object that can hold the necessary data in a standardized, immutable structure (using R6) that makes it easy to extract out necessary information when needed. Users can read in their metadata from their various sources. 

`r pkg("metatools")`: The goal of metatools is to enable the use of metacore objects. Metatools can be used to build datasets or enhance columns in existing datasets as well as checking datasets against the metadata in metacore.

## Utility

Several activities in clinical reporting go beyond the analysis, and focus on enabling repeatable workflows, assuring data quality, and providing traceability of program execution. The following packages assist with these activities:

`r pkg("logrx")`: The goal of {logrx} is to facilitate logging in a clinical environment with the goal of making code easily traceable and reproducible.

`r pkg("diffdf")`: The diffdf package is designed to enable detailed comparison of two data.frames. Whilst many packages exist for informing you if there are differences between data.frames, none provide as much detail on what and where those differences are as diffdf does. Currently, diffdf supports checking for differences in values, attributes, classes, column names, number of observations. Additionally, it checks matching rows by key/id variables, fuzz comparisons (i.e. treating dobules and integers as the same), and extracting datasets of different rows. 

# Developers

Pharmaverse also includes packages focused on developer activities, such as package validation, risk assessment, synthetic data, and more. The following packages support these activities:

## Package Validation

`r pkg("valtools")`: valtools helps automate the validation of R packages used in clinical research and drug development: It provides useful templates and helper functions for tasks that arise during project set up and development of the validation framework.

`r pkg("riskmetric")`: The risk of using an R package is evaluated based on a number of metrics meant to evaluate development best practices, code documentation, community engagement and development sustainability. We hope to provide a framework to quantify risk by assessing these metrics. This package serves as a starting point for exploring the heterogeneity of code quality, and begin a broader conversation about the validation of R packages. Primarily, this effort aims to provide some context for validation within regulated industries.

## Synthetic Data

`r pkg("pharmaversesdtm")`: Test data (SDTM) for the pharmaverse family of packages The purpose is to provide a one-stop-shop for SDTM test data in the pharmaverse family of packages. This includes datasets that are therapeutic area (TA)-agnostic (DM, VS, EG, etc.) as well TA-specific ones (RS, TR, OE, etc.).

`r pkg("pharmaverseadam")`: Test data (ADaM) for the pharmaverse family of packages. The ADaM contents of this package is automatically populated by a CICD action that executes the admiral, admiralonco, admiralophtha and admiralvaccine templates and saves the resulting datasets here. The ADaM datasets in pharmaverseadam are updated any time the templates are updated in admiral or the source data in pharmaversesdtm is updated.


# Other Useful Packages

There are a number of other useful packages that are not specific to the pharmaverse scope, but are immensely useful for clinical reporting activities. 

## Tables 

`r pkg("flextable")`: Creates tables for HTML, PDF, Microsoft Word and PowerPoint documents from R Markdown

`r pkg("gt")`: Easily generate information-rich, publication-quality tables from R

`r pkg("huxtable")`: An R package to create styled tables in multiple output formats, with a friendly, modern interface.

`r pkg("mmtable2")`: Create and combine tables with a ggplot2/patchwork syntax.

## Graphs

`r pkg("ggplot2")`: ggplot2 is a system for declaratively creating graphics, based on The Grammar of Graphics. You provide the data, tell ggplot2 how to map variables to aesthetics, what graphical primitives to use, and it takes care of the details. While ggplot2 is a lower level, non-pharma specific plotting package. It is universally accepted as the package for graphics, so it is included here and as a non-pharma package. 

`r pkg("virdisLite")`: Colorblind-Friendly Color Maps for R

## Utilities

`r pkg("tidyverse")`: Set of packages with a common API for data manipulation and TLGs (includes dplyr, ggplot2, etc)

`r pkg("lintr")`: Static code analysis for R that checks adherence to a given style, syntax errors and possible semantic issues

`r pkg("styler")`: Pretty-prints R code without changing the user's formatting intent

`r pkg("renv")`: Helps you create reproducible environments for your R projects

# Other Relevant Task Views

Pharmaceutical data analysis is very broad, and there are several important and relevant task views that might prove helpful.

-   [Clinical Trials](https://cran.r-project.org/web/views/ClinicalTrials.html)
-   [Survival](https://cran.r-project.org/web/views/Survival.html)
-   [Bayes](https://cran.r-project.org/web/views/Bayesian.html)
-   [Missing Data](https://cran.r-project.org/web/views/MissingData.html)
-   [Pharmacokinetics](https://cran.r-project.org/web/views/Pharmacokinetics.html)

### Links

-   [CDISC Data Standards](https://www.cdisc.org/)
-   [ICH E3](https://database.ich.org/sites/default/files/E3_Guideline.pdf)
-   [Tables in Clinical Trials with R](https://rconsortium.github.io/rtrs-wg/)
-   [eCTD (Common Technical Document)](https://www.fda.gov/drugs/electronic-regulatory-submission-and-review/electronic-common-technical-document-ectd) 
-   [Study Data Technical Conformance Guide](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/study-data-technical-conformance-guide-technical-specifications-document)
-   [Version 5 Transport File (XPT)](https://documentation.sas.com/doc/en/pgmsascdc/9.4_3.5/movefile/n1xbwdre0giahfn11c99yjkpi2yb.htm)