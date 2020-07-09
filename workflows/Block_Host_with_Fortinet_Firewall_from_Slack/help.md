# Description

This workflow blocks or unblocks a host with Fortinet Firewall via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-host 198.51.100.100/32`

`@Rapid7 InsightConnect block-host 198.51.100.0/24`

`@Rapid7 InsightConnect block-host example.com`

`@Rapid7 InsightConnect unblock-host 198.51.100.100/32`

`@Rapid7 InsightConnect unblock-host 198.51.100.0/24`

`@Rapid7 InsightConnect unblock-host example.com`

# Key Features

* Block and unblock hosts 

# Requirements


* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* A Fortigate firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
An optional whitelist can be added to the Fortigate Add Host to be Blocked action. To add this list add IP's or domains in the following format `["198.51.100.100", "example.com", "198.51.100.1"]` and they will not be blocked.

By default, this workflow will automatically skip blocking private IP addresses, if you’d like to block these as well, set `Skip RFC 1918` option to false in the "Add Host to be Blocked" step.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect block-host`.


Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Fortinet FortiGate|4.0.3|4|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Update workflow to handle block requests for address that already exist | Update workflow to continue on failure and send messages indicating that something went wrong
* 1.0.2 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.1 - Help amendments
* 1.0.0 - Initial workflow

# Links

## References

* [Fortigate](https://www.fortinet.com/products/next-generation-firewall.html)
* [Rapid7 Slack Chatbot](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
