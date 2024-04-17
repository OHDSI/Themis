---
title: How to populate days_supply when days supply is missing in the source data
keywords: drug, drug_exposure, days_supply
last_updated: April 16, 2024
tags: [drug_exposure, days_supply]
sidebar: mydoc_sidebar
permalink: /missing_days_supply.html
---

## Issue # and location

- [Themis issue #125](https://github.com/OHDSI/Themis/issues/125)
 
## Issue summary
How should days_supply be populated when it is missing from the source data?

## Convention type
Table

## CDM table
`drug_exposure`

## CDM field
`days_supply`

## Links to issue discussion

- [OHDSI Forums discussion](https://forums.ohdsi.org/t/days-supply-yet-again/4741/16)
- [THEMIS issue #76](https://github.com/OHDSI/Themis/issues/76)   

## Provenance of data
General

## The ratified convention
The field should be left empty if the source data does not contain a verbatim days_supply, and should not be calculated from other fields.

## Date of ratification/published
Sept 24, 2021 (CDM v5.4 release date)

## Downstream implications
No

## Link to DQD check
No

## Related conventions/further information
NA
