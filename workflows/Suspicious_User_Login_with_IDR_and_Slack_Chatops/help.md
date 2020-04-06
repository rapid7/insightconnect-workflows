# Description

Suspicious User Login with InsightIDR and Slack automates the process of validating IPs against other office locations tracked in a global artifact and if no match is found, escalates the alert via Slack chatbot to the security team. 

# Key Features

* Parses IP addresses and looks up Geolocation with Whois
* Every location is compared to the Office Location Global Artifact
* If there is not a match, the InsightConnect workflow will then automatically create a ticket in Jira and escalate alert details to security via Slack Chatbot for a user response.
* Based if the responder confirms that the user is traveling, the ticket will be transitioned to a closed state.
* If the alert is truly suspicious, the workflow will query for the user in Active Directory and disabled.

# Requirements

* InsightConnect Orchestrator Deployed
* Slack Chatbot
* Active Directory Connection
* Jira Connection

# Documentation

## Setup

Once the workflow has been imported and the Slack Chatbot selected for your Slack Workspace, edit the workflow and setup your Active Directory connection in the Query and Disable user steps. Also, setup up your Jira connection and confirm where applicable.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|3.2.6|4|
|WHOIS|1.0.5|1|
|Jira|3.2.1|6|
|Datetime|2.0.4|2|

## Troubleshooting

_There is no troubleshooting information at this time._

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
* [InsightIDR](https://extensions.rapid7.com/extension/rapid7_insightidr)
* [Active Directory LDAP](https://extensions.rapid7.com/extension/active_directory_ldap)
* [Datetime](https://extensions.rapid7.com/extension/datetime)
* [Jira](https://extensions.rapid7.com/extension/jira)
