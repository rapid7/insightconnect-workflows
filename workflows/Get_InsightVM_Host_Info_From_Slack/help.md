# Description

This workflow provides fast, convenient access to information about a given host from InsightVM. When triggered, the workflow fetches asset details from InsightVM and posts them in a Slack thread. Host info includes hostname, IP address, MAC address, operating system, running services, and vulnerability stats.

Sample Slack Trigger Commands: 

`@Slackbot get host info workstation123`

`@Slackbot get host info 192.168.1.2`

# Key Features

* Find details about a specified host
* Find details about a specified IP address
* Quickly check running services for a given asset

# Requirements

* InsightVM Console URL and account credentials
* Slack integration

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and configure connections and orchestrators in each step.

If you do not already have a Slack connection configured, please refer to our [Help documentation](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops).

### Usage

To trigger this workflow, @ the Slackbot in Slack or send the bot a DM in the following format:

`get host info workstation123`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Slack](https://slack.com)
