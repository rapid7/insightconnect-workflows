# Description

This workflow blacklists a MD5 hash globally with Symantec Endpoint Protection via Slack command and reports information back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-hash 9de5069c5afe602b2ea0a04b66beb2c0`

The hashes will show up in the "File Fingerprint List" under "Policies" in the Symantec Endpoint Protection console.

# Key Features

* Blacklist a hash globally

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Symantec Endpoint Protection account

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Broadcom Symantec Endpoint Protection|1.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Pass channel name from trigger to all subsequent steps so user only has to configure channel once
* 1.0.1 - Update title to include new branding
* 1.0.0 - Initial workflow

# Links

## References

* [Symantec Endpoint Protection](https://www.broadcom.com/products/cyber-security/endpoint/end-user)
* [Symantec Endpoint Protection plugin](https://extensions.rapid7.com/extension/broadcom_symantec_endpoint_protection)
* [Slack](https://slack.com)
