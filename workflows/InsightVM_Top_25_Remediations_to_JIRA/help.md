# Description

This workflow checks assets scanned in the last 30 days. For each of the 25 assets with the highest vulnerability score, it creates one solution-based issue in JIRA per vulnerability found. These tickets list the asset(s) affected. If there is already an issue open for a given remediation, the workflow updates the existing issue with a current list of impacted assets.

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

This workflow runs daily at 12:00 UTC. Adjust the time as necessary to suit your organization's needs by changing input in "Time in UTC." We recommend running this workflow during off-hours, as it is data and CPU intensive.

Note: Editing any of the following can significantly increase or decrease the time this workflow takes to run.

By default, this workflow gets assets scanned in the last 30 days. To alter the limit from 30 days to a different number, edit the `Get assets scanned in the last 30 days` step. Find the input variable {"match":"all","filters":[{"field":"last-scan-date","operator":"is-within-the-last","value":30}]}. Change the number 30 within this variable to fit the needs of your organization.

To change the limit for number of assets scanned, go to the `Top 25 Remediations` step. Edit the `Asset Limit` field. To change the limit number of vulnerabilities found, you can edit the `Vulnerability limit` Field

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Advanced Regex|1.0.3|1|
|Rapid7 InsightVM|4.8.1|2|
|Base64|1.1.6|3|
|Timers|2.0.4|1|
|Jira|6.0.3|3|
|Storage|1.0.1|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.0 - Add a filter to only list assets from the last 30 days
* 1.0.4 - Update all plugins used by the workflow.
* 1.0.3 - Updated workflow to better identify and update existing tickets
* 1.0.2 - Updated documentation
* 1.0.1 - Fix filename
* 1.0.0 - Initial workflow

# Links

## References

* [JIRA] (https://www.atlassian.com/software/jira)
* [InsightVM](https://www.rapid7.com/products/insightvm/)
