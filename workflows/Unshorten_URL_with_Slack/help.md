# Description

This workflow accepts a Slack command containing a URL, looks up the URL with unshorten.me, and posts the full URL to Slack.

Sample Slack Trigger Commands:

`unshorten-url https://bit.ly/39HoYMu`

# Key Features

* Lookup full URL with Slack

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After import, activate the workflow in order to trigger it.

### Usage

*This workflow will only trigger in direct messages to your Slackbot. This is by design to avoid posting potentially malicious URLs in shared Slack channels.*

To run the workflow, send a direct message to your InsightConnect Slack Chatbot starting with the command `unshorten-url`.

For example:
* `unshorten-url https://bit.ly/39HoYMu`

The workflow will post a response in a thread.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|Unshorten.me|1.0.3|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Updated trigger syntax and documentation
* 1.0.2 - Fix image clarity | Fix documenation URL | Added keywords
* 1.0.1 - Fix image filename
* 1.0.0 - Initial workflow

# Links

## References

* [Unshorten.me](https://unshorten.me)
* [Slack](https://slack.com)
