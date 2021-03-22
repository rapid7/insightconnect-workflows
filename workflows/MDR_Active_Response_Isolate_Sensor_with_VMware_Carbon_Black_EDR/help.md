# Description

This workflow is part of the MDR Active Response add-on and is required to complete quarantine actions with VMware Carbon Back EDR when the MDR team validates a threat in your environment.

# Key Features

* Isolate Sensor with VMware Carbon Back EDR
* Send real-time updates to actions using Slack as the communication method.
* Accelerate or cancel containment actions from your mobile or desktop devices via Slack.


# Requirements

* Type Converter
* REST 
* Python 3 Script 
* VMware Carbon Black EDR (Not required if using the Insight Agent)
* Active Directory LDAP 
* REST 
* Slack (ChatOps)


# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.
 
## Technical Details

|Plugin|Version|Count|
|----|----|--------|
|HTTP Requests|4.0.1|1|
|VMware Carbon Black EDR|3.1.10|1|

For Technical details, please refer to MDR Containment Isolate Sensor with VMware Carbon Back EDR import instructions.

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update HTTP Requests Plugin
* 1.0.0 - Initial workflow

# Links

## References
