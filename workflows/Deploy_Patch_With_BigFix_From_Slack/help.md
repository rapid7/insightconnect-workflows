# Description

Deploy a patch with HCL BigFix to a target system with a Slack message. This workflow accepts a Patch Title and Target Host, searches HCL BigFix for relevant fixlets, and attempts to deploy those fixlets to the Target Host. If successful, a link to the HCL BigFix action is returned in Slack.

# Key Features

* Deploy a specific patch to a specific system
* Receive real-time updates on workflow execution, including links to InsightConnect jobs and HCL BigFix actions
* Keep your team in the loop when deploying hotfixes or missing patches with patching commands in Slack channels

# Requirements

The following connections will need to be setup: 

* HCL BigFix server URL and credentials
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

## Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `deploy-patch`. The command accepts two parameters: `patch` and `target`. Input the title (may be a partial match) of the patch that should be deployed and the hostname of the target.

For example, in a direct message to your Chatbot:
* `deploy-patch patch=Title of Patch target=targetHostName`

Or in a channel including your Chatbot:
* `@Rapid7 InsightConnect deploy-patch patch=Title of Patch target=targetHostName`

Both the `patch` and `target` parameters must be specified in order to run the workflow successfully. This workflow does not support deploying multiple patches to a single target or a single patch to multiple targets.

The workflow will post status updates throughout execution. When complete, it will post a link to the resulting Action in HCL BigFix.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|BigFix|7.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 2.0.0 - Updated workflow to use newly branded "HCL BigFix" plugin
* 1.0.0 - Initial workflow

# Links

## References

* [HCL BigFix](https://bigfix.com)
* [Slack](https://slack.com)
