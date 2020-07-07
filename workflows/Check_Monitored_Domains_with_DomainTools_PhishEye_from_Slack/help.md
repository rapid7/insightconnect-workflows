# Description

This workflow accepts a Slack command containing a DomainTools PhishEye search term. It will search PhishEye and return the results of matching domains back to Slack.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect check-phisheye example`

# Key Features

* Check for phishing domains related to a search term

# Requirements

* [Slack connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* DomainTools PhishEye API key and username

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.
The workflow is set to search back 1 day but this value can be changed in the _Search PhishEye_ step.

To run the workflow, @ your Slackbot in the chosen channel or in a direct message along with the command "check-phisheye <term>". The workflow will post responses in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|DomainTools PhishEye|1.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [DomainTools Phisheye](https://www.domaintools.com/products/phisheye/)
* [Slack](https://slack.com)
