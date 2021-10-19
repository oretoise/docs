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




## Arguments

| Flag | Description                                    | Example |
| :--- | :--------------------------------------------- | :------ |
| -a   | Plan acronym. Must match website subdirectory. | `mba`   |
| :--- | :--------------------------------------------- | :------ |
| -s   | Skip first _ email. Optional Integer value arg | `3`     |


## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following commands in a terminal:

```bash
pip install --upgrade pyautogui pyperclip requests argparse beautifulsoup4
```

In addition, you will need to create an environment file, `.env`, in the scripts folder containing the following data:

```bash
HOST="YOUR_WEBSERVER_IP_ADDRESS_HERE"
```

The last dependency to be aware of is that this script uses the hotkey combination `win`+`1` to open up a browser. Ensure that your preferred browser is the first application on your taskbar, as this is a neccessary for the hotkeys to execute the intended operation.

## Usage


## Troubleshooting


## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.