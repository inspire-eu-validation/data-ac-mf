# Atmospheric Conditions and Meteorological Geographical Features theme-specific requirements

**Purpose**: Verify that the features provided in the dataset adhere to the theme-specific requirements specified in the INSPIRE application schema.

The following check is performed for every feature in the dataset:

* Check whether the data related to the theme Atmospheric Conditions and Meteorological Geographical Features are made available using the [types](#allowedFT) defined in the Specialised Observations package in Annex I ([IR-ISDSS](./README.md#ref_IR-ISDSS)), the OM_Observation spatial object type or sub-types thereof.

The following checks shall be performed manually for all features in the dataset:

* By way of derogation from the requirements of Section 2.2. of Annex II ([IR-ISDSS](./README.md#ref_IR-ISDSS)), gridded data related to the theme Atmospheric Conditions and Meteorological Geographical Features may be made available using any appropriate grid.

* Check that the [observed property](#observedProperty) of an OM_Observation is identified by an identifier from the [EU Air Quality Reference Component](http://inspire.ec.europa.eu/codelist/EU_AirQualityReferenceComponentValue), the [WMO GRIB Code & Flags Table 4.2](http://inspire.ec.europa.eu/codelist/GRIB_CodeTable4_2Value), the [Climate and Forecast Standard Names](http://inspire.ec.europa.eu/codelist/CFStandardNamesValue) vocabularies or another appropriate vocabulary.


**Prerequisites**

**Test method**

Verify that the theme-specific requirements that are specified in the UML model of the application schema are met, i.e. validate features against the theme-specific requirements. For unmet theme-specific requirements report [constraintViolation](#constraintViolation).


**Reference(s)**: 

* [TG DS_AC-MF](./README.md#ref_TG_DS_AC-MF) Annex A - Part 1 - A.2.3; A.3.6
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex IV, Section 13.3

**Test type**: Automatic + Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.


## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
Allowed feature types <a name="allowedFT"></a> | //schema-element(omso:PointObservation) \| //schema-element(omso:PointTimeSeriesObservation)) \| //schema-element(omso:MultiPointObservation) \|  //schema-element(omso:GridObservation) \| //schema-element(omso:GridSeriesObservation) \| //schema-element(omso:PointObservationCollection) \| //schema-element(omso:ProfileObservation) \| //schema-element(omso:TrajectoryObservation) \| //schema-element(om:OM_Observation) | Not applicable | Not applicable
Observed Property <a name="observedProperty"></a> | //schema-element(omso:PointObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:PointTimeSeriesObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:MultiPointObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:GridObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:GridSeriesObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:PointObservationCollection)/omor:member/omso:PointObservation/om:observedProperty/@xlink:href <br> //schema-element(omso:ProfileObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:TrajectoryObservation)/om:observedProperty/@xlink:href <br> //schema-element(om:OM_Observation)/om:observedProperty/@xlink:href  | 1 | Yes