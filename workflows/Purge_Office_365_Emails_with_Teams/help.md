# Description

This workflow will delete all emails matching given search criteria from an organization using a command issued from Microsoft Teams.

# Key Features

* A simple command sent from Teams will purge all emails from an organization using an Office 365 compliance search

# Requirements

The following connections will need to be setup: 

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office365 Email Security](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

### Usage


This workflow uses the Microsoft Teams plugin to listen for key messages. When the Microsoft Teams command triggers this workflow, it will open a compliance search in Office 365 and optionally delete messages.

To trigger this workflow, send the following command to the channel being monitored by the Microsoft Teams plugin:

`!purge-email subject="A phishy email"`

This will kick off the workflow and prompt you when the search is completed.

Search criteria can be 'body', 'subject', or 'from' lines in the email. For example:

`!purge-email subject="A phishy email" from="example.com" body="Click here for free stuff" `

Any combination of 'body', 'subject', and 'from' can be used. At least one search item must be given.

If you'd like the workflow to delete emails you can use 'delete=true'. For example:

`!purge-email subject="A phishy email" delete=true`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.1|7|
|Microsoft Office365 Email Security|2.2.1|2|
|Python 3 Script|2.0.1|2|
|HTML|1.2.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office365](https://www.office.com)
* [Microsoft Office365 Email Security Plugin Configuration](https://insightconnect.help.rapid7.com/docs/mass-delete-with-powershell#section-set-up-office-365-dependencies)
* [Microsoft Teams Configuration](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Teams](https://teams.microsoft.com/)
