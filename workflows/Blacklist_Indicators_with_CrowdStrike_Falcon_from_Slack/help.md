# Description

Use the simplicity of a chat command in Slack to block indicators such as IPv4 and IPv6 address, MD5 and SHA256 hashes, and domains in CrowdStrike Falcon.

Multiple indicators can be specified within one command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-indicators 198.51.100.100 bd3b8dbb50fbd58e1bc2cc82effb9d81a2ea0aa6be235ff58ec7eb997deea1ab`

`@Rapid7 InsightConnect blacklist-indicators 198.51.100.100 example.com 2001:db8:8:4::2`

`@Rapid7 InsightConnect blacklist-indicators 9de5069c5afe602b2ea0a04b66beb2c0`

# Key Features

* **Block an Indicator** - Use Slack and Insight Connect to make firewall rules easy. 

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/chatops-step)
* CrowdStrike Falcon Client Secret and Client ID

# Documentation

## Setup

The workflow works by adding indicators in your CrowdStrike Falcon.

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.
And then **Edit Each CrowdStrike Falcon step to specify the group you are using** In these steps, specify the group you would like to add and remove host objects from.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

For example:
* `@Rapid7 InsightConnect blacklist-indicators 198.51.100.100`

The workflow will reply when it completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|CrowdStrike Falcon|2.2.0|1|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [CrowdStrike](https://www.crowdstrike.com/)
* [CrowdStrike Falcon API](https://falcon.crowdstrike.com/support/documentation)
* [Slack](https://slack.com)
