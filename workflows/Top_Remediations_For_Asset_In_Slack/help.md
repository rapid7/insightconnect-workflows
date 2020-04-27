# Description

This workflow gives a remediator direct access to top remediation steps for a specified asset in Slack. The workflow triggers from a Slack command containing the keywords `get top remediations`, searches for the specified hostname, and returns the Top Remediations for that asset from InsightVM.

Sample Slack Trigger Command:

`@Slackbot get top remediations workstation123`

# Key Features

* Quickly identify top asset remediation steps to reduce risk
* Easily access detailed patching information for each remediation step
* See vulnerabilities remediated by each patch

# Requirements

* InsightVM Console URL and account credentials
* Slack integration

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and configure connections and orchestrators in each step.

If you do not have a Slack connection configured already, then please refer to our [Help documentation](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops).

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.0|2|
|Type Converter|1.5.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Rapid7 InsightVM](https://www.rapid7.com/products/insightvm)
* [Slack](https://slack.com)
