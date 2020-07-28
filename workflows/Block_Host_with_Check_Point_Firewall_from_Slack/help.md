# Description

This workflow blocks or unblocks a host with Check Point Firewall via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect block-host 198.51.100.100`

`@Rapid7 InsightConnect block-host 198.51.100.100/32`

`@Rapid7 InsightConnect block-host 198.51.100.0/24`

`@Rapid7 InsightConnect unblock-host 198.51.100.100`

`@Rapid7 InsightConnect unblock-host 198.51.100.100/32`

`@Rapid7 InsightConnect unblock-host 198.51.100.0/24`

# Key Features

* Block and unblock hosts 

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Check Point firewall
* Check Point username and password

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported,

1. Update the first step with the channel name to suit your Slack environment! by editing the input with the preset text of `change_me` to match the channel to monitor.
2. Update the preset text of `change_me` in the Group field to the Address Group you want to manage in the following steps:

* **Add Host to Blocked Address Group**
* **Remove Host from Block Group**

After configuring those steps, activate the workflow and then issue a Slack command to trigger it. Note, that the Checkpoint API can take some time to respond to the request.

Additional customization can be provided with the following options:

1. An optional whitelist can be added to the Check Point `Add Host to be Blocked` action. To skip blocking these hosts, add IP addresses or CIDR IP addresses in the following format `["198.51.100.100", "198.51.100.1/32"]`
2. By default this workflow will automatically skip blocking private IP addresses. To block these, set the `Skip RFC 1918` option to false in the `Add Host to be Blocked` step.

### Usage

*This workflow will only trigger in the channel specified in the Slack workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect block-host` or `unblock-host`.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Check Point NGFW|2.0.1|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Update Acknowledge Request step's message to mention Checkpoint
* 1.0.2 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.1 - Help amendments
* 1.0.0 - Initial workflow

# Links

## References

* [Check Point](https://www.checkpoint.com/)
* [Slack](https://slack.com)
