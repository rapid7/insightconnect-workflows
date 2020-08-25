# Description

Quarantine an endpoint via IP address in Microsoft Defender ATP from a Microsoft Teams command.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint 10.0.2.15`

`!unquarantine-endpoint 10.0.2.15`

# Key Features

* Quarantine endpoints

# Requirements

* [Microsoft Teams connection](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Microsoft ATP Defender API Key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the channel and team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in each Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it. 

To run the workflow, use one of the example Microsoft Teams commands and the workflow will post repsonses in the channel. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.2.0|5|
|Microsoft Windows Defender ATP|4.4.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Check Point](https://www.checkpoint.com/)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Defender ATP](https://www.microsoft.com/en-us/microsoft-365/windows/microsoft-defender-atp)
