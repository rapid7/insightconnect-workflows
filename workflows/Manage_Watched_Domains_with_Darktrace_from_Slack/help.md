# Description

This workflow adds or removes hosts (domains and IP addresses) in the Darktrace watched domains list via Slack command and reports information back to Slack.

Multiple hosts can be specified in one command.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect add-host 1.1.1.1 google.com`

`@Rapid7 InsightConnect remove-host rapid7.com`

# Key Features

* Add or remove hosts to/from watched domains list

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Darktrace

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **Update the first step with the channel name to suit your Slack environment!** by editing the input with the preset text of `change_me` to match the channel to monitor.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Type Converter|1.6.0|1|
|Darktrace|2.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Update Darktrace plugin
* 1.0.0 - Initial workflow

# Links

## References

* [Darktrace](https://www.darktrace.com/)
* [Darktrace Plugin](https://extensions.rapid7.com/extension/darktrace)
* [Slack](https://slack.com)
