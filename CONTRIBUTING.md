# Contributing

Thank you for your interest in joining the InsightConnect community! Please review our [Code of Conduct] before making contributions. 

There are multiple ways you can help us at Rapid7 and our customers close the security achievement gap with InsightConnect. These include:

- Build and contribute workflows to share the power of automation with fellow security leaders -- YOU ARE HERE!
- [Build and contribute new plugins] to extend automation possibilities
- [Report a security vulnerability in InsightConnect] to Rapid7

## Workflow Contributions
For those looking to contribute workflows, your first step is to plan, build, and test your workflow in InsightConnect. You may want to check to see if a similar workflow is available in the [Rapid7 Extension Library] first! If you're new to workflow building, you may want to read [get started with InsightConnect] and [Workflows 101]. These walkthroughs will help you get familiar with the mechanics of workflow building and include examples for many common scenarios. 

Once you've finished building your workflow, be sure to include a Final Report artifact to summarize the outcome. Finally, test it and take screenshots of the workflow, the successful job, and the Final Report artifact. You'll then need to prepare a workflow directory. This includes the screenshots taken after testing and basic documentation for your workflow listing on the Rapid7 Extension Library. See our [Contributor's Guide] for a complete walkthrough.

Finally, you're ready to submit your workflow pull request! See our [PR checklist] and please follow our short list of do's and don'ts below to make sure your valuable contributions actually make it into the Rapid7 Extension Library! We consider all our pull requests fairly and in detail, but if you do not follow these rules, your request will be closed. We strive to keep all the workflows published to the extension library high-quality and and easily transferrable across our InsightConnect user base. Thank you for understanding.

## Code Contributions

- **Do** read the [user documentation]
- **Do** follow the [50/72 rule] for Git commit messages.
- **Do** license your code as MIT.
- **Do** create a [topic branch] to work on. This helps ensure users are aware of commits on the branch being considered for merge, allows for a location for more commits to be offered without mingling with other contributor changes, and allows contributors to make progress while a PR is still being reviewed.

### Pull Requests

- **Do** write "WIP" on your PR and/or open a [draft PR] if submitting unfinished code.
- **Do** target your pull request to the **master branch**.
- **Do** specify a descriptive title to make searching for your pull request easier e.g. "Okta: New user suspension workflow".
- **Do** include [console output], especially the JSON output for new features and bug fixes.
- **Do** list [verification steps] so your tests are reproducible.
- **Do** [reference associated issues] in your pull request description.
- **Don't** leave your pull request description blank.
- **Don't** abandon your pull request. Being responsive helps us land your code faster.

#### New Features

- **Do** include documentation showing sample run-throughs via screenshots.
- **Don't** include more than one workflow per pull request.

#### Bug Fixes

- **Do** include reproduction steps in the form of [verification steps].
- **Do** link to any corresponding [Issues] in the format of `See #1234` in your commit description.

## Bug Reports

Please report vulnerabilities in Rapid7 software directly to security@rapid7.com.
For more on our disclosure policy and Rapid7's approach to coordinated disclosure, [head over here](https://www.rapid7.com/security).

When reporting issues:

- **Do** write a detailed description of your bug and use a descriptive title.
- **Do** include reproduction steps, stack traces, and anything that might help us fix your bug.
- **Don't** file duplicate reports; search for your bug before filing a new report.

If you need additional guidance, reach out to the open source contribution owners at
`IntegrationAlliance@rapid7.com`

Finally, **thank you** for taking the few moments to read this far! You're already way ahead of the
curve, so keep it up!

[Code of Conduct]:./CODE_OF_CONDUCT.md
[Build and contribute new plugins]:https://github.com/rapid7/insightconnect-plugins#getting-started
[Report a security vulnerability in InsightConnect]:https://www.rapid7.com/disclosure.jsp
[get started with InsightConnect]:https://insightconnect.help.rapid7.com/docs/get-started-with-insightconnect
[Workflows 101]:https://insightconnect.help.rapid7.com/docs/workflows-101
[Contributor's Guide]:./Contributors_Guide.md
[PR Checklist]:./.github/PULL_REQUEST_TEMPLATE.md
[user documentation]:https://insightconnect.help.rapid7.com/docs/
[50/72 rule]:http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
[topic branch]:http://git-scm.com/book/en/Git-Branching-Branching-Workflows#Topic-Branches
[draft PR]:https://help.github.com/en/articles/about-pull-requests#draft-pull-requests
[console output]:https://help.github.com/articles/github-flavored-markdown#fenced-code-blocks
[verification steps]:https://help.github.com/articles/writing-on-github#task-lists
[reference associated issues]:https://github.com/blog/1506-closing-issues-via-pull-requests
[Issues]:https://github.com/rapid7/insightconnect-workflows/issues
