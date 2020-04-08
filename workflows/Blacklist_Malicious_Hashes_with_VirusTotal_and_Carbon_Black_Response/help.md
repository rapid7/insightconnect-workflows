# Description

This workflow automated the process of looking up an associated file hash in VirusTotal from an InsightIDR alert. InsightConnect then posts a user response prompt to the security channel in a synopsis of the incident. Based upon the details, the incident responder will either dismiss as a false positive or block the file with Carbon Black Response. 

# Key Features

* Data enrichment with VirusTotal
* File blacklist on endpoint with Carbon Black Response

# Requirements

* Slack Chatbot
* Carbon Black Response Connection
* VirusTotal Connection

# Documentation

## Setup

Once the workflow has been imported and the Slack chatbot selected for your workstation, edit the workflow and setup or select your CB Response connection in the Block Hash step. Also setp up your VirusTotal connection and confirm where applicable. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Cb Response|3.1.8|1|
|VirusTotal|6.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [CB Response](https://extensions.rapid7.com/extension/carbon_black_response)
* [VirusTotal](https://extensions.rapid7.com/extension/virustotal)