# Description

This workflow triggers from directly slack messaging the chatbot to \"!reset_password\" the defined indicator. This workflow supports automatically Forcing a specified user to reset their password. The workflow will post back results to the specific user.

# Key Features

* Force a password reset for a specified user

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops
* Microsoft Active Directory

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and "Import" it into the workflow builder. Once imported, you will initially be prompted to configure the connection for slack and active directory.
In addition The `Find DN` step Will need the Search Base field to be defined. This field should be based on your Active Directory domain.
For example if your domain is example.com then the Search Base would be DC=example,DC=com

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "!reset_password <hash>".
Or use !nvestigate help for more information and examples.
The workflow will post with the results of the lookup.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Dig|1.0.5|1|
|Team Cymru MHR|1.0.4|1|
|Whois|2.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

[Slack](https://slack.com)