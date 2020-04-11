# Description

This workflow will block a sender in Office 365 using a command sent from Microsoft Teams

# Key Features

* A simple command sent from Microsoft Teams will block a malicious email or domain using Exchange transport rules

# Requirements

The following connections will need to be setup: 

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office365 Email Security](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

### Usage

This workflow uses the Microsoft Teams plugin to listen for key messages and will block a domain or email address when triggered.

To trigger this workflow, in the target Teams channel, send the following message.

`!block_sender user@example.com`

You can also block a malicious domain. For example: 

`!block_sender example.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.1|5|
|Microsoft Office365 Email Security|2.2.1|1|
|HTML|1.2.1|1|
|String Operations|1.2.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Microsoft Teams](https://teams.microsoft.com)
* [Mail Flow Rules (Transport Rules)](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)
* [Microsoft Teams Plugin Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
