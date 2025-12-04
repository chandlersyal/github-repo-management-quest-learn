# Quest Sample Issues

This folder is a placeholder. The sample issues for Scenario 3 are created dynamically by the **Setup Quest Issues** workflow.

## How to Create Sample Issues

1. Go to your repository's **Actions** tab
2. Select the **Setup Quest Issues** workflow
3. Click **Run workflow**
4. Wait for the workflow to complete
5. Navigate to the **Issues** tab to see the created issues

## What Gets Created

The workflow creates 12 sample GitHub issues representing common Microsoft Learn content challenges:

| Issue Type | Description | Example |
|------------|-------------|---------|
| Content bugs | Broken images, non-working code samples | Broken image in lakehouse module |
| Metadata issues | Outdated ms.date, YAML syntax errors | ms.date needs update |
| Enhancement requests | New content requests | Add troubleshooting section |
| Consistency issues | Terminology inconsistencies | Copilot naming varies across modules |
| Accessibility issues | Missing alt text | Images missing alt text |
| Duplicates | Same issue reported differently | Multiple reports of same broken image |
| Vague issues | Need more information | "The Fabric module is wrong" |
| Questions | Clarification requests | Prerequisites unclear |

## Identifying Quest Issues

All sample issues are tagged with the `quest-sample` label. Use this to filter and find them in your repository's Issues tab.

## Cleanup

To remove the sample issues after completing the quest:

```bash
# Using GitHub CLI
gh issue list --label quest-sample --state open --json number --jq '.[].number' | ForEach-Object { gh issue close $_ }
```

Or manually close issues with the `quest-sample` label.
