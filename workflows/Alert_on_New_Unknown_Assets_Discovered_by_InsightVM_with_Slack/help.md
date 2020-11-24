# Description

This workflow warns users in Slack if InsightVM discovers a new Windows device that is not present in Active Directory. The workflow listens for InsightVM’s Asset Found webhook event, checks the operating system, attempts to look up Windows devices in Active Directory, and posts a notification in Slack if the device is not found.

This notification helps Security and IT teams raise the visibility of newly discovered, unmanaged assets on the network.

# Key Features

* Identify and alert on rogue Windows assets
* VM Events trigger utilizes InsightVM's new webhook feature
* Flexible workflow design allows for easy customization

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Insight Platform User API Key](https://docs.rapid7.com/insight/managing-platform-api-keys#generating-a-user-key)
* InsightVM
* InsightConnect

# Documentation

## Setup

*In order to use this workflow, you will need to subscribe to the InsightVM Vulnerabilities Found webhook event. You will also need to adjust the Active Directory Search Base and the Slack channel name to match your environment.*

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, open the workflow, and view the `Asset Found Event` trigger step. Click “Save Step” so that you reach the “Instructions” menu. Proceed through the instructions to subscribe to the InsightVM Asset Found Webhook Event. This will require an [Insight Platform User API Key](https://docs.rapid7.com/insight/managing-platform-api-keys#generating-a-user-key). Insert your User API Key, copy the API request, run it from a command-line interface, and look for a JSON response including an ID. If you receive a JSON response, then your webhook event subscription is active! Close your command-line interface and return to the workflow in InsightConnect.

After subscribing to the asset found webhook event, return to the workflow editor, and open the `Find Hostname` step. In the “Search Base” field, enter the appropriate Search Base for your domain. For example, if your domain is `acme.com` then the Search Base would be `DC=acme,DC=com`. Save your changes.

Finally, open the `Send Warning to Slack` step. Change the `#change_me    ` input for the channel name, replacing it with the name of a channel where you would like to receive unknown Windows device notifications. Save your changes.

Once you’ve subscribed to the InsightVM webhook event, updated the Active Directory search base, and changed the Slack channel name, your workflow is ready to be activated!

## Usage

This workflow is triggered automatically by InsightVM’s Asset Found Webhook Event. This occurs anytime an asset is discovered by InsightVM for the first time.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|String Operations|1.3.1|1|
|Active Directory LDAP|4.0.3|1|

## Troubleshooting

Experiencing delays? InsightVM Events are delivered to InsightConnect from InsightVM as soon as the Insight platform is notified of a change by the on-premises InsightVM Security Console. This can take anywhere from 5 minutes to several hours. Please be patient!

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
* [InsightVM Events Trigger](https://docs.rapid7.com/insightconnect/set-up-an-insightvm-events-trigger)
