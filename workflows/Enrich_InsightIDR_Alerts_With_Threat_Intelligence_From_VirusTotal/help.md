# Description

This workflow is meant to introduce InsightIDR users to workflows using the Orchestrator, Connections, Loop Steps, and Join Steps. It uses the IDR UBA Alert trigger and automatically identifies the type of indicator of compromise (IP address, URL, domain, or hash) that is present in the alert, looks up the indicator in VirusTotal, and produces an Artifact card that provides a summary of the findings, including a link back to the results in VirusTotal.

This workflow is easy to test out for InsightIDR users who are new to InsightConnect and automation workflows.

# Key Features

* Learn how to use more complex workflows for incident investigation and response
* Learn how to set up a Connection on your own Orchestrator
* Learn how Loop Steps work in InsightConnect
* Learn how Join Steps work in InsightConnect

# Requirements

* InsightIDR License
* InsightConnect License

# Documentation

## Setup

**This workflow requires an Insight Orchestrator and an API Key from VirusTotal!**

If you have not yet deployed and activated an Orchestrator, then you'll need to either deploy the OVA or run the install script on a vanilla server. Start by visiting our Help docs here: https://docs.rapid7.com/insightconnect/install-and-activate-the-orchestrator

Once you have activated on Orchestrator, you'll need an API key from VirusTotal.

1. Sign up for a free account here: https://www.virustotal.com/gui/join-us
2. Log in and click on your user profile in the top right, then click on `API key`
3. Copy your API key

Now, simply import the workflow, import the VirusTotal plugin, create a connection using your VirusTotal API Key, and activate the workflow in InsightConnect! No additional setup is required for this workflow.

### Usage

To run the workflow, follow the below steps:

1. Open an Investigation in InsightIDR that includes an external IP address, URL, domain, or process hash
2. Click the `Take Action` button in the Investigation to open the response panel
3. Select `Custom InsightConnect Workflows` from the `Action Category` list
4. Select the `Enrich InsightIDR Alerts with Threat Intelligence from VirusTotal` workflow (Note: If you changed the name of the workflow during the import process, then you will see a different workflow name!)
5. Select the indicator(s) of compromise to enrich
6. Click `Take Action`!

An event will be automatically added to your Investigation Timeline in InsightIDR. Click on it to see the results of your workflow!

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VirusTotal|6.0.3|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References
* [VirusTotal](https://virustotal.com)
