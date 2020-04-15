# Description

Initiate Azure AD password resets from Microsoft Teams.

Sample Microsoft Teams Trigger Commands:

`!reset_password user@example.com`

# Key Features

* Reset an Azure AD user password directly from Microsoft Teams

# Requirements

* Microsoft Teams connection
* Azure AD connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Microsoft Teams connection in the _Teams Message_ 
step and the _Update Teams With Success_ step. In addition, edit the _Reset User Password_ step with your correct Azure AD connection information.
Each Microsoft Teams step will need the team name and channel name updated as well (edit the input with the preset text of `change_me`).

To run the workflow, send the command `!reset_password <user_email>` in your configured team and channel.
The workflow will post after it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|1.3.0|2|
|ExtractIt|2.0.0|1|
|Azure AD Admin|1.4.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Azure AD](https://azure.microsoft.com/en-us/services/active-directory/)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
