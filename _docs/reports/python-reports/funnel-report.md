---
layout: default
title: Funnel Report
nav_order: 5
parent: Python Reports
grand_parent: Reports
permalink: /reports/python-r/funnel-report
---

# Funnel Report
The goal of the Funnel Report is to facilitate understanding of prospects progression through the application process grouped by program and college. The questions that this report answers are:

* How many prospects do each program/college have?
* How many prospects fill out an application for each program/college?
* How far do most prospects get in the application process for each program/college?
* How many prospects filled out an application for the program they are a prospect for?
* How many students fill out an application for the same term that they are a prospect for?

This report takes in Prospect and Application data from slate and outputs a pivot table to an excel file titled `report_funnel.xlsx`

## Arguments

| Flag | Description                                              | Example          |
| :--- | :------------------------------------------------------- | :--------------- |
| -a   | Applications `.csv` file preferrably exported from Slate | `applicants.csv` |
| -p   | Prospects `.csv` file preferrably exported from Slate    | `prospects.csv`  |

For these `.csv` files the data dimensions exported are meaningful. Below is a list of the columns that should be included in these files.

`applicants.csv`:

`prospects.csv`:

## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following command in a terminal:

```bash
pip install --upgrade numpy pandas
```
This script refrences information contained in supporting `colleges.csv` and `programs.csv` files for formatting of the associated namesake. Make sure to have files titled as such in the working directory of this script when executing.

The `colleges.csv` should contain

The `programs.csv` should contain

## Usage
Running of this script is rather simple after fulfilling all of the dependencies. Navigate to the script’s directory in a terminal and run the following command:

```bash
python funnel_report.py -a applicants.csv -p prospects.csv
```

The script will need some time to complete, as Pandas is a big module doing many things under the hood. Once finished, you will have an excel file `report_funnel.xlsx` in the working directory of the script. This workbook will have two sheets, one titled `Prospects-Program Info` and another titled `Prospects-College Info`. 

## Troubleshooting
Script is not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section.

If you have any other errors, Python and the script's messages printed to the terminal should guide you on fixing the error.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.