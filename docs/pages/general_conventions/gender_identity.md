---
title: How to map gender identity
keywords: gender, gender identity, sex
last_updated: April 10, 2024
tags: [gender, gender_identity, sex]
sidebar: mydoc_sidebar
permalink: /gender_identity.html
---

## Issue # and location
- [Themis issue #102]([#102](https://github.com/OHDSI/Themis/issues/102))

## Issue summary
The term "gender_concept_id" is outdated and really should be "sex_concept_id". Since changing gender_concept_id is a huge lift for developers and package maintainers, this change will be implemented at the next major release. In the meantime, how should gender identity be stored in the CDM?

## Convention type
Global

## CDM table
NA

## CDM field
NA

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/can-we-migrate-from-gender-to-sex-please/18875)

## Provenance of data
Applies to any database that captures gender identity, regardless of provenance

## The ratified convention
Any gender-related information that can change over time, like gender identify, should be put in the OBSERVATION table.

## Date of ratification/published
Sept 24, 2021 

## Downstream implications
No

## Link to DQD check
Yes, [fkDomain](https://ohdsi.github.io/DataQualityDashboard/articles/checks/fkDomain.html)

## Related conventions/further information
[Related to issue #94](https://github.com/OHDSI/Themis/issues/94)