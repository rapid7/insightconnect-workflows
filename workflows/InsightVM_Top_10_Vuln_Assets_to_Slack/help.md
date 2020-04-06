# Description

This workflow returns the top 10 most vulnerable assets in each site in InsightVM.

Sample Slack Trigger Commands:

`@Slack bot list most vulnerable assets`

# Key Features

* Lists most vulnerable assets from InsightVM in Slack

# Requirements

API and account credentials for

* InsightVM
* Slack

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "list most vulnerable assets". The workflow will post responses in a thread.


## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|CSV|1.1.5|1|
|Rapid7 InsightVM|4.0.0|2|
|Type Converter|1.5.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [InsightVM] (https://www.rapid7.com/products/insightvm/)
* [Slack] (https://www.slack.com)
