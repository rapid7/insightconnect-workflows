# Description

Quickly look up inactive assets in Rapid7 InsightVM using Slack, and make a decision to delete them. This workflow helps teams maintain a clean and accurate count of assets in their environment through shared Slack channels.

# Key Features

* Lookup inactive assets in InsightVM from Slack
* Delete inactive assets in InsightVM through human decisions

# Requirements

* Rapid7 InsightVM
* Slack

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

### InsightVM

This workflow requires a pre-configured InsightVM (or Nexpose) asset group in order to list and delete inactive assets.

1. Create a new dynamic asset group in InsightVM with a filter similar to this: **`Last scan date earlier than 90 days ago.`**
2. Save the asset group configuration and navigate to the Asset Group page. View the URL in your web browser to find the `Group ID`. For example, if my console URL is `https://10.1.2.3:3780/group.jsp?groupid=123`, then my `Group ID` is `123`.

Once you have found the Group ID, move on to configure the Get Inactive Assets step in the InsightConnect workflow.

### InsightConnect

Once the workflow has been imported:
1. Update the first step with the channel name to suit your Slack environment by editing the input with the preset text of `change_me` to match the channel to monitor. The InsightConnect Slack chatbot will need to be added to this channel. This workflow is configured by default so that it may only be started from this channel.
2. Edit the `Get Inactive Assets` step. Insert the `Group ID` into the first input field, replacing the existing number, and save the step.
3. Activate the workflow in order to trigger it.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.8.1|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Slack](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops)
