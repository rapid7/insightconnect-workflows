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

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder.
After import, you will initially be prompted to configure the connection for Microsoft Teams.
You will then need to configure the Microsoft Teams trigger and actions.
In the "Team" and "Channel" inputs replace `change_me` with the appropriate team and channel.

To run the workflow, message in the channel the command "!geoip <IP Address>". The workflow will post a response in a thread.

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
