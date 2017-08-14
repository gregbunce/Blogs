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

### Major update to the SGID Statewide Roads Data Model

After much statewide [coordination](https://gis.utah.gov/road-centerlines-schema-update-and-regional-workshop-notes/) and [feedback](https://gis.utah.gov/feedback-wanted-draft-statewide-road-centerlines-schema-v-3-0-x/), AGRC has officially adopted a [new statewide roads data model](https://docs.google.com/spreadsheets/d/1jQ_JuRIEtzxj60F0FAGmdu5JrFpfYBbSt3YzzCjxpfI/edit#gid=811360546). The two main drivers for this update were the Next Generation 911 GIS requirements and the Federal Highway Administration’s all roads network (ARNOLD) reporting requirements for state DOTs.

This new data model is now in effect and immediately ready for your consumption. We encourage you to download it and itegrate it into your own workflow's as soon as possible. If you are obtaining the SGID Roads layer from our website via File Geodatabase download you will now notice two statewide layers available. The download labled... is the new... Likewise, if you are accessing the SGID roads layer via our SDE connection (only available inside the State network) you will also notice two statewide layers. The layer named "RoadsODM" is the older data model, whereas "Roads" is now the newer data model.

For your convience, we will contininue to provide the older data model as a [File Geodatabase download](link here) and as a published SDE Data Layer on the SGID. The data will be current and will match what is in the new model.  We will provide the deprecated model data until March 21st, 2018. 

[Click here](https://docs.google.com/spreadsheets/d/1-oxxE6Ib45tJrySXmz3KnpGtBz_xJBMpVYR4T49CwPI/edit?usp=sharing) for a detailed look at our ETL process, showing a a side-by-side comparison of what fields were pushed where, as well as what fields are new or deprecated (note: there are three sheets in this spreadsheet).


**What you need to know:**
- New data model is based on the NextGen911 and FHA's ARNOLD requirements
- Data was ETL'ed from the old model
- spatial assignments for polygon fields
- Left / Right field values
- Recalculation of FULLNAME field
- New fields, deprecated fields
- Publishing both models until March 21sth, 2018.

Please donn't hesitate to [contact me](email link here) if you have any questions or concerns about the new data model or this transistion.

We enthused are provide this new model on a statwide roads dataset this mature and it is our hope that you will be enouraged to also adopt it. Let us know if you thinking about transistioning your data to this model and are looking for guidance or assistnce. It has always been goal to stay ahead of the coming changes at the NextGen 911 and FHA level, and to encourage and assist other agencies to do so as well.

