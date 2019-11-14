# Description

This workflow attempts to enrich all following IoCs (IPs, Domains, URLs, Hashes), if available. Can be associated with almost any alert.

# Key Features

* Indicator of compromise enrichment

# Requirements

* Admin access to Rapid7 InsightIDR

# Documentation

## Setup

* Configure the connections for the Active Directory plugin in Rapid7 InsightConnect
* Navigate to Rapid7 InsightIDR's automation page at #/automation/workflows
* Click Create Workflow from Template
* Select Containment Workflow in the Action Category
* Select Enable User in Active Directory for the Workflow or Template
* Name the workflow
* Select the connection you setup in the beginning
* Finish by creating the workflow

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|1.1.6|2|
|Whois|1.0.3|2|
|Dig|1.0.1|1|
|Unshorten.me|1.0.0|1|
|Team Cymru MHR|1.0.2|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

_There is no references information at this time_