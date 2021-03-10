# Description

This workflow blacklists or unblacklists a SHA1 globally for all operating systems with SentinelOne via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-hash 02699626f388ed830012e5b787640e71c56d42d8`

`@Rapid7 InsightConnect unblacklist-hash 02699626f388ed830012e5b787640e71c56d42d8`

The hashes will show up on the "Blacklist" tab from the "Sentinels" page on the main menu in the SentinelOne console.

# Key Features

* Blacklist a hash globally

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* SentinelOne account with permission to manage blacklist

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|SentinelOne|5.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Update to use latest SentinelOne plugin | Replace pattern match with indicator extraction
* 1.0.2 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.1 - Add Job URL to failure messages
* 1.0.0 - Initial workflow

# Links

## References

* [SentinelOne](https://www.sentinelone.com/)
* [SentinelOne plugin](https://extensions.rapid7.com/extension/sentinelone)
* [Slack](https://slack.com)
