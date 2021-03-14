# Description

This workflow accepts a Slack command containing an IP address or domain. This object will be checked against a pre-defined address group in a Palo Alto firewall to determine if the object is present or not. It is assumed that this address group will be used to store address objects for a block policy. A message with the results will be returned.

Multiple hosts can be specified in one command

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-status 198.51.100.100`

`@Rapid7 InsightConnect block-status 198.51.100.100 198.51.100.101`

`@Rapid7 InsightConnect block-status example.com`

# Key Features

* The ability to see if an IP address or domain is currently blocked by the firewall

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Username and password for a Palo Alto firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow. 

There are two parameters you will need to configure in order to complete setup of your workflow:

* Slack Channel - enter the Slack channel name matching your environment ex: `#channelname`
* Palo Alto Object Group Name - enter the name of the group you would like to add and remove host objects from, ex: `ICON Block List`

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

To run the workflow, @ your Slackbot or in a direct message along with the command "block-status <host>". The workflow will post responses in a thread.

For example:

* `@Rapid7 InsightConnect block-host example.com`
* `@Rapid7 InsightConnect block-host 198.10.198.100`
* `@Rapid7 InsightConnect block-host 198.10.198.100 198.10.198.101`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Palo Alto Firewall|6.1.0|1|
|Type Converter|1.8.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Update Palo Alto Firewall to latest version | Update Type Converter to latest version
* 1.2.0 - Add automatic indicator extraction, allow for multiple hosts
* 1.1.1 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.1.0 - Update Palo Alto Firewall to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://www.slack.com/)
* [Palo Alto Networks](https://www.paloaltonetworks.com/)
