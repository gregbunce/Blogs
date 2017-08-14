---
status: publish
layout: post
author:
  display_name: Greg Bunce
  email: GBunce@utah.gov
tags:
  - roads
  - data model
  - sgid
  - next generation 911
  - Federal Highway Administration ARNOLD
published: true
date: 2017-08-14 00:38:49
title: 'Major update to the SGID Statewide Roads Data Model'
categories:
  - SGID Data
---

### Major update coming to the SGID Statewide Roads Data Model

After much statewide [coordination](https://gis.utah.gov/road-centerlines-schema-update-and-regional-workshop-notes/) and [feedback](https://gis.utah.gov/feedback-wanted-draft-statewide-road-centerlines-schema-v-3-0-x/), AGRC is officially adopting a [new statewide roads data model](https://docs.google.com/spreadsheets/d/1jQ_JuRIEtzxj60F0FAGmdu5JrFpfYBbSt3YzzCjxpfI/edit#gid=811360546) in early September. The two main drivers for this update are the Next Generation 911 GIS requirements and the Federal Highway Administration’s all roads network (ARNOLD) reporting requirements for state DOTs.

The purpose of this blog post is to give users a heads-up on the changes coming, and to allow the necessary time to adjust your internal workflows. We will continue to provide the older data model unit March 21st, 2018, but we encourage you to adopt this one sooner than later as it will become the offical statewide model in early September. There will be a subsequent blog post detailing that change.  

For your convience, we will contininue to provide and maintain both data models throughout the transistion process.

If you obtain the statewide roads layer from our website via the download links, you will now notice both data models. Simaraly, if you are accessing the roads layer via our SDE connection (only available inside the State network) you will now notice a statewide layer named "Roads_NextGen". This NextGen layer will replace the Roads layer in early September. At that time, the current "Roads" layer will be renamed to "RoadsODM" (RoadsOldDataModel).  This older SDE layer will also be maiantened and available until March 21, 2018.

[Click here](https://docs.google.com/spreadsheets/d/1-oxxE6Ib45tJrySXmz3KnpGtBz_xJBMpVYR4T49CwPI/edit?usp=sharing) for a detailed look at our ETL process, showing a a side-by-side comparison of what fields were pushed where, as well as what fields are new or deprecated (note: there are three sheets in this spreadsheet).

Please don't hesitate to [contact me](mailto:gbunce@utah.gov) if you have any questions or concerns about the new data model or this transistion.

It has always been goal to stay ahead of the coming changes at the NextGen 911 and FHA level, and to encourage and assist other agencies to do so as well. The desire is to best position the state to meet requirements for Next Generation 911, as well as new federal reporting requirements placed on state DOTs. 

We are enthused to provide this dataset and it is our hope that you will adopt it within your own agency. Let us know if you are planning on doing so and are looking for guidance or assistnce in the process.

**The Take Away**
- New data model is based on the NextGen911 and FHA's ARNOLD requirements
- Data ETL was directly derived from the former data model
- During the ETL, all spatial fields were assigned via point-in-polygon queries (from SGID polygon data layers), with a 50 foot offset for categories containing right and left fields (ie: ZIPCODE_R; ZIPCODE_L)
- Left / Right field values
- Recalculation of FULLNAME field
- New fields, deprecated fields
- Publishing both models until March 21sth, 2018
