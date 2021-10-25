---
layout: default
title: Batch Scripts
nav_order: 99
parent: Scripts
grand_parent: Communication Plans
description: "How to run operations for multiple plans"
permalink: /comm-plans/scripts/batch-scripts/
---

# Batch Operations
This article describes all the scripts starting with "batch" in their filename. These are used when multiple communication plans need to be updated, uploaded, or deleted. As with doing anything in bulk, verify the basic scripts work for you before executing these bulk scripts. You don't want to end up with more work than what you started with!

---

## Arguments
All of these scripts take a single argument: a list of plans in CSV format.

| Flag | Description                                                                             | Example             |
| :--- | :-------------------------------------------------------------------------------------- | :------------------ |
| -l   | List of plans in CSV format. Remember that these must match their website subdirectory. | `plans.example.csv` |

Below is an example of the `.csv` format that these batch scripts expect as input. Note the header row.

```csv
Plans
mba-pm
msei
msgb
msis
msit
phcl
psychology
seed
veterans
wel
wellness
```

## Dependencies
Each batch script requires the same dependencies as its single-plan version. In case you have yet to install Python or the common dependencies, follow the instructions below:

Make sure you install [Python 3](https://www.python.org/downloads/) and run the following commands in a terminal:

```bash
pip install --upgrade pandas pyautogui pyperclip requests python-dotenv
```

In addition, you will need to create an environment file, `.env`, in the scripts folder containing the following data:

```bash
HOST="YOUR_WEBSERVER_IP_ADDRESS_OR_FQDN_HERE"
```

The last dependency to be aware of is that `batch_update.py` uses the hotkey combination `win`+`1` to open up a browser. Ensure that your preferred browser is the first item on your taskbar, as this is neccessary for the hotkeys to execute the intended operation.

## Usage
Before running this script remember to verify that the associated single program script works for your configurations. 

Once you have the single program script working, you're a couple steps away from executing your batch task. 

* List the programs that you'd like to edit into a `.csv` file and save it in the same directory as the batch script. 
* Navigate to the script's directory in a terminal and run the following command:

```bash
python <Batch_Task_Script_Here>.py -l list_of_programs.csv
```

This script will take some time to complete, as it is navigating through the user interface of Slate with a pause between each action.   

## Troubleshooting
Script not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section. We recommend reading the associated single program script documentation and ensureing that your system meets all of the dependencies listed there.

If you have any other errors, Python and the script's messages printed to the terminal should guide you on fixing the error.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.
