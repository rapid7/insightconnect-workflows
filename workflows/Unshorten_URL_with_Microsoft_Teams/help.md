# Description

This workflow accepts a Microsoft Teams command containing a URL, looks up the URL with unshorten.me, and posts the full URL back.

Sample Teams Trigger Commands:

`!unshorten-url https://bit.ly/39HoYMu`

# Key Features

* Unshorten a shortened URL directly from Microsoft Teams

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams) 

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.
The following are the 4 Microsoft Teams steps:
- _Unshorten URL Trigger_
- _Print No URL Found_
- _Print Failed to Unshorten URL_
- _Print Long URL_

After configuring the Teams steps, activate the workflow in order to trigger it.

# Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!unshorten-url` in your configured team and channel. 

For example:
`!unshorten-url https://bit.ly/39HoYMu`

The workflow will post after it has completed.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.2|4|
|ExtractIt|2.0.0|1|
|Unshorten.me|1.0.3|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Updated trigger syntax and documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Unshorten.me](https://unshorten.me)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
