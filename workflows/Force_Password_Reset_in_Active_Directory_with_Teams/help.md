# Description

Force an Active Directory user password reset from Microsoft Teams.

Sample Slack command:

`!reset_password user`

# Key Features

* Reset an Active Directory user password directly from Microsoft Teams

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Microsoft Active Directory

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder.
After import, you will initially be prompted to configure the connection for Microsoft Teams and Microsoft Active Directory.
You will then need to configure the Teams trigger and actions.
In the Team and chanel inputs replace `change_me` with the appropriate team and channel.

To run the workflow, in the configured channel and enter the command `!reset_password <username>`.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.2|4|
|Active Directory LDAP|3.2.8|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
