---
title: Duplicate National Provider Identifiers 
keywords: provider, npi
last_updated: April 29, 2024
tags: 
summary: "What to do when two different providers have the same NPI."
sidebar: mydoc_sidebar
permalink: /duplicate_npi.html
---

## Issue # and location
[Themis issue #44](https://github.com/OHDSI/Themis/issues/44)

## Issue summary
While we should only have one records per provider in the PROVIDER table it is possible for the NPI to be duplicated.

## Convention type
Table

## CDM table
`PROVDER`

## CDM field
NA

## Links to issue discussion
- [NPI for Multiple Physicians #44](https://github.com/OHDSI/Themis/issues/44)
- [Multiple Provider Specialities #43](https://github.com/OHDSI/Themis/issues/43)
  - This states we can only have one record
- [CDM GitHub.io PROVIDER](https://ohdsi.github.io/CommonDataModel/cdm53.html#provider)
- [Mapping Facility NPI #s into the Care_Site table? ](https://forums.ohdsi.org/t/mapping-facility-npi-s-into-the-care-site-table/13395)
  - Although this is about CARE_SITES not providers
- [Provider table ](https://forums.ohdsi.org/t/provider-table/5494)
 - Seems to be a fair amount of discussion about what happens when you have multiple records for one provider with same NPI

## Provenance of data
General

## The ratified convention
The PROVIDER table contains a list of uniquely identified healthcare providers. However, duplicate NPI numbers may occur because the source data might provide the NPI representing the care site rather than the individual provider's NPI.  NPI should not represent a primary key within the PROVIDER table.

## Date of ratification/published
June 2018

## Downstream implications
NA

## Link to DQD check
NA

## Related conventions/further information
- NPI = National Provider Identifier
- not a primary key, it can be duplicated, but each provider should only have one record in the provider table.
- provider THEMIS rule , NPI THEMIS rule