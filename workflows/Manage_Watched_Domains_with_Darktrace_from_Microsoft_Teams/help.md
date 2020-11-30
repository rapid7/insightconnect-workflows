# Description

This workflow adds or removes hosts (domains and IP addresses) in the Darktrace watched domains list via Microsoft Teams command and reports information back to Microsoft Teams.

Multiple hosts can be specified in one command.

Sample Microsoft Teams Trigger Commands:

`!add-domain 1.1.1.1 google.com`

`!remove-domain rapid7.com`

# Key Features

* Add or remove hosts to/from watched domains list

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Darktrace

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the channel name and a team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in each Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Type Converter|1.6.0|1|
|Darktrace|2.0.1|2|
|Microsoft Teams|3.1.0|6|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Darktrace plugin
* 1.0.0 - Initial workflow

# Links

## References

* [Darktrace](https://www.darktrace.com/)
* [Darktrace Plugin](https://extensions.rapid7.com/extension/darktrace)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
