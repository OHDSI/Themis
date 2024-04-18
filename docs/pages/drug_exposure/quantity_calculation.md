---
title: Should quantity be recalculated if the patient discontinues the drug?
keywords: drug, drug_exposure, quantity
last_updated: April 16, 2024
tags: [drug_exposure, quantity]
sidebar: mydoc_sidebar
permalink: /quantity_calculation.html
---

## Issue # and location

- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)
- [Forum](https://forums.ohdsi.org/t/drug-exposure-quantity-recalculation/9607/6)

## Issue summary

Patients can choose to discontinue drugs, this can make the quantity of a drug inconsistent with the duration exposed. The question then becomes, should drug_exposure.quantity be recalculated if a patient discontinues a drug?

## Convention type
Table

## CDM table
`DRUG_EXPOSURE`

## CDM field
`quantity`

## Links to issue discussion
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)
- [Forum](https://forums.ohdsi.org/t/drug-exposure-quantity-recalculation/9607/6)

Format as follows:
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/drug-exposure-quantity-recalculation/9607)
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)   

## Provenance of data
General, all types of data

## The ratified convention
The quantity should represent the actual quantity of the drug dispensed and should not be recalculated/inferred based on dates if a patient discontinues a drug.

## Date of ratification/published


## Downstream implications
No

## Link to DQD check
No

## Related conventions/further information
NA