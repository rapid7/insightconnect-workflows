# Description

Lookup a vulnerability to receive an overview, including risk, publish date, description, and solutions for remediation. This workflow helps teams share vulnerability intelligence through shared Slack channels.

Sample Slack trigger commands:

`@Rapid7 InsightConnect lookup-vuln CVE-2020-0674`

`@Rapid7 InsightConnect lookup-vuln bluekeep`

# Key Features

* Lookup vulnerability information from Slack
* Find all vulnerabilities that match a search term
* Get severity, description, publish date, and solution information in a Slack message

# Requirements

* InsightConnect License
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There is one parameter you will need to configure in order to complete setup of your workflow:

* Channel: The Slack channel name in your environment where the workflow should be triggered

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameter, activate the workflow in order to trigger it.

## Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `lookup-vuln`.

For example, in a direct message to your Chatbot:
* `lookup-vuln CVE-2020-0674`

Or in a channel including your Chatbot:
* `@Rapid7 InsightConnect lookup-vuln bluekeep`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 Vulnerability & Exploit Database|2.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Update documentation | Update Rapid7 Vulnerability & Exploit Database plugin to version 2.1.0
* 1.1.4 - Update workflow to be entirely cloud based
* 1.1.3 - Updated trigger syntax, updated Rapid7 Vuln DB plugin, updated documentation
* 1.1.2 - Updated documentation
* 1.1.1 - Updated plugin versions in help.md
* 1.1.0 - Updated workflow to work with v2.0.2 of the Rapid7 Vulnerability & Exploit Database plugin | Added a Final Report workflow artifact including a summary of workflow results
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability Database](https://www.rapid7.com/db)
* [Slack](https://slack.com)
