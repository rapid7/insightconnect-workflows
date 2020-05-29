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

Once the workflow has been imported, **each Slack step will need the channel name updated to suit your Slack environment!** Edit the input with the preset text of `change_me` in each Slack step in the workflow.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
A optional whitelist can be added to the Fortigate Add Host to be Blocked action. To add this list add IP's or domains in the following format `["198.51.100.100", "example.com", "198.51.100.1"]`

By default, this workflow will automatically skip blocking private IP addresses, if you’d like to block these as well, set `Skip RFC 1918` option to false in the "Add Host to be Blocked" step.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect block-host`.


Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Fortinet FortiGate|4.0.0|3|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Fortigate](https://www.fortinet.com/products/next-generation-firewall.html)
* [Slack](https://teams.microsoft.com)
