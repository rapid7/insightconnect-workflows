# Description

This workflow will block a sender in Office 365 using a command sent from Slack.

# Key Features

* A simple command sent from Slack will block a malicious email or domain using Exchange transport rules

# Requirements

The following connections will need to be setup: 

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Microsoft Office365 Email Security](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

### Usage

This workflow uses the Slack App trigger to listen for key messages and will block a domain or email address when triggered.

To trigger this workflow, in a direct message to the Rapid7 InsightConnect App in slack, send the following message.

`block_sender user@example.com`

You can also block a malicious domain. For example: 

`block_sender example.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office365 Email Security|2.2.1|1|
|Python 3 Script|2.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Mail Flow Rules (Transport Rules)](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)
* [Microsoft Office365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
* [Slack Configuration](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Slack](https://slack.com/)
