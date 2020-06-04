# Description

Understanding the scope of a phishing campaign is critical to ensuring no one in your organization takes the bait. This workflow runs a search from a command in Microsoft Teams and deletes emails across Office 365 inboxes.

Sample Trigger Commands:

`!delete-emails subject="A phishy email"`

`!delete-emails subject="A phishy email" from="example.com" body="Click here for free stuff" `


# Key Features

* **Know the Blast Radius** - More often than not with phishing attacks, where there’s one email, there’s many. Quickly find all users affected by the same campaign.
* **Eliminate the Threat** - Once a phishing message is verified, automatically remove that message from every inbox in your organization.
* **Rapidly Respond** - Every second wasted adds more risk to your environment. Rather than hopping from tool to tool to respond, take action directly from Microsoft Teams.

# Requirements

The following connections will need to be setup: 

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office 365 Email Security](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow is successfully imported, edit each Microsoft Teams step to reflect your team name and channel.

To run the workflow, in the channel you are monitoring enter the following:
`!delete-emails subject="A phishy email" from="example.com" body="Click here for free stuff" `

The workflow will reply when it has completed.

### Usage

This workflow uses the Microsoft Teams plugin to listen for key messages (commands). When the Microsoft Teams command triggers this workflow, it will open a compliance search in Office 365 and optionally delete messages.

To trigger this workflow, send the following command to the channel being monitored by the Microsoft Teams plugin:

`!delete-emails subject="A phishy email"`

This will kick off the workflow and prompt you when the search is completed.

Search criteria can be 'body', 'subject', or 'from' lines in the email. For example:

`!delete-emails subject="A phishy email" from="example.com" body="Click here for free stuff" `

Any combination of 'body', 'subject', and 'from' can be used. At least one search item must be given.

If you'd like the workflow to delete emails you can use 'delete=true'. For example:

`!delete-emails subject="A phishy email" delete=true`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.4|7|
|Microsoft Office365 Email Security|2.2.1|2|
|Python 3 Script|2.0.1|2|
|HTML|1.2.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.5 - Update to make Microsoft Teams plugin the latest version
* 1.0.4 - Set "change_me" items in workflow input
* 1.0.3 - Change trigger command from `purge-email` to `delete-emails`
* 1.0.2 - Updated documentation
* 1.0.1 - Update to Microsoft Teams 2.0.2
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office 365](https://www.office.com)
* [Microsoft Office 365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
* [Microsoft Teams Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Teams](https://teams.microsoft.com/)
