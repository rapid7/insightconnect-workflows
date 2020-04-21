# Description

This workflow accepts a Slack command and performs a GeoIP lookup using the IPStack plugin.

Sample Slack Trigger Commands:

`@Slack bot !geoip <IP Address>`

# Key Features

* Geo-location lookup on an IP address from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _GeoIP Lookup Slack Trigger_ step.

To run the workflow, @ your Slackbot in the channel along with the command "!geoip <IP Address>". The workflow will post a response in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|IPStack|1.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update help
* 1.0.0 - Initial workflow

# Links

## References

* [IPStack](https://ipstack.com/)
* [Slack](https://slack.com)
