# Description

This workflow will delete emails matching given search criteria by sending a notification to InsightConnect with Microsoft Teams. It will look for any emails that match the 'body', 'subject', and 'from'. 

# Key Features

* Removes malicious emails using a Slack message

# Requirements

The following connections will need to be setup: 

* Microsoft O365
* Microsoft Teams

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

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

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Exchange](https://products.office.com/en-us/exchange/email)
* [Slack](https://slack.com/)
