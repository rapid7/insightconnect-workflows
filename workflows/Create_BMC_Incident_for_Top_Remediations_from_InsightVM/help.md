# Description

This workflow will get the top remediations from InsightVM, and create a BMC Remedy ITSM Incident for each remediation. The Incident will have details on the affected endpoints as well as the fix and risk score.

# Key Features

* Get the top remediations from InsightVM
* Create a BMC remedy ITSM Incident for each of the top remediations

# Requirements

* An InsightVM instance that has run at least one scan. 
* BMC Remedy ITSM 9.1.x server.

# Documentation

## Setup

* Download the workflow or clone the repository: `git clone https://github.com/rapid7/insightconnect-workflows.git`.
* Login to InsightConnect, and “Import” the .icon file into the workflow builder
* Configure the connections for both InsightVM and BMC Remedy ITSM.
* The Timers trigger step is set to run this workflow once a week on Sunday at 10AM. Change this to your desired time interval
* The InsightVM Top Remediations action is set to pull the top ten remediations. This can be changed to a larger number if desired.
* Configure BMC Remedy ITSM plugin action inputs as needed per your organization
* Activate your workflow.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Timers|2.0.2|1|
|Datetime|2.0.3|1|
|Rapid7 InsightVM|3.5.0|1|
|Python 3|2.0.0|1|
|BMC Remedy ITSM|1.7.0|1|

## Troubleshooting

_There is no troubleshooting information at this time._

# Links

## References
