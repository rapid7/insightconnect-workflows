# Description

Suspend Azure AD users from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect !suspend_user user@example.com`

# Key Features

* Suspend an Azure AD user directly from Slack

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Azure AD connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Microsoft Teams connection in the _Suspend User Teams Trigger_ 
step. In addition, edit the _Suspend User Account_ step with your correct Azure AD connection information.

Each Microsoft Teams step will need the team name and channel name updated as well (edit the input with the preset text of `change_me`).

To run the workflow, in the channel you are monitoring enter the following:
`!suspend_user <user_email>`. 

The workflow will reply when it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.2|4|
|ExtractIt|2.0.0|1|
|HTML|1.2.1|1|
|Azure AD Admin|1.4.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Azure AD](https://azure.microsoft.com/en-us/services/active-directory/)
* [Slack](https://slack.com)
