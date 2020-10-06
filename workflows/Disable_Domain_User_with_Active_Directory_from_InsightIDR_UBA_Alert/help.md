# Description

Disabling a compromised user account can limit the scope of an attack and buy valuable time to investigate and contain the threat. This workflow triggers on an InsightIDR UBA alert to disable a domain user with Active Directory.

This workflow can be used with the following types of UBA alerts:

`Harvested Credentials`

`Multi-Country Authentication Alerts`

`Ingress From Community Threat`

`Account Leaked`

`Brute Force - Domain Account`

# Key Features

* **Break the Kill Chain** - Disabling a user account can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, disabling a user account can limit your threat exposure and buy your team valuable time to investigate and contain a threat. 

# Requirements

* InsightIDR
* Active Directory

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **it is recommended that you add the appropriate email addresses to the `Block Domain Account Decision` step so that the appropriate users are alerted that action needs to be taken**

Activate the workflow in order to trigger it.

Log into InsightIDR and go to the Automation tab, then Alert Triggers. Click on Create Alert Trigger.
Select Custom InsightConnect Workflows, then `Disable Domain User with Active Directory from InsightIDR UBA Alert`,
then choose the type of alert you would like to trigger on. For example: Brute Force - Domain Account.
This will set up the workflow to run any time the selected alert is triggered.

# Usage

The workflow will run automatically when the selected InsightIDR UBA alert is created.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightIDR|1.2.0|1|
|Active Directory LDAP|3.2.9|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.
* 1.0.0 - Initial workflow

# Links

## References

* [InsightIDR](https://www.rapid7.com/products/insightidr/)
