# Description

This workflow quarantines or unquarantines endpoints with VMware Carbon Black Cloud via Slack command and reports information back to Slack.
This workflow supports endpoints in the form of Device IDs, hostnames, or IP addresses.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint example-host`

`@Rapid7 InsightConnect quarantine-endpoint 198.51.100.100`

`!unquarantine-endpoint 198.51.100.100`

`!unquarantine-endpoint example-host`


# Key Features

* Quarantine and unquarantine endpoints

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* VMware Carbon Black Cloud account with [Automation API Access Settings configured](https://developer.carbonblack.com/reference/carbon-black-cloud/authentication/#creating-an-api-key)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Carbon Black Cloud|1.0.1|2|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Updated VMware Carbon Black branding
* 1.0.1 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.0 - Initial workflow

# Links

## References

* [VMware Carbon Black Cloud](https://www.carbonblack.com/products/vmware-carbon-black-cloud)
* [VMware Carbon Black Cloud plugin](https://extensions.rapid7.com/extension/carbon_black_cloud)
* [Slack](https://slack.com)
