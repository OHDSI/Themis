---
title: What to do when birth day, month or time are missing from the source
keywords: birthdate, birth datetime
last_updated: April 10, 2024
tags: [birthdate, person]
sidebar: mydoc_sidebar
permalink: /missing_birthdatetime.html
---

## Issue # and location
[Themis Issue #93](https://github.com/OHDSI/Themis/issues/93)

## Issue Summary
How to populate the `birth_datetime` field when any or all of day/month/time of birth is not provided in the source.

## Convention type
Table 

## CDM table
`PERSON`

## CDM field
`birth_datetime`

## Links to issue discussion
NA

## Provenance of data
General

## The ratified convention
Use the following logic to infer the `birth_datetime` value:

- If only year of birth is given and the person has records during their year of birth - then use the date of the earliest record
- If only year of birth is given, and there are no records during their year of birth, use the 15th of June of that year.
- If year of birth and month of birth are given, but no day of birth, then use the first day of the month in that year.
- If time of birth is not given use midnight (00:00:0000).

## Date of ratification/published
2021-09-25 (CDM v5.4 release)

## Downstream implications
No, `birth_datetime` is little used in OHDSI tooling.

## Link to DQD check
plausibleAfterBirth

## Related conventions/further information
NA
