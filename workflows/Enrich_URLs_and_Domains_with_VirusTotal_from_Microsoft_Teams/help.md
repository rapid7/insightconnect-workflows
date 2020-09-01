# Description

Lookup and enrich suspicious URLs and domains with a simple Microsoft Teams command. URL and domain analysis provided by VirusTotal is returned in a Microsoft Teams thread.

Multiple URLs or domains can be specified in a single command.

Sample Microsoft Teams Trigger Commands:

`!enrich-url aadroid.net`

`!enrich-url www.aadroid.net`

`!enrich-url https://www.google.com`

`!enrich-url aadroid.net google.com`

# Key Features

* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Offload Repetitive Tasks** - Parsing out, analyzing, and enriching URLs manually can be repetitive and mind-numbing. Give that time back to your team so you can elevate your focus to identifying and resolving threats.
* **Shorten the Investigation Timeline** - Manage timely responses to real attacks by eliminating the investigation of false positives and spam. If the URLs are found to be malicious, pivot seamlessly to incident response.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* VirusTotal API Key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams step, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!enrich-url`. 

For example:

* `!enrich-url badsite.com`
* `!enrich-url http://another.badsite.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.2.0|6|
|VirusTotal|6.0.3|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Add automatic indicator extraction
* 1.0.4 - Update to make Microsoft Teams plugin the latest version
* 1.0.3 - Fix workflow syntax
* 1.0.2 - Updated trigger syntax and documentation
* 1.0.1 - Update workflow title to enrichment
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office Teams](https://products.office.com/en-us/microsoft-teams/group-chat-software)
* [VirusTotal](https://www.virustotal.com/)
