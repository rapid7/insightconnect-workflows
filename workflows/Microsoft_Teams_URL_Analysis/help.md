# Description

This workflow will scan a Microsoft Teams channel for a specific message. When the workflow detects a message matching that signature, it will automatically scan the URL in VirusTotal and return the results to Microsoft Teams.

# Key Features

* Listens for incoming messages in a specified channel
* Scans for specific input and breaks that apart into useable data for other actions
* Scans a URL for any malicious indicators
* Reports the results of a URL scan to Microsoft Teams

# Requirements

API and account credentials for

* Microsoft Teams
* VirusTotal

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

To run the workflow, in the channel being monitored, type `!check_url http://www.google.com`. This will tell VirusTotal to go scan the given workflow and return the results to Teams. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|HTML|1.2.0|1|
|Microsoft Teams|1.2.2|1|
|String Operations|1.2.0|1|
|VirusTotal|5.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update workflow title to enrichment
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office Teams](https://products.office.com/en-us/microsoft-teams/group-chat-software)
* [VirusTotal](https://www.virustotal.com/)