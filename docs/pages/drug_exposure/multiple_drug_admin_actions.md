---
title: How to populate drug_exposure from drug administration data when there are multiple actions (like drug given, on hold, rate changed, stopped etc)
keywords: drug, drug_exposure, drug administration, on hold, rate changed, drug stopped
last_updated: April 16, 2024
tags: [drug_exposure, drug_administration]
sidebar: mydoc_sidebar
permalink: /multiple_drug_admin_actions.html
---

## Issue # and location

- [Themis issue #108](https://github.com/OHDSI/Themis/issues/108)

## Issue summary

In EHR data for drug administration data, there are often multiple actions (like drug given, on hold, rate changed, stopped etc) recorded for the same drug administered to the patient. The CDM does not record a status on drug records, so how should these actions be modeled?

## Convention type
Table

## CDM table
`DRUG_EXPOSURE`

## CDM field
NA

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/drug-administration-records-in-drug-exposure-table/18950/3)
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/how-to-map-drug-frequency-contraindications-administration-actions-in-omop/19741)   

## Provenance of data
EHR

## The ratified convention
- The OMOP CDM is only interested in events that happen to the patient (i.e include actions that suggest the drug was administered to the patient). If a patient missed or refused a dose of medication, then a record should not be created in the CDM.
- When the rate changes, you end the first record and start the 2nd record with then new quantity of medication a person receives.
- Administrations should use the appropriate drug_type_concept_id [Accepted Concepts(https://athena.ohdsi.org/search-terms/terms?domain=Type+Concept&standardConcept=Standard&page=1&pageSize=15&query=)

## Date of ratification/published
NA

## Downstream implications
No

## Link to DQD check
No

## Related conventions/further information
NA