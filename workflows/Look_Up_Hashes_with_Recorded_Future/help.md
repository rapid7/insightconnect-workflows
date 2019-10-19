# Description

This workflow enriches an IDR alert by performing a lookup on all hashes in the investigation with Recorded Future.

# Key Features

* Perform a has lookup automatically from any IDR alert

# Requirements

API and account credentials for Recorded Future

# Documentation

## Setup

* Download the workflow or clone the repository `git clone https://github.com/rapid7/insightconnet-workflows.git`
* Login to InsightConnect, and “Import” the .icon file into the workflow builder
* Configure the connections for the Cb Response plugin
* Activate your workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select Look Up Hashes with Recorded Future
* While Selecting Alerts, check any alerts you would like to automatically enrich

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Recorded Future|1.5.2|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows/tree/master/workflows/Look_Up_Hashes_with_Recorded_Future

## References

* [Recorded Future API Documentation](https://support.recordedfuture.com/hc/en-us/categories/115000803507-Raw-API)