# Description

This workflow will get the top remediations from InsightVM, and create a BMC Remedy ITSM Incident for each remediation. The Incident will have details on the affected endpoints as well as the fix and risk score.

# Key Features

* Get the top remediations from InsightVM
* Create a BMC remedy ITSM Incident for each of the top remediations

# Requirements

* An InsightVM instance that has run at least one scan. 
* A BMC Remedy ITSM 9.1.x server

# Documentation

## Setup

* Download the workflow or clone the repository `git clone https://github.com/rapid7/insightconnet-workflows.git`
* Login to InsightConnect, and “Import” the .icon file into the workflow builder
* Configure the connections for the InsightVM and BMC remedy ITSM
* The Timers trigger step is set to run this workflow once a week on Sunday at 10AM change this if you want
* The InsightVM top remediations action is set to pull the top 10 remediations. This can be changes to larger numbers if you want
* The BMC remedy ITSM action requires inputs that are unique to your organisation.
* Review and update the BMC remedy ITSM action inputs other than `Other Inputs` as needed
* Activate your workflow


## Technical Details

Plugins leveraged by workflow:

* Timers 2.0.2
* Datetime 2.0.3
* Rapid7 InsightVM 3.5.0
* Python 3 2.0.0
* BMC Remedy ITSM 1.7.0

## Troubleshooting

# Links

## Source Code

https://github.com/rapid7/insightconnect-workflows

## References
