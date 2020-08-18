# Description

This workflow helps a user find information about a given CVE and identify all hosts affected by that vulnerability.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect cve-report <cve-number>`

# Key Features

* Rapid7 AttackerKB Lookup
* Rapid7 InsightVM Affected Assets Search

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Rapid7 AttackerKB](https://attackerkb.com/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `cve-report`, followed by the CVE number.

For example:

* `cve-report CVE-2020-1350`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.1|5|
|Python 3 Script|2.0.2|1|
|Rapid7 AttackerKB|1.0.1|1|
|Type Converter|1.6.0|1|
|Base64|1.1.6|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Rapid7 AttackerKB](https://attackerkb.com/)
