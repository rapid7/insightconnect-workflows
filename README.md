# InsightConnect Workflows

A repository for sharing InsightConnect workflows. Find existing automations as well as share yours!

If you have questions, reach out to us at `IntegrationAlliance@rapid7.com`.

![Workflow](./imgs/workflow.png)

### Table of Contents

1. [Getting Started](#getting-started)
2. [Contributing](#contributing)

### Getting Started

See the documentation on building workflows in [InsightConnect](https://insightconnect.help.rapid7.com/docs/).

1. Build your workflow in InsightConnect
2. Export the intended workflow from the Workflows page
![Workflow](./imgs/export.png)
3. Create a PR of the workflow including screenshots demonstrating its use
4. Add documentation in `help.md` and a `workflow.spec.yaml` file to define the workflow for release

Organize using the following directory structure:

```
└── workflows
    └── Basic_Domain_Enrichment_Report
        ├── Basic_Domain_Enrichment_Report.icon
        ├── help.md
        ├── workflow.spec.yaml
        └── screenshots
            ├── artifact1.png
            ├── artifact2.png
            ├── workflow1.png
            └── workflow2.png
```

For contributions, follow the [PR Template Checklist](./.github/PULL_REQUEST_TEMPLATE.md).

### Contributing

See our [contributing guide](./CONTRIBUTING.md).
