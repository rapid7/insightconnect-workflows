# Description

Don’t fall for the same phish twice. This workflow uses a Microsoft Teams command to block domains and senders in Office365.

Example Trigger Commands:

`!block_sender user@example.com`

`!block_sender anotherexample.com`


# Key Features

* **Block the Source** - Once the immediate threat has been contained, blocking the source of the phish prevents your organization from being targeted by the same threat actor twice.
* **Defense Wins Championships** - While you can’t prevent every attack, that doesn’t mean defense isn’t important.
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

The following connections will need to be setup: 

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office365 Email Security](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow is successfully imported, edit each Microsoft Teams step to reflect your team name and channel.

To run the workflow, in the channel you are monitoring enter the following:
`!block_sender <user_email>`. 

Your chat bot will reply when the workflow completes.

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

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Microsoft Teams](https://teams.microsoft.com)
* [Mail Flow Rules (Transport Rules)](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)
* [Microsoft Teams Plugin Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
