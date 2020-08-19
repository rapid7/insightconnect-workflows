# Description

This workflow blacklists or unblacklists indicators with Microsoft Defender ATP via Slack command and reports information back to Slack.
Indicators supported in this workflow are SHA1 hashes, SHA256 hashes, IPv4 addresses, IPv6 addresses, URLs and domains.

Multiple indicators can be specified within a single command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-indicators 08518B71617EB0B46C053F3766069649F664E9A3FBACA168D6A861FBEC870082`

`@Rapid7 InsightConnect blacklist-indicators 9.9.9.9 aadroid.net CF80CD8AED482D5D1527D7DC72FCEFF84E6326592848447D2DC0B0E87DFC9A90`

`@Rapid7 InsightConnect unblacklist-indicators 08518B71617EB0B46C053F3766069649F664E9A3FBACA168D6A861FBEC870082`

`@Rapid7 InsightConnect unblacklist-indicators 9.9.9.9 aadroid.net CF80CD8AED482D5D1527D7DC72FCEFF84E6326592848447D2DC0B0E87DFC9A90`

The indicators will show up in the "Indicators" list within Settings in the Microsoft Defender Security Center. They will be sorted by indicator type (file hash, IP addresses, URLs/domains).

# Key Features

* Blacklist indicators from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Microsoft Security ATP](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

Additionally, in order to use the Microsoft Defender ATP blacklist action, create a connection using your Application ID, Directory ID and Secret Key from Microsoft Defender ATP.

After configuring the steps, activate the workflow in order to trigger it. 
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Windows Defender ATP|4.4.0|2|
|Datetime|2.0.6|2
|Type Converter|1.6.0|2

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Defender ATP](https://docs.microsoft.com/en-us/windows/security/threat-protection/)
* [Microsoft Defender Security Center](https://securitycenter.windows.com/)
* [Slack](https://slack.com)
