# Description

This workflow enables you to set asset tags in InsightVM from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect tag-asset <hostname> <tag>`

# Key Features

* Set Asset Tag in Rapid7 InsightVM

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `tag-asset`.

For example:

* `tag-asset <hostname>`
* `tag-asset <hostname> <tag>`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.1|4|
|Type Converter|1.6.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
