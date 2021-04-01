# Description

This workflow adds the Cisco Meraki L3 firewall rule to all networks in the organization via Microsoft Teams command and reports information back to Microsoft Teams. This workflow updates the L3 firewall rules of each SSID on an MR network by adding a new rule with a deny traffic policy for each destination IP address provided in the command.

Sample Microsoft Teams Trigger Commands:

`!add-rule 198.51.100.100`

`!add-rule 198.51.100.100 198.51.100.101 198.51.100.102`

# Key Features

* Add the Cisco Meraki L3 firewall rule to all networks in the organization

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Cisco Meraki API key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are three parameters you will need to configure in order to complete setup of your workflow:

* Team Name: The Microsoft Teams team name in your environment where the workflow should be triggered and respond
* Channel Name: The Microsoft Teams channel name in your environment where the workflow should be triggered and respond (the channel should exist in the aforementioned team)
* Organization ID: The Cisco Meraki organization ID e.g 845737

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!add-rule`.

For example:

`!add-rule 198.51.100.100`

`!add-rule 198.51.100.100 198.51.100.101 198.51.100.102`

The workflow will post status updates in the designated Microsoft Teams channel as it runs.

## Technical Details

Plugins utilized by the workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Meraki|4.0.0|3|
|Microsoft Teams|3.1.2|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cisco Meraki](https://meraki.cisco.com/)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
