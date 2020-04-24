# Description

Lookup and enrich suspicious URLs and domains with a simple Microsoft Teams message. URL and domain analysis provided by urlscan.io is returned in a Microsoft Teams message.

Sample Teams Trigger Commands:

`!enrich-url https://bit.ly/39HoYMu`

# Key Features

* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Offload Repetitive Tasks** - Parsing out, analyzing, and enriching URLs manually can be repetitive and mind-numbing. Give that time back to your team so you can elevate your focus to identifying and resolving threats.
* **Shorten the Investigation Timeline** - Manage timely responses to real attacks by eliminating the investigation of false positives and spam. If the URLs are found to be malicious, pivot seamlessly to incident response.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* urlscan.io API Key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment (edit the input with the preset text of `change_me`).
The following are the 5 Microsoft Teams steps:
- _!enrich-url Trigger_
- _Print No URL Found_
- _Print Failed to get Scan ID_
- _Print Failed to get Report_
- _Print URLScan Report_

# Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*
To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!enrich-url`.
For example:
* `!enrich-url badsite.com`
* `!enrich-url http://another.badsite.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|Microsoft Teams|2.0.2|5|
|Python 3 Script|2.0.1|1|
|Sleep|1.0.2|1|
|URLScan|2.1.4|2|

## Troubleshooting

If a URL is submitted but no report is generated, urlscan.io may have blacklisted the domain.

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
* [URLScan](https://urlscan.io)

