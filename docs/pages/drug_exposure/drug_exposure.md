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
| DRUG_EXPOSURE_END_DATE   | [How to determine drug_exposure_end_date when not given explicitly in the data](drug_end_date_not_in_data.html)   |
|----
| DAYS_SUPPLY   | [How to populate days_supply when days supply is missing in the source data](missing_days_supply.html)    |
|----
| DAYS_SUPPLY   | [How to populate days_supply when days supply is negative in the source data](negative_days_supply.html)    |
|----
| QUANTITY      | [Should quantity be recalculated if the patient discontinues the drug?](quantity_calculation.html) |
|=====