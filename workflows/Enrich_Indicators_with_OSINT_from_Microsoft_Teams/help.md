# Description

Threat Intelligence doesn’t have to come with a cost. This workflow uses open-source intelligence (OSINT) to perform domain lookups, header analysis, hash analysis, and more directly from Slack. Just connect Slack and activate this instant indicator enrichment workflow.

Sample Trigger Commands:

`!enrich-indicator 8.8.8.8`

`!enrich-indicator rapid7.com`

`!enrich-indicator 009f1e9b72cfb6daa3de82093a755bdb3685e0eb`

# Key Features

* **Automation in Minutes** - Get your first automation workflow up and running in minutes with this connectionless enrichment workflow.
* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Shorten the Investigation Timeline** - Manage timely responses to real attacks by eliminating the investigation of false positives and spam. If the URLs are found to be malicious, pivot seamlessly to incident response.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!enrich-indicator`. 

Commands should be in the following format:
`!enrich-indicator <indicator>`

`!enrich-indicator ip 8.8.8.8`
`!enrich-indicator url badsite.com`
`!enrich-indicator hash 009f1e9b72cfb6daa3de82093a755bdb3685e0eb`


Alternatively, use `!enrich-indicator help` for more information and examples. 

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Dig|1.0.5|1|
|Team Cymru MHR|1.1.1|1|
|Microsoft Teams|3.1.0|8|
|WHOIS|2.0.2|2|
|Type Converter|1.6.0|2|

## Troubleshooting

In some instances using copy & paste for `!enrich-indicator` commands may introduce unicode characters. These characters may be misinterpreted by the workflow, resulting in the help response triggering for what appear to be valid commands. It is recommended to avoid copying & pasting commands.

# Version History

* 2.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 2.0.0 - Update workflow to use loop outputs
* 1.0.2 - Update to make Microsoft Teams plugin the latest version
* 1.0.1 - Updated trigger syntax and documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
