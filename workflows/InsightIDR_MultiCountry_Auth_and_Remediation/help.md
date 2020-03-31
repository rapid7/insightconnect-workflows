# Description

This workflow is designed to respond to InsightIDR's Multi Country Authentication alert by confirming if the user authenticated from more than two locations. Due to an influx of VPN logins, the amount of false positive alerts is increasing. This workflow will automatically reduce false positives by closing alerts with two or less locations or by automatically responding to alerts with more than two locations. If a user account is shown to be associated with two or more locations InsightConnect will respond by disabling the user account.

# Key Features

* Parses authentication count using Pattern Match & Python
* If locations are two or less, the InsightIDR investigation is automatically closed.
* If there are more than 2 locations Active Directory is automatically querying for the associated user. If the user is found, they are disabled.

# Requirements

* InsightConnect Orchestrator deployed
* Active Directory connection
* [Insight Cloud Platform API key](https://insight.rapid7.com/platform#/apiKeyManagement)

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and either configure or select an existing Active Directory connection in the Query and Disable User steps. Your InsightIDR connection will also need to be configured using your Insight Cloud Platform API key.

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
