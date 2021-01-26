# Description

This workflow blacklists or unblacklists a SHA1 globally for all operating systems with SentinelOne via Microsoft Teams command and reports information back.

Sample Microsoft Teams Trigger Commands:

`!blacklist-hash 4e1243bd22c66e76c2ba9eddc1f91394e57f9f83`

`!unblacklist-hash 4e1243bd22c66e76c2ba9eddc1f91394e57f9f83`

The hashes will show up on the "Blacklist" tab from the "Sentinels" page on the main menu in the SentinelOne console.

# Key Features

* Blacklist a hash globally

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* SentinelOne account with permission to manage blacklist

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|SentinelOne|5.0.0|2|
|Microsoft Teams|3.1.0|7|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Update to use latest SentinelOne and Microsoft Teams plugins | Replace pattern match with indicator extraction | Remove extra HTML step
* 1.0.0 - Initial workflow

# Links

## References

* [SentinelOne](https://www.sentinelone.com/)
* [SentinelOne plugin](https://extensions.rapid7.com/extension/sentinelone)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
