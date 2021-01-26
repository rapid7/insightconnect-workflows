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

Once the workflow has been imported, **Update the first step with the team name and the channel name to suit your Microsoft Teams environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After import, activate the workflow in order to trigger it.

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
|Microsoft Teams|3.1.0|5|
|Zscaler|1.2.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Zscaler](https://www.zscaler.com/)
* [Microsoft Teams Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Teams](https://teams.microsoft.com/)
