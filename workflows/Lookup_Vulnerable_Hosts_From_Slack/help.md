# Description

Search InsightVM for hosts with a particular vulnerability present directly from Slack. Receive a summary of the vulnerability and all affected assets in a thread.

Sample Slack command:

`@Rapid7 InsightConnect lookup-vuln-hosts <vulnerability>`

`@Rapid7 InsightConnect lookup-vuln-hosts CVE-2019-0708`

# Key Features

* Identify vulnerable hosts
* Share context with team members in the same Slack channel

# Requirements

* InsightVM Console URL and account credentials
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are three parameters you will need to configure in order to complete setup of your workflow:
* `Slack Channel`: The Slack channel name in your environment where the workflow should be triggered and respond
* `Max Hosts`: The maximum number of hosts listed per vulnerability (recommended default is 10)
* `Max Vulnerabilities`: The maximum number of returned vulnerabilities (recommended default is 50)

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `lookup-vuln-hosts`.

Commands should be in the following format: `lookup-vuln-hosts <vulnerability>`

`<vulnerability>` in the command can be any InsightVM vulnerability reference including the following:
* KB Number
* CVE ID
* Nexpose ID
* Other references InsightVM knows

For example, in a direct message to your Chatbot:
* `lookup-vuln-hosts bluekeep`

Or in a channel including your Chatbot:
* `@Rapid7 InsightConnect lookup-vuln-hosts CVE-2019-0708`

The workflow will post status updates in a Slack thread throughout execution.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|CSV|1.1.6|1|
|Rapid7 Vulnerability & Exploit Database|2.0.3|1|
|Type Converter|1.7.0|2|
|Rapid7 InsightVM|4.8.1|5|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Leverage Parameters Feature | Use Workflow Parameters to configure Slack channel name, max vulnerabilities, and max hosts values (and remove the Settings step) | Update CSV to version 1.1.6 | Update Type Converter to 1.7.0
* 1.1.0 - Use the automatic extraction functionality instead of Pattern Match step to extract a vulnerability | Improve workflow messaging | Improve documentation | Update screenshots | Update Rapid7 InsightVM to version 4.8.1 | Update Type Converter to version 1.6.0
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Slack](https://slack.com)
