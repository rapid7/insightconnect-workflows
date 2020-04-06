# Description

This workflow automates the process of parsing all IP addresses associated with the InsightIDR alert, and enriches them with geo locations and threat intelligence. From the findings, the workflow will automatically post a Slack response prompt to the security team as a point of escalation. Based upon the incident responders decision, the address will be blocked by updating a Palo Alto Pan-OS policy.

# Key Features

* InsightIDR alert with IPs
* Parse IPs with Pattern Match step
* Confirm geo-location with IPStack and Whois
* Automated Decision - is this address in the United States or Outside? 
* Automated Decision - Malicious reputation found?
* Generate Findings Report
* Post Findings Report to Slack Channel with user response prompt via chatbot
* Path - Create Ticket
* Path - Block IP
* Path - Do Both
* User Response via chatbot - Block Outbound / Inbound / or Traffic from both
* Block traffic from both outbound and inbound traffic by updating Palo Alto PAN-OS
* Confirm Success Block with Slack

# Requirements

* InsightConnect Orchestrator Deployed
* Slack Chatbot
* VirusTotal Connection
* Jira Connection
* IP Stack Connection

# Documentation

## Setup

Once the workflow has been imported and the Slack chatbot selected for your workstation, edit the workflow and configure your Jira connection. Also, configure your VirusTotal & AbuseIPDB connection and confirm where applicable.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|IPStack|1.0.1|1|
|WHOIS|1.0.7|1|
|Type Converter|1.5.1|2|
|VirusTotal|6.0.0|1|
|NASA|1.0.2|1|
|Palo Alto PAN-OS|1.5.6|2|

## Troubleshooting

_There is no troubleshooting information at this time._

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [IP Stack](https://extensions.rapid7.com/extension/ipstack)
* [VirusTotal](https://extensions.rapid7.com/extension/virustotal)
* [WhoIs](https://extensions.rapid7.com/extension/whois)
* [Nasa](https://extensions.rapid7.com/extension/nasa)
* [Palo Alto PAN-OS](https://extensions.rapid7.com/extension/palo_alto_pan_os)
