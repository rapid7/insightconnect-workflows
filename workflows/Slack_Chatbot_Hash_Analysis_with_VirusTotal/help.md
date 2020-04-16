# Description

Initiate and receive VirusTotal hash scan reports with the Slack chatbot.

Sample Slack Trigger Commands:

`@Security Bot !hash_lookup 44d88612fea8a8f36de82e1278abb02f`

`@Security Bot !hash_lookup 3395856ce81f2b7382dee72602f798b642f14140`

`@Security Bot !hash_lookup 275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f`


# Key Features

* Lookup a VirusTotal hash scan
* Get a VirusTotal scan report with total positive detections and a results permalink in a Slack message

# Requirements

* Slack connection

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and setup or select your Slack connection in the _Start Lookup_ 
step, the _Post Hash Lookup Confirmation_ step, and the _Post Hash Found Scan Report_ and Post Hash Not Found Scan Report steps.
Each Slack step will need the channel name updated as well (edit the input with the preset text of `change_me`).

To run the workflow, @ your Slackbot in any channel or in a direct message along with the command "!hash_lookup <hash>".
The workflow will post when it is starting the lookup and then again with the results of the lookup.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
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
