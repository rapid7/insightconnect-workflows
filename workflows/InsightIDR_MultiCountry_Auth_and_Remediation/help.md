# Description

This workflow is designed to respond to InsightIDR's Multi Country Authentication alert by confirming if the user authenticated from more than 2 locations. With a flux of VPN loggings,a way to automatically reduce false positives would be to close alerts that have 2 or less locations or automatically respond to alerts with more than 2 locations. I this workflow, InsightConnect is responding by disabling the user account associated with more than 2 locations. 

# Key Features

* Parses authentication count using Pattern Match & Python
* If locations are two or less, the InsightIDR investigation is automatically closed.
* If there are more than 2 locations Active Directory is automatically querying for the associated user. If the user is found, they are disabled.

# Requirements

* InsightConnect Orchestrator Deployed
* Active Directory Connection
* Insight Platform Organization Key

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Active Director connection in the Query and Disable user steps. Also setp up your InsightIDR connection with an Organization Key for the Insight Platform.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Python 3 Script|2.0.0|1|
|Rapid7 InsightIDR|1.1.0|1|
|Active Directory LDAP|3.2.6|2|

## Troubleshooting

_This plugin does not contain any troubleshooting information._

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability Database](https://www.rapid7.com/db)
* [Slack](https://slack.com)
