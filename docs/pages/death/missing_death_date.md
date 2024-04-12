---
title: How to populate the death date when it is missing from the source data
keywords: death, death date
last_updated: April 10, 2024
tags: [death, death_date, dates]
sidebar: mydoc_sidebar
permalink: /missing_death_date.html
---

## Issue # and location

- [Forum](https://forums.ohdsi.org/t/what-to-do-with-null-death-dates-in-omop/4241/19)
- [Forum](https://forums.ohdsi.org/t/what-to-do-with-null-death-dates-in-omop/4241/41)

## Issue summary
In order to insert a record in the death table, the death_date must be populated. However, some data sources only contain a death flag. In this case, what should the ETL do when there is not a date at the source, but there is a flag indicating the person is deceased?

## Convention type
Table

## CDM table
Death

## CDM field
NA

## Links to issue discussion

- [Forum](https://forums.ohdsi.org/t/what-to-do-with-null-death-dates-in-omop/4241/19)
- [Forum](https://forums.ohdsi.org/t/what-to-do-with-null-death-dates-in-omop/4241/41) 

## Provenance of data
All

## The ratified convention
If your source data do not have a method to properly identify a realistic death_date, then do not create a record in the Death table.  If you think you have a robust method to do the imputation, and you checked that against the data where you do have the death date, you use it. One method of imputation uses the date of the last Patient-Provider interaction.

## Date of ratification/published
January 29, 2022 

## Downstream implications
No

## Link to DQD check
[isRequired](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isRequired.html).

## Related conventions/further information
NA
