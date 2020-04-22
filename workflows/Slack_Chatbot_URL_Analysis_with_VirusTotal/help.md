# Description

Lookup and enrich suspicious URLs and domains with a simple Slack command. URL and domain analysis provided by VirusTotal is returned in a Slack thread.

Sample Slack Trigger Commands:

`@Slackbot !url_lookup example.com`

`@Slackbot !url_lookup www.example.com`

`@Slackbot !url_lookup https://www.example.com`

# Key Features

* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Offload Repetitive Tasks** - Parsing out, analyzing, and enriching URLs manually can be repetitive and mind-numbing. Give that time back to your team so you can elevate your focus to identifying and resolving threats.
* **Shorten the Investigation Timeline** - Manage timely responses to real attacks by eliminating the investigation of false positives and spam. If the URLs are found to be malicious, pivot seamlessly to incident response.

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* VirusTotal API Key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After importing, activate the workflow in order to trigger it.

### Usage

This workflow uses the Chat Ops Slack integration to listen for messages sent to your InsightConnect Slack Chatbot and will lookup the provided URL or domain in VirusTotal when triggered.

To trigger this workflow, either @ your Chat Bot in  a channel or send a direct message to the bot in Slack using the `!url_lookup` keyword:

`!url_lookup badsite.com/suspicious/link`

`!url_lookup badsite.com`

This will kick off the workflow. The VirusTotal scan results will be posted in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|VirusTotal|6.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.4 - Updated documentation
* 1.0.3 - Update workflow title to enrichment
* 1.0.2 - Fix name matching
* 1.0.1 - Fix filename
* 1.0.0 - Initial workflow

# Links

## References

* [VirusTotal](https://www.virustotal.com/gui/home/upload)
* [Slack](https://slack.com)
