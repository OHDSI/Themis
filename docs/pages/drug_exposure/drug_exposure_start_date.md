---
title: What date should be used to populate drug_exposure_start_date?
keywords: drug, drug exposure start date
last_updated: April 16, 2024
tags: [drug_exposure, dates]
sidebar: mydoc_sidebar
permalink: /drug_exposure_start_date.html
---

## Issue # and location
[Themis issue #110](https://github.com/OHDSI/Themis/issues/110)

## Issue summary
Since drug exposure records may have multiple dates associated, which date should be used as the drug_exposure_start_date?

## Convention type
Table

## CDM table
`DRUG_EXPOSURE`

## CDM field
`drug_exposure_start_date`

## Links to issue discussion
[CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)   

## Provenance of data
EHR

## The ratified convention
- For prescriptions take the date the prescription was filled
- For administrations take the date the drug administration was recorded
- For orders take the date the drug was ordered

## Date of ratification/published
NA

## Downstream implications
NA

## Link to DQD check
No

## Related conventions/further information
NA
