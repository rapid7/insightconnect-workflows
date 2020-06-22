# Description

Use the simplicity of a chat command in Slack to manage the quarantine state of an endpoint with
Broadcom Symantec Endpoint Protection.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect quarantine-endpoint example-host`

`@Rapid7 InsightConnect quarantine-endpoint 00:A0:C9:14:C8:29`

`@Rapid7 InsightConnect unquarantine-endpoint example-host`

`@Rapid7 InsightConnect unquarantine-endpoint 00:A0:C9:14:C8:29`


# Key Features

* Manage the quarantine state of endpoints via hostname or MAC address

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Broadcom Symantec Endpoint Protection
* Credentials for a Broadcom Symantec Endpoint Protection user with System Administrator privileges

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Slack step will need the channel name updated to suit your Slack environment!** Edit the input with the preset text of `change_me` in each Slack step in the workflow.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
An optional whitelist can be added to the Broadcom Symantec Endpoint Protection `Quarantine` action. To use this list 
add MAC addresses or hostnames in the following format (colons or hyphens are acceptable for MAC addresses) `["00:A0:C9:14:C8:29", "example-host"]`

### Usage

To run the workflow, @ your Slack chatbot starting with the command `@Rapid7 InsightConnect quarantine-endpoint` or `@Rapid7 InsightConnect unquarantine-endpoint`.

Your chat bot will reply when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Broadcom Symantec Endpoint Protection|1.0.2|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Broadcom Symantec Endpoint Protection](https://www.broadcom.com/products/cyber-security/endpoint/end-user)
* [Slack Configuration](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Slack](https://slack.com/)
