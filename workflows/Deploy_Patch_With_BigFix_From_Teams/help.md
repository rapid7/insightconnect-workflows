# Description

Deploy a patch with HCL BigFix to a target system with a Microsoft Teams message. This workflow accepts a Patch Title and Target Host, searches HCL BigFix for relevant fixlets, and attempts to deploy those fixlets to the Target Host. If successful, a link to the HCL BigFix action is returned in Microsoft Teams.

# Key Features

* Deploy a specific patch to a specific system
* Receive real-time updates on workflow execution, including links to InsightConnect jobs and HCL BigFix actions
* Keep your team in the loop when deploying hotfixes or missing patches with patching commands in a Microsoft Teams channel

# Requirements

The following connections will need to be setup: 

* HCL BigFix server URL and credentials
* Microsoft Teams

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After import, activate the workflow in order to trigger it.

## Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the `!deploy-patch` command. The command accepts two parameters: `patch` and `target`. Input the title (may be a partial match) of the patch that should be deployed and the hostname of the target.

For example:
* `!deploy-patch patch=Title of Patch target=HostName`

Both the `patch` and `target` parameters must be specified in order to run the workflow successfully. This workflow does not support deploying multiple patches to a single target or a single patch to multiple targets.

The workflow will post status updates throughout execution. When complete, it will post a link to the resulting Action in HCL BigFix.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|6|
|HTML|1.2.1|1|
|BigFix|7.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.1.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 2.0.0 - Updated workflow to use newly branded "HCL BigFix" plugin
* 1.0.1 - Update to make Microsoft Teams plugin the latest version 
* 1.0.0 - Initial workflow

# Links

## References

* [HCL BigFix](https://bigfix.com)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
