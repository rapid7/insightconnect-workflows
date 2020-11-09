# Description

Disabling a compromised account can limit the scope of an attack and buy valuable time to investigate and contain the
threat. This workflow disables or enables a domain user account with a command in Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect disable-user-ad <username>`

`@Rapid7 InsightConnect enable-user-ad <username>`

# Key Features

* Disable an Active Directory LDAP user directly from Slack
* Enable an Active Directory LDAP user directly from Slack

# Requirements

* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Active Directory LDAP connection

# Documentation

## Setup

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by
editing the input with the preset text of `change_me` to match the channel to monitor.

In addition, edit the Active Directory LDAP steps with your correct Active Directory LDAP connection information. Notably,
edit the search base in the `Find DN` step.

After configuring the Slack steps, activate the workflow in order to trigger it.

To run the workflow, @ your Slackbot in the channel along with the command `disable-user-ad <username>` or
`enable-user-ad <username>`. The workflow will acknowledge the request and reply when it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|4.0.2|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - New functionality - Enable AD User
* 1.0.1 - Update trigger syntax, update documentation, fix naming scheme, add clarity to setup for LDAP search base
* 1.0.0 - Initial workflow

# Links

## References

* [Active Directory LDAP](https://extensions.rapid7.com/extension/active_directory_ldap)
* [Slack](https://slack.com)
