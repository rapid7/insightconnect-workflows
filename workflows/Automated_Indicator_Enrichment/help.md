# Description

This workflow triggers from directly slack messaging the chatbot to \"!investigate\" the defined indicator. To date, this workflow supports automatically looking up URLs and IPs in open source threat intelligence such as VirusTotal and Whois. Lastly, the workflow will post back results to the specific user.

# Key Features

* IP and URL enrichment from Slack

# Requirements

API and account credentials for

* AbuseIPDB
* VirusTotal

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder.  Once imported, you will initially be prompted to configure the connections for each of the plugins.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|AbuseIPDB|3.0.1|1|
|ExtractIt|1.1.6|1|
|IPStack|1.0.0|1|
|VirusTotal|4.0.0|1|
|Whois|1.0.3|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows/blob/master/workflows/Office_365_Analysis

## References

* https://github.com/rapid7/insightconnect-workflows