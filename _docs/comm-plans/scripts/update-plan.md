---
layout: default
title: Updating a Communication Plan
nav_order: 3
parent: Scripts
grand_parent: Communication Plans
description: "Updating an existing Communication Plan"
permalink: /comm-plans/scripts/update-plan/
---

# Update Plan
 This script updates a program's communication plan in Slate to the version contained in our Slate repository. 



## Arguments

| Flag | Description                                                    | Example |
| :--- | :------------------------------------------------------------- | :------ |
| -a   | Plan acronym. Must match website subdirectory.                 | `mba`   |
| -s   | Skip first _ emails. **Optional** Integer value, 0 is default. | `3`     |


## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following commands in a terminal:

```bash
pip install --upgrade pyautogui pyperclip requests beautifulsoup4
```

In addition, you will need to create an environment file, `.env`, in the scripts folder containing the following data:

```bash
HOST="YOUR_WEBSERVER_IP_ADDRESS_HERE"
```

The last dependency to be aware of is that this script uses the hotkey combination `win`+`1` to open up a browser. Ensure that your preferred browser is the first application on your taskbar, as this is a neccessary for the hotkeys to execute the intended operation.

## Usage
Be warned, to use the script effectively, you need to meet several prerequisites:

* You have met all dependencies listed above
* You have opened Slate on the leftmost monitor in a maximized Firefox window at 120% zoom.
* You have the necessary permissions in Slate to create and send Deliver mailings.

From a terminal prompt, navigate to the scripts folder in your local copy of the repository, then run the following command with your program and skip parameters.

We will use MBA as an example.

```bash
python update_plan.py -a 'mba' '1'
```

The script will need some time to complete, as it has to click its way through Slate. Keep an eye on your terminal for updates on how this program is progressing through updating each email.  

Once finished, you will have a set of emails in Slate in `/Distance/MBA` under Deliver. These emails will be live, so be sure they're 100% ready before you run the script.

## Troubleshooting
Script is not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section.

If you have any other errors, Python and the script's messages printed to the terminal should guide you on fixing the error. 

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.