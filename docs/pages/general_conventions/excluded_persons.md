---
title: When to exclude persons from the CDM
keywords: person
last_updated: April 10, 2024
tags: [person]
summary: "Considerations for excluding persons from the CDM."
sidebar: mydoc_sidebar
permalink: /excluded_persons.html
---

## Issue # and location
- [Themis issue #9]([#9](https://github.com/OHDSI/Themis/issues/9))

## Issue summary
How and when should persons be excluded from the CDM? What factors go into this decision?

## Convention type
Global

## CDM table
NA

## CDM field
NA

## Links to issue discussion
- [OHDSI Forums discussion](http://forums.ohdsi.org/t/eliminating-persons-themis-wg3-topic-2/3974)

## Provenance of data
General, All

## The ratified convention
It is not required that all subjects from the raw data be carried over to the CDM, in fact removing people that are not of high enough quality may help researchers using the CDM. Persons should be removed if:

  - Their year of birth or age are unreasonable (e.g. born in year 0, 1800 or 2999)
  - They do not have a year of birth and it cannot be derived
  - They do not have a gender
  - There is reason to believe their data is not of high quality
  
  Removal of a patient is not required and should be made in consideration of the raw data source. Reasons for removal of persons should be documented in the ETL documentation and METADATA table.

## Date of ratification/published
April 24, 2018 

## Downstream implications
No

## Link to DQD check

- [isRequired](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isRequired.html)
- [plausibleValueHigh](https://ohdsi.github.io/DataQualityDashboard/articles/checks/plausibleValueHigh.html)
- [plausibleValueLow](https://ohdsi.github.io/DataQualityDashboard/articles/checks/plausibleValueLow.html)

## Related conventions/further information
NA