# Description

This workflow will dissect an email and return all potential malicious indicators to Microsoft Teams in a message. 

# Key Features

* Automatically post potential malicious indicators to Microsoft Teams

# Requirements

The following connections will need to be setup: 

* [Microsoft Office 365](https://insightconnect.help.rapid7.com/docs/office365)
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow is successfully imported, edit each Microsoft Teams step to target the channel you would like indicators posted to. Change the New Message trigger inputs to monitor the mailbox and folder where phish emails will be sent. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|4|
|Microsoft Teams|3.1.2|2|
|HashIt|2.0.4|2|
|String Operations|1.3.1|2|
|Python 3 Script|2.0.2|1|
|Microsoft Office 365 Email|5.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Update step `Nested Headers` and `Top Level Headers` inputs | Update Microsoft Teams version to 3.1.2 | Update String Operations version to 1.3.1 | Update Python 3 Script version to 2.0.2 | Update Microsoft Office 365 Email version to 5.0.1 | Update HashIt version to 2.0.4
* 1.0.7 - Update Microsoft Teams to version 3.1.0
* 1.0.6 - Update to make Microsoft Teams plugin the latest version
* 1.0.5 - Fix issue where Nested Headers artifact incorrectly defined an each loop
* 1.0.4 - Update description
* 1.0.3 - Set more "change_me" items in workflow input
* 1.0.2 - Set "change_me" items in workflow input
* 1.0.1 - Update to fix title
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office 365](https://office.microsoft.com)
* [Microsoft Office 365 Setup Guide](https://insightconnect.help.rapid7.com/docs/office365)
* [Microsoft Teams](https://teams.microsoft.com/)
* [Microsoft Teams Setup Guide](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
