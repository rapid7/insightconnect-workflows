# Description

This workflow listens for InsightVM Webhook Events for newly remediated vulnerabilities and notifies a Slack channel of which vulnerabilities were remediated. It also includes asset information to easily identify which system the vulnerabilities were remediated from.

This notification helps Security and IT teams raise the visibility of newly patched vulnerabilities. This heightened awareness can improve cross-functional team communication and performance.

# Key Features

* Heightened awareness of newly remediated vulnerabilities
* VM Events trigger utilizes InsightVM's new webhook feature
* Flexible workflow design allows for easy customization


# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Insight Platform User API Key
* InsightVM
* InsightConnect

# Documentation

## Setup

*In order to use this workflow, you will need to subscribe to the InsightVM Vulnerabilities Found webhook event. You will also need to adjust the Slack channel name to match your environment.*
Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.
Once the workflow has been imported, open the workflow, and view the InsightVM Events trigger step. Click “Save Step” so that you reach the “Instructions” menu. Proceed through the instructions to subscribe to the InsightVM Vulnerabilities Remediated Webhook Event. This will require an Insight Platform User API Key . Insert your User API Key, copy the API request, run it from a command-line interface, and look for a JSON response including an ID. If you receive a JSON response, then your webhook event subscription is active! Close your command-line interface and return to the workflow in InsightConnect.
After subscribing to the vulnerabilities remediated webhook event, return to the workflow editor, and open the `Post To Slack` step. In the input field, change the preset `change_me` inputs to the team and channel names from your Slack environment where you would like vulnerability notifications delivered. We recommend a private channel with representatives from security and remediation teams for the best visibility.
After configuring the Slack step, activate the workflow. Any newly remediated vulnerability will generate a webhook event, triggering your workflow and delivering a message to the specified Slack channel!

## Usage

This workflow is triggered automatically by InsightVM’s Vulnerabilities Remediated Webhook Event. This occurs anytime an asset is scanned in InsightVM and pre-existing vulnerabilities disappear and anytime a vulnerability exception is approved.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Type Converter|1.6.0|1|
|Rapid7 Vulnerability & Exploit Database|2.0.3|1|

## Troubleshooting

Experiencing delays? InsightVM Events are delivered to InsightConnect from InsightVM as soon as the Insight platform is notified of a change by the on-premises InsightVM Security Console. This can take anywhere from 5 minutes to several hours. Please be patient!

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability & Exploit Database](https://rapid7.com/db)
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
