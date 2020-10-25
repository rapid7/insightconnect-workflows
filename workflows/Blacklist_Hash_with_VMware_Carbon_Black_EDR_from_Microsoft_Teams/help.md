# Description

This workflow blacklists a MD5 hash globally with VMware Carbon Black EDR via Microsoft Teams command and reports information back to Microsoft Teams.

Sample Microsoft Teams Trigger Commands:

`!blacklist-hash 9de5069c5afe602b2ea0a04b66beb2c0`

The hashes will show up in the Banned Hashes list in VMware Carbon Black EDR.

# Key Features

* Blacklist a hash globally

# Requirements

* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
* [VMware Carbon Black EDR REST API](https://developer.carbonblack.com/guide/enterprise-response/)
* API Key from VMware Carbon Black EDR

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name and team name to suit your Microsoft Teams environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VMware Carbon Black EDR|3.1.10|1|
|Microsoft Teams|2.3.1|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [VMware Carbon Black EDR REST API](https://developer.carbonblack.com/guide/enterprise-response/)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
