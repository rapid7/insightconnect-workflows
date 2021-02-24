# Description

The workflow automatically synchronizes URL blacklists across Palo Alto Firewall and Zscaler by adding or removing address objects from an address object group in your Palo Alto Firewall and blacklisting or unblacklisting URLs in Zscaler to keep them in sync bi-directionally on an hourly schedule.

This workflow ensures that hosts blocked in the firewall are also blocked at the web proxy, and that hosts blocked in the web proxy are also blocked in the firewall creating a more consistent defensive perimeter across the organization.

# Key Features

* **Sync URL blacklists** - Use InsightConnect to synchronize blacklisted URLs across Palo Alto Firewall and Zscaler easily.

# Requirements

* Palo Alto Firewall username and password
* Zscaler base URL, API key, username and password

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow. 

There is one parameter you will need to configure in order to complete the setup of your workflow:

* `Group Name`: The Palo Alto Firewall address object group to monitor. This is the group from which address objects will be synced with Zscaler.

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameter, activate the workflow in order to trigger it.

### Usage

This workflow will trigger automatically on an hourly schedule to sync blacklisted URLs across Palo Alto Firewall and Zscaler.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Palo Alto Firewall|6.1.0|7|
|Storage|1.0.1|6|
|Timers|2.0.5|1|
|Type Converter|1.8.0|10|
|Zscaler|1.3.0|5|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Palo Alto Firewall](https://www.paloaltonetworks.com/)
* [Zscaler](https://www.zscaler.com/)
