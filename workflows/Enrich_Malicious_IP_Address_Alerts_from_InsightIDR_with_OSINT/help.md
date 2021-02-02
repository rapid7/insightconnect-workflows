# Description

Enrich a potentially malicious IP address with threat intelligence provided by Threat Crowd and information from Dig and Whois.

# Key Features

* Threat Crowd Lookup

# Requirements

* [InsightIDR](https://www.rapid7.com/products/insightidr/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

The workflow can be triggered automatically when an InsightIDR alert is raised or manually from the InsightIDR investigation.
The results are accessible in the investigation timeline.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Threat Crowd|3.0.0|1|
|DNS|2.0.0|1|
|WHOIS|3.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Threat Crowd](https://www.threatcrowd.org/)
* [InsightIDR](https://www.rapid7.com/products/insightidr/)
