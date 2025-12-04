# Quest Sample Pull Request

This folder is a placeholder. The sample pull request for Scenario 2 is created dynamically by the **Setup Quest PR** workflow.

## How to Create the Sample PR

1. Go to your repository's **Actions** tab
2. Select the **Setup Quest PR** workflow
3. Click **Run workflow**
4. Wait for the workflow to complete
5. Navigate to the **Pull Requests** tab to find the created PR

## What Gets Created

The workflow creates a sample pull request titled **"[Quest Sample] Add advanced Copilot data agent content"** that includes:

### New Content Files

| File | Description |
|------|-------------|
| `copilot-advanced-scenarios.md` | Multi-turn conversations, cross-source correlation, automated insights |
| `copilot-best-practices.md` | Data preparation, security config, performance optimization |
| `copilot-troubleshooting.md` | Common issues, error codes, diagnostic steps |

### Modified Files

| File | Changes |
|------|---------|
| `index.yml` | Updated to include three new units in the module structure |

### Intentional Issues for Review Practice

The PR contains intentional issues for you to find during your review:

- **YAML Issues:** Missing colon after `prerequisites`, outdated `ms.date`
- **Content Issues:** Typos ("avialable", "setings", "Intermitent", "occured")
- **Link Issues:** Broken link to `http://old-support.fabric.com/help`
- **Code Issues:** Deprecated `fabric.dataagent` import path
- **Terminology:** Inconsistent "Copilot" vs "data agents" usage

## Identifying the Quest PR

Look for the PR labeled with `quest-sample`. The PR title will be:
```
[Quest Sample] Add advanced Copilot data agent content
```

## Cleanup

To remove the sample PR after completing the quest:

1. Navigate to the Pull Requests tab
2. Find the PR with `quest-sample` label
3. Close or delete the PR
4. Delete the associated branch (`quest-sample-pr-*`)
