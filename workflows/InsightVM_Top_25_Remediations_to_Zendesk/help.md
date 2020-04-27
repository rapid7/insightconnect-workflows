# Description

This workflow creates solution-based tickets in Zendesk for each of the top 25 remediations in InsightVM.  If there is already a ticket open for a given remediation, the workflow updates the existing ticket with a current list of impacted assets.

# Key Features

* Creates tickets in Zendesk for the top 25 solutions from InsightVM
* Updates tickets for a solution with current impacted assets if ticket already exists

# Requirements

API and account credentials for

* InsightVM
* Zendesk

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Advanced Regex|1.0.1|1|
|Rapid7 InsightVM|3.6.0|1|
|Base64|1.1.3|3|
|Timers|2.0.4|1|
|Zendesk|3.1.1|3|
|Storage|1.0.1|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Zendesk](https://www.zendesk.com)
* [InsightVM] (https://www.rapid7.com/products/insightvm/)
