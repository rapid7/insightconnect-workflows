# Description

This workflow triggers from directly slack messaging the chatbot to \"!reset_password\" the defined indicator. This workflow supports automatically Forcing a specified user to reset their password. The workflow will post back results to the specific user.

# Key Features

* Reset an Active Directory user password directly from Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops
* Microsoft Active Directory

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder.
Once imported, you will initially be prompted to configure the connection for Slack and Active Directory.
In addition The `Find DN` step will need the Search Base field to be defined. This field should be based on your Active Directory domain.
For example if your domain is `example.com` then the Search Base would be `DC=example,DC=com`.

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "!reset_password <username>".
The workflow will post whether the force reset was successful or not.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|3.2.8|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

[Slack](https://slack.com)
