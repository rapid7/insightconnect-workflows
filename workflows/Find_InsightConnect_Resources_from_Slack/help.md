# Description

This workflow is designed to provide two benefits; first and foremost, it will allow you to easily find InsightConnect documentation through an interaction with the Slack app, and secondly, it will provide an example of how to structure Slack-based InsightConnect workflows in the future! This workflow allows you to seamlessly interact with the InsightConnect Slack app in order to find helpful resources to support your implementation. By kicking this workflow off in Slack using a custom command, you will be asked a series of questions to determine what stage of your implementation you are in, and what resources you may need. Behind the scenes, this workflow leverages a "Repeat Until" Loop in order to deliver a seamless user experience in Slack that allows you to change your answer several times, within a single execution of the Workflow. 


# Key Features

* Find resources and consume content without ever leaving Slack
* Explore multiple different paths within a single execution of the Workflow, all through Slack's interactive message experience
* This workflow does not require an orchestrator

# Requirements

* InsightConnect License
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Follow the [Configure Slack for ChatOps](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops) instructions to get the InsightConnect Slack app added to your organization's Slack instance. Then, import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Select your Slack workspace, and optionally rename the workflow. Select the _Activate workflow upon import_ box, and finish the import.

## Usage

_This workflow will trigger in any direct messages to the InsightConnect app, or any message in a channel directed @ the InsightConnect app. The app must first be invited to the channel in order to trigger the workflow this way._

To run the workflow, send a direct message to your InsightConnect Slack app or @ the app in a channel starting with the command `icon-start`.

For example, in a direct message with the InsightConnect app:

* `icon-start`

Or, in a channel including the app:

* `@Rapid7 InsightConnect icon-start`

## Technical Details

_There are no plugins utilized by this workflow, only the InsightConnect Slack app_.

Plugins utilized by workflow:
|Plugin|Version|Count|
|----|----|--------|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
