# Description

This workflow returns enriched CVE details by performing a vulnerability lookup with Recorded Future.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect enrich-cve CVE-2019-0708`

# Key Features

* Perform a CVE lookup

# Requirements

* Recorded Future API Key
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, update the first step with the channel name to suit your Slack environment by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring those steps, activate the workflow and then issue a Slack command to trigger it. 

### Usage

*This workflow will only trigger in the channel specified in the ChatOps workflow steps.*

To run the workflow, send a message to the specified Slack channel starting with the command `@Rapid7 InsightConnect enrich-cve` and then provide the CVE ID of the vulnerability you would like to get more details on.

Your chat bot will reply to the message thread when the workflow completes.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Recorded Future|2.2.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Recorded Future API Documentation](https://support.recordedfuture.com/hc/en-us/categories/115000803507-Raw-API)
* [Slack](https://slack.com)
