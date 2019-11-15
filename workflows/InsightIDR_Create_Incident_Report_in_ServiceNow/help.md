# Description

This workflow takes an incident from Rapid7 InsightIDR and creates an ticket in ServiceNow.

# Key Features

* Create a ticket in ServiceNow

# Requirements

* Account credentials and URL for ServiceNow
* Admin access to Rapid7 InsightIDR

# Documentation

## Setup

* Configure the connections for the ServiceNow plugin in Rapid7 InsightConnect
* Navigate to Rapid7 InsightIDR's alert triggers page at #/automation/workflows
* Click Create Workflow from Template
* Select Ticketing Workflow in the Action Category
* Select ServiceNow for the Workflow or Template
* Name the workflow
* Select the connection you setup in the beginning
* Finish by creating the workflow

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ServiceNow|3.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [ServiceNow API](https://developer.servicenow.com/app.do#!/api_doc?v=newyork&id=client)