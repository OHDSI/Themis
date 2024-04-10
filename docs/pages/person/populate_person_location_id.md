---
title: How to populate location_id in the PERSON table
keywords: location, address
last_updated: April 10, 2024
tags: [location, location_id, address]
sidebar: mydoc_sidebar
permalink: /populate_person_location_id.html
---

## Issue # and location
NA

## Issue summary
How should the location_id be used to represent the location of a person?
What level of information should be included when modeling the person's location?

## Convention type
Table

## CDM table
`PERSON`

## CDM field
`location_id`

## Links to issue discussion
NA

## Provenance of data
All

## The ratified convention
The location_id in the PERSON table should represent the most granular level of information available for the person's home address, or where they live the majority of the time.

This could represent anything from postal code or parts thereof, state, or county for example. Since many databases contain de-identified data, it is common that the precision of the location is reduced to prevent re-identification.

## Date of ratification/published


## Downstream implications
No

## Link to DQD check

[isForeignKey](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isForeignKey.html).

## Related conventions/further information