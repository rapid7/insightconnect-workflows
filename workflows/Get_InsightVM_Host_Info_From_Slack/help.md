# Description

This workflow provides fast, convenient access to information about a given host from InsightVM by fetching asset details from InsightVM and posting them in a Slack thread. Host info includes hostname, IP address, MAC address, operating system, running services, last assessment date, and vulnerability stats. Lookup can be performed by either hostname or IP address.

# Key Features

* Fetch host information from InsightVM quickly in Slack
* Determine when the system was last assessed for vulnerabilities
* Positively identify a system by looking up its IP or hostname
* Get an overview of vulnerabilities by criticality
* View running services

# Requirements

* InsightVM Console URL and account credentials
* InsightConnect License
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

## Usage

*This workflow will trigger in any direct messages to your Chatbot **or** any message in a channel directed @ your Chatbot. Note the Chatbot must be in the channel in order to trigger the workflow this way.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot or @ your Chatbot in a public channel starting with the command `lookup-host`.

For example, in a direct message to your Chatbot:
* `lookup-host hostname123`
* `lookup-host 10.1.2.34`

Or in a channel including your Chatbot:
* `@Rapid7 InsightConnect lookup-host hostname123`
* `@Rapid7 InsightConnect lookup-host 10.1.2.34`

The workflow will post matching host details in a thread. If multiple hosts meet the search criteria, the details of each will posted in separate messages in the same thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.2 - Removed ExtractIt Plugin to use a more reliable variable from the Slack Plugin.
* 1.0.1 - Updated workflow to include last assessment date, updated trigger syntax, updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Slack](https://slack.com)
