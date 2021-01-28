# Description

This workflow provides fast, convenient access to information about a given host from InsightVM by fetching asset details from InsightVM and posting them in a Microsoft Teams message. Host info includes hostname, IP address, MAC address, operating system, running services, last assessment date, and vulnerability stats. Lookup can be performed by either hostname or IP address.

# Key Features

* Fetch host information from InsightVM quickly in Microsoft Teams
* Determine when the system was last assessed for vulnerabilities
* Positively identify a system by looking up its IP or hostname
* Get an overview of vulnerabilities by criticality
* View running services

# Requirements

* InsightVM Console URL and account credentials
* InsightConnect License
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the team name and channel name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.

## Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!lookup-host`.

For example:

* `!lookup-host hostname123`
* `!lookup-host 10.1.2.34`

The workflow will post matching host information to the specified Microsoft Teams channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.0|1|
|HTML|1.2.1|1|
|Microsoft Teams|3.1.0|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Replace the Settings step with automatic team and channel name extraction in all Microsoft Teams steps except the first one | Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.2 - Fix incorrect variable used in Clean Teams Message
* 1.0.1 - Update to make Microsoft Teams plugin the latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
