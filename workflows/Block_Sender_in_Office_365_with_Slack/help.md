# Description

Don’t fall for the same phish twice. This workflow uses a Slack command to block domains and senders in Office 365.

Sample Slack Trigger Commands:

`@Slackbot !block_sender user@example.com`

# Key Features

* **Block the Source** - Once the immediate threat has been contained, blocking the source of the phish prevents your organization from being targeted by the same threat actor twice.
* **Defense Wins Championships** - While you can’t prevent every attack, that doesn’t mean defense isn’t important.
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Microsoft Office365 Email Security](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Active the workflow in order to trigger it from Slack.

### Usage

To trigger this workflow, @ the Slackbot in Slack or send the bot a DM in the following format:

`!block_sender user@example.com`

You can also block a malicious domain. For example: 

`!block_sender example.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office365 Email Security|2.2.1|1|
|Python 3 Script|2.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Updated documentation
* 1.0.1 - Fix to Slack input command to standardize with leading exclamation point
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Mail Flow Rules (Transport Rules)](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)
* [Microsoft Office365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
* [Slack Configuration](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Slack](https://slack.com/)
