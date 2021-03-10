# Description

This workflow will dissect an email and return all potential malicious indicators to Slack in a message. 

# Key Features

* Automatically post potential malicious indicators to Slack

# Requirements

The following connections will need to be setup: 

* [Gmail Setup Guide](https://insightconnect.help.rapid7.com/docs/gmail-api)
* [Slack ChatOps](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow is successfully imported, edit each Slack ChatOps step to target the channel you would like indicators posted to. Change the New Message trigger inputs to monitor the mailbox and folder where phish emails will be sent. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|4|
|HashIt|2.0.3|2|
|String Operations|1.2.1|2|
|Python 3 Script|2.0.1|1|
|Gmail|5.1.4|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Fix change_me typo in Slack `recipient` input field
* 1.0.0 - Initial workflow

# Links

## References

* [Gmail](https://mail.google.com/)
* [Gmail Setup Guide](https://insightconnect.help.rapid7.com/docs/gmail-api)
* [Slack](https://slack.com/)
* [Slack ChatOps Setup Guide](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
