# Description

This workflow adds the Cisco Meraki L3 firewall deny rule to all networks in the organization via Slack command and reports information back to Slack. This workflow updates the L3 firewall rules of each SSID on an MR network by adding a new rule with a deny traffic policy for each destination IP address provided in the command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect add-deny-rule 198.51.100.100`

`@Rapid7 InsightConnect add-deny-rule 198.51.100.100 198.51.100.101 198.51.100.102`

# Key Features

* Add the Cisco Meraki L3 firewall deny rule to all networks in the organization

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Cisco Meraki API key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are two parameters you will need to configure in order to complete setup of your workflow:

* Slack Channel: The Slack channel name in your environment where the workflow should be triggered and respond
* Organization ID: The Cisco Meraki organization ID e.g 845737

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect add-deny-rule <ip address>`.

For example:

`@Rapid7 InsightConnect add-deny-rule 198.51.100.100`

`@Rapid7 InsightConnect add-deny-rule 198.51.100.100 198.51.100.101 198.51.100.102`

Your Chatbot will post status updates in a Slack thread throughout execution.

## Technical Details

Plugins utilized by the workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Meraki|4.0.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cisco Meraki](https://meraki.cisco.com/)
* [Slack](https://slack.com)
* [Rapid7 Slack Chatbot](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
