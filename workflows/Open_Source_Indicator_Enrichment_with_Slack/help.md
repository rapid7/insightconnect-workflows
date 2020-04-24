# Description

Threat Intelligence doesn’t have to come with a cost. This workflow uses open-source intelligence (OSINT) to perform domain lookups, header analysis, hash analysis, and more directly from Slack. Just connect Slack and activate this instant indicator enrichment workflow.

Sample Slack Trigger Commands:

`@Slackbot investigate ip 8.8.8.8`

`@Slackbot investigate url badsite.com`

`@Slackbot investigate hash 36c5012e100c8e91221e9891cad37df0cac938cee1e8f69b6fdf99821cb05339`

# Key Features

* **Automation in Minutes** - Get your first automation workflow up and running in minutes with this connectionless enrichment workflow.
* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Shorten the Investigation Timeline** - Manage timely responses to real attacks by eliminating the investigation of false positives and spam. If the URLs are found to be malicious, pivot seamlessly to incident response.

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

### Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

## Usage

*This workflow will only trigger in direct messages to your Slackbot. This is by design to avoid posting potentially malicious URLs in shared Slack channels.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot starting with the command `investigate`. 

Commands should be in the following format:
`investigate <indicator type> <indicator>`

`investigate ip 8.8.8.8`
`investigate url badsite.com`
`investigate hash 009f1e9b72cfb6daa3de82093a755bdb3685e0eb`

Use `investigate help` for more information and examples. 

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Dig|1.0.3|1|
|Team Cymru MHR|1.0.3|1|
|WHOIS|1.0.7|2|

## Troubleshooting

In some instances using copy & paste for `!enrich-indicator` commands many introduce unicode characters. These characters may be misinterpreted by the workflow, resulting in the help response triggering for what appear to be valid commands. It is recommended to avoid copying & pasting commands.

# Version History

* 1.0.3 - Updated trigger syntax and documentation
* 1.0.2 - Updated workflow title, description, and key features
* 1.0.1 - Update help document
* 1.0.0 - Initial workflow

# Links

## References

[Slack](https://slack.com)
