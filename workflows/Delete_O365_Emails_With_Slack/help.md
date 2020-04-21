# Description

Don’t fall for the same phish twice. This workflow uses a Slack command to find all emails in Office 365 that match the provided search criteria. It will look for any emails that match the 'body', 'subject', and 'from'. It can either automatically delete these emails or prompt the user for further action.

Sample Slack trigger command:

`!delete-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff" `

`!delete-email user@example.com subject="A phishy email" delete=true`


# Key Features

* **Eliminate the Threat** - Once a phishing message is verified, the first thing you should do is remove that message from the affected user’s inbox. 
* **Work with Unparalleled Flexibility** - Take your work mobile and respond to reported threats from your phone, tablet, or PC.
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

The following connections will need to be setup: 

* [Microsoft Office365](https://insightconnect.help.rapid7.com/docs/office365)
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After importing, activate the workflow in order to trigger it.

### Usage

This workflow uses the Chat Ops Slack connection to listen for key messages from the InsightConnect Rapid7 connection and will search for and delete emails when triggered.

To trigger this workflow, send a direct message to Rapid7 InsightConnect from Slack like the following:

`!delete-email user@example.com subject="A phishy email"`

This will kick off the workflow and prompt you when the search is completed. If any emails are found that match the criteria, you can choose the delete button in Slack to delete them.

Search criteria can be 'body', 'subject', or 'from' lines in the email. For example:

`!delete-email user@example.com subject="A phishy email" from="example.com" body="Click here for free stuff" `

Any combination of 'body', 'subject', and 'from' can be used. At least one search item must be given.

If you'd like the workflow to just delete emails without prompting, you can also use 'delete=true' For example:

`!delete-email user@example.com subject="A phishy email" delete=true`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Office 365 Email|4.1.1|3|
|Python 3 Script|2.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.5 - Updated documentation
* 1.0.4 - Update to remove join step
* 1.0.3 - Fix name matching
* 1.0.2 - Fix filename
* 1.0.1 - Fix to Slack input command to standardize with leading exclamation point
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Slack](https://slack.com/)
