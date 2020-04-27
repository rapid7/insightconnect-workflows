# Description

This workflow responds to any user event from InsightIDR and determines if the event occurred during or after office hours. Depending on the alert timestamp, the workflow will either automatically disable the user or post a human decision in Slack. Throughout the whole workflow, InsightConnect is creating and tracking the life cycle of the incident through Jira. 

# Key Features

* Security team prompted to disable user if security event occurs during office hours
* Automatically disable user if user event occurs outside office hours
* Track event lifecycle in Jira
* Respond with disable action directly from Slack

# Requirements

* InsightConnect Orchestrator Deployed
* Slack Chatbot
* Active Directory Connection
* Jira Connection

# Documentation

## Setup

Once the workflow has been imported and the Slack chatbot selected for your workstation, edit the workflow and configure your Active Directory connection in the Query and Disable user steps. Also, configure up your Jira connection and confirm where applicable. 

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|3.2.0|6|
|WhoIs|1.0.7|1|
|Jira|3.0.5|9|
|Datetime|2.0.5|4|
|Python 2 Script|2.0.3|1|

# Version History

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [InsightIDR](https://extensions.rapid7.com/extension/rapid7_insightidr)
* [Active Directory LDAP](https://extensions.rapid7.com/extension/active_directory_ldap)
* [Datetime](https://extensions.rapid7.com/extension/datetime)
* [Jira](https://extensions.rapid7.com/extension/jira)
