# Description

This workflow accepts a Microsoft Teams command containing a CVE ID or vulnerability keyword(s), looks up the vulnerability in Rapid7's vulnerability database, and posts the vulnerability details back to the Microsoft Teams channel.

Sample Trigger Commands:

`!lookup-vuln CVE-2020-0674`

`!lookup-vuln heartbleed`

`!lookup-vuln heartbleed vmware`

# Key Features

* Lookup vulnerability information from a designated Microsoft Teams channel
* Find all vulnerabilities that match a search term
* Get solution, severity, description, and publish date information in a Microsoft Teams message

# Requirements

* InsightConnect License
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are two parameters you will need to configure in order to complete setup of your workflow:

* Team Name: The Microsoft Teams team name in your environment where the workflow should be triggered and respond
* Channel Name: The Microsoft Teams channel name in your environment where the workflow should be triggered and respond (the channel should exist in the aforementioned team)

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!lookup-vuln`.

For example:

`!lookup-vuln CVE-2020-0674`

`!lookup-vuln heartbleed`

The workflow will post status updates in the designated Microsoft Teams channel as it runs.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.2|7|
|HTML|1.2.2|1|
|Rapid7 Vulnerability & Exploit Database|2.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Remove unnecessary steps that used Basename, Type Converter and URL Extractor plugins | Update documentation | Update screenshots | Update Microsoft Teams plugin to version 3.1.2 | Update HTML plugin to version 1.2.2 | Update Rapid7 Vulnerability & Exploit Database plugin to version 2.1.0
* 1.1.0 - Replace the Settings step with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update sample trigger commands in description | Update documentation
* 1.0.2 - Fix to correct invalid version of Rapid7 Vulnerability & Exploit Database
* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability Database](https://www.rapid7.com/db)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
