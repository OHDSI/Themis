---
title: What to do when a provider has multiple addresses
keywords: provider, location, address
last_updated: April 10, 2024
tags: [address, location, provider]
sidebar: mydoc_sidebar
permalink: /multiple_provider_addresses.html
---

## Issue # and location

- [Themis issue #48](https://github.com/OHDSI/Themis/issues/48)

## Issue summary
A provider may have multiple addresses through work at multiple facilities. This can result in multiple locations associated with care (e.g. provider address and provider location).

## Convention type
Global

## CDM table
NA

## CDM field
NA

## Links to issue discussion

- [OHDSI Forums discussion](http://forums.ohdsi.org/t/multiple-addresses-per-provider-provider-address-differs-from-care-site/5653)
- [CDM Documentation](https://github.com/OHDSI/CommonDataModel/wiki/VISIT_OCCURRENCE)   

## Provenance of data
General, any database with provider location information

## The ratified convention
The CDM allows us to capture location of visits, so knowing where a patient was treated is quantified in the CDM. If a provider has multiple addresses the ETL should just choose one to associate with the provider in the PROVIDER table as the analytical use case for storing multiple addresses per provider is unknown.

The question of how to handle a situation where the billing address differs from where the patient received care is already handled in the CDM. The VISIT_OCCURRENCE table has a separate PROVIDER_ID and CARE_SITE_ID for expressly this purpose. 

## Date of ratification/published
Nov 27, 2018

## Downstream implications
No

## Link to DQD check
No. The [isPrimaryKey](https://ohdsi.github.io/DataQualityDashboard/articles/checks/isPrimaryKey.html) check will make sure the provider ids are not duplicated in the PROVIDER table but there is no explicit check for the same provider_source_value and different location_ids

## Related conventions/further information
NA