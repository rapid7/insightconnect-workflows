# Description

Threat Intelligence doesn’t have to come with a cost. This workflow uses open-source intelligence (OSINT) to perform domain lookups, header analysis, hash analysis, and more directly from Slack. Just connect Slack and activate this instant indicator enrichment workflow.

Sample Slack Trigger Commands:

`@Slackbot !investigate ip 8.8.8.8`

`@Slackbot !investigate url badsite.com`

`@Slackbot !investigate hash 36c5012e100c8e91221e9891cad37df0cac938cee1e8f69b6fdf99821cb05339`

# Key Features

* **Automation in Minutes** - Get your first automation workflow up and running in minutes with this connectionless enrichment workflow.
* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Shorten the Investigation Timeline** - Manage timely responses to real attacks by eliminating the investigation of false positives and spam. If the URLs are found to be malicious, pivot seamlessly to incident response.

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, you will need to activate the workflow in order to trigger it.

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command `!investigate <command> <data>`. Example: `!investigate ip 8.8.8.8`

Alternatively, use `!investigate help` for more information and examples. The workflow will post with the results of the lookup.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Dig|1.0.3|1|
|Team Cymru MHR|1.0.3|1|
|WHOIS|1.0.7|2|

## Troubleshooting

In some instances using copy & paste for `!investigate` commands many introduce unicode characters.
These characters may be misinterpreted by the workflow, resulting in the help response triggering for
what appear to be valid commands. It is recommended to avoid copying & pasting commands.

# Version History

* 1.0.2 - Updated workflow title, description, and key features
* 1.0.1 - Update help document
* 1.0.0 - Initial workflow

# Links

## References

[Slack](https://slack.com)
