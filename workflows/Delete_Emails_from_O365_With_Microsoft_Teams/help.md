# Description

Once you’ve positively identified a phish, removing it from the user’s inbox is critical. This workflow searches for an email with specific criteria such as sender, receiver, or subject and provides the option to delete matches from Slack or Microsoft Teams.

Sample trigger commands:

`!delete-email user@example.com subject="A phishy email"`

`!delete-email user@example.com subject="A phishy email" delete="True"`

`!delete-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff"`

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

Once the workflow is successfully imported, edit each Microsoft Teams step to reflect your team name and channel.

To run the workflow, in the channel you are monitoring enter the following:
`delete-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff"`.

The workflow will reply when it has completed.

### Usage

This workflow uses the Microsoft Teams plugin to listen for key messages from a Microsoft Teams channel and will search for and optionally delete emails when triggered.

To trigger this workflow, in the Teams channel being monitored, enter a message like this:

`!delete-email user@example.com subject="A phishy email"`

This will kick off the workflow search for any emails with "A phishy email" in the subject. It will return the number found to the target Teams channel.

If you would like to automatically delete these emails, add `delete="True"` to the command, like this: 

`!delete-email user@example.com subject="A phishy email" delete="True"`

Search criteria can be 'body', 'subject', or 'from' lines in the email. For example:

`delete-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff"`

Any combination of 'body', 'subject', and 'from' can be used. At least one search item must be given.

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

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Exchange](https://products.office.com/en-us/exchange/email)
* [Slack](https://slack.com/)
