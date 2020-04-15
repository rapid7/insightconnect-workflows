# Description

Suspend Azure AD users from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect !suspend_user user@example.com`

# Key Features

* Suspend an Azure AD user directly from Slack

# Requirements

* Slack connection
* Azure AD connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _Slack Message_ 
step and the _Reply with Success_ and _Reply with Failure_ steps. In addition, edit the _Suspend User Account_
step with your correct Azure AD connection information.
Each Slack step will need the channel name updated as well (edit the input with the preset text of `change_me`).

To run the workflow, @ your Slackbot in any channel or in a direct message
along with the command `!suspend_user <user_email>`. The workflow will reply when it has completed.

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
