# Description

This workflow accepts a Microsoft Teams command containing a CVE ID or vulnerability keyword(s), looks up the vulnerability in Rapid7's vulnerability database, and posts the vulnerability details back to the Microsoft Teams channel.

Sample Trigger Commands:

`!vuln-check CVE-2020-0674`

`!vuln-check heartbleed`

`!vuln-check heartbleed vmware`


# Key Features

* Lookup vulnerability information from a designated Microsoft Teams channel
* Find all vulnerabilities that match a search term
* Get solution, severity, description, and publish date information in a Microsoft Teams message

# Requirements

* InsightConnect License
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the trigger and Settings step will both need to be updated to properly define the team name and channel name used by the workflow!** Edit the input with the preset text of `change_me` for both values in the step.

After updating the steps with your Microsoft Teams configuration, activate the workflow in order to trigger it.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.4|6|
|HTML|1.2.1|1|
|Rapid7 Vulnerability & Exploit Database|2.0.3|3|
|Type Converter|1.5.1|2|
|Basename|1.0.1|2|
|URL Extractor|1.0.3|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Fix to correct invalid version of Rapid7 Vulnerability & Exploit Database
* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability Database](https://www.rapid7.com/db)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
