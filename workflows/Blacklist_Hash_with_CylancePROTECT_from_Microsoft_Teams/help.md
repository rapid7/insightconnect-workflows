# Description

This workflow blacklists or unblacklists a SHA256 globally with CylancePROTECT via Microsoft Teams command and reports information back.

Sample Microsoft Teams Trigger Commands:

`!blacklist-hash 30f800f97aeaa8d62bdf3a6fb2b0681179a360c12e127f07038f8521461e5050`

`!unblacklist-hash 30f800f97aeaa8d62bdf3a6fb2b0681179a360c12e127f07038f8521461e5050`

The hashes will show up in the Global Quarantine list in CylancePROTECT.

# Key Features

* Blacklist a hash globally

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* CylancePROTECT
* Create a "Custom Application" in CylancePROTECT (Settings -> Integrations -> Add Application)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your  Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|BlackBerry CylancePROTECT|1.0.3|2|
|Microsoft Teams|3.1.0|8|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [BlackBerry CylancePROTECT](https://www.cylance.com)
* [BlackBerry CylancePROTECT plugin](https://extensions.rapid7.com/extension/cylance_protect)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
