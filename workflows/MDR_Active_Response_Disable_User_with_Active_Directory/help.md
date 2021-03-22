# Description

This workflow is part of the MDR Active Response add-on and is required to disable users with Active Directory.

# Key Features

* Disable User with Active Directory
* Send real-time updates to actions using your preferred communication methods: email, Slack, and SMS.
* Accelerate or cancel containment actions from your mobile or desktop devices via Slack.

# Requirements

* Active Directory LDAP
* Python3 Script
* Slack (ChatOps)
* REST

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.
 
## Technical Details

|Plugin|Version|Count|
|----|----|--------|
|HTTP Requests|4.0.1|1|
|Active Directory LDAP|5.1.0|1|

For Technical details, refer to the MDR Containment Disable User with Active Directory import instructions. 

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Upgrade HTTP Rest Plugin
* 1.0.1 - Fix AD backslash issue
* 1.0.0 - Initial workflow

# Links

## References
