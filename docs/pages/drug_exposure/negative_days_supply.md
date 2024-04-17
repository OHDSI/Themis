---
title: How to populate days_supply when days supply is negative in the source
keywords: drug, drug_exposure, days_supply
last_updated: April 16, 2024
tags: [drug_exposure, days_supply]
sidebar: mydoc_sidebar
permalink: /negative_days_supply.html
---

## Issue # and location

- [Themis issue #76](https://github.com/OHDSI/Themis/issues/76)

## Issue summary
How should drug exposure records with negative days supply be handled in the CDM?

## Convention type
Table

## CDM table
`drug_exposure`

## CDM field
`days_supply`

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/days-supply-yet-again/4741/16)
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)   

## Provenance of data
General

## The ratified convention
The CDM documentation states: Negative values are not allowed. If the source has negative days supply the record should be dropped as it is unknown if the patient actually took the drug.

Several actions are possible: 1) record is not trustworthy and we remove the record entirely. 2) we trust the record and leave days_supply empty or 3) record needs to be combined with other record (e.g. reversal of prescription). High values (>365 days) should be investigated. If considered an error in the source data (e.g. typo), the value needs to be excluded to prevent creation of unrealistic long eras.

## Date of ratification/published
July 5, 2023

## Downstream implications
No

## Link to DQD check

Yes - plausibleValueLow (page under construction) 

## Related conventions/further information
NA
