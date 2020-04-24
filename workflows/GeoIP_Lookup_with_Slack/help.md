# Description

Use a Slack command to geolocate an IP address using IPStack's geoip database. 

Sample Slack Trigger Commands:

`@Slackbot geoip <IP Address>`

# Key Features

* **Leverage Trusted Tools** - Attackers often spoof emails to make them look like they were sent from somewhere else. Leverage the tools at your disposal to investigate and enrich indicators automatically.
* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Pinpoint a Targeted Response** - Positively identifying a malicious IP address allows you to block the phishing campaign’s origin, mitigating the risk of repeated attacks from that same source.
# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `geo-ip`.

For example:

* `geoip 8.8.8.8`
* `geoip 2001:4860:4860::8888`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|IPStack|1.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Updated documentation
* 1.0.2 - Updated trigger syntax and documentation
* 1.0.1 - Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [IPStack](https://ipstack.com/)
* [Slack](https://slack.com)
