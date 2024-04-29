---
title: Events Outside Observation Period
keywords: observable time, observation period
last_updated: April 29, 2024
tags: [observation_period]
summary: "Conventions related to mapping data with dates outside of the observation period."
sidebar: mydoc_sidebar
permalink: /events_outside_obs_period.html
---

## Issue # and location

- [Themis issue #23](https://github.com/OHDSI/Themis/issues/23)

## Issue summary
In databases with defined enrollment that is used to define the observation period, it is possible for there to be events observed outside of the observation period. What should be done with these events?

## Convention type
Global

## CDM table
NA

## CDM field
NA

## Links to issue discussion

- [OHDSI Forums discussion](https://forums.ohdsi.org/t/patient-medical-history-events-outside-observation-period/6945)
- [CDM Documentation](https://ohdsi.github.io/CommonDataModel/cdm54.html#drug_exposure)   

## Provenance of data
General

## The ratified convention
Events CAN fall out of observation period but they cannot be used to identify people in a cohort (as the index date). 

## Date of ratification/published
Oct 2, 2018

## Downstream implications
No

## Link to DQD check

Yes - plausibleTemporalAfter (page under construction)

## Related conventions/further information
This is related to the convention that every person in the CDM has to have at least one observation period. 
