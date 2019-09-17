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
This article describes all the scripts starting with "batch" in their filename. These are used when multiple plans need to be updating, uploaded, or deleted. As with doing anything in bulk, verify the basic scripts work for you before doing things in bulk. You don't want to end up with more work than what you started with.

---

## Arguments
All of these scripts take a single argument: a list of plans in CSV format.

| Flag | Description | Example |
|:--- |:--- |:---|
| -l | List of plans in CSV format. Remember that these must match their website subdirectory. | `plans.csv` |

See the included `plans.csv` document for an example. Note the header row.

## Dependencies
Each batch script requires the same dependencies as its single-plan version. In case you have yet to install Python or the common dependencies, follow the instructions below:

Make sure you install [Python 3.7](https://www.python.org/downloads/release/python-374/) and run the following commands in a terminal:

```bash
pip install --upgrade pandas pyautogui pyperclip requests python-dotenv
```

In addition, you will need to create an environment file, `.env`, in the scripts folder containing the following data:

```bash
HOST="YOUR_WEBSERVER_IP_ADDRESS_HERE"
```

## Usage

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.
