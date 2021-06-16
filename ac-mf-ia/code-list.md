# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code list:

* [EU_AirQualityReferenceComponentValue](#EU_AirQualityReferenceComponentValue): http://inspire.ec.europa.eu/codelist/EU_AirQualityReferenceComponentValue
* [GRIB_CodeTable4_2Value](#GRIB_CodeTable4_2Value): http://inspire.ec.europa.eu/codelist/GRIB_CodeTable4_2Value


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS MR](./README.md#ref_TG_DS_AC-MF) Annex C

**Test type**: Automated

**Notes**


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
EU_AirQualityReferenceComponentValue <a name="EU_AirQualityReferenceComponentValue"></a> | //schema-element(omso:PointObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:PointTimeSeriesObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:MultiPointObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:GridObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:GridSeriesObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:PointObservationCollection)/omor:member/omso:PointObservation/om:observedProperty/@xlink:href <br> //schema-element(omso:ProfileObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:TrajectoryObservation)/om:observedProperty/@xlink:href <br> //schema-element(om:OM_Observation)/om:observedProperty/@xlink:href | 1 | Yes
GRIB_CodeTable4_2Value <a name="GRIB_CodeTable4_2Value"></a> | //schema-element(omso:PointObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:PointTimeSeriesObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:MultiPointObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:GridObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:GridSeriesObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:PointObservationCollection)/omor:member/omso:PointObservation/om:observedProperty/@xlink:href <br> //schema-element(omso:ProfileObservation)/om:observedProperty/@xlink:href <br> //schema-element(omso:TrajectoryObservation)/om:observedProperty/@xlink:href <br> //schema-element(om:OM_Observation)/om:observedProperty/@xlink:href | 1 | Yes