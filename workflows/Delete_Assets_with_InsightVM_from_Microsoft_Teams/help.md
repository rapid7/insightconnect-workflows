# Description

Delete assets from InsightVM using a command from [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/).

Sample trigger commands:

`!delete-asset 12345`

`!delete-asset-confirm 12345`

# Key Features

* **Quick Management of Retired or Inactive Assets** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Update the first step with the team and channel name to suit your Microsoft Teams environment by editing the inputs with the preset text of `change_me` to match the team and channel to monitor.

## Usage

To run the workflow, send a message to the channel you are monitoring starting with the command `!delete-asset`.

For example:
`!delete-asset 12345`

You can also delete multiple assets at once. For example: 
`!delete-asset 12345 32145`

This will retrieve information about the assets you would like to delete. It will also present you a command to use if you would like to confirm deletion of the assets. 

To confirm deletion of an asset or assets: 
`!delete-asset-confirm 1234`

or 

`!delete-asset-confirm 1234 2345`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Type Converter|1.6.0|2|
|Rapid7 InsightVM|4.2.1|2|
|String Operations|1.3.1|1|
|Microsoft Teams|2.2.0|8|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Teams](https://docs.rapid7.com/insightconnect/microsoft-teams/)
* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
