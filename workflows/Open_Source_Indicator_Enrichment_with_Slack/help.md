# Description

This workflow triggers from directly slack messaging the chatbot to \"!investigate\" the defined indicator. This workflow supports automatically looking up URLs, IPs, and hashs in open source threat intelligence such as Dig DNS and Whois. Lastly, the workflow will post back results to the specific user.

# Key Features

* IP, URL, and hash enrichment from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder. Once imported, you will initially be prompted to configure the connection for slack.

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "!investigate <command> <data>".
example: !investigate ip 8.8.8.8
Or use !investigate help for more information and examples.
The workflow will post with the results of the lookup.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Dig|1.0.5|1|
|Team Cymru MHR|1.0.4|1|
|Whois|2.0.1|2|

## Troubleshooting

In some instances using copy paste for !investigate commands many introduce unicode characters.
These characters may be misinterpreted by the workflow,
resulting in the help response triggering for what look like valid commands.
It is recommend to not copy past the word `!investigate` or the <command>.
No issues have been encountered when copy pasting the hash's IP's or URL's them selves.

# Version History

* 1.0.0 - Initial workflow

# Links

## References

[Slack](https://slack.com)