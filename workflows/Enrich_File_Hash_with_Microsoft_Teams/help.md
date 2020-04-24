# Description

Look up and enrich file hashes in VirusTotal directly from Microsoft Teams, providing a fast, convenient way to check potential indicators of compromise. 

Sample Microsoft Teams Trigger Commands:

`!enrich-hash 9de5069c5afe602b2ea0a04b66beb2c0`

`!enrich-hash 02699626f388ed830012e5b787640e71c56d42d8`

`!enrich-hash 275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f`


# Key Features

* **Easily Enrich Indicators** - Investigate suspicious file hashes without leaving the comfort of your Microsoft Teams window.
* **Respond Rapidly** - Give your teams a head start on shutting down phishing attacks by automating routine tasks during investigations.

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams) connection

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the team name and channel name updated to suit your Teams environment!** Edit the input with the preset text of `change_me` in each Teams step in the workflow.

After configuring the Teams steps, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in the channel specified in the Microsoft Teams workflow steps.*

To run the workflow, send a message to the specified Microsoft Teams channel starting with the command `!enrich-hash <hash>`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.2|4|
|HTML|1.2.1|1|
|VirusTotal|6.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Updated trigger syntax and documentation
* 1.0.0 - Initial workflow

# Links

## References

* [VirusTotal](https://www.virustotal.com/gui/home/upload)
* [Microsoft Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)
