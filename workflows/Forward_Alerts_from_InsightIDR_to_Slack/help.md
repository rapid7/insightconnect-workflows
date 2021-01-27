# Description

This workflow forwards IDR alerts to a Slack channel.

# Key Features

* Send IDR alert to Slack channel

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [InsightIDR](https://www.rapid7.com/products/insightidr/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **update the last step with the channel name to suit your Slack environment** by editing the input with the preset text of `change_me` to match the channel to monitor.

After the workflow was activated [create a new alert trigger in InsightIDR](https://docs.rapid7.com/insightidr/alert-triggers#configure-alert-triggers) and select all alert types that should be forwarded to Slack.

### Usage

You can also manually trigger this workflow from the investigation. To do this click the **Take Action** button and choose **Custom InsightConnect Workflows**. From the list select the imported workflow.

## Technical Details

By default this workflow forwards the IDR Alerts to the Slack channel `#change_me`. This can be changed in the last workflow step.

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
* [InsightIDR](https://www.rapid7.com/products/insightidr/)
