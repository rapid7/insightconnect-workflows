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

Once the workflow has been imported, **each Microsoft Teams step will need the channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in each Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Blackberry CylancePROTECT|1.0.2|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [BlackBerry CylancePROTECT](https://www.cylance.com)
* [BlackBerry CylancePROTECT plugin](https://extensions.rapid7.com/extension/cylance_protect)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
