# Description

This workflow creates a ticket in Jira from an incident triggered in InsightIDR

# Key Features

* Create ticket based on an incident triggered in InsightIDR

# Requirements

Admin access to InsightIDR and InsightConnect
API and account credentials for Jira

# Documentation

## Setup

* Configure the connections for the Jira plugin
* Navigate to IDR's automation page at #/automation/workflow
* Click Create Workflow from Template
* Select Ticketing Workflow in the Action Category
* Select Create Issue with Jia for the Workflow or Template
* Name the workflow
* Select the connection you setup in the beginning
* Finish by creating the workflow

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|jira|3.0.4|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows

## References

* [Jira API Documentation](https://developer.atlassian.com/server/jira/platform/rest-apis/)