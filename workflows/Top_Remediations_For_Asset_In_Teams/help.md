# Description

Lookup the top 10 remediation steps from InsightVM for a given host from a Microsoft Teams message. The workflow returns the top 10 remediation steps for the specified entity to the designated Microsoft Teams channel, making it easy to identify top risk-reducing actions and share with your team!

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

Once the workflow has been imported, **edit the Settings step to specify the Microsoft Teams team name and channel name to suit your Teams environment!** Edit the input with the preset text of `Your Team` and `Your Channel` in each Teams step in the workflow.

After configuring the Settings step with your Microsoft Teams details, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!insert-command-here`.

For example:
* `!top-remediations hostname123`

The workflow will post the top 10 remediation steps for the specified entity to the channel where the command was triggered.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.0.|5|
|Microsoft Teams|2.0.3|5|
|HTML|1.2.1|1|
|Type Converter|1.5.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow


# Links

## References

* [Slack](https://slack.com)
