# Description

Reset a domain user's password with a command in Microsoft Teams. Quickly respond, whether it be to an emerging threat or to another user that locked themselves out of their account.

Sample Microsoft Teams command:

`!reset-password-ad <username>`

# Key Features

* **Break the Kill Chain** - Credentials provide attackers with easy access to numerous targets. Disabling a compromised account or forcing a password reset can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, disabling a user account can limit your threat exposure and buy your team valuable time to investigate and contain a threat. Disabling the user may not remediate the root cause, but it can mitigate the immediate risk while you work on fixing underlying issues.
* **Minimize Disruption to the User** - Forcing a user to reset their password is a small inconvenience compared to re-imaging their entire system. Acting fast can save valuable time and teach a valuable lesson without a noticeable impact to your business.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Microsoft Active Directory

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

In addition to updating the Teams steps, the `Find DN` step will need the Search Base field to be defined. Edit the workflow, open the `Find DN` step, and provide the appropriate Search Base for your domain. For example, if your domain is `acme.com` then the Search Base would be `DC=acme,DC=com`.

After configuring the Teams steps and the `Find DN` step, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!reset-password`. 

Commands should be in the following format:
`!reset-password <username>`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.4|4|
|Active Directory LDAP|4.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Update Active Directory LDAP to version 4.0.1
* 1.0.2 - Update to make Microsoft Teams plugin the latest version
* 1.0.1 - Updated trigger syntax and documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
