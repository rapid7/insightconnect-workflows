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

Once the workflow has been imported, **edit the Settings step to specify the Microsoft Teams team name and channel name to suit your Teams environment!** Edit the input with the preset text of `Your Team` and `Your Channel` in each Teams step in the workflow.

After configuring the Settings step with your Microsoft Teams details, activate the workflow in order to trigger it.

## Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!insert-command-here`.

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
|Microsoft Teams|2.0.2|4|
|Type Converter|1.5.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
