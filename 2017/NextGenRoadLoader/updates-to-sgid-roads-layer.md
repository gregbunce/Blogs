---
status: publish
layout: post
author:
  display_name: Greg Bunce
  email: GBunce@utah.gov
tags:
  - roads
  - data model update
  - sgid
  - next generation 911
  - Federal Highway Administration ARNOLD
published: true
date: 2017-08-15 00:00:00
title: 'Major update coming to the SGID Statewide Roads Data Model'
categories:
  - SGID Data
---

It has always been one of our goals to stay ahead of the coming changes at the NextGen 911 and FHA level, so after much statewide [coordination](https://gis.utah.gov/road-centerlines-schema-update-and-regional-workshop-notes/) and [feedback](https://gis.utah.gov/feedback-wanted-draft-statewide-road-centerlines-schema-v-3-0-x/), AGRC is officially adopting a [new statewide roads data model](https://docs.google.com/spreadsheets/d/1jQ_JuRIEtzxj60F0FAGmdu5JrFpfYBbSt3YzzCjxpfI/edit#gid=811360546). The two main drivers for this update are the Next Generation 911 GIS requirements and the Federal Highway Administration’s all roads network (ARNOLD) reporting requirements for state DOTs.

AGRC will officially adopt this new roads data model on September 13th, 2017. The purpose of this blog post is to give our users a heads-up on the coming changes, and to allow the necessary time to adjust your internal workflows, beforehand. After that date, we will continue to provide downloadable data (and an SDE layer) in the older model, until March 21st, 2018.  However, we encourage you to adopt this newer model sooner than later, as it will be the official statewide roads data model. There will be a subsequent blog post in September, before the official change.  

**Download the New Data**

If you obtain the statewide roads layer from our website via the Road Centerline [download links](https://gis.utah.gov/data/transportation/roads-system/), you will now notice both data models. Similarly, if you are accessing the roads layer via our SDE connection (only available inside the State network) you will temporarily notice a statewide layer named "Roads_NextGen". This NextGen layer will replace the Roads layer on September 13th, 2017. At that time, the current "Roads" layer in SDE will be renamed to "RoadsODM" (RoadsOldDataModel).  For both the download links and the SDE layer, the older data model will be maintained, and kept current, until March 21, 2018.


**Further Details of the ETL**

Spatial data for this model was directly derived from the former data model. During the ETL, all spatial fields were reassigned via point-in-polygon queries (from SGID data layers), based on the segment's midpoint. In order to capture the correct polygon boundaries for fields with right and left values (ie: ZIPCODE_R; ZIPCODE_L), a 50 foot offset (from the segment's midpoint) was applied for each side. The FULLNAME field was also recalculated, based on a field concatination formula. [Click here](https://docs.google.com/spreadsheets/d/1-oxxE6Ib45tJrySXmz3KnpGtBz_xJBMpVYR4T49CwPI/edit?usp=sharing) for a detailed look at our ETL process, showing a side-by-side comparison of what fields were pushed where, as well as what fields are new or deprecated (note: see the sheet titled, "SideBySideComp").

**The Take Away**
- AGRC will officially adopt this new data model on September 13th, 2017
- AGRC will maintain and publish both models until March 21sth, 2018
- New data model is based on the NextGen911 and FHA's ARNOLD requirements

Please don't hesitate to [contact me](mailto:gbunce@utah.gov) if you have any questions or concerns about the new data model or this transition. We hope that you will adopt this new model within your own agency. Let me know if you are planning on doing so and are looking for guidance or assistance with the process (ETL).
