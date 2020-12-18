# Description

This workflow quarantines or unquarantines endpoints with Trend Micro Apex via Microsoft Teams command and reports information back to Microsoft Teams.
This workflow supports endpoints in the form of Agent IDs, hostnames, MAC addresses, or IP addresses.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint 08-00-27-96-86-8E`

`!quarantine-endpoint 198.51.100.100`

`!unquarantine-endpoint 198.51.100.100`

`!unquarantine-endpoint 08-00-27-96-86-8E`

To view quarantine logs, click "Directories" and then "Users/Endpoints" from the main menu in the Trend Micro Apex console.
Next, select the endpoint you would like to view and click the "Notes" tab. The quarantine logs are found there.

# Key Features

* Quarantine and unquarantine endpoints

# Requirements

* [Microsoft Teams setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Trend Micro Apex account with Automation API Access Settings configured

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the channel name and a team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|7|
|Trend Micro Apex|3.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Trend Micro Apex](https://www.trendmicro.com/en_us/business/products/user-protection/sps/endpoint.html)
* [Trend Micro Apex plugin](https://extensions.rapid7.com/extension/trendmicro_apex)
* [Microsoft Teams](https://teams.microsoft.com)
