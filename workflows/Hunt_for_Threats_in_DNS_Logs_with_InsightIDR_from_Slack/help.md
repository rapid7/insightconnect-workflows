# Description

Lookup suspicious domains in IDR DNS Query logs with a simple slack command. This workflow accepts domains and URLs as input.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect get-logs aadroid.net`

`@Rapid7 InsightConnect get-logs https://aadroid.net`

# Key Features

* **Quickly analyze the scope of a malicious domain** - Quickly find out how many of your users were affected by a malicious domain

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [InsightIDR](https://www.rapid7.com/products/insightidr/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

To run the workflow, send a direct message to your InsightConnect Slack Chatbot starting with the command `get-logs`. 

For example:

* `@Rapid7 InsightConnect get-logs badsite.com`

The workflow will also accept full URLS and convert those into domains for you. For example: 

* `@Rapid7 InsightConnect get-logs http://www.badsite.com`

The workflow will pull the domain out of the command and search for `badsite.com`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Datetime|2.2.0|2|
|Type Converter|1.6.1|1|
|Rapid7 InsightIDR|2.0.1|1|
|ExtractIt|2.0.0|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [InsightIDR](https://www.rapid7.com/products/insightidr/)
* [Slack](https://slack.com)
