# Description

Reset a user's password straight from Microsoft Teams. Respond quickly, albeit to contain a potential threat or to reset another user's locked out account.

Sample Microsoft Teams Trigger Commands:

`!reset_password user@example.com`

# Key Features

* **Break the Kill Chain** - Credentials provide attackers with easy access to numerous targets. Disabling a compromised account or forcing a password reset can quickly and effectively interrupt an attacker’s kill chain.
* **Minimize Disruption to the User** - Forcing a user to reset their password is a small inconvenience compared to re-imaging their entire system. Acting fast can save valuable time and teach a valuable lesson without a noticeable impact to your business.
* **Make Persistence Inconsistent** - Attackers love using credentials for persistent access to networks or cloud applications. Changing a compromised password is the easiest way to cut off an attacker’s access to your systems and data.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Azure AD connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams steps and the `Find DN` step, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!reset-password`. 

Commands should be in the following format:
`!reset-password john.doe@acme.inc`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|1.3.0|2|
|ExtractIt|2.0.0|1|
|Azure AD Admin|1.4.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.4 - Update to newest plugin versions | Update to message formatting
* 1.0.3 - Updated trigger syntax and documentation
* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Azure AD](https://azure.microsoft.com/en-us/services/active-directory/)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
