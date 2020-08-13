# Description

Quarantining a compromised asset can limit the scope of an attack and buy valuable time to investigate and contain the threat. This workflow quarantines an asset that has an Insight agent on it from an InsightIDR Flagged Hash UBA alert.

# Key Features

* **Break the Kill Chain** - Quarantining an asset can quickly and effectively interrupt an attacker’s kill chain.
* **Buy Time to Investigate and Remediate** - In a pinch, quarantining an asset can limit your threat exposure and buy your team valuable time to investigate and contain a threat. 

# Requirements

* InsightIDR
* Insight Agent on the asset to be quarantined

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **It is recommended that you add you add the appropriate emails to the `Block Domain Account Decision` step so that the appropriate people are alerted that action needs to be taken**

Activate the workflow in order to trigger it.

Log into IDR and go to the automation tab. From there go to Alert Triggers. Click on Create Alert Trigger.
Select Custom InsightConnect Workflows, then Block Flagged Hash with Insight Agent from InsightIDR, then Flagged Hash on Asset
This will set up the workflow to run any time a Flagged Hash on Asset is triggered

# Usage

The workflow will run automatically when a InsightIDR Flagged Hash UBA alert is created

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightIDR|1.1.1|3|
|Rapid7 Insight Agent|1.0.0|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [InsightIDR](https://www.rapid7.com/products/insightidr/)
