# Description

This workflow creates solution-based issues in JIRA for each of the top 25 remediations in InsightVM. If there is already an issue open for a given remediation, the workflow updates the existing issue with a current list of impacted assets.

# Key Features

* Creates issues in JIRA for the top 25 solutions from InsightVM
* Updates issue for a solution with current impacted assets if issue already exists

# Requirements

* InsightVM Console URL and account credentials
* InsightConnect License
* JIRA URL and account credentials

# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. Once imported, you will initially be prompted to configure the connections for each of the plugins.

*Two steps need to be updated to reflect the local JIRA environment:*
* In the "Process Remediations" loop, change the "Search for Existing Issue" step's JQL input. "change_me" must be the name of the project in JIRA that will be searched for issues. 
* In the "Process Remediations" loop, change the "Create Issue" step's Project input. "change_me" must be the ID of the project in JIRA where the issue will be created.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Advanced Regex|1.0.1|1|
|Rapid7 InsightVM|4.0.0|1|
|Base64|1.1.4|3|
|Timers|2.0.4|1|
|Jira|4.0.2|3|
|Storage|1.0.1|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Updated workflow
* 1.0.2 - Updated documentation
* 1.0.1 - Fix filename
* 1.0.0 - Initial workflow

# Links

## References

* [JIRA] (https://www.atlassian.com/software/jira)
* [InsightVM](https://www.rapid7.com/products/insightvm/)
