# Description

This workflow is meant to introduce InsightIDR users to plugins, actions, and running workflows. The workflow uses an API trigger, which accepts a single string input, to lookup a hash in Threat Crowd, a free-to-use threat intelligence service. This workflow is easy to test out for users who are new to InsightConnect and automation workflows.

**To run this workflow**, simply activate it with the toggle and click `Run` in the `...` menu. Paste an MD5 hash into the input field and click `Run Workflow`. That's it!
* Here's a sample hash to use as an input: `02914C82CDFC5504242B4C47B09FCEC1`.

# Key Features

* Learn how to Run a workflow
* Learn how to use the API Trigger
* See how third-party threat intelligence can help your incident investigations

# Requirements

_There are no requirements at this time_
# Documentation

## Setup

Simply import the workflow, import the Threat Crowd plugin, set the plugin to `Run on Cloud`, and activate the workflow in InsightConnect! No additional setup is required for this workflow.

### Usage

To run the workflow, follow the below steps:

1. Activate the workflow from the Control Panel page.
2. Click the `...` menu from the Control Panel page and click `Run`.
3. Paste an MD5 hash into the `Hash` input box. You can use `02914C82CDFC5504242B4C47B09FCEC1` if you need an example.
4. Click `Run Workflow`. You'll see your workflow Job open in a new tab!

To run the workflow in production using the API Trigger, follow the below steps:

1. Import and open the workflow so you see it in the Builder view
2. Click on the `API Trigger` step
3. Click `Save Step` to reach the `How To Use` panel
4. Copy the sample cURL command and paste it into a text editor or command line utility
6. Insert an MD5 hash into the sample cURL command
7. Run the cURL command from a command prompt. You should see a response including a `jobId`.
8. Open the Jobs page in InsightConnect. You should find a job with the same `jobId` value.


## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Threat Crowd|3.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.3 - Update Threat Crowd plugin to version 3.0.1
* 1.0.2 - Fix spelling of cloud_enabled tag | Update documentation
* 1.0.1 - Updated Artifact
* 1.0.0 - Initial workflow

# Links

## References
