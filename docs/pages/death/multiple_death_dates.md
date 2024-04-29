---
title: Multiple Death Dates
keywords: multiple deaths, death
last_updated: April 29, 2024
tags: [death_date]
summary: "How to map multiple death dates per person."
sidebar: mydoc_sidebar
permalink: /multiple_death_dates.html
---

## Issue # and location
[Themis issue #155](https://github.com/OHDSI/Themis/issues/155)

## Issue summary
Handling multiple deaths on different days

## Convention type
Table

## CDM table
`DEATH`

## CDM field
NA

## Links to issue discussion
- [OHDSI Forums discussion](https://forums.ohdsi.org/t/multiple-deaths-on-different-days/4552)
- [Themis GitHub](https://github.com/OHDSI/Themis/issues/6)

## Provenance of data
General

## The ratified convention
Only one death date per individual can be used. If a patient has clinical activity (e.g. prescriptions filled, labs performed, etc) more than 60+ days after death you may want to drop the death record as it may have been falsely reported. If multiple records of death exist on multiple days you may select the death that you deem most reliable (e.g. death at discharge) or select the latest death date.

## Date of ratification/published
June 2018

## Downstream implications
This convention is important for survival studies. Having multiple deaths per person in the death table is not expected, and would lead to double counting of deaths.

## Link to DQD check
Currently, there is no DQD check for uniqueness of person_id in death table. We should implement this (i.e. enable `isPrimaryKey` for death.person_id)

## Related conventions/further information
NA