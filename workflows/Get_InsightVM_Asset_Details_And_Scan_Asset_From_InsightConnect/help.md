# Description

This workflow uses an API trigger to lookup an asset by its IP address in InsightVM and scan the target IP. This form of ad hoc scanning can help quickly identify and collect vulnerability data about a given device.

By default, the scanning step of this workflow is disabled. By simply configuring an ad hoc scanning site in InsightVM, you can easily enable the step and any target included in the asset scope of the site may be scanned ad hoc using this workflow.

*The [Scan Asset with InsightVM from Slack](https://extensions.rapid7.com/extension/Scan_Asset_With_InsightVM_From_Slack) and [Scan Asset with InsightVM from Microsoft Teams](https://extensions.rapid7.com/extension/Scan_Asset_With_InsightVM_From_Teams) workflows are closely related to this workflow and may be implemented to allow for ad hoc scanning from chat!*

# Key Features

* Retrieve asset and vulnerability data on an IP address
* Scan a target IP on an ad hoc basis
* Maintain visibility into approved exception requests with Job History in InsightConnect

# Requirements

* InsightConnect
* InsightVM

# Documentation

## Setup

*This workflow requires deployment of the [Insight Orchestrator](https://docs.rapid7.com/insightconnect/install-and-activate-the-orchestrator) and a [connection to the InsightVM Console](https://extensions.rapid7.com/extension/rapid7_insightvm#Documentation-Setup).*

Import the workflow and proceed through the Import Workflow wizard in InsightConnect. Import plugins and create connections during the import process as necessary.

## Readme

*This workflow can be activated immediately without enabling the Scan Asset step. If this is done, then the workflow will only collect host details; it will not start a scan of the target IP address.*

When configured to include the Scan Asset step, this workflow utilizes existing InsightVM (or Nexpose) sites and scan engines to run ad hoc single-asset scans. These ad hoc scans will not skip the scan engine queue. As such, if a scan engine is running a scheduled scan, then the scan triggered by this workflow will be added to the back of the scan engine queue.

This workflow may only scan assets that are in the site's asset scope. As such, administrators should configure the site so that the asset scope is broad enough to be useful for consumers of this workflow. On the other hand, explicitly exclude critical systems from the site scope to prevent unauthorized scanning activity.

### InsightVM Setup

In order to activate the Scan Asset step in this workflow, you will need to configure a site in InsightVM (or Nexpose). The scan will inherit all configuration settings for this site, including credentials, scan engine, and scan template, and the asset specified must be in the Asset scope for the selected site.

The following guidelines are recommended for use when configuring the site within InsightVM (or Nexpose) for this workflow:

1. **Create New Site.** Create a new site in InsightVM. This site will be used solely for ad hoc scans with this InsightConnect workflow.
2. **Add Assets.** Add all possible scan targets. Using Class A, B, or C subnets (eg, 10.1.2.0/24, 10.1.0.0/16, or 10.0.0.0/8) or an asset group (eg, Windows Workstations) is recommended.
3. **Add Authentication.** Add scan credentials in order to perform authenticated scans. Authenticated scans yield significantly more accurate results than non-authenticated scans. Administrative credentials are highly recommended for best results.
4. **Select Scan Template.** Choose a scan template for the site. The default `Full Audit without Web Spider` is appropriate in most cases.
5. **Select Scan Engine.** Select the `Engine most recently used for that asset` option. Also, select the scan engine with the broadest network access from the scan engine list below.
6. **No Scheduled Scans.** Given this site likely has an extremely broad scope, it is not recommended that this site be used for regular vulnerability scanning. As such, it is recommended that there be no scheduled scans for the site.

Save the site configuration and navigate to the Site Summary page. View the URL in your web browser to find the `Site ID`. For example, if my console URL is `https://10.1.2.3:3780/site.jsp?siteid=123`, then my `Site ID` is `123`.

Once you have found the site ID, move on to activate the Scan Asset step in the InsightConnect workflow.

### InsightConnect Setup

1. Import the workflow, import plugins, and create connections as necessary. 
2. Open the workflow draft. 
3. Edit the `Scan Asset` step. Insert the `Site ID` into the first input field, replacing the `INSERT_SITE_ID`. Save the step and it should be enabled automatically.
4. Enable the final `Scan Report` step.

## Usage

To try out the workflow, after configuring your site in InsightVM and the `Scan Asset` step in the workflow, click the blue Test button. Enter an IP address that is within the asset scope of your site in InsightVM and click Test. You should see a new scan start in your InsightVM console within a couple of minutes!

You can also activate the workflow and run it using the cURL command associated with the trigger or by clicking the `Run` option in the workflow menu on the Active Workflows page in InsightConnect.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Rapid7 InsightVM|4.2.0|2|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References


