# Description

Enrich potentially malicious process hashes with threat intelligence provided by Threat Crowd and Team Cymru MHR from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect enrich-hash <hash>`

# Key Features

* ThreadCrowd Lookup
* Team Cymru MHR Lookup

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `enrich-hash`, followed by one or more hashes.

For example:

* `enrich-hash 86DD715A8D28788E68A575207D66DF34`
* `enrich-hash 86DD715A8D28788E68A575207D66DF34 1cf7724052b5aba962bc6ba81743e2a9`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Threat Crowd|3.0.0|2|
|Team Cymru MHR|1.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Threat Crowd](https://www.threatcrowd.org/)
* [Team Cymru MHR](https://team-cymru.com/community-services/mhr/)
* [Slack](https://slack.com)
