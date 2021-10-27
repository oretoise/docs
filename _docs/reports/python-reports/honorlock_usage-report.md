---
layout: default
title: Honorlock Usage Report
nav_order: 5
parent: Python Reports
grand_parent: Reports
permalink: /reports/python-r/honorlock_usage-report
---

# Honorlock Usage Report
The goal of the Honorlock Usage Report is to total up honorlock usage hours per instructor and department. The questions that this report answers are:

* Which instructors use honorlock the most/least?
* Which department use honorlock the most/least?
* How many hours does each department/instructor use for honorlock?

This report takes in honorlock usage metrics and outputs a file `Honorlock_Usage.xlsx` with the totals per instructor and department. 

## Arguments

| Flag | Description                                                       | Example               |
| :--- | :---------------------------------------------------------------- | :-------------------- |
| -p   | Honorlock usage file in  `.csv` formate                           | `honorlock-usage.csv` |
| -s   | List of emails that should be skipped during execution (Optional) | `bad-emails.csv`      |

For these `.csv` files the data dimensions exported are meaningful. Below is a list of the columns that should be included in these files.

`honorlock-usage.csv`:

`bad-emails.csv`:

## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following command in a terminal:

```bash
pip install --upgrade pandas pyautogui pyperclip
```
This script refrences information contained in supporting `prof_dept.csv`.  Make sure to have this file in the working directory of this script when executing. 

The `prof_dept.csv` should contain

## Usage
Running of this script is rather simple after fulfilling all of the dependencies. Navigate to the script’s directory in a terminal and run the following command:

```bash
python funnel_report.py -p honorlock-usage.csv -s bad-emails.csv
```

The script will need some time to complete, as Pandas is a big module doing many things under the hood. Once finished, you will have a file titled `sorted_prof.csv` in the working directory of the script.

## Troubleshooting
Script is not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section.

If you have any other errors, unwinding Python's error stack should guide you on fixing the issue.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.