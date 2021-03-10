# Description

Quarantine an endpoint in CylanceOPTICS from a Microsoft Teams command. This workflow supports endpoints in the form of IP address and/or MAC address.

More than one endpoint can be specified within a single command.

Sample Microsoft Teams Trigger Commands:

`!quarantine-endpoint 08:00:27:33:9F:CE`

`!quarantine-endpoint 10.0.2.15 08:00:27:33:9F:CE`

When you log into CylancePROTECT, choose "CylanceOPTICS" from the left side-bar menu. The quarantined endpoints can be found on the "Devices" tab. When the "Device Status" is set to "Locked Down", the endpoint is quarantined. 

**Note**: Cylance does not support undoing the lockdown from the API, as the network access is fully removed for the endpoint.


# Key Features

* Quarantine endpoints from Microsoft Teams

# Requirements

* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)
* CylancePROTECT account with permission to manage endpoints

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **the first Microsoft Teams step will need the channel and team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in the first Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.


## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|BlackBerry CylancePROTECT|1.4.0|1|
|Microsoft Teams|3.1.0|6|
|Type Converter|1.6.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Microsoft Teams to version 3.1.0 | Update documentation
* 1.0.0 - Initial workflow

# Links

## References

* [BlackBerry Cylance](https://www.cylance.com)
* [CylancePROTECT plugin](https://github.com/rapid7/insightconnect-plugins/tree/master/cylance_protect)
* [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/group-chat-software)
