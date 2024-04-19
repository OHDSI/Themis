---
title: Missing visit end datetime
keywords: visit, visit end date, visit end datetime
last_updated: April 18, 2024
tags: [visit_occurrence, visit_end_datetime, dates, datetime]
sidebar: mydoc_sidebar
permalink: /missing_visit_end_datetime.html
---

## Issue # and location
[Themis issue #128](https://github.com/OHDSI/Themis/issues/128)

## Issue summary
We have visit start datetime data at the source, but not end datetime. Is it ok to leave `visit_end_datetime` null when `visit_start_datetime` is populated?

## Convention type
Table

## CDM table
`VISIT_OCCURRENCE`

## CDM field
`visit_end_datetime`

## Links to issue discussion
NA 

## Provenance of data
General

## The ratified convention
`visit_end_datetime` is not a required field. Therefore, it is ok to leave `visit_end_datetime` null when `visit_start_datetime` is populated.

NOTE - while `visit_end_datetime` is not required, `visit_end_date` is. This convention applies to the datetime field only.

## Date of ratification/published
NA

## Downstream implications
NA

## Link to DQD check
NA

## Related conventions/further information
NA