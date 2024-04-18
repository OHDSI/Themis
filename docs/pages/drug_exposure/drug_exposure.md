---
title: DRUG_EXPOSURE
keywords: drug, drug_exposure, drug exposure
last_updated: March 27, 2024
tags: [drug_exposure]
summary: "Conventions related to mapping data into the DRUG_EXPOSURE table."
sidebar: mydoc_sidebar
permalink: /drug_exposure.html
---

## Table-level Conventions


## Field-level Conventions

| **Field** | **Convention** |
|:--------|:-------|
| DRUG_EXPOSURE_START_DATE   | [What date should be used to populate drug_exposure_start_date?](drug_exposure_start_date.html)   |
|----
| DRUG_EXPOSURE_END_DATE   | [How to determine drug_exposure_end_date when not given explicitly in the data](drug_end_date_not_in_data.html)   |
|----
| DAYS_SUPPLY   | [How to populate days_supply when days supply is missing in the source data](missing_days_supply.html)    |
|----
| DAYS_SUPPLY   | [How to populate days_supply when days supply is negative in the source data](negative_days_supply.html)    |
|----
| QUANTITY      | [Should quantity be recalculated if the patient discontinues the drug?](quantity_calculation.html) |
|----
| VERBATIM_END_DATE | [What date is meant to be put in verbatim_end_date?](populate_verbatim_end_date.html) |
|=====