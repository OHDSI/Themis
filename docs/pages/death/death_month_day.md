---
title: How to populate the death date when you only have the year or year and month
keywords: death, death date
last_updated: April 18, 2024
tags: [death, death_date, dates]
sidebar: mydoc_sidebar
permalink: /death_month_day.html
---

## Issue # and location
[Themis issue #104](https://github.com/OHDSI/Themis/issues/104)

## Issue summary
The `death.death_date` field has day resolution. Some source data may not have complete datestamp of the deceased persons' death date. How should the day be approximated if only the year or year and month of death are available?

## Convention type
Table

## CDM table
`DEATH`

## CDM field
`death_date`

## Links to issue discussion
[CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#death)   

## Provenance of data
General

## The ratified convention
- If the given death date only includes month and year, the last day of the month is used as the default. 
- If the given death date only includes year, December is used as the default month, and the last day of the month the default day.

## Date of ratification/published
NA

## Downstream implications
NA

## Link to DQD check
Yes - [plausibleDuringLife](https://ohdsi.github.io/DataQualityDashboard/articles/checks/plausibleDuringLife.html) and [plausibleBeforeDeath](https://ohdsi.github.io/DataQualityDashboard/articles/checks/plausibleBeforeDeath.html) 

## Related conventions/further information
NA