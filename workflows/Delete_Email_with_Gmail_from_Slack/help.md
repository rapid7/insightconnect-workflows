# Description

Once you’ve positively identified a phish, removing it from the user’s inbox is critical. This workflow searches for an email with specific criteria such as sender, receiver, or subject and provides the option to delete matches from Slack.

Sample trigger commands:

`delete-email user@example.com subject:"A suspicious email"`

`delete-email user@example.com delete=True subject:"A suspicious email"`

`delete-email user@example.com subject:"A suspicious email" from:"example.com" body:"free stuff"`

# Key Features

* **Eliminate the Threat** - Once a phishing message is verified, the first thing you should do is remove that message from the affected user’s inbox. 
* **Work with Unparalleled Flexibility** - Take your work mobile and respond to reported threats from your phone, tablet, or PC.
* **Reduce Portal Fatigue** - You have enough to do without logging into a different solution every 5 minutes. Control your response actions from chat instead.

# Requirements

* [Slack chatops connection](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [Gmail](https://insightconnect.help.rapid7.com/docs/gmail-api)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

The following will need to be setup for Gmail:
* A service account with the appropriate access to the [Gmail API](https://developers.google.com/gmail/api/auth/web-server)
* [OAuth](https://developers.google.com/gmail/api/auth/scopes) scope. note: Service account must have 'domain-wide' delegation enabled

### Usage

`delete-email <mailbox_user> [delete=True|False] <query>`

|Parameter Name|Required|Description|
|mailbox_user|True|The email address of the inbox to search|
|delete|False|The option to instruct the command to delete the emails when found. Can only equal _True_ or _False_. *False* is the default|
|query|True|Everything else will be passed _as-is_ to the Gmail plugin as the search|

*This workflow will only trigger when sent directly to the slackbot in the message*
To run the workflow, `@` the slackbot with the command `delete-email`.
For example:
`@Rapid7 InsightConnect delete-email user@example.com subject:"A phishy email" from:"example.com" body:"free stuff"`.

If you would like to automatically delete these emails, add `delete=True` to the command. This must be right after the account like this:

`!delete-email user@example.com delete=True subject:"A phishy email"`

See the references section for links on search operators that can be passed to the query.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Python 3 Script|2.0.1|1|
|Gmail|5.1.4|3|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Gmail](https://mail.google.com/)
* [Google Service Account Setup](https://developers.google.com/gmail/api/auth/web-server)
* [Delegating Domain Wide Authority to a Service Account](https://developers.google.com/identity/protocols/OAuth2ServiceAccount#delegatingauthority)
* [Google API Scopes](https://developers.google.com/gmail/api/auth/scopes)
* [InsightConnect Gmail Plugin Guide](https://insightconnect.help.rapid7.com/docs/gmail-api)
* [Gmail Search Operators](https://support.google.com/mail/answer/7190)
* [Slack](https://slack.com/)
