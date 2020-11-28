# Description

Lookup the top 10 remediation steps from InsightVM for a given host from a Microsoft Teams message. The workflow returns the top 10 remediation steps for the specified entity to the designated Microsoft Teams channel, making it easy to identify top risk-reducing actions and share with your team!

Sample Microsoft Teams command:

`!top-remediations hostname123`

# Key Features

* Lookup the top risk-reducing remediation steps for any InsightVM asset
* Get a summarized list of remediation steps AND details for each step in a Microsoft Teams message
* Create a shared understanding across team members by viewing the vulnerabilities and risk reduced for each step in the same Microsoft Teams channel
* Expedite your patching procedures with real-time access to remediation data from InsightVM without leaving the comfort of your chat window

# Requirements

* InsightConnect License
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **edit the Trigger step - with Microsoft Teams team name and channel name to suit your Teams environment!**

After configuring the Trigger step with your Microsoft Teams details, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!top-remediations`.

For example:

* `!top-remediations hostname123`

The workflow will reply to the request message with the top 10 remediation steps for the specified entity to the channel where the command was triggered.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.8.1|2|
|Microsoft Teams|3.1.0|5|
|HTML|1.2.2|1|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Updated screenshots, documentation, and plugins to the latest version
* 1.0.2 - Removed unnecessary type conversion step from workflow
* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
