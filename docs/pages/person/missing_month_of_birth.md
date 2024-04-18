---
title: How to populate month_of_birth when it is missing from the source
keywords: birthdate, birth
last_updated: April 18, 2024
tags: [birthdate, person]
sidebar: mydoc_sidebar
permalink: /missing_month_of_birth.html
---

## Issue # and location

- [Themis issue #94](https://github.com/OHDSI/Themis/issues/94)

## Issue summary
How should month_of_birth be populated when it is not provided in the source data? Month of birth is **not required in the CDM**, but it is a component of birth_datetime. 

## Convention type
Table

## CDM table
`PERSON`

## CDM field
`month_of_birth`

## Links to issue discussion
NA

## Provenance of data
General

## The ratified convention
 Month of birth is **not required in the CDM**, but it is a component of birth_datetime. For data sources that provide the precise date of birth, the day should be extracted and stored in this field. For data sources which lack this data point, but have a use case to infer the information (i.e. This is helpful for mother-child linkage algorithms), use the following heuristic:

- If month_of_birth is null or if day_of_birth AND month_of_birth are both null and the person has records during their year of birth then use the date of the earliest record, otherwise use the 15th of June of that year.

## Date of ratification/published
NA

## Downstream implications
No

## Link to DQD check
NA

## Related conventions/further information
NA