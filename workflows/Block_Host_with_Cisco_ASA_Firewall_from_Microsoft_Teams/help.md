# Description

This workflow blocks or unblocks IPv4 and IPv6 addresses with Cisco ASA via Microsoft Teams command and reports information back to Microsoft Teams.

Sample Slack Trigger Commands:

`!block-host 198.51.100.100`

`!unblock-host 198.51.100.100`

`!block-host 198.51.100.0 2001:db8:85a3:8d3:1319:8a2e:370:7348`

`!unblock-host 198.51.100.0 2001:db8:85a3:8d3:1319:8a2e:370:7348`

# Key Features

* Block and unblock IPv4 and IPv6 addresses

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Cisco ASA device with credentials and the REST API enabled

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Microsoft Teams environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!block-host` or `!unblock-host`.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cisco Adaptive Security Appliance|1.4.1|5|
|Type Converter|1.6.0|1|
|Microsoft Teams|2.2.1|8|

## Troubleshooting

The REST API server must be installed and enabled on the Cisco ASA device this plugin connects to. Cisco provides online documentation for this available [here](https://www.cisco.com/c/en/us/td/docs/security/asa/api/qsg-asa-api.html). In addition, the user account must have the necessary permissions for the intended actions:

* Actions that retrieve or check data require Cisco privilege level 5 or greater
* Actions that change or modify data require Cisco privilege level 15

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cisco Adaptive Security Appliance](https://www.cisco.com/c/en/us/products/security/adaptive-security-appliance-asa-software/index.html)
* [Microsoft Teams](https://teams.microsoft.com)
