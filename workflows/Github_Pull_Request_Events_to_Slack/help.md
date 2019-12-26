# Description

This workflow is designed to notify Github Pull Request Events to Slack.  Post messages directly into your Slack workspace in your preferred channels, private groups, or IM channels.
The way this works is that Github is configured to run a webhook each time a pull request event happens. This is configured in Github on the repo's settings page under webhooks. When this event occurs, Github will POST a body of information about the Pull Request to InsightConnect which will use that information to kick off the workflow and post a message in a Slack channel that a pull request has been open, closed, merged, etc.. This workflow allows the team to be easily notified when new code is up without having to go to Github and refresh the page.

# Key Features

* Post Merged Message
* Post Closed Message
* Post Review Label Message 
* Post Review Request Message
* Post Open Message

# Requirements

API Key 


# Documentation

## Setup

Once the workflow has been downloaded, login to InsightConnect and “Import” it into the workflow builder. 


## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
Python 2 Script 2.0.3



## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

