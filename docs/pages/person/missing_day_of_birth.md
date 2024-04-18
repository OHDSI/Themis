---
title: How to populate day_of_birth when it is missing from the source
keywords: birthdate, birth
last_updated: April 10, 2024
tags: [birthdate, person]
sidebar: mydoc_sidebar
permalink: /missing_day_of_birth.html
---

## Issue # and location
[Themis issue #96](https://github.com/OHDSI/Themis/issues/96)

## Issue summary
Day of Birth is not required in the CDM, but it is a component of birth_datetime. The CDM conventions have guidance listed for how to infer birth_datetime field, but not for the day_of_birth field itself. 

## Convention type
Table

## CDM table
`PERSON`

## CDM field
`day_of_birth`

## Links to issue discussion
[Themis issue #96](https://github.com/OHDSI/Themis/issues/96)
[CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#person)   

## Provenance of data
General

## The ratified convention
Day of birth is **not required in the CDM**, but it is a component of birth_datetime. For data sources that provide the precise date of birth, the day should be extracted and stored in this field. For data sources which lack this data point, but have a use case to infer the information (i.e. this is helpful for mother-child linkage algorithms), use the following heuristic:

- If day_of_birth is null and month_of_birth is not null, then populate day_of_birth with '01'.
- If day_of_birth AND month_of_birth are both null and the person has records during their year of birth, then use the date of the earliest record, otherwise use the 15th of June of that year. 

## Date of ratification/published
NA

## Downstream implications
No

## Link to DQD check

## Related conventions/further information
Themis issue #95 - If month_of_birth is null or if day_of_birth AND month_of_birth are both null and the person has records during their year of birth then use the date of the earliest record, otherwise use the 15th of June of that year.
