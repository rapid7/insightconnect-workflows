# Description

Use the simplicity of a chat command in Slack to block URLs in Zscaler.

Multiple indicators can be specified within one command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-url example.com`

`@Rapid7 InsightConnect blacklist-url example.com example2.com`

# Key Features

* **Blacklist URLs** - Use Slack and InsightConnect to make managing URL blacklist states in Zscaler easy

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/chatops-step)
* Zscaler base URL, API key, and credentials

# Documentation

## Setup

The workflow works by blacklisting or unblacklisting URLs in Zscaler through Slack chat commands.

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

For example:
* `@Rapid7 InsightConnect blacklist-url example.com example2.com`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Zscaler|1.2.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Zscaler](https://www.zscaler.com/)
* [Slack](https://slack.com)
