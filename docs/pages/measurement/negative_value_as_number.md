---
title: Can values in the value_as_number field be negative?
keywords: labs, lab values
last_updated: APril 10, 2024
tags: [labs, lab_values, value_as_number, negative]
sidebar: mydoc_sidebar
permalink: /negative_value_as_number.html
---

## Issue # and location

- [Themis issue #16](https://github.com/OHDSI/Themis/issues/16)
- [CDM issue #532](https://github.com/OHDSI/CommonDataModel/issues/532)

## Issue summary
Can VALUE_AS_NUMBER be negative?

## Convention type
Table

## CDM table
`MEASUREMENT`

## CDM field
`value_as_number`

## Links to issue discussion
- [Themis issue #16](https://github.com/OHDSI/Themis/issues/16)
- [CDM issue #532](https://github.com/OHDSI/CommonDataModel/issues/532)  
- [Forum](https://forums.ohdsi.org/t/negative-values-in-lab-test-records/4012) 

## Provenance of data
General

## The ratified convention
Only allow values for negative measurements (see list below). If you have negative values for positive measurements, then set it to NULL.

### Negative Measurements


concept_id | concept_name | concept_code 
|:--------|:-------|:------|
|----
3003396 | Base excess in Arterial blood by calculation | 1925-7
3004959 | Base excess in Arterial cord blood by calculation | 28638-5
3012501 | Base excess in Blood by calculation | 11555-0
3003129 | Base excess in Capillary blood by calculation | 1926-5
3002032 | Base excess in Venous blood by calculation | 1927-3
3007435 | Base excess in Venous cord blood by calculation | 28639-3
3051343 | DXA Bone [Mass/Area] Bone density | 46383-6
21494211 | DXA Calcaneus - left [Mass/Area] Bone density | 80956-6
21494205 | DXA Calcaneus - left [T-score] Bone density | 80950-9
21492970 | DXA Calcaneus - left [Z-score] Bone density | 80942-6
21494210 | DXA Calcaneus - right [Mass/Area] Bone density | 80955-8
21494204 | DXA Calcaneus - right [T-score] Bone density | 80949-1
21492969 | DXA Calcaneus - right [Z-score] Bone density | 80941-8
3052504 | DXA Calcaneus [Mass/Area] Bone density | 38262-2
3049581 | DXA Calcaneus [T-score] Bone density | 38266-3
21494209 | DXA Femur - left [Mass/Area] Bone density | 80954-1
21494203 | DXA Femur - left [T-score] Bone density | 80948-3
21492968 | DXA Femur - left [Z-score] Bone density | 80940-0
21494208 | DXA Femur - right [Mass/Area] Bone density | 80953-3
21494202 | DXA Femur - right [T-score] Bone density | 80947-5
21494199 | DXA Femur - right [Z-score] Bone density | 80939-2
3021722 | DXA Femur [Mass/Area] Bone density | 24701-5
3051450 | DXA Femur [T-score] Bone density | 38263-0
21494100 | DXA Femur [Z-score] Bone density | 80934-3
3051938 | DXA Hip - left [Mass/Area] Bone density | 46278-8
21494201 | DXA Hip - left [T-score] Bone density | 80946-7
21494198 | DXA Hip - left [Z-score] Bone density | 80938-4
3049418 | DXA Hip - right [Mass/Area] Bone density | 46279-6
21494200 | DXA Hip - right [T-score] Bone density | 80945-9
21494197 | DXA Hip - right [Z-score] Bone density | 80937-6
3052486 | DXA Hip [Mass/Area] Bone density | 38261-4
3049278 | DXA Hip [T-score] Bone density | 38264-8
21494099 | DXA Hip [Z-score] Bone density | 80933-5
36203243 | DXA Humerus - left [Mass/Area] Bone density | 85386-1
36203246 | DXA Humerus - left [T-score] Bone density | 85389-5
36204416 | DXA Humerus - left [Z-score] Bone density | 85393-7
36203244 | DXA Humerus - right [Mass/Area] Bone density | 85387-9
36203245 | DXA Humerus - right [T-score] Bone density | 85388-7
36204415 | DXA Humerus - right [Z-score] Bone density | 85392-9
36203242 | DXA Humerus [Mass/Area] Bone density | 85385-3
36204445 | DXA Humerus [T-score] Bone density | 85390-3
36204414 | DXA Humerus [Z-score] Bone density | 85391-1
3033804 | DXA Lumbar spine [Mass/Area] Bone density | 24966-4
3049654 | DXA Lumbar spine [T-score] Bone density | 38267-1
36204417 | DXA Lumbar spine [Z-score] Bone density | 85394-5
21494207 | DXA Radius and Ulna - left [Mass/Area] Bone density | 80952-5
21492972 | DXA Radius and Ulna - left [T-score] Bone density | 80944-2
21494196 | DXA Radius and Ulna - left [Z-score] Bone density | 80936-8
21494206 | DXA Radius and Ulna - right [Mass/Area] Bone density | 80951-7
21492971 | DXA Radius and Ulna - right [T-score] Bone density | 80943-4
21494101 | DXA Radius and Ulna - right [Z-score] Bone density | 80935-0
3002101 | DXA Radius and Ulna [Mass/Area] Bone density | 24890-6
3049273 | DXA Radius and Ulna [T-score] Bone density | 38265-5
21494098 | DXA Radius and Ulna [Z-score] Bone density | 80932-7
3006277 | QRS axis | 8632-2
3028303 | QRS axis.frontal plane Reference beat | 18517-3
3025448 | QRS axis.horizontal plane Reference beat | 18507-4
|======

A comma delimited list of CONCEPT_IDs: `3003396,3004959,3012501,3003129,3002032,3007435,3051343,21494211,21494205,21492970,21494210,21494204,21492969,3052504,3049581,21494209,21494203,21492968,21494208,21494202,21494199,3021722,3051450,21494100,3051938,21494201,21494198,3049418,21494200,21494197,3052486,3049278,21494099,36203243,36203246,36204416,36203244,36203245,36204415,36203242,36204445,36204414,3033804,3049654,36204417,21494207,21492972,21494196,21494206,21492971,21494101,3002101,3049273,21494098,3006277,3028303,3025448`

## Date of ratification/published
Jul 9, 2018

## Downstream implications
No

## Link to DQD check
Unsure if this is a current check

## Related conventions/further information
This may be an incomplete list of concepts that allow negative values, please open an issue on the [THEMIS github](https://github.com/ohdsi/Themis) if you believe there are others that should be added. 
