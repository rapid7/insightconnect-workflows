# Description

This workflow allows for fast quarantine and unquarantine from Microsoft Teams of an asset that has the [Insight Agent](https://docs.rapid7.com/insight-agent/) installed. 

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint 198.51.100.100"`

`!unquarantine-endpoint 198.51.100.100"`

For batches of assets, more than one IP can be specified

`!unquarantine-endpoint 198.51.100.100 198.51.100.101 198.51.100.102"`

# Key Features

* Quickly respond to threats by quarantining endpoints from Microsoft Teams
* Reduce the time it takes to contain an endpoint

# Requirements

* [Insight Platform API Key](https://docs.rapid7.com/insight/managing-platform-api-keys/)
* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **update the first step with the channel name to suit your Microsoft Teams environment** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Microsoft Teams step, activate the workflow in order to trigger it with a Microsoft Teams command.

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

* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)
* [Insight Agent](https://docs.rapid7.com/insight-agent/)
* [Insight Platform API Key](https://docs.rapid7.com/insight/managing-platform-api-keys/)
