# Description

Use the simplicity of a chat command in Slack to block URLs in Zscaler.

Multiple indicators can be specified within one command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-url example.com`

`@Rapid7 InsightConnect blacklist-url example.com example2.com`

# Key Features

* **Blacklist URLs** - Use Slack and InsightConnect to make managing URL blacklist states in Zscaler easy

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/chatops-step)
* Zscaler base URL, API key, and credentials

# Documentation

## Setup

The workflow works by blacklisting or unblacklisting URLs in Zscaler through Slack chat commands.

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are two parameters you will need to configure in order to complete setup of your workflow:

* Channel: The Slack channel name in your environment where the workflow should be triggered
* Activate Configuration: Set to true to activate configuration changes in Zscaler

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

For example:
* `@Rapid7 InsightConnect blacklist-url example.com example2.com`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Zscaler|1.4.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Update documentation | Update Zscaler plugin to version 1.4.0
* 1.0.0 - Initial workflow

# Links

## References

* [Zscaler](https://www.zscaler.com/)
* [Slack](https://slack.com)
