# Description

Disabling a compromised account can limit the scope of an attack and buy valuable time to investigate and contain the threat. This workflow disables an Azure AD account with a simple Slack command.

Sample Slack Trigger Commands:

`@Slackbot disable-user user@example.com`

# Key Features

* **Break the Kill Chain** - Credentials provide attackers with easy access to numerous targets. Disabling a compromised account or forcing a password reset can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, disabling a user account can limit your threat exposure and buy your team valuable time to investigate and contain a threat. Disabling the user may not remediate the root cause, but it can mitigate the immediate risk while you work on fixing underlying issues.
* **Minimize Disruption to the User** - Forcing a user to reset their password is a small inconvenience compared to re-imaging their entire system. Acting fast can save valuable time and teach a valuable lesson without a noticeable impact to your business.

# Requirements

* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Azure AD connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `disable-user <user_email>`. The workflow will reply when it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|Azure AD Admin|1.4.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Updated trigger syntax and documentation
* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Azure AD](https://azure.microsoft.com/en-us/services/active-directory/)
* [Slack](https://slack.com)
