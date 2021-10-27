---
layout: default
title: Date Report
nav_order: 5
parent: Python Reports
grand_parent: Reports
permalink: /reports/python-r/date-report
---

# Date Report
The goal of the Date Report is to help us understand how much time an applicant to go through the application process and how much time each department spends on processing applications. The questions that this report answers are:

* What is the average time it takes an applicant to get through the application process?
* What are the differences in average application time between undergraduate and graduate applications? 
* On average which steps in the application process takes the longest/shortest?
* For graduate applications how long does it take for departments to process applications?
* What do summary statistics on date differences per bin movement look like?

This report takes in applicant bin movement data from slate and outputs a pivot table to an excel file. 

## Arguements


| Flag | Description                                  | Example     |
| :--- | :------------------------------------------- | :---------- |
| -i   | Applications `.csv` file exported from Slate | `input.csv` |

For this `.csv` file the data dimensions exported are meaningful. Below is a list of the columns that should be included in these files.

`input.csv`: 


## Dependencies

Make sure you install [Python 3](https://www.python.org/downloads/) and run the following command in a terminal:

```bash
pip install --upgrade pandas
```
This script refrences information contained in files, `bins.py` and `classes.py`, for supporting data structures and application process step validation. Make sure to have these files in the working directory when executing this report.

## Usage
Running of this script is rather simple after fulfilling all of the dependencies. Navigate to the script’s directory in a terminal and run the following command:

```bash
python date_report.py -i input.csv
```

The script will need some time to complete, as Pandas is a big module doing many things under the hood. Once finished, you will have an excel file in the working directory of the script with the output.

## Troubleshooting
Script is not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section.

If you have any other errors, Python and the script's messages printed to the terminal should guide you on fixing the error.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.
