# Description

This workflow will scan a Microsoft Teams channel for `!check_url http://example.url`. When the workflow dectects a message matching that signature, it will automatically scan the url in VirusTotal and return the results to Microsoft Teams.

# Key Features

* Uses `New Message Received` to listen for incoming messages in a specified channel
* Scans for specific input and breaks that apart into useable data for other actions
* Scans a URL for any malicious indicators

# Requirements

API and account credentials for

* Microsoft Teams
* VirusTotal

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

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

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows

## References

* [Microsoft Office Teams](https://products.office.com/en-us/microsoft-teams/group-chat-software)
* [VirusTotal](https://www.virustotal.com/)