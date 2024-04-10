---
title: How to determine the drug_exposure_end_date when it is not given explicitly in the data
keywords: drug, date, drug_exposure, drug_exposure_end_date, end date, drug exposure
last_updated: March 27, 2024
tags: [dates, drug_exposure, drug_exposure_end_date]
sidebar: mydoc_sidebar
permalink: /drug_end_date_not_in_data.html
---

## Issue # and location
- [Themis issue #57](https://github.com/OHDSI/Themis/issues/57)
- [CDM issue #156](https://github.com/OHDSI/CommonDataModel/issues/156)

## Issue summary
The drug_exposure_end_date is a required field. How do you determine drug_exposure_end_date when it is not given explicitly in the data?                                                                                                                     

## Convention type
Table

## CDM table
`DRUG_EXPOSURE`                                                                                                            

## CDM field
`drug_exposure_end_date`

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/drug-exposure-quantity-recalculation/9607)
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)       

## Provenance of data
All data                    

## The ratified convention
If the drug end date or stop date is not explicitly available in the data, infer the end date using the following methods:

1.  Start first with duration or days supply using the calculation drug start date + days supply -1 day. 
2.  Use quantity divided by daily dose that you may obtain from the sig or a source field (or assumed daily dose of 1) for solid, indivisibile, drug products. If quantity represents ingredient amount, quantity divided by daily dose * concentration (from drug_strength) drug concept id tells you the dose form. 
3.  If it is an administration record, set drug end date equal to drug start date. 
4.  If the record is a written prescription then set end date to start date + 29. 
5.  If the record is a mail-order prescription set end date to start date + 89. 

**Note:** The end date must be equal to or greater than the start date. Ibuprofen 20mg/mL oral solution concept tells us this is oral solution. Calculate duration as quantity (200 example) * daily dose (5mL) /concentration (20mg/mL) 200*5/20 = 50 days.             

## Date of ratification/published


## Downstream implications
No, this is a current convention. And Atlas, the Dose Era table, and the Drug Era table rely on this field being populated to determine Era's in the Drug Era and Dose Era tables. And Atlas relies on this field being populated to determine the period of time a person was exposed to a drug.                                          

## Link to DQD check
Yes - [isRequired](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isRequired.html).

## Related conventions/further information
