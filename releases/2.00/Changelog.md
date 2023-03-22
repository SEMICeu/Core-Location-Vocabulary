# Core Location Changelog

## Introduction

This document describes the (major) changes to [the current version 1.0.0](https://github.com/SEMICeu/Core-Location-Vocabulary/tree/master/releases/1.00) of the Core Location Vocabulary for which a new version is being proposed ([version 2.0.0](https://semiceu.github.io/Core-Location-Vocabulary/releases/2.00/)). The list of changes results in the new version to be considered as a major release.

## Detailed changes from v1.0.0 to v2.0.0

The table below gives an overview of the classes (and their definitions) within both data models. Classes that are related are juxta-positioned.

**C** stands for changes in classes

**R** stands for changes in relationships

**P** stands for changes in properties

**D** stands for changes in data types

| Nr | Core Location Vocabulary v1.0.0 | Core Location Vocabulary v2.0.0 | Rationale | GitHub / Change |
| --- | --- | --- | --- | --- |
| C1 | **Definition of Location: A spatial region or named place.** | An identifiable geographic place or named place. | Proposition made by SDG WP4. | Change |
| C2 | **Geometry (alternative representation)** | **Geometry (alternative representation) class removed and properties put** | Decrease ambiguity. | Change |
| C3 | **Definition of Address: Representation of an address spatial object for use in external application schemas that need to include the basic, address information in a readable way.** | A spatial object that in a human-readable way identifies a fixed location of a property. | Proposition made by SDG WP4. | Change |
| C4 | **-** | Resource | Addition of the resource class | Change |
| D1 | **Location:** Geographic name expects a string value | **Location:** Geographic name expects a text value. Also updated the usage note example accordingly. | Adapted data type for consistency. | Change |
| P1 | **-** | **Address: added an example in the usage notes for most properties** | To increase understandability. | Change |
| D2 | **Address.adminUnitL1: String** | **Address.adminUnitL1: Code** | Proposition made by SDG WP4. | Change |
| D3 | **Address.adminUnitL2: String** | **Address.adminUnitL2: Text** | Proposition made by SDG WP4 to allow for multi-language + alignment with INSPIRE. | Change |
| P2 | **-** | **Address.adminUnitL2: added recommended codelists** | To facilitate usage. | Change |
| D4 | **Address.fullAddress: String** | **Address.fullAddress: Text** | Proposition made by SDG WP4 to allow for multi-language. | Change |
| D5 | **Address.addressArea: String** | **Address.addressArea: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| D6 | **Address.locatorName: String** | **Address.locatorName: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| D7 | **Address.postName: String** | **Address.postName: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| D8 | **Address.thoroughfare: String** | **Address. thoroughfare: Text** | To allow for multi-language + alignment with INSPIRE. | Change |
| P3 | **Address.locatorDesignator:** A number or a sequence of characters that uniquely identifies the locator within the relevant scope(s). The full identification of the locator could include one or more locator designators. | A number or a sequence of characters which allows a user or an application to interpret, parse and format the locator within the relevant scope. A locator may include more locator designators. | Update from INSPIRE. | Change |
| P4 | **Address.adminUnitL1:** The uppermost administrative unit for the address, almost always a country. | The name or names of a unit of administration where a Member State has and/or exercises jurisdictional rights, for local, regional and national governance. Level 1 refers to the uppermost administrative unit for the address, almost always a country. | Update from INSPIRE. | Change |
| P5 | **Address.adminUnitL2:** The region of the address, usually a county, state or other such area that typically encompasses several localities. | The name or names of a unit of administration where a Member State has and/or exercises jurisdictional rights, for local, regional and national governance. Level 2 referst to the region of the address, usually a county, state or other such area that typically encompasses several localities. | Update from INSPIRE. | Change |

## Changes since April 2021 

### Terms

| Nr | Core Location Vocabulary v2.0.0 2021 | Core Location Vocabulary v2.0.0 2022 | Rationale                                                             | GitHub/Change                                                                                                                  |
| -- | ------------------------------------ | ------------------------------------ | --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| C1 | \-                                   | AdminUnit                            | A granular administrative unit allowing a hierarchical classification | [https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12) |
| R1 | Location.geometry:Geometry           | Resource.geometry:Geometry           | Improved reusability of geometry                                      |                                                                                                                                |
| R2 | Location.address:Address             | Resource.address:Address             | Improved reusability of address                                       |                                                                                                                                |
| R3 | \-                                   | Resource.registeredAddress:Address   | moved from Core Person                                                |                                                                                                                                |
| R4 | \-                                   | Address.adminUnit:AdminUnit          | An address can refer to an administrative unit                        | [https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12) |
| P1 | \-                                   | AdminUnit.code                       | The classification of the administrative unit                         | [https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12) |
| P2 | \-                                   | AdminUnit.level                      | The level of the administrative unit in the hierarchy                 | [https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12) |
| D1 | Address:AdminUnitL1:Code             | Address:AdminUnitL1:Text             | In compliance with W3C location                                       | [https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12) |
| D2 | Address:AdminUnitL2:Code             | Address:AdminUnitL1:Text             | In compliance with W3C location                                       | [https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12](https://github.com/SEMICeu/Core-Location-Vocabulary/issues/12)

### Definitions

Changes in definitions are registered in [this file](Changelog_definitions.md)