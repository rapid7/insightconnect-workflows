# Description

This workflow accepts a Microsoft Teams command and performs a GeoIP lookup using the IPStack plugin.

Sample Microsoft Teams Trigger Commands:

`!geoip <IP Address>`

# Key Features

* Geo-location lookup on an IP address from Microsoft Teams

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment (edit the input with the preset text of `change_me`).

To run the workflow, send the command `!geoip <IP address>` in your configured team and channel. The workflow will post after it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|1.3.0|4|
|ExtractIt|2.0.0|1|
|IPStack|1.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [IPStack](https://ipstack.com/)
