---
layout: default
title: Uploading a New Communication Plan
nav_order: 2
parent: Scripts
grand_parent: Communication Plans
description: "Uploading a Communication Plan"
permalink: /comm-plans/scripts/upload-plan/
---

# Uploading a Communication Plan
Once you've added email-specific content to each of the email files, you can upload the new communication plan into Slate.

---

## Arguments

| Flag | Description                                    | Example |
| :--- | :--------------------------------------------- | :------ |
| -a   | Plan acronym. Must match website subdirectory. | `mba`   |

## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following commands in a terminal:

```bash
pip install --upgrade pandas pyautogui pyperclip requests python-dotenv
```

In addition, you will need to create an environment file, `.env`, in the scripts folder containing the following data:

```bash
HOST="YOUR_WEBSERVER_IP_ADDRESS_HERE"
```

## Usage
Be warned, to use the script effectively, you need to meet several prerequisites:

* Each numbered email file has an `<h3>` tag containing the text `<h3>Day __ - Subject: <YOUR SUBJECT HERE></h3>`.
* You have made the population in Slate and added it to `populations.csv`. See [this page]() for details.
* You have opened Slate on the leftmost monitor in a maximized Firefox window at 120% zoom.
* You have the necessary permissions in Slate to create and send Deliver mailings.

From a terminal prompt, navigate to the scripts folder in your local copy of the repository, then run the following command with your program parameter.

We will use MBA as an example.

```bash
python create_plan.py -a 'mba'
```

The script will need some time to complete, as it has to click its way through Slate. Once finished, you will have a set of emails in Slate in `/Distance/MBA` under Deliver.

![MBA Emails]({{site.url}}{{site.baseurl}}/assets/images/scripts/mba_mail_listing.png)

These emails will be live, so be sure they're 100% ready before you run the script.

## Troubleshooting
Before creating a communication plan for a program, make sure the old one doesn't exist. If you need to massively revamp an existing plan, I recommend archiving the old plan's directory first. 

Make sure to install [Python 3](https://www.python.org/downloads/) and use `pip` to install [Pandas](https://pandas.pydata.org/) and other dependencies.

If there are any other errors, the script (or Python itself) should let you know.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.
