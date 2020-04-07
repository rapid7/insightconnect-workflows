# Description

This workflow will delete emails matching given search criteria by sending a notification to InsightConnect with Slack. It will look for any emails that match the 'body', 'subject', and 'from'. It can either automatically delete these emails or prompt the user for further action.

# Key Features

* Removes malicious emails using a slack message

# Requirements

The following connections will need to be setup: 

* [Microsoft Office365](https://insightconnect.help.rapid7.com/docs/office365)
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

### Usage

This workflow uses the Chat Ops Slack connection to listen for key messages from the InsightConnect Rapid7 connection and will search for and delete emails when triggered.

To trigger this workflow, send a direct message to Rapid7 InsightConnect from Slack like the following:

`delete-email user@example.com subject="A phishy email"`

This will kick off the workflow and prompt you when the search is completed. If any emails are found that match the criteria, you can choose the delete button in Slack to delete them.

Search criteria can be body, subject, or from lines in the email. For example:

`delete-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff" `

Any combination of body, subject, and from can be used. At least one search item must be given.

If you'd like the workflow to just delete emails without prompting, you can also use 'delete=true' For example:

`delete-email user@example.com subject="A phishy email" delete=true`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office 365 Email|4.1.1|2|
|Python 3 Script|2.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Slack](https://slack.com/)
