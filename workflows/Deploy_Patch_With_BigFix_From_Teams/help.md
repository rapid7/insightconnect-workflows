# Description

Deploy a patch with BigFix to a target system with a Microsoft Teams message. This workflow accepts a Patch Title and Target Host, searches BigFix for relevant fixlets, and attempts to deploy those fixlets to the Target Host. If successful, a link to the BigFix action is returned in Microsoft Teams.

# Key Features

* Deploy a specific patch to a specific system
* Receive real-time updates on workflow execution, including links to InsightConnect jobs and BigFix actions
* Keep your team in the loop when deploying hotfixes or missing patches with patching commands in a Microsoft Teams channel

# Requirements

The following connections will need to be setup: 

* HCL BigFix server URL and credentials
* Microsoft Teams

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `Dream Team` and `change_me` in each Teams step in the workflow.

After import, activate the workflow in order to trigger it.

## Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the `!deploy-patch` command. The command accepts two parameters: `patch` and `target`. Input the title (may be a partial match) of the patch that should be deployed and the hostname of the target.

For example:
* `!deploy-patch patch=Title of Patch target=HostName`

Both the `patch` and `target` parameters must be specified in order to run the workflow successfully. This workflow does not support deploying multiple patches to a single target or a single patch to multiple targets.

The workflow will post status updates throughout execution. When complete, it will post a link to the resulting Action in BigFix.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.4|6|
|HTML|1.2.1|1|
|IBM BigFix|6.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update to make Microsoft Teams plugin the latest version 
* 1.0.0 - Initial workflow

# Links

## References

* [BigFix](https://bigfix.com)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
