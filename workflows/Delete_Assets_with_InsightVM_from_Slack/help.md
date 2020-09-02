# Description

Delete assets from InsightVM using a command from Slack

Sample trigger commands:

`delete-asset 12345`

`delete-asset 12345 123456`

# Key Features

* **Quick Management of Retired or Inactive Assets** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Update the first step with the channel name to suit your Slack environment by editing the input with the preset text of `change_me` to match the channel to monitor.

## Usage

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `delete-asset`.

For example:
`@Rapid7 InsightConnect delete-asset 12345`

You can also delete multiple assets at once. For example: 
`@Rapid7 InsightConnect delete-asset 12345 32145`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.2.1|1|
|String Operations|1.3.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
