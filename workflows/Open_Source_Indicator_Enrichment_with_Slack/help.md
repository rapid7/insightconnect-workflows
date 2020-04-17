# Description

Look up and enrich URLs, IP addresses, and hashes directly from Slack using open source threat intelligence tools
such as Dig DNS and Whois.

# Key Features

* IP address, URL, and hash enrichment from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder.
After import, you will initially be prompted to configure the connection for slack.

To run the workflow, @ your Slackbot in any channel or in a direct message along with
the command `!investigate <command> <data>`. Example: `!investigate ip 8.8.8.8`

Alternatively, use `!investigate help` for more information and examples. The workflow will post with the results of the lookup.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Dig|1.0.3|1|
|Team Cymru MHR|1.0.3|1|
|WHOIS|1.0.7|2|

## Troubleshooting

In some instances using copy & paste for `!investigate` commands many introduce unicode characters.
These characters may be misinterpreted by the workflow, resulting in the help response triggering for
what appear to be valid commands. It is recommended to avoid copying & pasting commands.

# Version History

* 1.0.1 - Update help document
* 1.0.0 - Initial workflow

# Links

## References

[Slack](https://slack.com)