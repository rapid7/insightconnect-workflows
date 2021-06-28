# Description

This workflow enriches an IDR alert by performing a lookup on all domains, hashes, URLs and IPs in the investigation with Recorded Future.

# Key Features

* Perform a domain, hash, URL and IP lookup automatically from any IDR alert

# Requirements

* InsightConnect License
* Recorded Future API Key and Account Credentials

# Documentation

## Setup

* Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.
* Configure the connections for the Cb Response plugin
* Activate your workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select Enrich Indicators with Recorded Future from IDR Alert
* While Selecting Alerts, check any alerts you would like to automatically enrich

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Recorded Future|5.0.1|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Update Recorded Future plugin version
* 1.0.0 - Initial workflow

# Links

## References

* [Recorded Future API Documentation](https://support.recordedfuture.com/hc/en-us/categories/115000803507-Raw-API)
