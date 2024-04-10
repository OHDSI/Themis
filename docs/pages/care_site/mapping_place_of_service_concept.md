--- 
title: How to populate the place_of_service_concept_id in the CARE_SITE table 
keywords: care_site, place_of_service, place of service, place_of_service_concept_id, place of service concept id 
last_updated: April 10, 2024 
tags: [care_site, place_of_service, visit_concept_id] 
sidebar: mydoc_sidebar 
permalink: /mapping_place_of_service_concept.html 
--- 

## Issue # and location

- [Themis issue #99](https://github.com/OHDSI/Themis/issues/99)

## Issue summary
If a care site has multiple types of visits or care associated with it, it is unclear which place of service concept should be used to appropriately represent the setting of care.

## Convention type
Table

## CDM table
`CARE_SITE`

## CDM field
`place_of_service_concept_id`

## Links to issue discussion

- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#care_site)   

## Provenance of data
General, any database with care site information

## The ratified convention

Choose the concept in the visit domain that best represents the setting in which healthcare is provided in the Care Site. If most visits in a Care Site are Inpatient, then the place_of_service_concept_id should represent Inpatient. If information is present about a unique Care Site (e.g. Pharmacy) then a Care Site record should be created.

It is also possible to set a specific visit_concept_id in the VISIT_OCCURRENCE table that represents the exact setting of care for that visit, which may differ from the place_of_service_concept_id in the CARE_SITE table. For example, a patient may go to an inpatient hospital for an outpatient procedure. In this case, the hospital entry in the care_site table should identify it as an inpatient hospital but the specific visit_concept_id for the outpatient procedure should identify that it was an outpatient encounter.

In an EHR system the care site can represent a department rather than the institution as a whole.

## Date of ratification/published
Nov 27, 2018

## Downstream implications
No

## Link to DQD check
No. The [isPrimaryKey](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isPrimaryKey.html) check will make sure the care site ids are not duplicated in the CARE_SITE table but there is no explicit check for the same care_site_source_value and different place_of_service_concept_ids. 

## Related conventions/further information
Interesting to note that there is an open issue about retaining this field and the place_of_service_source_value in the model: Remove place_of_service_concept_id and source_value from CARE_SITE [CommonDataModel #273](https://github.com/OHDSI/CommonDataModel/issues/273)
