# Description

Lookup URLs using Threat Crowd's database to determine malicious nature. This workflow uses the InsightIDR UBA trigger to allow users to run this workflow from an Investigation in InsightIDR.

# Key Features

* Query for reputation data to a URL
* Get URL reputation data in InsightIDR Investigation
* Easily identify known malicious URLs

# Requirements

* InsightIDR License
* InsightConnect License

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

### Usage

To run the workflow, open an Investigation in InsightIDR that includes a potentially malicious URL. Using the **Take Action** menu, select **Custom InsightConnect Workflow**, then select the `Enrich Malicious URL Alerts from InsightIDR with Threat Crowd` workflow. Select the URL from the investigation and Take Action.

You may also set this workflow to run automatically by attaching it to one or more alert types in the Alert Triggers in the Automation tab of InsightIDR.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Threat Crowd|3.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Threat Crowd](https://www.threatcrowd.org)
