# Description

This workflow allows for fast quarantine and unquarantine from Slack of an asset that has the [Insight Agent](https://docs.rapid7.com/insight-agent/) installed. 

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint 198.51.100.100"`

`@Rapid7 InsightConnect unquarantine-endpoint 198.51.100.100"`

For batches of assets, more than one IP can be specified

`@Rapid7 InsightConnect unquarantine-endpoint 198.51.100.100 198.51.100.101 198.51.100.102"`

# Key Features

* Quickly respond to threats by quarantining endpoints from Slack. 
* Keep users happy by getting them back online quickly

# Requirements

* [Insight Agent](https://docs.rapid7.com/insight-agent/)
* [Insight Platform](https://docs.rapid7.com/insight/managing-platform-api-keys/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Activate the workflow in order to trigger with a Slack command.

### Usage

This workflow uses the Chat Ops Slack connection to listen for key messages. When the Slack command triggers this workflow, it will quarantine or unquarantine assets.

To trigger this workflow, send a direct message to Rapid7 InsightConnect from Slack like the following:

`@Rapid7 quarantine-endpoint 198.51.100.100"`

To unquarantine an endpoint you can use:

`@Rapid7 unquarantine-endpoint 198.51.100.100"`

For batches of assets, more than one IP can be specified

`@Rapid7 unquarantine-endpoint 198.51.100.100 198.51.100.101 198.51.100.102"`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 Insight Agent|1.0.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Change trigger command from `purge-email` to `delete-emails`
* 1.0.2 - Changed content search query to use double quotes | Workflow no longer prompts a manual purge when 0 emails are found | Trigger no longer requires an exclamation mark | Updated documentation
* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Microsoft Office365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
* [Slack Configuration](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Slack](https://slack.com/)
