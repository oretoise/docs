---
layout: default
title: Event Report
nav_order: 5
parent: Python Reports
grand_parent: Reports
permalink: /reports/python-r/event-report
---

# Event Report
The goal of the Event Report is to report key metrics about events hosted by the CDE. The questions that this report answers are:

* How many events were held online within a specified date range?
* How many people attended each event?
* How many prospects that attended each event applied/admitted/enrolled?
* How many events were held in conjunction with community colleges?

This report takes in an event registration data file exported from slate and outputs a file `pivot.csv` which is a pivot table with data answering the above questions. 

## Arguments

| Flag | Description                                              | Example     |
| :--- | :------------------------------------------------------- | :---------- |
| -i   | Event Registration Data File in `.csv` format from Slate | `input.csv` |

For this `.csv` file the data dimensions exported are meaningful. Below is a list of the columns that should be included in this file.

`input.csv`:


## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following command in a terminal:

```bash
pip install --upgrade numpy pandas
```

## Usage
Running of this script is rather simple after fulfilling all of the dependencies. Navigate to the script’s directory in a terminal and run the following command:

```bash
python event_report.py -i input.csv
```

The script will need some time to complete, as Pandas is a big module doing many things under the hood. Once finished, you will have a `pivot.csv` file in the working directory of the script. This pivot table have each event within the specified date range in the first column with their associated admit, applicant, enroll, inquiry, and total prospect values across the row.  

## Troubleshooting
Script is not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section.

If you have any other errors, unwinding Python's error stack should guide you on fixing the issue.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.