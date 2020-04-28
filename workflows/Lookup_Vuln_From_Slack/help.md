# Description

This workflow accepts a Slack command containing a CVE ID or vulnerability keyword(s), looks up the vulnerability in Rapid7's vulnerability database, and posts the vulnerability details back to the same Slack channel.

Sample Slack Trigger Commands:

`@Slackbot vuln check CVE-2020-0674`

`@Slackbot vuln check heartbleed`

`@Slackbot vuln check heartbleed vmware`


# Key Features

* Lookup vulnerability information from Slack
* Find all vulnerabilities that match a search term
* Get severity, description, publish date, and solution information in a Slack message

# Requirements

* InsightConnect License
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _Vuln Check Slack Trigger_ step, the _Searching Notification_ step, the _Post to Slack_ step, and the _Post to Slack (multiple results loop)_ step inside the _Loop over URLs_ loop.

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "vuln check <vulnerability>". The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 Vulnerability & Exploit Database|2.0.2|1|
|Type Converter|1.5.1|1|
|Basename|1.0.1|1|
|URL Extractor|1.0.3|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.2 - Updated documentation
* 1.1.1 - Updated plugin versions in help.md
* 1.1.0 - Updated workflow to work with v2.0.2 of the Rapid7 Vulnerability & Exploit Database plugin | Added a Final Report workflow artifact including a summary of workflow results
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 Vulnerability Database](https://www.rapid7.com/db)
* [Slack](https://slack.com)
