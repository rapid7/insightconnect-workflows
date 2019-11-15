
# Description

This workflow removes a user from suspension in Okta from an event in InsightIDR. 

# Key Features

* User management

# Requirements

* Admin access to Rapid7 InsightIDR
* API and account credentials for Okta

# Documentation

## Setup

* Configure the connections for the Okta plugin in Rapid7 InsightConnect
* Navigate to Rapid7 InsightIDR's automation page at #/automation/workflows
* Click Create Workflow from Template
* Select Containment Workflow in the Action Category
* Select Unsuspend User in Okta for the Workflow or Template
* Name the workflow
* Select the connection you setup in the beginning
* Finish by creating the workflow

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Okta|3.2.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Okta API Documentation](https://developer.okta.com/docs/concepts/api-access-management/)