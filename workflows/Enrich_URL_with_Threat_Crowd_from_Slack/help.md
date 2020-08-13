# Description

Enrich a potentially malicious web URL with threat intelligence provided by Threat Crowd from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect enrich-url <URL>`

# Key Features

* ThreadCrowd URL Lookup

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*To limit the risk of users sharing malicious URLs in Slack channels, this workflow will ONLY trigger on direct messages to your Chatbot.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot starting with the command `enrich-url`, followed by one or more URLs for enrichment.

For example:

* `enrich-url aoldaily.com`
* `enrich-url aoldaily.com flushupdate.com`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Threat Crowd|3.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Threat Crowd](https://www.threatcrowd.org/)
* [Slack](https://slack.com)
