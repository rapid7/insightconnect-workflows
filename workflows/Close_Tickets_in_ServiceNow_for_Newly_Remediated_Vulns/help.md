# Description

*This workflow works in conjunction with the [Open Tickets in ServiceNow for Newly Discovered Vulnerabilities](https://extensions.rapid7.com/extension/Open_Tickets_in_ServiceNow_for_Newly_Discovered_Vulns) workflow! Use these two workflows together to automatically open and close incident tickets in ServiceNow when vulnerabilities are discovered and remediated.*

This workflow automatically finds and closes tickets previously opened by the [Open Tickets in ServiceNow for Newly Discovered Vulnerabilities](https://extensions.rapid7.com/extension/Open_Tickets_in_ServiceNow_for_Newly_Discovered_Vulns) workflow. If a ticket is found, then it is marked as `Resolved` with a close note indicating the incident was resolved by the Rapid7 InsightConnect. Make sure you import and activate both workflows for closed-loop vulnerability ticketing!

These workflows help IT and Security teams open, track, and close remediation tasks as vulnerabilities are discovered by InsightVM and subsequently remediated. Both workflows use InsightConnect's [VM Events trigger](https://docs.rapid7.com/insightconnect/set-up-an-insightvm-events-trigger). This workflow uses the [vulnerabilities remediated](https://docs.rapid7.com/insightconnect/set-up-an-insightvm-events-trigger#vulnerabilities-remediated) event trigger.



# Key Features

* Automatically close tickets in ServiceNow for newly remediated vulnerabilities
* Raise the visibility of completed remediation tasks
* Synchronize vulnerability data with ServiceNow

# Requirements

* ServiceNow
* Insight Platform User API Key
* InsightVM
* InsightConnect

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary. Don't forget to include a time savings estimate!

Once the workflow has been imported, open the workflow and view the InsightVM Events trigger step. Save the trigger configuration step and proceed through the Instructions on subscribing to the InsightVM Vulnerabilities Found Webhook Event. This will require an [Insight Platform User API Key](https://docs.rapid7.com/insight/managing-platform-api-keys#generating-a-user-key). Insert your User API Key, copy the API request, run it from a command prompt, and look for a JSON response including an ID. If you receive a JSON response, then your webhook event subscription is active! Close your command prompt and return to the workflow in InsightConnect.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ServiceNow|5.0.1|3|
|Type Converter|1.7.0|1|


## Troubleshooting

Experiencing delays? InsightVM Events are delivered to InsightConnect from InsightVM as soon as the Insight platform is notified of a change by the on-premises InsightVM Security Console. This can take anywhere from 5 minutes to several hours. Please be patient!

# Version History

* 1.0.1 - Updated setup documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability & Exploit Database](https://rapid7.com/db)
* [InsightVM Events Trigger](https://docs.rapid7.com/insightconnect/set-up-an-insightvm-events-trigger)
* [ServiceNow](https://www.servicenow.com/)
