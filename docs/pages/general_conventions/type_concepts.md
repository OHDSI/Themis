---
title: Patient reported data
keywords: provenance
last_updated: April 29, 2024
tags: [pro, patient_reported]
sidebar: mydoc_sidebar
permalink: /type_concepts.html
---


## Issue # and location
For this ratified convention, the issue number given when the issue was created by GitHub. Was this a CDM issue, Themis issue, found in CDM documentation or found on the forum?

Format as follows:
- [Themis issue #25](https://github.com/OHDSI/Themis/issues/25)


## Issue summary
What should be done with patient reported clinical events?

## Convention type
Global 

## CDM table
NA

## CDM field
All *_type_concept_id fields in the CDM

## Links to issue discussion
Links to location of discussion on forums, CDM GitHub, Themis GitHub, etc.

Format as follows:
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/patient-reported-drugs-and-conditions/3152/28)
- [Themis issue #25](hhttps://github.com/OHDSI/Themis/issues/25)   

## Provenance of data
EHR

## The ratified convention
Patient reported data should be inserted into the appropriate domain table (e.g. if a patient reports they had lymphoma, it should be inserted into the CONDITION_OCCURRENCE table or if a patient reports using ibuprofen, it should be inserted into the DRUG_EXPOSURE table). Use concept_id = 32865, "Patient self-report" to identify these records.

## Date of ratification/published
June 5, 2018

## Downstream implications
NO

## Link to DQD check
NA

## Related conventions/further information
