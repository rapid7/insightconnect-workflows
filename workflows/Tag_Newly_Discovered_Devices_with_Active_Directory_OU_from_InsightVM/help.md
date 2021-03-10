# Description

This workflow listens using InsightVM Webhook Events for newly discovered devices, looks for an organizational unit for the asset in Active Directory, and tags the device in InsightVM with the respective organizational unit.

This workflow helps to organize the assets in your network, similar to how they are organized in your Active Directory environment.  

# Key Features

* Creates parity in the organization of Active Directory and InsightVM assets
* VM Events trigger utilizes InsightVM's new webhook feature

# Requirements

* Insight Platform User API Key
* Active Directory
* InsightVM
* InsightConnect

# Documentation

## Setup

**In order to use this workflow, you will need to subscribe to the InsightVM Asset Found webhook event. You will also need to adjust the Active Directory domain components to match your environment.**

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, open the workflow and view the InsightVM Events trigger step. Save the trigger configuration step and proceed through the Instructions on subscribing to the InsightVM Asset Found Webhook Event. This will require an [Insight Platform User API Key](https://docs.rapid7.com/insight/managing-platform-api-keys#generating-a-user-key). Insert your User API Key, copy the API request, run it from a command prompt, and look for a JSON response including an ID. If you receive a JSON response, then your webhook event subscription is active! Close your command prompt and return to the workflow in InsightConnect.

After subscribing to the asset found webhook event, return to the workflow editor and open the `Find Asset in AD` step. In the `Search Base` input field, change the pre-specified Active Directory domain name from `DC=change, DC=me` to the Active Directory domain name that is used in your InsightVM instance. This workflow will now query for organizational units using your Active Directory's domain components and tag new assets with those organizational units in InsightVM.

After configuring the Active Directory step, activate the workflow. Any newly discovered asset will generate a webhook event, which will trigger your workflow and attempt to find an organizational unit for that asset. If an organizational unit is found, the workflow will tag the newly discovered asset in InsightVM with the organizational unit!
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Active Directory LDAP|4.0.3|1|
|Rapid7 InsightVM|4.7.0|3|
|Type Converter|1.6.0|2|


## Troubleshooting

Experiencing delays? InsightVM Events are delivered to InsightConnect from InsightVM as soon as the Insight platform is notified of a change by the on-premises InsightVM Security Console. This can take anywhere from 5 minutes to several hours. Please be patient!

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Active Directory](https://docs.microsoft.com/windows-server/identity/ad-ds/ad-ds-getting-started)  
* [InsightVM](https://www.rapid7.com/products/insightvm/)
