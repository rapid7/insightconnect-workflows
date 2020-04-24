# Description

Look up and enrich file hashes in VirusTotal directly from Slack, providing a fast, convenient way to check potential indicators of compromise. 

Sample Slack Trigger Commands:

`@Slackbot enrich-hash 44d88612fea8a8f36de82e1278abb02f`

`@Slackbot enrich-hash 3395856ce81f2b7382dee72602f798b642f14140`

`@Slackbot enrich-hash 275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f`

# Key Features

* **Easily Enrich Indicators** - Investigate suspicious file hashes without leaving the comfort of your Slack window
* **Respond Rapidly** - Give your teams a head start on shutting down phishing attacks by automating routine tasks during investigations.

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

## Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `enrich-hash`.

For example, in a channel with your Chatbot:

* `@slackbot enrich-hash 44d88612fea8a8f36de82e1278abb02f`

For example, in a direct message to your Chatbot:

* `enrich-hash 44d88612fea8a8f36de82e1278abb02f`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VirusTotal|6.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.4 - Updated trigger syntax and documentation
* 1.0.3 - Updated documentation
* 1.0.2 - Fix name matching
* 1.0.1 - Fix filename
* 1.0.0 - Initial workflow

# Links

## References

* [VirusTotal](https://www.virustotal.com/gui/home/upload)
* [Slack](https://slack.com)
