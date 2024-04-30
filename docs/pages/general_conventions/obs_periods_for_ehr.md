---
title: Observation Periods for EHR Data
keywords: observation period
last_updated: April 29, 2024
tags: [observation_period]
summary: "How to define observation periods for EHR data."
sidebar: mydoc_sidebar
permalink: /obs_periods_for_ehr.html
---

## Observation Period Start Date

- Generally an Observation Period does NOT begin before birth, however, it might begin before birth IF the pregnant mother receives care recorded in your EHR. The child’s record is then split from the mother’s record at birth but may retain care given during pregnancy. For these children in your dataset, the field **observation_period_start_date should be the birth date minus 9 months**
- An **Observation Period does NOT begin before the implementation of the EHR at your site**. Any records prior to implementation are probably “history of” record types and not a complete EHR record of clinical events.
- Special consideration should be given to migration from previous EHR, implementation at different sites within your healthcare system, implementation of different modules, etc.

## Observation Period end date

Set the **observation_period_end_date** as the first date from the following:

- **Date of death + 60 days** 
  - This is a CDM convention to allow events after death (autopsy, final notes, etc). 
- **Last clinical event + 60 days** 
  - The assumption is that  person will return to the same health provider if an adverse reaction/complication/unresolved condition occurs. 
- **Date of the data pull from the system**

## Observation Period Gaps and Persistence Windows 

### Observation Period Gaps 

Periods of time when a Person does not receive care from your institution and therefore is not observed and should not have an Observation Period. These gaps are usually hard to determine because most Persons don’t announce their departure from an EHR/healthcare institution. Therefore, a heuristic will need to be instituted to determine Observation Period Gaps where the information is not explicit. 

### Observation Period Persistence Window

Defined as the maximum time allowed between two clinical events under the assumption a Person would have a clinical event recorded, if they are not healthy and seek care.

**Example:** Person 1 has a series of clinical events recorded from **Jan. 1, 2010 to June 15, 2012**, where the time between clinical events does not exceed 60 days. The next clinical event for Person 1 is on **Oct. 1, 2018**. Starting Oct. 1, 2018 Person 1 has clinical events occurring at least every 90 days up to the present date.

There is a 6+ year gap between groups of clinical events recorded in the CDM. After discussion in the EHR WG, we believe this 6+ year gap is indicative of a Person not being seen within our EHR/healthcare institution. Per convention #4 for Observation Period table, “As a general assumption, during an Observation Period any clinical event that happens to the patient is expected to be recorded. Conversely, the absence of data indicates that no clinical events occurred to the patient." Person 1 has two Observation Periods. 

**1st Observation Period**

- observation_period_start_date = **01/01/2010** 
- observation_period_end_date = **08/15/2012** (Per the end_date guideline above)

**2nd Observation Period**

- observation_period_start_date = **10/01/2018**
- observation_period_end_date = **09/01/2020** (Date of the data pull, per the end_date guideline above)


Now, there are cases where a Person only receives care within you EHR system when absolutely necessary. And if your EHR doesn’t offer primary care services, the majority of Persons who lack healthcare insurance or any other reason why Persons are only seen in urgent or emergent situations, the above heuristic might be too restrictive. This is a guideline. A question the EHR WG debated was how long between clinical events should we assume any clinical event that happens to the Person is expected to be recorded? When should we end one Observation Period and begin another? What should be the time between events for an Observation Period Persistence Window? Wellness checkups/Visits happen approximately every 12-18 months depending on a multitude of factors. 

**Our recommendation: If Observation Period Gaps are 548 days or more, then the previous Observation Period should end and another Observation Period should begin on the date of the next clinical event as per the Person 1 example above.** 

## Additional ETL considerations

- Implementation of your EHR, migration from previous EHR, implementation at different sites within your healthcare system, implementation of different modules
- Coverage of your healthcare system within your area, population served by the healthcare system
- All decisions should be tempered by local understanding of patients in the EHR you are ETLing.

The Observation Period can be created by only one clinical event. However, the clinical event must NOT be from the Death table. If a Death date does not have any other clinical records 18 months before AND 18 months after the death date, then an Observation Period will not be created. We believe this logic is needed because if a Person only has a death death_date without other clinical event records, a Person is most likely not being “observed” when the death occurred. If a Person was being observed at their time of death, then other records (visit, condition, measurement, etc.) would be created. This rule is most relevant for those with death registry data since a Person who dies in the hospital has many clinical event records.
