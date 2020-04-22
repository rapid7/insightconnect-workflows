# Description

Disable User in Microsoft Active Directory with Microsoft Teams.

Sample Slack Trigger Commands:

`!disable_user <exampleuser>`

# Key Features

* Suspend an Active Directory LDAP user directly from Microsoft Teams

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Active Directory LDAP connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.
Once the workflow has been imported, each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment (edit the input with the preset text of `change_me`).
To run the workflow, send the command `!disable_user <exampleuser>` in your configured team and channel. The workflow will post after it has completed.
In the Team and chanel inputs replace `change_me` with the appropriate team and channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|3.2.8|2|
|Microsoft Teams|2.0.2|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Active Directory LDAP](https://extensions.rapid7.com/extension/active_directory_ldap)
* [Microsoft Teams](https://teams.microsoft.com)
