---
title: What date is meant to be put in verbatim_end_date?
keywords: drug, drug exposure end date
last_updated: April 16, 2024
tags: [drug_exposure, dates]
sidebar: mydoc_sidebar
permalink: /populate_verbatim_end_date.html
---

## Issue # and location
- [CDM_documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)


## Issue summary
There are several "end" dates in the drug_exposure table: drug_exposure_end_date, drug_exposure_end_datetime and verbatim_end_datetime. It is unclear how/when verbatim_end_date should be stored.

## Convention type
Table

## CDM table
`DRUG_EXPOSURE`

## CDM field
`verbatim_end_date`

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/drug-exposure-quantity-recalculation/9607/4)
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/the-difference-between-verbatim-end-date-and-drug-exposure-end-date-in-drug-exposure-table-of-v5-2/3281/2)

## Provenance of data
General

## The ratified convention
verbatim_end_date represents the "discontinue day" or date the physician explicitly stopped the medication.
Populate the field only when it is directly defined in the source as a date. If this is not available, then leave the field blank.

## Date of ratification/published
NA

## Downstream implications
NA

## Link to DQD check
NA

## Related conventions/further information
NA