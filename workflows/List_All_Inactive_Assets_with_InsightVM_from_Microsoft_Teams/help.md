# Description

Quickly look up inactive assets in [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/) using a Microsoft Teams command. This workflow helps teams share vulnerability intelligence through shared Microsoft Teams channels.

# Key Features

* Look up inactive assets in InsightVM using a Slack command

# Requirements

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported,

Update the first step with the team name and channel name to suit your Microsoft Teams environment by editing the input with the preset text of `change_me` to match the team and channel to monitor.

After import, activate the workflow in order to trigger it.

## Usage

To run the workflow, send the command `!list-inactive` to the Microsoft Teams channel you are monitoring.

The workflow is set to list assets that haven't been scanned in 14 days. To edit this number, please change the input for the "Get Inactive Assets" step.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.2.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)
