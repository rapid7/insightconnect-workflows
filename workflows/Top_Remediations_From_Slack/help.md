# Description

Lookup the top 10 remediation steps from InsightVM for a given host, asset group, site, or tag from a Slack message. The workflow returns the top 10 remediation steps for the specified entity in a Slack thread, making it easy to identify top risk-reducing actions and share with your team in Slack!

Sample Slack command:

`top-remediations asset hostname123`

# Key Features

* Lookup the top risk-reducing remediation steps for any InsightVM asset, asset group, site, or tag
* Get a summarized list of remediation steps AND details for each step in a Slack message
* Create a shared understanding across team members by viewing the vulnerabilities and risk reduced for each step in the same Slack channel
* Expedite your patching procedures with real-time access to remediation data from InsightVM without leaving the comfort of your chat window

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a channel starting with the command `top-remediations`, followed by the type (`asset`, `group`, `site`, or `tag`) and the name of the target.

For example, in a direct message to your Chatbot:
* top-remediations asset hostname123
* top-remediations group Windows Servers
* top-remediations site DMZ
* top-remediations tag John

Or in a channel including your Chatbot:
* @Rapid7 InsightConnect top-remediations asset win8s1
* @Rapid7 InsightConnect top-remediations group SQL
* @Rapid7 InsightConnect top-remediations site Headquarters
* @Rapid7 InsightConnect top-remediations tag Very High

The workflow will post the top 10 remediation steps for the specified entity to the Slack channel where the command was triggered.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.9.0|5|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.3 - Removed unecessary steps, updated plugins
* 1.1.2 - Updated documentation, and plugins to the latest version
* 1.1.1 - Updated spec files
* 1.1.0 - Workflow updated to support different types (asset, group, site, or tag). Updated documentation.
* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
