# Description

Create a ServiceNow Incident directly from Slack. If your team is collaborating on and handling Incidents in Slack you can now send the information you need to ServiceNow in a matter of seconds. 

# Key Features

* Automatically create a ServiceNow Incident 
* Return Incident identifying information to Slack for future updates

# Requirements

* InsightConnect
* Slack
* ServiceNow

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

## Usage

This workflow will trigger in any direct messages to your Chatbot or any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `create-incident` and then follow with your desired combination of the following parameters:
 * short_description
 * assignment_group
 * category
 * subcategory
 * company
 * description
 * impact
 * state
 * urgency

 For example, in a direct message to your Chatbot:
 * `create-incident short_description="New Alert to triage" description="The new alert contained indicators x, y, and z"`

 Or in a channel including your Chatbot:
 * `@Rapid7 InsightConnect create-incident short_description="New Alert to triage" impact="2" urgency="1"`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Python 3 Script|2.0.1|1|
|ServiceNow|4.0.0|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
