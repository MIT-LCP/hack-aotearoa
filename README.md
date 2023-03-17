# Hack Aotearoa 2023 (March 17th to March 19th 2023)

This repository contains resources for [Hack Aotearoa 2023](http://hackaotearoa.nz)

## Contents

1. Getting started
2. Documentation
3. Databases on BigQuery
4. Analysing data with Google Colab
5. Python notebooks that we prepared earlier
6. An example in R
7. Sample projects


## 1. Getting started

The datasets are hosted on Google Cloud, which requires a Gmail account to manage permissions.

1. Create a [Gmail account](https://www.google.com/gmail/about/), if you don't already have one. It will be used to manage your access to the resources.
2. Complete the form at: https://uoaevents.eventsair.com/hack-aotearoa-2023/dua2023/Site/Register.

## 2. Documentation

- MIMIC Clinical Database: https://mimic.physionet.org/
- eICU Collaborative Research Database: https://eicu-crd.mit.edu/

## 3. Databases on BigQuery

BigQuery is a database system that makes it easy to explore data with Structured Query Language ("SQL"). There are several datasets on BigQuery available for you to explore, including `eicu_crd` (the eICU Collaborative Research Database) and `mimiciii_clinical` (the MIMIC-III Clinical Database).

You will also find "derived" databases, which include tables derived from the original data using the code in the [eICU](https://github.com/MIT-LCP/eicu-code) and [MIMIC](https://github.com/MIT-LCP/mimic-code) code repositories. These are helpful if you are looking for something like a sepsis cohort or first day vital signs.

1. [Open BigQuery](https://console.cloud.google.com/bigquery?project=physionet-data).
2. At the top of the console, select `hack-aotearoa` as the project. This indicates the account used for billing.
<!-- 3. "Pin" a project to the resources menu to view available datasets. In the Resources menu on the left, click "Add data", "Pin a project", then add the following project names: `physionet-data` and `hack-aotearoa`. -->
3. You should be able preview the data available on these projects using the graphical interface.
4. Now try running a query. For example, try counting the number of rows in the demo eICU patient table:

   ```SQL
   SELECT count(*)
   FROM `physionet-data.eicu_crd_demo.patient` 
   ```

## 4. Analysing data with Google Colab

Python is an increasingly popular programming language for analysing data. We will explore the data using Python notebooks, which allow code and text to be combined into executable documents. First, try opening a blank document using the link below:

- [https://colab.research.google.com/](https://colab.research.google.com/)

## 5. Python notebooks that we prepared earlier

Several tutorials are provided below. Requirements for these notebooks are: (1) you have a Gmail account and (2) your Gmail address has been added to the appropriate Google Group by the workshop hosts.

Notebook 1 (eICU): Exploring the patient table. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/01_explore_patients.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 2 (eICU): Severity of illness. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/02_severity_of_illness.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 3 (eICU): Summary statistics. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/03_summary_statistics.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 4 (eICU): Timeseries. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/04_timeseries.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 5 (eICU): Mortality prediction. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/05_mortality_prediction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 6 (eICU): Acute kidney injury. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/06_aki_project.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 7 (eICU): Project work. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/07_project_work.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Notebook 8 (MIMIC): Weekend effect on mortality. <a href="https://colab.research.google.com/github/MIT-LCP/hack-aotearoa/blob/master/mimic-weekend-effect.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

## 6. An example in R

If you prefer working in R, then you can connect to Google Cloud from your code in a similar way:

- https://github.com/MIT-LCP/hack-aotearoa/blob/master/mimic-iii-los.rmd

## 7. Sample projects

These papers and repositories may be helpful for reference. They are **not** perfect! Code may be untidy, poorly documented, buggy, outdated etc. Think about how they can be improved, adapted, etc. For example, you could:

- replicate the study on a different dataset (e.g. MIMIC vs eICU)
- improve the methodology

1. The association between mortality among patients admitted to the intensive care unit on a weekend compared to a weekday

- Python Notebook: https://github.com/MIT-LCP/bhi-bsn-challenge/blob/master/challenge-demo.ipynb
- R Markdown Notebook: https://github.com/MIT-LCP/bhi-bsn-challenge/blob/master/rmarkdown_example_notebook.Rmd
- More reading: https://physionet.org/content/bhi-2018-challenge/1.0/

2. Predicting in-hospital mortality of intensive care patients using decision trees.

- Python Notebook: https://github.com/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/eicu/05-prediction.ipynb 

3. Comparison of methods for identifying patients with sepsis.

- Code: https://github.com/alistairewj/sepsis3-mimic
- Paper: https://www.ncbi.nlm.nih.gov/pubmed/29303796

4. Evaluating the reproducibility of mortality prediction studies that use the MIMIC-III database. 

- Code: https://github.com/alistairewj/reproducibility-mimic/blob/master/notebooks/reproducibility.ipynb
- Paper: http://proceedings.mlr.press/v68/johnson17a.html

5. Optimising treatment of sepsis with reinforcement learning

- Code: https://github.com/matthieukomorowski/AI_Clinician
- Paper: https://www.nature.com/articles/s41591-018-0213-5

6. Association of hypokalemia with an increased risk for medically treated arrhythmia

- Code: https://github.com/nus-mornin-lab/PotassiumAA
- Paper: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0217432
