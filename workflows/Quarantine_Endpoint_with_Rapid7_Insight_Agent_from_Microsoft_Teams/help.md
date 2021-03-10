# Description

This workflow allows for fast quarantine and unquarantine from Microsoft Teams of an asset that has the [Insight Agent](https://docs.rapid7.com/insight-agent/) installed. 

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint 198.51.100.100"`

`!unquarantine-endpoint 198.51.100.100"`

For batches of assets, more than one IP can be specified

`!unquarantine-endpoint 198.51.100.100 198.51.100.101 198.51.100.102`

# Key Features

* Quickly respond to threats by quarantining endpoints from Microsoft Teams
* Reduce the time it takes to contain an endpoint

# Requirements

* [Insight Platform API Key](https://docs.rapid7.com/insight/managing-platform-api-keys/)
* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the channel and team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams step, activate the workflow in order to trigger it with a Microsoft Teams command.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|6|
|Rapid7 Insight Agent|1.0.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)
* [Insight Agent](https://docs.rapid7.com/insight-agent/)
* [Insight Platform API Key](https://docs.rapid7.com/insight/managing-platform-api-keys/)
