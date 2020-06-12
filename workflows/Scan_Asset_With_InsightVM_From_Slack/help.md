# Description

Scan and report on an asset's vulnerabilities and risk posture without leaving your Chat window. Built for patching administrators who may not have access to InsightVM, this workflow fetches the last vulnerability statistics for a given host, triggers a new scan for that host, and returns the updated vulnerability statistics. 

By displaying the last known vulnerability and risk data, the user is able to easily identify any change in vulnerability count or overall risk with the newly collected scan data.

Sample Trigger Commands:

`scan-asset workstation123`

# Key Features

* Launch a scan of a single asset with a Slack message
* Extend single-asset scanning capabilities to users without access to InsightVM
* Receive vulnerability and risk score statistics in a Slack thread
* Quickly compare previous vulnerability data with newly collected vulnerability data
* Confirm the effectiveness of patches and remediation actions without leaving Chat

# Requirements

* InsightConnect License
* InsightVM Site ID
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Readme

This workflow utilizes existing InsightVM (or Nexpose) sites and scan engines to run ad hoc single-asset scans. These ad hoc scans will not skip the scan engine queue. As such, if a scan engine is running a scheduled scan, then the scan triggered by this workflow will be added to the back of the scan engine queue.

This workflow may only scan assets that are in the site's asset scope. As such, administrators should configure the site so that the asset scope is broad enough to be useful for consumers of this workflow. On the other hand, explicitly exclude critical systems from the site scope to prevent unauthorized scanning activity.

## Setup

### InsightVM Setup

This workflow requires a pre-configured InsightVM (or Nexpose) site in order to scan a target. The scan will inherit all configuration settings for this site, and the asset specified must be in the Asset scope for the selected site.

The following guidelines are recommended for use when configuring the site within InsightVM (or Nexpose) for this workflow:

1. **Create New Site** Create a new site in InsightVM. This site will be used solely for this InsightConnect workflow.
2. **Add Assets** Add all possible scan targets. Using Class A, B, or C subnets (eg, 10.1.2.0/24, 10.1.0.0/16, or 10.0.0.0/8) or an asset group (eg, Windows Workstations) is recommended.
3. **Add Authentication** Add scan credentials in order to perform authenticated scans. Authenticated scans yield significantly more accurate results than non-authenticated scans. Administrative credentials are highly recommended for best results.
4. **Select Scan Template** Choose a scan template for the site. The default `Full Audit without Web Spider` is appropriate in most cases.
5. **Select Scan Engine** Select the `Engine most recently used for that asset` option. Also, select the scan engine with the broadest network access from the scan engine list below.
6. **No Scheduled Scans** Given this site likely has an extremely broad scope, it is not recommended that this site be used for regular vulnerability scanning. As such, it is recommended that there be no scheduled scans for the site.

Save the site configuration and navigate to the Site Summary page. View the URL in your web browser to find the `Site ID`. For example, if my console URL is `https://10.1.2.3:3780/site.jsp?siteid=123`, then my `Site ID` is `123`.

Once you have found the site ID, move on to configure the InsightConnect workflow.

### InsightConnect Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, the following steps will need to be edited to reflect your Slack and InsightVM configurations:

1. Update the `scan-asset Trigger` step to reflect your Slack environment. Edit the preset text of `change_me` in the `Match Channel` input, replacing it with a channel name from your Slack instance. The InsightConnect Slack chatbot will need to be added to this channel. This workflow is configured by default so scans may only be started from this channel.
2. In the `Remediations Loop`, the `Scan Asset` step will need the `Site ID` input updated to reflect your newly created InsightVM (or Nexpose) site. Edit the input with the preset text of `change_me`.

After updating the Slack scan-asset Trigger and the InsightVM scan step, activate the workflow in order to trigger it from the channel specified in the trigger.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.0.1|5|
|Type Converter|1.5.1|1|
|Timers|2.0.4|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
