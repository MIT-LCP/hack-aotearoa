# Hack Aotearoa 2020 (17-19 January)

This repository contains resources for [Hack Aotearoa 2020](http://hackaotearoa.co.nz/).

## Getting started

The datasets are hosted on Google Cloud, which requires a Gmail account to manage permissions.

1. Create a [Gmail account](https://www.google.com/gmail/about/), if you don't already have one. It will be used to manage your access to the resources.
2. Give your gmail address to the session hosts.

## Documentation

- MIMIC-III Clinical Database: https://mimic.physionet.org/
- eICU Collaborative Research Database: https://eicu-crd.mit.edu/

## Databases on BigQuery

BigQuery is a database system that makes it easy to explore data with Structured Query Language ("SQL"). There are several datasets on BigQuery available for you to explore, including `eicu_crd` (the eICU Collaborative Research Database) and `mimiciii_clinical` (the MIMIC-III Clinical Database).

You will also find "derived" databases, which include tables derived from the original data using the code in the [eICU](https://github.com/MIT-LCP/eicu-code) and [MIMIC](https://github.com/MIT-LCP/mimic-code) code repositories. These are helpful if you are looking for something like a sepsis cohort or first day vital signs.

1. [Open BigQuery](https://console.cloud.google.com/bigquery?project=hack-aotearoa).
2. At the top of the console, select `hack-aotearoa` as the project. This indicates the account used for billing.
3. "Pin" a project to the resources menu to view available datasets. In the Resources menu on the left, click "Add data", "Pin a project", then add the following project names: `physionet-data` and `hack-aotearoa`.
4. You should be able preview the data available on these projects using the graphical interface.
5. Now try running a query. For example, try counting the number of rows in the demo eICU patient table:

   ```SQL
   SELECT count(*)
   FROM `physionet-data.eicu_crd_demo.patient` 
   ```

## Analysing data with Google Colab

Python is an increasingly popular programming language for analysing data. We will explore the data using Python notebooks, which allow code and text to be combined into executable documents. First, try opening a blank document using the link below:

- [https://colab.research.google.com/](https://colab.research.google.com/)

## Python notebooks that we prepared earlier...

Several tutorials are provided below. Requirements for these notebooks are: (1) you have a Gmail account and (2) your Gmail address has been added to the appropriate Google Group by the workshop hosts.

Notebook 1: Exploring the patient table. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/01_explore_patients.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 2: Severity of illness. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/02_severity_of_illness.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 3: Summary statistics. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/03_summary_statistics.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 4: Timeseries. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/04_timeseries.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 5: Mortality prediction. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/05_mortality_prediction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 6: Acute kidney injury. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/06_aki_project.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 7: Project work. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/07_project_work.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

## An example in R

If you prefer working in R, then you can connect to Google Cloud from your code in a similar way:

- https://github.com/MIT-LCP/hack-aotearoa/blob/master/mimic-iii-los.rmd
