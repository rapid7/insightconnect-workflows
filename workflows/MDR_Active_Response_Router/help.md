# Description

This workflow is part of the MDR Active Response add-on. When the MDR team identifies a threat, such as a compromised user, this workflow enables them to send an email, SMS, and Slack notification that you can review and respond to within a grace period of 10 minutes. This workflow also triggers the MDR Containment DIsable User with Active Directory and MDR Containment Isolate Sensor in Cb Response workflows.

# Key Features

* Quarantine Asset with Insight Agent or Cb Response
* Send real-time updates to actions using your preferred communication methods: phone, email, Slack, and SMS.
* Accelerate or cancel containment actions from your mobile or desktop devices via Slack.


# Requirements

* Insight Platform Organization-level API key
* Python3 Script 
* Type Converter
* REST
* Active Directory LDAP
* Microsoft Office 365 Email 
* Twilio (Optional) 
* Slack (ChatOps)


# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.
 
## Technical Details

For Technical Details, please refer to the import MDR Active Response Asset Quarantine Workflow page.

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow
* 1.0.0 - Fix null issue affecting the filter step

# Links

## References
