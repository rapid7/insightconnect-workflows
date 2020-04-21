# Description

This workflow accepts a Microsoft Teams command containing a URL, looks up the URL with unshorten.me, and posts the full URL back.

Sample Teams Trigger Commands:

`!unshorten https://bit.ly/39HoYMu`

# Key Features

* Unshorten a shortened URL directly from Microsoft Teams

# Requirements

* Microsoft Teams Connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment (edit the input with the preset text of `change_me`).
The following are the 4 Microsoft Teams steps:
- _Unshorten URL Trigger_
- _Print No URL Found_
- _Print Failed to Unshorten URL_
- _Print Long URL_

To run the workflow, send the command `!unshorten <URL>` in your configured team and channel. The workflow will post after it has completed.

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

* 1.0.0 - Initial workflow

# Links

## References

* [Unshorten.me](https://unshorten.me)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
