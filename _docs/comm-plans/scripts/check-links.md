---
layout: default
title: Checking Links
nav_order: 4
parent: Scripts
grand_parent: Communication Plans
description: "Checking for bad links in a Communication Plan"
permalink: /comm-plans/scripts/check-links/
---

# Check links
This script audits the validity of each link sent out for a program's Communication Plan. Each email in a program's communication plan is checked to ensure that the link is secure, not outdatated, and does not return a 404 error.

## Arguments
This script takes no arguments

## Dependencies
 In case you have yet to install Python or the common dependencies, follow the instructions below:

Make sure you install [Python 3](https://www.python.org/downloads/) and run the following commands in a terminal:

```bash
pip install --upgrade beautifulsoup4 requests urllib3
```

In addition, you will need to create an environment file, `.env`, in the scripts folder containing the following data:

```bash
HOST="YOUR_WEBSERVER_IP_ADDRESS_OR_FQDN_HERE"
```

This script refrences other folders within the slate repository so if running of this script is attempted outside of the Slate repository, it will output errors. `utilities.py` is an essential helper file that needs to be in the same working directory as this script. 

## Usage
Running of this script is rather simple after fulfilling all of the dependencies. Navigate to the script’s directory in a terminal and run the following command:

```bash
python check_links.py
```

Keep an eye on your terminal as this script is executing.  in the case that all of the links work there should be nothing printed out to the terminal. If there is an issue with a link, the issue will be printed to the terminal followed by the faulty url.

## Troubleshooting
Script not working? Make sure your system meets all of the listed dependencies and that you have performed the neccessary prerequisites listed in the usage section.

If you have any other errors, Python and the script's messages printed to the terminal should guide you on fixing the error.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.