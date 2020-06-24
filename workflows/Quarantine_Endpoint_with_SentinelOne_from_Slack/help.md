# Description

This workflow will quarantine and unquarantine an endpoint in SentinelOne from a Slack command. This workflow supports endpoints in the form of Agent IDs, hostnames, MAC addresses, or IP addresses.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint 198.51.100.100`

`@Rapid7 InsightConnect unquarantine-endpoint 198.51.100.100`

Under the "Endpoints" tab from the "Sentinels" page on the main menu in the SentinelOne console, the quarantined endpoint will show "Network status" as "Disabled" after being quarantined.

# Key Features

* Quarantine endpoints

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* SentinelOne account with permission to manage endpoints

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|SentinelOne|1.4.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.1 - Update product vendor text in Slack post
* 1.0.0 - Initial workflow

# Links

## References

* [SentinelOne](https://www.sentinelone.com/)
* [SentinelOne plugin](https://extensions.rapid7.com/extension/sentinelone)
* [Slack](https://slack.com)
