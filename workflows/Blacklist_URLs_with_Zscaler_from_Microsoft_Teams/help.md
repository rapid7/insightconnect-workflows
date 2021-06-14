# Description

Use the simplicity of a chat command in Microsoft Teams to block or unblock URLs in Zscaler.

Multiple indicators can be specified within one command.

Sample Microsoft Teams command:

`!blacklist-url example.com`
`!blacklist-url http://example.com example2.com`
`!unblacklist-url example.com`
`!unblacklist-url http://example.com example2.com`

# Key Features

* **Blacklist URLs** - Use Microsoft Teams and InsightConnect to make managing URL blacklist states in Zscaler easy

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Zscaler base URL, API key, and credentials

# Documentation

## Setup

The workflow works by blacklisting or unblacklisting URLs in Zscaler through Microsoft Teams chat commands.

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are three parameters you will need to configure in order to complete setup of your workflow:

* Team Name: The Microsoft Teams team name in your environment where the workflow should be triggered and respond
* Channel Name: The Microsoft Teams channel name in your environment where the workflow should be triggered and respond (the channel should exist in the aforementioned team)
* Activate Configuration: Set to true to activate configuration changes in Zscaler

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps, or from any channel if left empty.*

For example:
* `!blacklist-url http://example.com example2.com`
* `!unblacklist-url http://example.com example2.com`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.2|5|
|Zscaler|1.4.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Update documentation | Update Zscaler plugin to version 1.4.0 | Update Microsoft Teams plugin to version 3.1.2
* 1.0.0 - Initial workflow

# Links

## References

* [Zscaler](https://www.zscaler.com/)
* [Microsoft Teams Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Teams](https://teams.microsoft.com/)
