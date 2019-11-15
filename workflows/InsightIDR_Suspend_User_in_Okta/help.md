# Description

This workflow suspends a user in Okta from an event in InsightIDR.

# Key Features

* User management

# Requirements

* API and account credentials for Okta

# Documentation

## Setup

* Configure the connections for the Okta plugin in Rapid7 InsightConnect
* Navigate to Rapid7 InsightIDR's automation page at #/automation/workflows
* Click Create Workflow from Template
* Select Containment Workflow in the Action Category
* Select Suspend User in Okta for the Workflow or Template
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

## Source Code

https://github.com/rapid7/insightconnect-workflows

## References

* [Okta API Documentation](https://developer.okta.com/docs/concepts/api-access-management/)