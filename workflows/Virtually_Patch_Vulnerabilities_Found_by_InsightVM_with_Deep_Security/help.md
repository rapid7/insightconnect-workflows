# Description

Automatically protect your assets against exploitation of vulnerabilities found by InsightVM with Deep Security Virtual Patching (IPS).

# Key Features

* Search IPS rules for every found vulnerability
* Find matching assets in Deep Security
* Assign the IPS rules to the Deep Security assets
* Set exceptions for protected vulnerabilities in InsightVM

# Requirements

* Rapid7 InsightConnect
* Rapid7 InsightVM
* Trend Micro Deep Security (Intrusion Prevention Module)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.


## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.8.1|5|
|Trend Micro Deep Security|2.2.1|4|
|Advanced Regex|1.0.3|1|
|Python 3 Script|2.0.2|5|
|Type Converter|1.6.1|1|
|Base64|1.1.6|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Improve the job run time
* 1.0.3 - Revert and rename workflow file to fix import failure
* 1.0.2 - Rename workflow file to fix import failure
* 1.0.1 - Fix issue in name which caused workflow to fail import from Extension Library
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm/)
* [Trend Micro Deep Security](https://www.trendmicro.com/en_us/business/products/hybrid-cloud/deep-security.html)
* [Rapid7 InsightConnect](https://www.rapid7.com/products/insightconnect/)
* [Rapid7 Vulnerability Database](https://www.rapid7.com/db)
* [Rapid7 InsightVM - InsightConnect Plugin](https://extensions.rapid7.com/extension/rapid7_insightvm)
* [Trend Micro Deep Security - InsightConnect Plugin](https://extensions.rapid7.com/extension/trendmicro_deepsecurity)
