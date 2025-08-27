---
title: How to handle multiple races or ethnicities per person
keywords: race, ethnicity
last_updated: April 16, 2024
tags: [race, ethnicity]
sidebar: mydoc_sidebar
permalink: /multiple_races_per_person.html
---

## Issue # and location

- [Themis issue #71](https://github.com/OHDSI/Themis/issues/71)

## Issue summary

Data sources might have more than one race value per a person, have more than one source with differing race values or have a source value semantically equivalent to “multiple race” (I.e. multi-racial, > 1 race, etc.)

## Convention type
Table

## CDM table
`OBSERVATION`

## CDM field
`PERSON.race_concept_id`, `OBSERVATION.observation_concept_id`, `OBSERVATION.value_as_concept_id`

## Links to issue discussion
- [OHDSI Forums discussion #1](https://forums.ohdsi.org/t/race-and-ethnicity-in-the-omop-cdm/8700/33)
- [OHDSI Forums discussion #2](https://forums.ohdsi.org/t/dealing-with-multiple-races-and-other-exceptions/20091/85)   

## Provenance of data
All data

## The ratified convention
**Where do the data go?**

•If your data has only one race source value, then map this to PERSON.race_concept_id
*Example:* There is one race source value, ‘Black or African American’, for a person. Then PERSON.race_concept_id = 8516, ‘Black or African American’

•If your data has > 1 race source value
	1. Use 1546847, [‘More than one race’](https://athena.ohdsi.org/search-terms/terms/1546847), to populate PERSON.race_concept_id
	2. In the Observation table, populate OBSERVATION.observation_concept_id = 4013886, ‘Race’. THEN populate OBSERVATION.value_as_concept_id with the concept_id for the person’s race. Create as many records for a person as the source data have.

*Example:* There are two source race values for a person: ‘Asian’ and ‘White’. You will create two records in the Observation table:
	Record #1: OBSERVATION.observation_concept_id = 4013886, ‘Race’ AND OBSERVATION.value_as_concept_id = 8515, ‘Asian’
	Record #2: OBSERVATION.observation_concept_id = 4013886, ‘Race’ AND OBSERVATION.value_as_concept_id = 8527, ‘White’

**What do I do if my race source value isn’t present as a standard concept_id with domain_id = ‘Race’?**

•If you have race source values which don’t map to a standard concept_id with domain_id = ‘Race’, create an issue in the [Themis Github](https://github.com/OHDSI/Themis/issues). 

**What date do I put into the OBSERVATION.observation_date for the records?**

•The OBSERVATION.observation_date represents the date in which the fact was recorded. IF your source data do not have a date associated with the record or the visit in which the fact was recorded, THEN use the date of the most recent visit record for a person. Logic for this decision: We never use default dates far in the past or future because this will make our Observation Period erroneously long. The same goes for birth date. It is against CDM rules to leave this field NULL. So, since we don’t know when the fact was recorded, but do know when the person had their most recent visit with the health system, we use this date. It’s not perfect, but neither are race data. And this is the best approximation taking into consideration the requirements of the CDM and limitations of the source data.

**What do I do with flavors of NULL?**

•If your data include race source values such as: ‘unknown’, ‘unspecified’, ‘patient refused to answer’, etc.; don’t bring these data into the CDM. 
*Example:* If a person only has one race source value and it is a flavor of NULL, then PERSON.race_concept_id = 0

•IF your data have one valid race source value and one flavor of NULL race source value, THEN create only one record in the Person table.
*Example:* There are two race source values for a person: ‘American Indian or Alaskan Native’ and ‘Unknown’. PERSON.race_concept_id = 8657

## Date of ratification/published
NA

## Downstream implications
No

## Link to DQD check
- [isRequired](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isRequired.html)
- [cdmDatatype](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#cdmdatatype)
- [isForeignKey](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#isforeignkey)
- [fkDomain](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#isforeignkey)
- [isStandardValidConcept](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#isstandardvalidconcept)
- [standardRecordConceptCompleteness](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#standardConceptRecordCompleteness)

## Related conventions/further information
If you have a research use case for race or ethnicity data which isn't covered by the conventions above, please create an issue in the [Themis Github](https://github.com/OHDSI/Themis/issues). 
