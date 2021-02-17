# Description

This workflow automatically looks up IP addresses and URLs using open source threat intelligence via Slack command and reports information back to Slack.

VirusTotal, Whois, AbuseIPDB, and IPStack are all used to obtain information about the given indicator. 

Multiple indicators can be specified within a single command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect investigate aadroid.net`

`@Rapid7 InsightConnect investigate 192.168.1.1`

`@Rapid7 InsightConnect investigate 192.168.0.0 118.25.6.39 aadroid.net`


# Key Features

* IP and URL enrichment from Slack

# Requirements

* API and account credentials for the following:
    * [AbuseIPDB](https://docs.abuseipdb.com/#introduction)
    * [VirusTotal](https://developers.virustotal.com/v3.0/reference)
    * [IPStack](https://ipstack.com/documentation) 

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow. 

There is one parameter you will need to configure in order to complete setup of your workflow:

* `Slack Channel`:  the Slack channel name in your environment where the workflow should be triggered and respond

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the steps, activate the workflow in order to trigger it. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Type Converter|1.6.0|1|
|AbuseIPDB|5.0.3|1|
|IPStack|2.0.0|1|
|VirusTotal|6.0.3|1|
|WHOIS|2.0.2|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.2.0 - Leverage Parameters Feature | Update AbuseIPDB, VirusTotal, Whois, and Type Converter plugins
* 1.1.0 - Replace pattern match with Automatic indicator extraction | Update plugins
* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com/)
* [InsightConnect with Slack](https://docs.rapid7.com/insightconnect/trigger-workflows-with-slack-chatops/)
* [VirusTotal](https://www.virustotal.com/gui/)
* [Whois](https://www.whois.net/)
* [AbuseIPDB](https://www.abuseipdb.com/)
* [IPStack](https://ipstack.com/) 
