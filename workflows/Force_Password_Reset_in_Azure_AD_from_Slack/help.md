# Description

Initiate Azure AD password resets from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect reset_password user@example.com`

# Key Features

* Reset an Azure AD user password directly from Slack

# Requirements

* Slack connection
* Azure AD connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _Slack Message_ 
step and the _Reply With Success_ step. In addition, edit the _Reset User Password_ step with your correct Azure AD connection information.
Each Slack step will need the channel name updated as well (edit the input with the preset text of `change_me`).

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command `!reset_password <user_email>`.
The workflow will reply when it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|Azure AD Admin|1.4.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Azure AD](https://azure.microsoft.com/en-us/services/active-directory/)
* [Slack](https://slack.com)
