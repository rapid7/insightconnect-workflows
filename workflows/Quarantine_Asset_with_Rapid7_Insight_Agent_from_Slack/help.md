# Description

This workflow allows for fast quarantine and unquarantine from Slack of an asset that has the [Insight Agent](https://docs.rapid7.com/insight-agent/) installed. 

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint 198.51.100.100"`

`@Rapid7 InsightConnect unquarantine-endpoint 198.51.100.100"`

For batches of assets, more than one IP can be specified

`@Rapid7 InsightConnect unquarantine-endpoint 198.51.100.100 198.51.100.101 198.51.100.102"`

# Key Features

* Quickly respond to threats by quarantining endpoints from Slack
* Reduce the time it takes to contain an endpoint

# Requirements

* [Insight Platform API Key](https://docs.rapid7.com/insight/managing-platform-api-keys/)
* [Slack](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, Update the first step with the channel name to suit your Slack environment by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it with a Slack command.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 Insight Agent|1.0.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops/)
* [Insight Agent](https://docs.rapid7.com/insight-agent/)
* [Insight Platform API Key](https://docs.rapid7.com/insight/managing-platform-api-keys/)
