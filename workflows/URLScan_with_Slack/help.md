# Description

This workflow looks up a URL given via Slack command in urlscan.io and reports information on the URL back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect enrich-url https://example.com/suspicious/url`

# Key Features

* Enrich URL from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* urlscan.io API Key

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _URLScan Slack Trigger_ step.

The URLScan connection needs to be setup for steps _Submit URL for Scan_ and _Get URLScan Report_.

To run the workflow, @ your Slackbot in the channel along with the command "enrich-url <URL>". The workflow will post a response in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|URLScan|2.1.4|2|
|Python 3 Script|2.0.1|1|
|Sleep|1.0.2|1|

## Troubleshooting

If a URL is submitted but no report is generated, urlscan.io may have blacklisted the domain.

# Version History

* 1.0.2 - Updated documentation
* 1.0.1 - Updated Documentation and names
* 1.0.0 - Initial workflow

# Links

## References

* [URLScan](https://urlscan.io)
* [Slack](https://slack.com)