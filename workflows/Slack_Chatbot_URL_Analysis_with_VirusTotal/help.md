# Description

Initiate and receive VirusTotal URL scan reports with the Slack chatbot.

Sample Slack Trigger Commands:

`@Security Bot !url_lookup example.com`

`@Security Bot !url_lookup www.example.com`

`@Security Bot !url_lookup https://www.example.com`


# Key Features

* Lookup a VirusTotal URL scan
* Get a VirusTotal scan report with total positive detections and a results permalink in a Slack message

# Requirements

* Slack connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _Start Lookup_ step, the _Post URL Lookup Confirmation_ step, and the _Post URL Scan Report step._
Each Slack step will need the channel name updated as well (edit the input with the preset text of `change_me`).

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "!url_lookup <url>". The workflow will post when it is starting the lookup and then again with the results of the lookup.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|ExtractIt|2.0.0|1|
|VirusTotal|6.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Fix filename
* 1.0.0 - Initial workflow

# Links

## References

* [VirusTotal](https://www.virustotal.com/gui/home/upload)
* [Slack](https://slack.com)
