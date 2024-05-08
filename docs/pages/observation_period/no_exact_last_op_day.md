---
title: Resolving Observation Period End Date without Exact Information on a Last Day
keywords: observation period, survival, end date
last_updated: April 30, 2024
tags: [observation_period, dates]
summary: "Resolving observation period end date without exact information on a last day"
sidebar: mydoc_sidebar
permalink: /no_exact_last_op_day.html
---

## Issue # and location
[Themis Issue #106](https://github.com/OHDSI/Themis/issues/106)

## Issue Summary
Resolving `observation_period_end_date` without exact information on a last day

## Convention type
Table 

## CDM table
`OBSERVATION_PERIOD`

## CDM field
`observation_period_end_date`

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/resolving-observation-period-end-date-without-exact-information-on-a-last-day/13048)
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#observation_period)

## Provenance of data
General

## The ratified convention
It is often the case that the idea of Observation Periods does not exist in source data. In those cases, the `observation_period_end_date` can be inferred as the last event date available for the person.

## Date of ratification/published
NA

## Downstream implications
This convention can lead to a bias in survival studies. Namely, healthy persons will have shorter observation periods and not contributing to survival time as much.

## Link to DQD check
No

## Related conventions/further information
NA
