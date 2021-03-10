# Description

This workflow blacklists or unblacklists a SHA256 globally with CylancePROTECT via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-hash 30f800f97aeaa8d62bdf3a6fb2b0681179a360c12e127f07038f8521461e5050`

`@Rapid7 InsightConnect unblacklist-hash 30f800f97aeaa8d62bdf3a6fb2b0681179a360c12e127f07038f8521461e5050`

The hashes will show up in the Global Quarantine list in CylancePROTECT.

# Key Features

* Blacklist a hash globally

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* CylancePROTECT
* Create a "Custom Application" in CylancePROTECT (Settings -> Integrations -> Add Application)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|BlackBerry CylancePROTECT|1.0.3|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.1 - Add Job URL to failure messages
* 1.0.0 - Initial workflow

# Links

## References

* [BlackBerry CylancePROTECT](https://www.cylance.com)
* [BlackBerry CylancePROTECT plugin](https://extensions.rapid7.com/extension/cylance_protect)
* [Slack](https://slack.com)
