# Description

Disabling a compromised account can limit the scope of an attack and buy valuable time to investigate and contain the threat. This workflow disables or enables an Azure AD account straight from Microsoft Teams.

Sample Trigger Commands:

`!disable-user-azure user@example.com`

`!enable-user-azure user@example.com`

# Key Features

* **Break the Kill Chain** - Credentials provide attackers with easy access to numerous targets. Disabling a compromised account or forcing a password reset can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, disabling a user account can limit your threat exposure and buy your team valuable time to investigate and contain a threat. 
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Azure AD connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in first Teams step in the workflow.

After configuring the Teams step, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!disable-user-azure` or `!enable-user-azure`. 

For example:
* `!disable-user-azure user@example.com`
* `!enable-user-azure user@example.com`

The workflow will acknowledge the request and reply when it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|3.1.0|6|
|Azure AD Admin|2.2.3|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Add Enable User functionality | Use the automatic extraction functionality instead of ExtractIt step to extract an email address | Remove HTML step | Improve workflow messaging | Improve documentation | Update screenshots | Update Azure AD Admin to version 2.2.3 | Update Microsoft Teams to version 3.1.0
* 1.0.4 - Update to make Microsoft Teams plugin the latest version
* 1.0.3 - Updated trigger syntax and documentation
* 1.0.2 - Updated trigger syntax and documentation
* 1.0.1 - Updated documentation | Updated images
* 1.0.0 - Initial workflow

# Links

## References

* [Azure AD](https://azure.microsoft.com/en-us/services/active-directory/)
* [Microsoft Teams](https://products.office.com/en-us/microsoft-teams/group-chat-software)
