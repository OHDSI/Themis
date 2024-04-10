---
title: How to populate gender_concept_id
keywords: gender, gender concept id, gender_concept_id, sex
last_updated: April 10, 2024
tags: [gender, gender_concept_id, sex, gender_identity]
sidebar: mydoc_sidebar
permalink: /populate_gender_concept_id.html
---

## Issue # and location

- [Themis issue #94](https://github.com/OHDSI/Themis/issues/94)

## Issue summary
The term "gender_concept_id" is outdated and really should be "sex_concept_id". Since changing gender_concept_id is a huge lift for developers and package maintainers, this change will be implemented at the next major release. In the meantime, what value should be used to populate gender_concept_id?

## Convention type
Table

## CDM table
`PERSON`

## CDM field
`gender_concept_id`

## Links to issue discussion

- [OHDSI Forums discussion #1](https://forums.ohdsi.org/t/can-we-migrate-from-gender-to-sex-please/18875/22)
- [OHDSI Forums discussion #2](https://forums.ohdsi.org/t/can-we-migrate-from-gender-to-sex-please/18875)   

## Provenance of data
All data

## The ratified convention
PERSON.gender_concept_id should hold the standard concept representing the patient's assigned sex at birth

## Date of ratification/published
NA

## Downstream implications
NA

## Link to DQD check

[isRequired](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isRequired.html)
[cdmDatatype](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#cdmdatatype)
[isForeignKey](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#isforeignkey)
[fkDomain](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#isforeignkey)
[isStandardValidConcept](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#isstandardvalidconcept)
[standardRecordConceptCompleteness](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#standardConceptRecordCompleteness)


## Related conventions/further information
If the source data captures gender identity it should be stored in the [OBSERVATION](https://ohdsi.github.io/CommonDataModel/cdm531.html#observation) table. See the [gender identity](gender_identity.html) convention for more information.
