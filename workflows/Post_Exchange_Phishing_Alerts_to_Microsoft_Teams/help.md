# Description

This workflow will dissect an email and return all potential malicious indicators to Microsoft Teams in a message. 

# Key Features

* Automatically post potential malicious indicators to Microsoft Teams

# Requirements

The following connections will need to be setup: 

* [Microsoft Exchange](https://insightconnect.help.rapid7.com/docs/microsoft-exchange)
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect.
Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow is successfully imported, edit each Microsoft Teams step to target the channel you would like
indicators posted to. Change the Email Received trigger inputs to monitor the mailbox and folder where phishing
emails will be sent. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|4|
|HashIt|2.0.3|1|
|String Operations|1.2.1|1|
|Python 3 Script|2.0.1|1|
|Microsoft Exchange|5.2.0|1|
|Microsoft Teams|3.1.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Update Microsoft Teams to version 3.1.0
* 1.0.2 - Update to make Microsoft Teams plugin the latest version
* 1.0.1 - Change Microsoft Teams input fields to match new standards
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Exchange](https://www.microsoft.com/en-us/microsoft-365/exchange/email)
* [Microsoft Exchange Setup Guide](https://insightconnect.help.rapid7.com/docs/microsoft-exchange)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
* [Microsoft Teams Setup Guide](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
