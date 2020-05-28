# Description

Search InsightVM for hosts with a particular vulnerability present directly from Slack. Receive a summary of the vulnerability and all affected assets in a thread.

# Key Features

* Identify vulnerable hosts
* Share context with team members in the same Slack channel

# Requirements

* InsightVM Console URL and account credentials
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

There is a settings step which can be edited to change the maximum number of vulnerabilities and maximum hosts listed per vulnerability which are returned.  The defaults are 50 vulnerabilities and 10 assets per vulnerability.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `lookup-vuln-hosts`.

For example, in a direct message to your Chatbot:
* `lookup-vuln-hosts bluekeep`

Or in a channel including your Chatbot:
* `@Rapid7 InsightConnect lookup-vuln-hosts CVE-2019-0708`

The workflow will post status updates in a Slack thread throughout execution.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|CSV|1.1.5|1|
|Rapid7 Vulnerability & Exploit Database|2.0.3|1|
|Type Converter|1.5.1|3|
|Rapid7 InsightVM|4.0.0|5|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Slack](https://slack.com)
