# Description

Revoke a user session forcing them to log in after their next page refresh with a command from Microsoft Teams. 

# Key Features

* Revoke a user session

# Requirements

* [Azure AD Admin](https://insightconnect.help.rapid7.com/docs/office365)
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.

### Usage

This workflow uses the Microsoft Teams plugin to monitor a channel for a specific command. To trigger this workflow enter the following in that channel

`!revoke-session user@example.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|5|
|String Operations|1.2.1|2|
|Azure AD Admin|2.2.0|1|
|HTML|1.2.1|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Replace the preset text of "change_me" with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.2 - Update to make Microsoft Teams plugin the latest version
* 1.0.1 - Update to correct `source_url` reference in spec
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office 365](https://www.office.com)
* [Azure](https://azure.microsoft.com)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup Guide](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office 365 Permissions and Setup](https://insightconnect.help.rapid7.com/docs/office365)
