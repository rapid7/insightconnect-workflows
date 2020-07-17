# Description

This workflow will quarantine an endpoint in CylanceOPTICS from a Slack command. This workflow supports endpoints in the form of IP address, MAC address, hostname, or device ID.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint 198.51.100.100`

In menu from the "CylancePROTECT" page in tab "CylanceOPTICS", the quarantined endpoints will show after choose tab "Devices". When the "Device Status" is "Locked Down", endpoint is quarantined.


# Key Features

* Quarantine endpoints

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* CylancePROTECT account with permission to manage endpoints

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|BlackBerry CylancePROTECT|1.1.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [BlackBerry CylancePROTECT](https://www.cylance.com)
* [CylancePROTECT plugin](https://github.com/rapid7/insightconnect-plugins/tree/master/cylance_protect)
* [Slack](https://slack.com)
