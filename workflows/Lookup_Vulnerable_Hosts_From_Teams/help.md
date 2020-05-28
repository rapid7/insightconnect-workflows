# Description

Search InsightVM for hosts with a particular vulnerability present directly from Microsoft Teams. Receive a message summarizing the vulnerability and all affected assets in a Microsoft Teams channel.

# Key Features

* Identify vulnerable hosts
* Share context with team members in the same Microsoft Teams channel

# Requirements

* InsightVM Console URL and account credentials
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **edit the Settings step to specify the Microsoft Teams team name and channel name to suit your Teams environment!** Edit the input with the preset text of `Your Team` and `Your Channel` in each Teams step in the workflow. You may also choose to edjust the `max hosts` setting, which controls the maximum number of hosts listed per vulnerability.

Once the Settings step has been updated to reflect your Microsoft Teams environment, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!lookup-vuln-hosts`.

For example:
* `!lookup-vuln-hosts bluekeep`
* `!lookup-vuln-hosts CVE-2019-0708`

The workflow will post status updates in the designated Microsoft Teams channel as it runs.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.0|5|
|Microsoft Teams|2.0.3|8|
|HTML|1.2.1|1|
|CSV|1.1.5|1|
|Rapid7 Vulnerability & Exploit Database|2.0.3|1|
|Type Converter|1.5.1|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
