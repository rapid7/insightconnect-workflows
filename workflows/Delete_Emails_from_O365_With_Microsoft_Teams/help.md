# Description

Don’t let your users fall for the same phish twice. This workflow uses a Slack command to find all emails in the target user's Office 365 inbox that match the provided search criteria. It will look for any emails that match the 'body', 'subject', and 'from'. It will automatically delete these emails by using the `delete` flag.

Sample trigger commands:

`!find-email user@example.com subject="A phishy email"`

`!find-email user@example.com subject="A phishy email" delete="True"`

`!find-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff"`

# Key Features

* **Eliminate the Threat** - Once a phishing message is verified, the first thing you should do is remove that message from the affected user’s inbox. 
* **Work with Unparalleled Flexibility** - Take your work mobile and respond to reported threats from your phone, tablet, or PC.
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

The following connections will need to be setup: 

* [Microsoft O365](https://insightconnect.help.rapid7.com/docs/office365)
* Microsoft Teams

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams steps, activate the workflow in order to trigger it.

## Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!find-email`. 

For example:
* `!find-email user@example.com subject="A phishy email"`.

This will kick off the workflow search for any emails with "A phishy email" in the subject. It will return the number found to the target Teams channel.

Search criteria can be 'body', 'subject', or 'from' lines in the email. 

For example:
* `!find-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff" `

Any combination of 'body', 'subject', and 'from' can be used. At least one search item must be given.

If you'd like the workflow to delete matching emails, use `delete=true` 

For example:
* `!find-email user@example.com subject="A phishy email" delete=true`

The workflow will reply with the number of found emails.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office 365 Email|4.1.1|2|
|Microsoft Teams|2.0.1|6|
|Python 3 Script|2.0.1|2|
|HTML|1.2.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Updated trigger syntax and documentation
* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Exchange](https://products.office.com/en-us/exchange/email)
* [Slack](https://slack.com/)
