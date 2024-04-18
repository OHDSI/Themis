---
title: Rules for records with values
keywords: measurement, observation, values
last_updated: April 18, 2024
tags: [measurement, lab_values, value_as_number, labs]
sidebar: mydoc_sidebar
permalink: /records_with_values.html
---

## Issue # and location

- [Themis issue #123](https://github.com/OHDSI/Themis/issues/123)
- [Forum Post](https://forums.ohdsi.org/t/measurement-table-are-value-as-concept-id-and-value-as-number-mutually-exclusive/10975)

## Issue summary
For a given record in the MEASUREMENT table, are VALUE_AS_NUMBER and VALUE_AS_CONCEPT_ID mutually exclusive, meaning if one has a value can the other also have a value?

## Convention type
General

## CDM table
`MEASUREMENT`, `OBSERVATION`

## CDM field
`value_as_number`, `value_as_concept_id`

## Links to issue discussion

- [OHDSI Forums discussion](https://forums.ohdsi.org/t/measurement-table-are-value-as-concept-id-and-value-as-number-mutually-exclusive/10975)
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#measurement)   
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/operator-and-value-concept-id-measurement-table-in-cdm/6662)
- [Related THEMIS issue](https://github.com/OHDSI/Themis/issues/11)

## Provenance of data
General

## The ratified convention
Only records where the source value maps to a CONCEPT_ID in the 'Measurement' domain should be included in this table.

For some MEASUREMENT concepts the result is included in the test. For example, ICD10 CONCEPT_ID [45548980](https://athena.ohdsi.org/search-terms/terms/45548980) ‘Abnormal level of unspecified serum enzyme’ indicates a Measurement and the result (abnormal). In those situations, the CONCEPT_RELATIONSHIP table in addition to the ‘Maps to’ record contains a second record with the RELATIONSHIP_ID set to ‘Maps to value’. In this example, the ‘Maps to’ relationship directs to [4046263](https://athena.ohdsi.org/search-terms/terms/4046263) ‘Enzyme measurement’ as well as a ‘Maps to value’ record to [4135493](https://athena.ohdsi.org/search-terms/terms/4135493) ‘Abnormal’.

If the raw data provides categorial results as well as continuous results for measurements, it is a valid ETL choice to preserve both values. Thus, VALUE_AS_NUMBER and VALUE_AS_CONCEPT_ID are not mutually exclusive. The continuous value should go in the VALUE_AS_NUMBER field and the categorical value should be mapped to a standard concept and put in the VALUE_AS_CONCEPT_ID field. For example, it would be feasible to receive a measurement for a LOINC 8867-4-heart rate from a source system that both indicates that a patient experienced a heart rate of 60 beats per minute and this measurement was considered normal. The 60 can be stored in VALUE_AS_NUMBER, the beats per minute in UNIT_CONCEPT_ID (8541-per minute), and finally the "normal" in VALUE_AS_CONCEPT_ID (4069590-Normal).

It is also not mandatory to have one or both VALUE_AS_NUMBER and VALUE_AS_CONCEPT_ID as it is possible for the result to not be given in the source data. When the result is not known, the MEASUREMENT record represents just the fact that the corresponding measurement was carried out, which in itself is already useful information for some use cases.

## Date of ratification/published
Sept 24, 2021 (CDM v5.4 release date)

## Downstream implications
No

## Link to DQD check
NA

## Related conventions/further information
NA
