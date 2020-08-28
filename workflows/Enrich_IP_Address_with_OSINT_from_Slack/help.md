# Description

Enrich a potentially malicious IP address with open source threat intelligence from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect enrich-ip <IP Address>`

# Key Features

* ThreadCrowd Lookup
* Reverse DNS Lookup
* WHOIS Lookup

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `enrich-ip`, followed by one or more IP addresses for enrichment.

For example:

* `enrich-ip 8.8.8.8`
* `enrich-ip 8.8.8.8 8.8.4.4`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Threat Crowd|3.0.0|1|
|Dig|1.0.5|1|
|WHOIS|2.0.2|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Threat Crowd](https://www.threatcrowd.org/)
* [Slack](https://slack.com)
