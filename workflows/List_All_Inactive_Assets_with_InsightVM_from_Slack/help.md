# Description

Quickly look up inactive assets in [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/) using a Slack command. This workflow helps teams share vulnerability intelligence through shared Slack channels.

# Key Features

* Look up inactive assets in InsightVM using a Slack command

# Requirements

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages insightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow. 

There is one parameter you will need to configure in order to complete setup of your workflow:

* `Slack Channel`: The Slack channel name in your environment where the workflow should be triggered and respond

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

## Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `list-inactive`.

For example, in a direct message to your Chatbot:
* `@Rapid7 InsightConnect list-inactive`

The workflow is set to list assets that haven't been scanned in 14 days. To edit this number, please change the input for the "Get Inactive Assets" step.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.8.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow
* 2.0.0 - Leverage Parameters Feature | Update InsightVM Plugin

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Slack](https://slack.com)
