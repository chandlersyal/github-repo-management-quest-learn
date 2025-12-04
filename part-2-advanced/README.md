# Part 2: Advanced Copilot Workflows for Enterprise Scale

## Overview

Welcome to **Part 2** of the GitHub Copilot Repository Management Quest! This 60-minute lab builds on Part 1 fundamentals to tackle advanced workflows, bulk operations, and agent orchestration for enterprise-scale documentation management.

**Duration:** ~60 minutes  
**Difficulty:** Intermediate to Advanced  
**Prerequisites:** Completed Part 1 (or equivalent Copilot experience)

## What You'll Learn

By completing Part 2, you will:

1. **Create advanced custom agents** for specialized documentation workflows
2. **Triage issues at scale** using AI-powered bulk analysis
3. **Design agent ecosystems** that work together on complex tasks
4. **Implement enterprise automation** patterns for sustainable workflows

## Lab Structure

| Module | Duration | Focus |
|--------|----------|-------|
| **Recap + Advanced Setup** | 10 min | Review Part 1, add advanced agents |
| **Scenario 3: Advanced PR Review** | 25 min | Multi-agent pull request review |
| **Scenario 4: Agent Orchestration** | 20 min | Multi-agent workflows |
| **Wrap-up** | 5 min | Enterprise application discussion |

---

## Prerequisites Check

Before starting Part 2, ensure you have:

- ✅ Completed Part 1 (or have equivalent experience)
- ✅ `.agents` and `.prompts` files from Part 1 configured
- ✅ Sample PR created by running "Setup Quest PR" workflow
- ✅ Repository open in VS Code with Copilot active

**Need to set up sample PR?**
1. Go to your repository's **Actions** tab on GitHub
2. Run **"Setup Quest PR"** workflow
3. Check **Pull requests** tab for the sample PR with `quest-sample` label

---

## Recap + Advanced Setup (10 minutes)

### Quick Review: Part 1 Concepts

From Part 1, you learned:
- **@workspace** provides repository-wide context
- **Custom agents** specialize Copilot for specific tasks
- **Prompts** create consistent, reusable templates

### Module 0.2-0.4: Advanced Agent Creation

Now let's extend your agent toolkit with specialized agents for advanced workflows.

#### Add PR Review and Orchestration Agents

Update your `.agents` file with these advanced agents:

```yaml
pr-reviewer:
  description: Specialized agent for comprehensive pull request analysis
  instructions: |
    You are a PR review specialist for documentation repositories. Your expertise includes:
    - Content quality assessment for new and modified files
    - Cross-reference and link validation
    - Style guide compliance checking
    - YAML metadata validation for Microsoft Learn modules
    
    When reviewing PRs:
    1. Summarize the scope and impact of changes
    2. Identify potential issues (broken links, typos, style violations)
    3. Check for consistency with existing content
    4. Validate technical accuracy where possible
    5. Provide constructive, actionable feedback
    
    Always be constructive and prioritize feedback by importance.

link-checker:
  description: Validates links, includes, and cross-references in documentation
  instructions: |
    You are a link validation specialist. Your expertise includes:
    - Checking relative and absolute link paths
    - Validating include file references
    - Identifying broken cross-references
    - Verifying image and media paths
    
    When checking links:
    1. Identify all link types in the content
    2. Validate paths exist and are correct
    3. Flag potential 404 errors
    4. Suggest corrections for broken links
    
    Provide a clear report of valid and invalid links.

workflow-orchestrator:
  description: Coordinates multi-step workflows and agent collaboration
  instructions: |
    You are a workflow orchestration specialist. Your expertise includes:
    - Breaking complex tasks into coordinated steps
    - Delegating to specialized agents appropriately
    - Managing dependencies between tasks
    - Optimizing for efficiency and quality
    
    When orchestrating workflows:
    1. Identify the overall goal and success criteria
    2. Break into logical, sequenced steps
    3. Assign appropriate agents to each step
    4. Define handoffs and quality gates
    5. Suggest automation opportunities
    
    Create workflows that are efficient, repeatable, and scalable.
```

#### Add Advanced Prompts

Update your `.prompts` file:

```yaml
bulk-issue-analysis:
  description: Analyze multiple issues for patterns and prioritization
  prompt: |
    Analyze the provided issues and create a comprehensive triage report:
    
    **Categorization:**
    | Issue | Type | Priority | Effort | Labels |
    |-------|------|----------|--------|--------|
    [Populate table for each issue]
    
    **Patterns Identified:**
    - Common themes across issues
    - Potential root causes
    - Related issue groups
    
    **Recommended Actions:**
    1. Quick wins (< 1 hour each)
    2. High-priority items for this week
    3. Backlog items for later
    
    **Duplicates/Relationships:**
    - List any duplicate or related issues

agent-workflow:
  description: Design a multi-agent workflow for a complex task
  prompt: |
    Design a workflow for the specified task using available agents:
    
    **Available Agents:**
    - documentation-auditor: Content analysis
    - style-enforcer: Style consistency
    - link-checker: Link validation
    - issue-triager: Issue management
    - template-generator: Template creation
    
    **Workflow Design:**
    1. Step-by-step breakdown
    2. Agent assignments for each step
    3. Expected outputs and handoffs
    4. Quality checkpoints
    5. Estimated time per step
    
    Make the workflow repeatable and efficient.
```

### Test Your Advanced Agents

```
@issue-triager Analyze the issues in this repository with the quest-sample label. Categorize and prioritize them.
```

```
@workflow-orchestrator Design a workflow for auditing and improving a Microsoft Learn module.
```

**Full Task Details:** 
- [module-0-workspace-prep/tasks/task-0.2-custom-agent.md](../module-0-workspace-prep/tasks/task-0.2-custom-agent.md)
- [module-0-workspace-prep/tasks/task-0.3-prompt-library.md](../module-0-workspace-prep/tasks/task-0.3-prompt-library.md)
- [module-0-workspace-prep/tasks/task-0.4-optimization.md](../module-0-workspace-prep/tasks/task-0.4-optimization.md)

---

## Scenario 3: Advanced PR Review (25 minutes)

### The Story

A contributor has submitted a large pull request adding new Copilot for Fabric documentation. The PR includes new markdown files, YAML updates, and media files. You need to conduct a thorough, multi-faceted review using your advanced agents.

### Task 3.1: Comprehensive PR Analysis (15 min)

Open the sample PR created by the workflow. Use multiple agents for a thorough review:

**Initial Assessment:**
```
@pr-reviewer Analyze the pull request that adds Copilot for Fabric content. Summarize:
1. Scope of changes (files added/modified)
2. Overall quality assessment
3. Key areas requiring attention
4. Potential blockers or concerns
```

**Link Validation:**
```
@link-checker Check all links, includes, and cross-references in the PR changes. Identify any broken or potentially problematic links.
```

**Style Review:**
```
@style-enforcer Review the new content for Microsoft Learn style guide compliance. Check:
- Heading hierarchy and formatting
- Code block usage and language tags
- Terminology consistency
- Accessibility requirements (alt text, etc.)
```

**Key Skills:**
- Multi-agent PR review
- Systematic validation across dimensions
- Constructive feedback generation

**Full Task Details:** [scenario-3-big-merge/tasks/task-3.1-initial-review.md](../scenario-3-big-merge/tasks/task-3.1-initial-review.md)

### Task 3.2: Generate Review Comments (10 min)

Synthesize findings into actionable feedback:

```
@workflow-orchestrator Based on the PR review findings, create a prioritized list of review comments. Format as:
1. Critical issues (must fix before merge)
2. Important suggestions (should address)
3. Minor improvements (nice to have)
4. Positive feedback (what's done well)
```

**Draft a Review Summary:**
```
@pr-reviewer Write a constructive PR review summary that:
- Acknowledges the contributor's work
- Highlights key issues to address
- Provides specific, actionable suggestions
- Offers to help with complex fixes
```

**Key Skills:**
- Synthesizing multi-agent findings
- Writing constructive feedback
- Prioritizing review comments

**Full Task Details:** [scenario-3-big-merge/tasks/task-3.2-detailed-review.md](../scenario-3-big-merge/tasks/task-3.2-detailed-review.md)

---

## Scenario 4: Agent Orchestration (20 minutes)

### The Story

You've mastered individual agents. Now it's time to coordinate them for complex, multi-step workflows that can handle enterprise-scale documentation management.

### Task 4.1: Design Multi-Agent Workflows (10 min)

Create a workflow that uses multiple agents together:

```
@workflow-orchestrator Design a comprehensive documentation review workflow that:
1. Audits a Learn module for content quality
2. Checks all links and references
3. Reviews for style consistency
4. Generates an improvement plan with prioritized issues

Use available agents: documentation-auditor, link-checker, style-enforcer, issue-triager
```

**Execute the Workflow:**

```
@documentation-auditor Analyze the learn-pr/wwl/get-started-lakehouses module for content quality issues.
```

Then:
```
@link-checker Check all links and includes in the get-started-lakehouses module.
```

Then:
```
@style-enforcer Review the lakehouse module content for style consistency with Microsoft Learn standards.
```

Finally:
```
@issue-triager Based on the findings from the auditor, link-checker, and style-enforcer, create a prioritized improvement plan.
```

**Key Skills:**
- Multi-agent coordination
- Workflow design
- Result synthesis
- Quality gates

**Full Task Details:** [scenario-4-agent-arsenal/tasks/task-4.1-advanced-agents.md](../scenario-4-agent-arsenal/tasks/task-4.1-advanced-agents.md)

### Task 4.2: Create Reusable Workflow Patterns (10 min)

Document your workflow as a reusable pattern:

```
#agent-workflow Create a reusable workflow pattern for "New Module Review" that can be applied to any Microsoft Learn module. Include agent assignments, estimated times, and quality checkpoints.
```

**Build a Meta-Agent:**

Add to your `.agents` file:

```yaml
module-reviewer:
  description: Orchestrates comprehensive module reviews using multiple specialized agents
  instructions: |
    You are a module review coordinator. You orchestrate comprehensive reviews by:
    
    1. **Content Audit** (documentation-auditor)
       - Structure and organization
       - Completeness and accuracy
       - Learning objectives alignment
    
    2. **Technical Validation** (link-checker)
       - All links functional
       - Includes resolve correctly
       - Code samples validated
    
    3. **Style Review** (style-enforcer)
       - Microsoft Learn style guide compliance
       - Consistent terminology
       - Accessibility standards
    
    4. **Issue Planning** (issue-triager)
       - Prioritized fix list
       - Effort estimates
       - Quick wins identified
    
    When coordinating reviews:
    - Run agents in logical sequence
    - Synthesize findings into unified report
    - Prioritize by user impact
    - Identify automation opportunities
```

Test it:
```
@module-reviewer Coordinate a comprehensive review of the describe-medallion-architecture module.
```

**Key Skills:**
- Meta-agent design
- Workflow automation
- Enterprise-scale patterns

**Full Task Details:** [scenario-4-agent-arsenal/tasks/task-4.2-agent-orchestration.md](../scenario-4-agent-arsenal/tasks/task-4.2-agent-orchestration.md)

---

## Wrap-up (5 minutes)

### What You Accomplished

- ✅ Created advanced agents for PR review and workflow orchestration
- ✅ Performed comprehensive multi-agent PR analysis
- ✅ Generated constructive review feedback
- ✅ Built multi-agent workflows for complex tasks
- ✅ Created reusable workflow patterns for enterprise scale

### Key Takeaways

1. **Agents can specialize and collaborate** - each focuses on what it does best
2. **Multi-agent reviews are thorough** - catch issues a single pass might miss
3. **Constructive feedback matters** - AI helps structure comments effectively
4. **Workflow patterns are reusable** - invest once, benefit repeatedly
5. **Meta-agents orchestrate complexity** - coordinate without manual intervention

### Enterprise Applications

These patterns apply to:
- **Large documentation repositories** - scale reviews and maintenance
- **Team workflows** - standardize processes across contributors
- **Release management** - coordinate documentation updates
- **Quality assurance** - automate checks and balances
- **Onboarding** - help new team members be productive quickly

### Reflection Questions

1. How would you adapt these workflows for your team's specific needs?
2. What repetitive tasks could be automated with agent workflows?
3. How could you measure the impact of these automations?

---

## Quest Complete! 🎉

You've completed both parts of the GitHub Copilot Repository Management Quest!

### Your New Skills

| Part 1: Fundamentals | Part 2: Advanced |
|---------------------|------------------|
| @workspace exploration | Multi-agent PR review |
| Basic agents & prompts | Advanced agent design |
| Content auditing | Workflow orchestration |
| Issue triage basics | Enterprise automation |

### Continue Learning

- **Experiment** with new agent types for your specific workflows
- **Share** your agents and prompts with your team
- **Iterate** on workflows based on real-world usage
- **Contribute** improvements back to this quest

---

## Quick Reference

### Essential Commands

| Command | Purpose |
|---------|---------|
| `@pr-reviewer [query]` | Comprehensive PR analysis |
| `@link-checker [query]` | Validate links and references |
| `@workflow-orchestrator [query]` | Multi-agent coordination |
| `#agent-workflow [task]` | Design workflows |

### Files to Reference

- **Module 0 Advanced Tasks:** `module-0-workspace-prep/tasks/task-0.2-0.4`
- **Scenario 3 Tasks:** `scenario-3-big-merge/tasks/`
- **Scenario 4 Tasks:** `scenario-4-agent-arsenal/tasks/`
- **Sample PR:** Check repository Pull requests tab (filter: `quest-sample`)

### Need Help?

- Check solution guides in each scenario's `solutions/` folder
- Review `resources/copilot-prompts.md` for more examples
- See `resources/best-practices.md` for tips
