# Description

Quarantine an endpoint via IP address in Microsoft Defender ATP from a Slack command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint 10.0.2.15`

`@Rapid7 InsightConnect unquarantine-endpoint 10.0.2.15`

# Key Features

* Quarantine endpoints

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Microsoft ATP Defender API Key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.

To run the workflow, use one of the example Slack commands and the workflow will post responses in the channel. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Windows Defender ATP|4.4.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update default channel
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Defender ATP](https://www.microsoft.com/en-us/microsoft-365/windows/microsoft-defender-atp)
* [Slack](https://slack.com)
