---
layout: default
title: Generating a Communication Plan
nav_order: 1
parent: Scripts
grand_parent: Communication Plans
description: "Creating a Skeleton Plan"
permalink: /comm-plans/scripts/create-plan/
---

# Generating a Skeleton Communication Plan
To start developing a communication plan for a new program, this Python script will generate a program homepage file and a Blade file for each day specified. Once these are created, simply add in the email-specific content.

---

## Arguments

| Flag | Description                                    | Example                    |
| :--- | :--------------------------------------------- | :------------------------- |
| -a   | Plan acronym. Must match website subdirectory. | `mba`                      |
| -d   | Days in list form.                             | `0 3 5 7 10`               |
| -n   | Program name.                                  | `Master of Business Admin` |
| -s   | Signature file to use.                         | `mjimerson`                |

## Dependencies
Make sure you install [Python 3](https://www.python.org/downloads/) and run the following commands in a terminal:

```bash
pip install --upgrade pandas
```

## Usage
From a terminal prompt, navigate to the scripts folder in your local copy of the repository, then run the following command with your desire parameters. 

We will use the MBA program as an example.

```bash
python create_plan.py -a 'mba' -d 0 3 5 7 10 -n 'Master of Business Admin' -s 'mjimerson'
```

This will create a directory in `../resources/views/programs/`, named after the acronym provided, containing the following files:

* `home.blade.php`
* `zero.blade.php`
* `three.blade.php`
* `five.blade.php`
* `seven.blade.php`
* `ten.blade.php`

The file `home.blade.php` will contain a list of emails for you to navigate to easily. The other files are where your email content will live.

The signature argument specifies which file in `../resources/views/signatures/` will be automatically imported into the communication plan. Do note if the file does not exist, Laravel will throw an error, and you will need to create the file.

Upon running the script, you will also see that `../resources/views/home.blade.php` is updated with a link to the plan you just created. 

## Troubleshooting
Before creating a communication plan for a program, make sure the old one doesn't exist. If you need to massively revamp an existing plan, I recommend archiving the old plan's directory first. 

Make sure to install [Python 3](https://www.python.org/downloads/) and use `pip` to install [Pandas](https://pandas.pydata.org/).

If there are any other errors, the script (or Python itself) should let you know.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.
