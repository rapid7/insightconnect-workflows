# Description

Blacklist a SHA256 hash globally with Sophos Central via Microsoft Teams command and report information back to Microsoft Teams.

Sample Microsoft Teams Trigger Commands:

`!blacklist-indicators 30f800f97aeaa8d62bdf3a6fb2b0681179a360c12e127f07038f8521461e5050`

The hashes will show up in the Blocked Items list in Sophos Central Endpoint Protection.

# Key Features

* Blacklist a hash globally

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Sophos Central account

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Sophos Central|4.3.0|1|
|Microsoft Teams|3.1.0|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Sophos Central](https://www.sophos.com)
* [Sophos Central plugin](https://extensions.rapid7.com/extension/sophos_central)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
