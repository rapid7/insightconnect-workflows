# Description

This workflow enables a user in Active Directory from an alert sent by InsightIDR

# Key Features

* User provisioning

# Requirements

* Account credentials for an Active Directory user
* Admin access to Rapid7 InsightIDR

# Documentation

## Setup

* Configure the connections for the Active Directory plugin in Rapid7 InsightConnect
* Navigate to Rapid7 InsightIDR's automation page at #/automation/workflows
* Click Create Workflow from Template
* Select Containment Workflow in the Action Category
* Select Enable User in Active Directory for the Workflow or Template
* Name the workflow
* Select the connection you setup in the beginning
* Finish by creating the workflow

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|active_directory_ldap|3.2.4|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

_There is no references information at this time_