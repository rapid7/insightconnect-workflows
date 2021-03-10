# Description

Use a Slack command to geolocate an IP address using IPStack's geoip database.

Sample Microsoft Teams Trigger Commands:

`!geoip <IP Address>`

# Key Features

* **Leverage Trusted Tools** - Attackers often spoof emails to make them look like they were sent from somewhere else. Leverage the tools at your disposal to investigate and enrich indicators automatically.
* **Investigate Indicators at Scale** - Manually investigating every reported phishing attempt is extremely difficult to scale. Automatic analysis of common phishing IOCs reduces the overhead associated with every reported incident.
* **Pinpoint a Targeted Response** - Positively identifying a malicious IP address allows you to block the phishing campaign’s origin, mitigating the risk of repeated attacks from that same source.
# Requirements
# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!geoip <IP address>`. 

Commands should be in the following format:
* `!geoip 8.8.8.8`
* `!geoip 2001:4860:4860::8888`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|4|
|ExtractIt|2.0.0|1|
|IPStack|1.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [IPStack](https://ipstack.com/)
