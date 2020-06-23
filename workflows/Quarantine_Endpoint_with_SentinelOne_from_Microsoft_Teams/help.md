# Description

This workflow will quarantine and unquarantine an endpoint in SentinelOne from a Microsoft Teams command. This workflow supports endpoints in the form of Agent IDs, hostnames, MAC addresses, or IP addresses.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint 198.51.100.100`

`!unquarantine-endpoint 198.51.100.100`

Under the "Endpoints" tab from the "Sentinels" page on the main menu in the SentinelOne console, the quarantined endpoint will show "Network status" as "Disabled" after being quarantined.

# Key Features

* Quarantine and unquarantine endpoints

# Requirements

* [Microsoft Teams setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* SentinelOne account with permission to manage endpoints

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the channel and team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in each Microsoft Teams step in the workflow.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.5|7|
|SentinelOne|1.4.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [SentinelOne](https://www.sentinelone.com/)
* [SentinelOne plugin](https://extensions.rapid7.com/extension/sentinelone)
* [Microsoft Teams](https://teams.microsoft.com)
