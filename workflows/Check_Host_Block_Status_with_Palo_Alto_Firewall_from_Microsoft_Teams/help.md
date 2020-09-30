# Description

This workflow accepts a Microsoft Teams command containing an IP address or domain. This host will be checked against a pre-defined address group in a Palo Alto firewall to determine if the host is present or not. It is assumed that this address group will be used to store hosts for a block policy. A message with the results will be returned.

Multiple hosts can be specified in one command.

Sample Microsoft Teams Trigger Commands:

`!block-status 198.51.100.100`

`!block-status www.example.com`

`!block-status 198.51.100.100 198.51.100.101`

# Key Features

* The ability to see if a domain is currently blocked by the firewall

# Requirements

* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Username and password for a Palo Alto firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

In the Microsoft Teams steps change the Team and Channel from `change_me` to the channel you would like to monitor.

To run the workflow, enter a message such as `!block-status 198.51.100.100`. 

The workflow will also check on domain names and CIDR IP addresses:

`!block-status www.example.com`

`!block-status 198.51.0.0/24`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.2.1|6|
|Type Converter|1.6.0|1|
|Palo Alto Firewall|6.0.1|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.2.0 - Add automatic indicator extraction, allow for multiple hosts
* 1.1.1 - Update Microsoft Teams to the latest version
* 1.1.0 - Update Palo Alto Firewall to latest version
* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com/)
* [Palo Alto Networks](https://www.paloaltonetworks.com/)
