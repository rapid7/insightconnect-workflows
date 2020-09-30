# Description

This workflow is meant to introduce InsightIDR users to plugins, actions, and workflow tests. It uses an API trigger, which accepts a single string input, to lookup a hash in Threat Crowd, a free-to-use threat intelligence service. This workflow is easy to test out for users who are new to InsightConnect and automation workflows.

To try this workflow, simple click Test when editing the workflow and paste a hash into the input field. Here's a sample hash to use as an input: `02914C82CDFC5504242B4C47B09FCEC1`

# Key Features

* Learn how to Test a workflow
* Learn how to use the API Trigger
* See how third-party threat intelligence can help your incident investigations

# Requirements

* InsightConnect License

# Documentation

## Setup

Simply import the workflow, import the Threat Crowd plugin, set the plugin to `Run on Cloud`, and activate the workflow in InsightConnect! No additional setup is required for this workflow.

### Usage

To test the workflow, follow the below steps:

1. Import and open the workflow so you see it in the Builder view
2. Click `Test` in the top right
3. Paste a file or process hash into the `Hash` input box. You can use `02914C82CDFC5504242B4C47B09FCEC1` if you need an example.
4. Click `Test Workflow` and see the workflow run in the `Job Details` panel
5. Once the workflow is complete, click the `Artifacts` toggle in the `Job Details` panel to view a summary of the findings

To run the workflow in production using the API Trigger, follow the below steps:

1. Import and open the workflow so you see it in the Builder view
2. Click on the `API Trigger` step
3. Click `Save Step` to reach the `How To Use` panel
4. Copy the sample cURL command and paste it into a text editor or command line utility
5. Insert your Insight Platform User API Key into the designated space in the cURL command. If you do not have your User API Key, then navigate to `My Account` >> `User Key` >> `New User Key` (more information on Rapid7 Insight Clou API Keys is available here: https://docs.rapid7.com/insight/managing-platform-api-keys/#generating-a-user-key)
6. Insert a file or process hash into the sample cURL command
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

* 1.0.1 - Updated Artifact
* 1.0.0 - Initial workflow

# Links

## References
