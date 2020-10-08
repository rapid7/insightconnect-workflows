# Description

Use the simplicity of a chat command in Microsoft Teams to get enriched details about a vulnerability using your Recorded Future.

Sample Microsoft Teams Trigger Commands:

`!enrich-cve CVE-2019-0708`

# Key Features

* **Return Enriched CVE Details** - Use Microsoft Teams and Recorded Future to get enriched CVE details. 

# Requirements

* Recorded Future API Key
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring those steps, activate the workflow and then issue a Microsoft Teams command to trigger it. 

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!block-host` and then provide the CVE ID of the vulnerability you would like to get more details on.

For example:
* `!enrich-cve CVE-2019-0708`

The workflow will reply when it completes.

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
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
