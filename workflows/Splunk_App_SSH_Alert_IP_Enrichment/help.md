# Description

This workflow receives an event sent by the Rapid7 InsightConnect App for Splunk and performs enrichment on it.

# Key Features

* Enrich alerts triggered from Splunk

# Requirements

API and account credentials for

* AbuseIPDB

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|AbuseIPDB|5.0.0|1|
|ExtractIt|1.1.6|1|
|IPStack|1.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## Source Code

* https://github.com/rapid7/insightconnect-workflows/tree/master/workflows/Splunk_App_SSH_Alert_IP_Enrichment

## References

* https://github.com/rapid7/insightconnect-workflows