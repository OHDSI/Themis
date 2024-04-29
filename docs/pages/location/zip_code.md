---
title: What value to store in the zip field?
keywords: zip, zip code, address, post code
last_updated: April 18, 2024
tags: [address, zip, postcode]
sidebar: mydoc_sidebar
permalink: /zip_code.html
---

## Issue # and location

- [Forum post](https://forums.ohdsi.org/t/non-us-location-geography-hierarchy/1628/2)

## Issue summary
Zip codes are handled as strings of up to 9 characters length. For US addresses, these represent either a 3-digit abbreviated Zip code as provided by many sources for patient protection reasons, the full 5-digit Zip or the 9-digit (ZIP + 4) codes. Unless for specific reasons analytical methods should expect and utilize only the first 3 digits. For international addresses, different rules apply. [1](https://github.com/orgs/OHDSI/projects/27/views/1?pane=issue&itemId=59092644#user-content-fn-1-15f41f9f115442b6ffb846f54e99b656)

## Convention type
Table

## CDM table
`LOCATION`

## CDM field
`zip`

## Links to issue discussion
- [Forum](https://forums.ohdsi.org/t/non-us-location-geography-hierarchy/1628/2)

## Provenance of data
General

## The ratified convention
The zip field houses both US zip code and non-US post codes.


## Date of ratification/published


## Downstream implications
No

## Link to DQD check
No

## Related conventions/further information

- [Forum](https://forums.ohdsi.org/t/federal-information-processing-system-fips-codes/13637)
- [Forum](https://forums.ohdsi.org/t/masking-of-data-about-a-person/4373/4)
- [Forum](https://forums.ohdsi.org/t/location-table-uniqueness-and-inclusion-requirements/9535)

