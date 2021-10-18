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
This script audits the validity of each link sent out in a communication plan email. Each programs' communication plan emails are checked to ensure that the link is secure, not outdatated and does not return a 404 error. This script should be run prior to sending out emails to prospective students so we can be sure that all of the links that we send out to prospects work as intended.

---

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
HOST="YOUR_WEBSERVER_IP_ADDRESS_HERE"
```

This script refrences other folders within the slate repository so if running of this script is attempted outside of the Slate repository directory it will output error
messages. `utilities.py` is an essential helper file that needs to be in the same working directory of this script. 

## Usage
Running of this script is rather simple after fulfilling all of the dependencies. Navigate to the directory of this script in a terminal and run the following command:

```bash
python check_links_py
```

Keep an eye on your terminal as this script is executing. There should be nothing printed out to the terminal in the case that all of the links in the communication plans work. If there is an issue with a link, the issue will be printed to the terminal followed by the faulty url.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.