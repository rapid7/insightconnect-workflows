# Description

This workflow accepts a Microsoft Teams command containing an IP address. This IP address will be checked against a pre-defined address group in a Palo Alto firewall to determine if the IP address is present or not. It is assumed that this address group will be used to store IP addresses for a block policy. A message with the results will be returned.

Sample Microsoft Teams Trigger Commands:

`!block-status 198.51.100.100`

# Key Features

* The ablity to see if an IP is curently blocked by the firewall


# Requirements

* [Microsoft Teams Connection](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* An admin API key to a Fortigate firewall

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

In the Microsoft Teams steps change the Team and Channel from `change_me` to the channel you would like to monitor.
In the _Check if IP in Group_ step change the Group input from `change_me` to an appropriate address group.

To run the workflow, enter a message such as `!block-status 198.51.100.100`. 

The workflow will also check on domain names and CIDR IP addresses: 
`!block-status www.example.com`
`!block-status 198.51.0.0/24`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Fortinet FortiGate|1.1.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://teams.microsoft.com/)
* [Palo Alto Networks](https://www.paloaltonetworks.com/)
