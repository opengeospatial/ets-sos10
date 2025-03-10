# Release Notes OGC SOS 1.0.0 Test Suite

## 1.15 (2025-03-07)

Attention: Java 17 and Tomcat 10.1 are required.

* [#12](https://github.com/opengeospatial/ets-sos10/issues/12) Migrate test suite to TEAM Engine 6 (Java 17)
* [#11](https://github.com/opengeospatial/ets-sos10/issues/11) Deployment to Central Maven Repository fails

## 1.14
* [#7](https://github.com/opengeospatial/ets-sos10/issues/7) Update CTL with better information about conformance classes

## r14 (2015-03-04)
* When test operations via POST, user should select an URL (from GetCapabilities response). 

## r13 (2015-02-13)

* [6](https://github.com/opengeospatial/ets-sos10/issues/6) - clean readme file and structure of folders
* Remove updated URL of reference implementation 

## r12 (2014-03-06)

* Fix dependency on xlink schemas 1.1 (W3C XLink 1.1) . "http://schemas.opengis.net/xlink/1.0.0/xlinks.xsd" will be changed to "http://www.w3.org/1999/xlink.xsd" and "xlink:simpleLink" will be changed to "xlink: simpleAttrs"

## r11 (2013-12-03)

* Issue 908:Fixed sosFunctions:describeSensor schemaFile parameter value =  "'xsd/ogc/sensorML/1.0.1/sensorML.xsd'" (Got value from capabilities before).

## r10 (2013-11-22)

* Issue 894: Fixed sos:general-SOS.General-InvalidRequest.1 error.
	
## r9 (2013-10-23)

* Issue 894: 
	- function [sosFunctions:operationVersion] changed to get first POST element value.
	- function [sosFunctions:operationPostURL] changed to get first version value.
	- function [sosFunctions:operationVersion] modify scripts to get version according to priority below:
		1. Version  <ows:Parameter> in each <ows:Operation>.
			(Xpath = $capabilitiesDocument//ows:Operation[@name=$operation]/ows:Parameter[@name='version']//ows:AllowedValues/ows:Value[1])
		2. Version  <ows:Parameter> in <ows:OperationsMetadata>.
			(Xpath = $capabilitiesDocument//sos:Capabilities/ows:OperationsMetadata/ows:Parameter[@name='version']/ows:AllowedValues/ows:Value[1])
		3. <ows:ServiceTypeVersion> in <ows:ServiceIdentification>.
			(Xpath = $capabilitiesDocument//sos:Capabilities/ows:ServiceIdentification/ows:ServiceTypeVersion[1])
 

## r8 (2013-10-23)
* Issue 877,878
	- Add acceptVersion parameter in all GetCapabilities request via KVP.
	- Refer to: OWS 1.1.0 06-121r3 7.3.2 Version negotiation 
	- Version negotiation is performed using the optional AcceptVersions parameter in the GetCapabilities operation request. 
	- Although optional, client software should always include this parameter, to simplify version negotiation.
  
## r7 (2013-05-13)
* Fixed sosFunctions:describeSensorFirstProcedure sos:ObservationOffering change to sos:ObservationOffering[1] to avoid getting 2 procedures.

## r6

* Updated config file for TEAM-Engine v4.
* Fixed invalid function arguments (wrong datatype)
* Removed nested package elements in SOS_ETS.xml


## r5 (2012-07-20)
* The default getCapabilities URL in the form test change to be: [http://sensorweb.demo.52north.org/52nSOSv3.2.1/sos](http://sensorweb.demo.52north.org/52nSOSv3.2.1/sos)
	 .

## r4 (2012-07-20)
* Update test suite for new xlink policy

## r3 (2012-04-05)

- modified type="resource"
- added  sensorML schema
- modified sosFunctions:schemaPathFromMimeType
- modified kvp
- updated information about OWS and SOS
- fixed exceptionReportSchemaPath function error
- modified namepsace sosFunctions (4572)


## r2 (2012-01-23)

- User can now choose to execute a single-test or complete-tests.
- Use a  MissingParameterValue  as a valid exception code instead of InvalidRequest. InvalidRequest is not listed in SOS or in OWS Common v 1.1 or 2.0 as a valid exception code. "InvalidRequest" is listed in SWES 2.0, but SOS 1.0 uses SWE 1.0.1 (xmlns:swe=http://www.opengis.net/swe/1.0.1).
- In GetCapabilities the observedProperty can now be any URI (URN and URL) now. Before, the value of the observedProperty parameter was a URN. But In SOS 1.0.0 06-009r6 p29 it said that the observedProperty in GetObservation can be a URI.
- Added further check when testing DescribeSensor operation. The script check if there is response and that the response is a correct SensorML and TML response.
- Changed error tag "xsl:message" to "ctl:message" in test "getObservation:core-SOS.GetObservation-ResponseMatchingSRSData.1".
- Call new function "sosFunctions:capabilitiesOfferingName" now allows to test all observed properties, not only the first one.
- The value for Procedure is now extracted from the value of the identifier and not the value of the definition (which is optional) 
- Improved handling of MIME types, The test now allows use the use of subtypes and additional parameters. For example text/xml; subtype="myOrg/0.6.1"
- The sosFunctions:mimeSubtype now returns MIME type with a valid om subytpe  (text/xml; subtype="om/1.0.1") if there is no specified subtype information.

## r0 (2009-07-23)
- first release



