# Description

This workflow will dissect an email and return all potential malicious indicators to Microsoft Teams in a message.

# Key Features

* Automatically post potential malicious indicators to Microsoft Teams

# Requirements

The following connections will need to be setup: 

* [Gmail Setup Guide](https://insightconnect.help.rapid7.com/docs/gmail-api)
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
|HashIt|2.0.3|2|
|Microsoft Teams|2.0.4|2|
|String Operations|1.2.1|2|
|Python 3 Script|2.0.1|1|
|Gmail|5.1.4|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Gmail](https://mail.google.com/)
* [Gmail Setup Guide](https://insightconnect.help.rapid7.com/docs/gmail-api)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
* [Microsoft Teams Setup Guide](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
