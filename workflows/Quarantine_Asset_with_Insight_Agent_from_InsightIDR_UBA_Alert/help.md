# Description

Quarantining a compromised asset can limit the scope of an attack and buy valuable time to investigate and contain the threat. This workflow triggers on an InsightIDR UBA alert to quarantine an asset with the Insight Agent.

This workflow can be used with the following types of UBA alerts:

`Brute Force - Local Account`

`Flagged Hash on Asset`

`Flagged Process on Asset`

# Key Features

* **Break the Kill Chain** - Quarantining an asset can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, quarantining an asset can limit your threat exposure and buy your team valuable time to investigate and contain a threat. 

# Requirements

* InsightIDR
* Insight Agent on the asset to be quarantined

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **it is recommended that you add the appropriate email addresses to the `Block Domain Account Decision` step so that the appropriate users are alerted that action needs to be taken**

Activate the workflow in order to trigger it.

Log into InsightIDR and go to the Automation tab, then Alert Triggers. Click on Create Alert Trigger.
Select Custom InsightConnect Workflows, then `Quarantine asset with Insight Agent from InsightIDR UBA Alert`,
then chose they type of alert you would like to trigger on. For example: Flagged Hash on Asset.
This will set up the workflow to run any time the selected alert is triggered.

# Usage

The workflow will run automatically when the selected InsightIDR UBA alert is created

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightIDR|1.2.0|2|
|Rapid7 Insight Agent|1.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [InsightIDR](https://www.rapid7.com/products/insightidr/)
