---
title: How to handle One-to-Many Mappings
keywords: mapping, vocabulary
last_updated: April 29, 2024
tags: 
summary: "What to do when a source codes maps to two standard concepts."
sidebar: mydoc_sidebar
permalink: /one_to_many_mapping.html
---

## Issue # and location
- [Themis issue #162]([#162](https://github.com/OHDSI/Themis/issues/162))

## Issue summary
Mapping of disease, diagnosis or problem concepts to the condition table may not be 1:1 with standard concepts.

## Convention type
Global

## CDM table
NA

## CDM field
NA

## Links to issue discussion
- [OHDSI Forums discussion 1](https://forums.ohdsi.org/t/duplicate-concept-ids-for-different-condition-concept-ids/9336)
- [OHDSI Forums discussion 2](https://forums.ohdsi.org/t/one-condition-maps-to-2-condition-concept-id-what-to-do/2968)
- [OHDSI Forums discussion 3](https://forums.ohdsi.org/t/family-history-extension-model/17947/7)

## Provenance of data
General, All

## The ratified convention
Condition concepts are primarily mapped to SNOMED CT for standard concepts. Some concepts like Oncology diagnoses might be mapped to ICD-O. When mapping, source concepts should be mapped fully to standard concepts even if it requires more than one code. In such cases, two records should be created in the CDM, one for each standard concept. If the source system already maps to standard codes use them, rather than mapping first to ICD and then map to SNOMED. Additional information can be found [here](https://ohdsi.github.io/CommonDataModel/dataModelConventions.html#Source_Values,_Source_Concept_Ids,_and_Standard_Concept_Ids).


## Date of ratification/published
NA

## Downstream implications
No

## Link to DQD check

- [standardConceptRecordCompleteness](https://ohdsi.github.io/DataQualityDashboard/articles/CheckTypeDescriptions.html#standardConceptRecordCompleteness)

## Related conventions/further information
NA