# Description

This workflow accepts a Slack command containing a SHA256 hash which Cylance will blacklist.

Sample Slack commands:

`@Rapid7 InsightConnect !blacklist-hash 275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f`

`@Rapid7 InsightConnect !unblacklist-hash 275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f`

# Key Features

* Blacklist a hash from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/slack)
* Cylance API key

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

To configure the workflow to your environment, edit the first trigger step by changing the Slack channel from
`change_me` to your enviroments Slack channel.

To run the workflow,  Use one of the example Slack command and the workflow will post responses in the channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|BlackBerry CylancePROTECT|1.0.3|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Cylance](https://www.cylance.com/)
* [Slack](https://slack.com)