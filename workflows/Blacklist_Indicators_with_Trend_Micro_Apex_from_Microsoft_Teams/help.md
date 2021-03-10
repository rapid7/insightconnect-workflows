# Description

This workflow blacklists or unblacklists indicators with Trend Micro Apex via Microsoft Teams command and reports information back.
Indicators supported in this workflow are SHA-1 hashes and IP addresses.

Sample Microsoft Teams Trigger Commands:

`!blacklist-indicator 02699626f388ed830012e5b787640e71c56d42d8`

`!blacklist-indicator 198.51.100.100`

`!unblacklist-indicator 198.51.100.100`

`!unblacklist-indicator 02699626f388ed830012e5b787640e71c56d42d8`

The indicators will show up in the "User Defined Suspicious Objects" list in the Trend Micro Apex console.
The UDSO tab is located on the Custom Intelligence page under Threat Intel from the main menu.

# Key Features

* Blacklist indicators

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Trend Micro Apex account with Automation API Access Settings configured

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Trend Micro Apex|3.0.1|2|
|Microsoft Teams|3.1.0|7|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Trend Micro Apex](https://www.trendmicro.com/en_us/business/products/user-protection/sps/endpoint.html)
* [Trend Micro Apex plugin](https://extensions.rapid7.com/extension/trendmicro_apex)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
