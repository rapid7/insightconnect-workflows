# Description

Suspend Active Directory LDAP users from Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect disable-user-ad <exampleuser>`

# Key Features

* Suspend an Active Directory LDAP user directly from Slack

# Requirements

* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Active Directory LDAP connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in Slack chatbot steps.
In addition, edit the Active Directory LDAP steps with your correct Active Directory LDAP connection information. Notably, edit the search base in the `Find DN` step.

To run the workflow, @Rapid7 InsightConnect in any channel or in a direct message
along with the command `disable-user-ad <username>`. The workflow will acknowledge the request and reply when it has
completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|3.2.8|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update trigger syntax, update documentation, fix naming scheme, add clarity to setup for LDAP search base
* 1.0.0 - Initial workflow

# Links

## References

* [Active Directory LDAP](https://extensions.rapid7.com/extension/active_directory_ldap)
* [Slack](https://slack.com)
