---
layout: default
title: Releasing Decisions
nav_order: 4
parent: Applications
description: "How to Release Decisions"
permalink: /applications/release/
---

# Releasing Ready Decisions
Once a decision has been made and a decision letter assigned, an application has a couple more steps before it's ready.  ITS automatically pulls new decisions from Slate into Banner daily.  Once those have been matched to a student record (whether new or prior), ITS pushes the MSU 9-digit ID and netID back into Slate.  From there, we can then release the decision to the applicant.  

Simply follow this guide to release ready decisions for Campus 5.

---

## Requirements
You will need the "decision_release" permission in Slate. Currently, only Jordan and Lisa within CDE have this permission.

## Things to Keep in Mind
* You should only release decisions that are marked **Ready for Release**.  This means the decision has been pushed to Banner, matched with a student record, and had the applicant's MSU 9-digit ID and netID pushed *back* into Slate.
* Ready decisions are uploaded into Slate twice daily by ITS: once in the morning and once in the afternoon.
* It can take a couple of days for a decision to go through this process.

## Steps

### Getting to the Database
First, go to the Database page by clicking the cog/gear icon in the top right:

![Database icon]({{site.url}}{{site.baseurl}}/assets/images/applications/release/database.png)

### Getting the List
Click "Release Decisions" under the Decisions menu:

![The "Release Decisions" link]({{site.url}}{{site.baseurl}}/assets/images/applications/release/release_decisions.png)

Click "Awaiting Release" on the right-hand menu:

![The "Awaiting Release" link]({{site.url}}{{site.baseurl}}/assets/images/applications/release/awaiting_release.png)

From here, you will see a list of Decision Groups.  These are the counts of decisions awaiting release by Application Round, Decision, and finally Letter.

For our applicants, **only** release those with CDE decision letters.  You can tell these apart, as they all start with `CDE`.

![CDE Letters]({{site.url}}{{site.baseurl}}/assets/images/applications/release/cde_letters.png)

Select any and all CDE decision groups.

![CDE Letters selected]({{site.url}}{{site.baseurl}}/assets/images/applications/release/cde_selected.png)

### Building the Query
We still need to filter out those who aren't quite ready to be released.

Click the Filter button:

![Filter button]({{site.url}}{{site.baseurl}}/assets/images/applications/release/filter.png)

From the Local Filters group, click "Ready for Release":

![The "Ready to Release" filter]({{site.url}}{{site.baseurl}}/assets/images/applications/release/ready_to_release.png)

Click Continue:

![Continue button]({{site.url}}{{site.baseurl}}/assets/images/applications/release/continue.png)

Click Yes:

![Setting the "Ready to Release" filter to "Yes"]({{site.url}}{{site.baseurl}}/assets/images/applications/release/yes.png)

Click Save:

![The Save button]({{site.url}}{{site.baseurl}}/assets/images/applications/release/save.png)

### Who's Ready?
Click Display:

![Display button]({{site.url}}{{site.baseurl}}/assets/images/applications/release/display.png)

Slate will either provide you a list of decisions who are ready to release or it will tell you there are none matching that criteria.

If there are none, this is what it will display:

![No decisions to release.]({{site.url}}{{site.baseurl}}/assets/images/applications/release/no_decisions.png)

Otherwise, Slate will display the list of decisions that are ready to be released.  Like so:

![Available decisions]({{site.url}}{{site.baseurl}}/assets/images/applications/release/decision_list.png)

If there are some to be released, check the checkboxes next to each one (or use the very top checkbox).

![Selected decisions]({{site.url}}{{site.baseurl}}/assets/images/applications/release/decisions_checked.png)

You must then choose a date and time for the decisions to be released at.

![Date and time selection]({{site.url}}{{site.baseurl}}/assets/images/applications/release/decisions_checked.png)

For the time, enter a time like so: `1:00pm`. Keep in mind everything in Slate is in Eastern Time.

Finally, click Release.

![The big gray Release button]({{site.url}}{{site.baseurl}}/assets/images/applications/release/release_button.png)

Slate will ask you to confirm.  Take a moment and make sure you've selected the right decision letter(s), added the "Ready to Release" filter, checked the decisions, and verified the date and time.  If all is well, click OK.

![Are you sure prompt]({{site.url}}{{site.baseurl}}/assets/images/applications/release/confirm.png)

### Finished
You are all done, and the decisions will be released at the time specified.

## Questions?
Feel free to contact [Jordan](mailto:jordan.scruggs@msstate.edu) or the Tech Unit via email.