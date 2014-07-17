# Overview

This test suite is based on the following OGC specifications:

  * _OpenGIS Web Services Common Specification_, Version 1.1.0 [[OGC 06-121r3]](http://portal.opengeospatial.org/files/?artifact_id=20040)
  * _Definition Identifier URNs in OGC Namespace_, Version 1.1.0 [[OGC 06-023r1]](http://portal.opengeospatial.org/files/?artifact_id=4700) (ISO/CD 19136, OGC 03-105r1)
  * _OpenGIS Sensor Observation Service Implementation Specification_, Version 1.0 [[OGC 06-009r6]](http://portal.opengeospatial.org/files/?artifact_id=26667)

## What is tested

  * GetCapabilities, _GET_ method_
  * DescribeSensor, _POST_ method
  * GetObservation, _POST_ method

## What is not tested

  * DescribeSensor, _GET_ method
  * GetObservation, _GET_ method
  * GetObservation with "result" parameters/filters
  * Optional operations: 
    * DescribeFeatureType
    * DescribeObservationType
    * DescribeResultModel
    * GetObservationById
    * GetResult
    * GetFeatureOfInterest
    * GetFeatureOfInterestTime
    * InsertObservation
    * RegisterSensor
  

## Test Data

  * Not needed.

## Namespaces

  * ### Service being tested must use these namespaces:

gml

-
http://www.opengis.net/gml

ows

-
http://www.opengis.net/ows/1.1

ogc

-
http://www.opengis.net/ogc

om

-
http://www.opengis.net/om/1.0

sensorML v1.0.1

-
http://www.opengis.net/sensorML/1.0.1

sensorML v1.0

-
http://www.opengis.net/sensorML/1.0

sos

-
http://www.opengis.net/sos/1.0

tml

-
http://www.opengis.net/tml

## Schemas

All schemas used for validation in these tests can be found at:
<http://schemas.opengis.net/>

## Release Notes

Release notes are available from the [relnotes.txt](relnotes.txt).

