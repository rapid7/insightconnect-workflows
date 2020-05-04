# Description

Revoke a user session forcing them to log in after their next page refresh with a command from Slack. 

# Key Features

* Revoke a user session

# Requirements

* [Azure AD Admin](https://insightconnect.help.rapid7.com/docs/office365)
* [Slack Chat Ops](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

### Usage

This workflow uses the Slack Chat Ops trigger to monitor for a specific command. To trigger this workflow direct message the Rapid7 Insight Connect bot with:

`revoke-session user@example.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Python 3 Script|2.0.1|1|
|String Operations|1.2.1|1|
|Azure AD Admin|2.2.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office 365](https://www.office.com)
* [Azure](https://azure.microsoft.com)
* [Microsoft Office 365 Permissions and Setup](https://insightconnect.help.rapid7.com/docs/office365)
* [Slack](https://www.slack.com)
* [Slack Chat Ops](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)