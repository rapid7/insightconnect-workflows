# Description

Disabling a compromised account can limit the scope of an attack and buy valuable time to investigate and contain the threat. This workflow disables a domain user account with a command in Microsoft Teams.

Sample Microsoft Teams Trigger Commands:

`!disable-user-ad <exampleuser>`

`!enable-user-ad <exampleuser>`


# Key Features

* **Break the Kill Chain** - Credentials provide attackers with easy access to numerous targets. Disabling a compromised account or forcing a password reset can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, disabling a user account can limit your threat exposure and buy your team valuable time to investigate and contain a threat. 
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Active Directory connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **The `Find DN` step and each Microsoft Teams step will need to be updated to suit your Microsoft Teams and LDAP environments.** Edit the input with the preset text of `change_me` in each of these steps in the workflow.

After configuring the Teams steps, activate the workflow in order to trigger it.

# Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!disable-user-ad` or `!disable-user-ad`.

Commands should be in the following format:

`!disable-user-ad jdoe`

`!disable-user-ad jdoe`

The workflow will post the results in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|4.0.1|2|
|Microsoft Teams|3.0.1|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - New functionality - Enable AD User
* 1.0.3 - Update Active Directory LDAP to version 4.0.1
* 1.0.2 - Update to Microsoft Teams to make plugin the latest version
* 1.0.1 - Update trigger syntax, documentation, workflow name, and input parameters
* 1.0.0 - Initial workflow

# Links

## References

* [Active Directory LDAP](https://extensions.rapid7.com/extension/active_directory_ldap)
* [Microsoft Teams](https://teams.microsoft.com)
