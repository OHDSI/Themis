---
title: How to populate year_of_birth when it is missing from the source
keywords: birthdate, birth year, year_of_birth
last_updated: April 10, 2024
tags: [birthdate, year_of_birth, person]
sidebar: mydoc_sidebar
permalink: /missing_year_of_birth.html
---

## Issue # and location
[Themis #92](https://github.com/OHDSI/Themis/issues/92)

## Issue summary
The lack of year_of_birth creates a dilemma on how to process those records. The age of a patient is vital to observational research such that it is suggested that patients without known age should be excluded from the CDM standardized database. 

Discussions in the forums indicate that setting year of birth to NULL precludes finding those records in SQL queries. Incorrect and inconsistent results occur when setting year of birth to 0.  When year_of_birth is 0, Postgres calculates an age of 2021 years in but In SQL Server it would be 122 years old as year 0 is 1900-01-01. 

Setting all unknown year of birth to specific year creates problems in performing network studies as the tools and algorithms used in network studies do not include control structures (if/then or switch statements ) to identify unknown year of birth when set to an incorrect year of birth with the assumption that that year means "unknown year of birth". Modifying the code in tools to accomodate the idiosyncrasies of databases creates problems and requires additional work. This same issue occurs when year of birth is set to 0 or NULL.

The lack of year of birth raises an issue about years of birth known to be incorrect. Examples include year of birth after today's year, or year of birth after the most recent year of visit or other fields with year.

## Convention type
Table

## CDM table
`PERSON`

## CDM field
`year_of_birth`

## Links to issue discussion

- [OHDSI Forums discussion](https://forums.ohdsi.org/t/mandatory-fields-in-the-person-table/1618)
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/person-not-have-year-of-birth/16566)
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/eliminating-persons-themis-wg3-topic-2/3974/14)
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/missing-birth-date/18251)
-  [Themis issue #9](https://github.com/OHDSI/Themis/issues/9)

## Provenance of data.
General

## The ratified convention
For data sources with date of birth, the year should be extracted. For data sources where the year of birth is not available, the approximate year of birth could be derived based on age group categorization, if available. If no year of birth is available all the person’s data should be dropped from the CDM instance.

## Date of ratification/published
4/9/2024

## Downstream implications
No

## Link to DQD check

Yes - [isRequired](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isRequired.html).

## Related conventions/further information

Related to the general convention on dropping patient data from the CDM instance when certain conditions are met.
