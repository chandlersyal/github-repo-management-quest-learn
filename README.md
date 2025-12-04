# GitHub Copilot for Repository Management Quest

## Quest Overview

Welcome to the **GitHub Copilot for Repository Management Quest** - an interactive learning experience designed for content developers who want to master GitHub Copilot's native features for repository management workflows. This quest simulates real-world scenarios using **real Microsoft Learn documentation**, covering common challenges like taking over unfamiliar repositories, triaging issue backlogs, and managing complex pull requests.

**What makes this quest unique:** You'll work with actual Microsoft Fabric learning modules while mastering GitHub Copilot's workspace agent, issue analysis, PR summarization, and automated code generation features.

## 🎯 Two-Part Lab Structure

This quest is designed as **two 60-minute labs** that can be completed independently or as a full learning experience:

| Lab | Duration | Focus | Scenarios |
|-----|----------|-------|-----------|
| **[Part 1: Fundamentals](part-1-fundamentals/README.md)** | 60 min | Core Copilot skills | Workspace setup + Scenarios 1-2 |
| **[Part 2: Advanced](part-2-advanced/README.md)** | 60 min | Advanced automation | Custom agents + Scenarios 3-4 |

**Start here:** Choose the lab that matches your experience level and time available!

## Learning Objectives

By completing this quest, you will:

1. **Master GitHub Copilot workspace exploration** - Use Copilot's @workspace agent to quickly understand unfamiliar repositories and Microsoft Learn documentation structures
2. **Implement efficient issue management** - Use Copilot to analyze issues, categorize, prioritize, and suggest fixes
3. **Develop advanced PR review skills** - Leverage GitHub Copilot's PR summaries, review suggestions, and inline chat for efficient pull request reviews
4. **Create documentation standards** - Establish quality standards with Copilot-assisted reviews and automated checks
5. **Build practical workflows** - Develop repeatable processes using GitHub Copilot's native capabilities

## Quest Structure

This quest uses **real Microsoft Learn modules** from the `learn-pr/wwl/` folder and contains a foundational module plus four progressive scenarios:

### Module 0: Workspace Preparation
**Duration:** 15-20 minutes | **Covered in:** Part 1 (intro) + Part 2 (advanced)

Customize your GitHub Copilot workspace with agents and reusable prompts using examples from Microsoft Learn documentation.

- **Part 1 covers:** Task 0.1 - Introduction to agents and prompts
- **Part 2 covers:** Tasks 0.2-0.4 - Creating custom agents and prompt libraries

### Scenario 1: The Inheritance
**Duration:** 25-30 minutes | **Covered in:** Part 1

Take over an unfamiliar Microsoft Fabric documentation repository. Use Copilot to explore the module structure, identify issues, and create an improvement plan.

**Content:** Microsoft Fabric modules including lakehouses, medallion architecture, and semantic models

### Scenario 2: The Backlog Battle
**Duration:** 20-25 minutes | **Covered in:** Part 1

Triage 12 open issues in a Microsoft Learn repository. Categorize, prioritize, identify duplicates, and create fix proposals.

**Content:** Workflow-created issues covering broken images, outdated dates, accessibility, and more

### Scenario 3: The Big Merge
**Duration:** 25-30 minutes | **Covered in:** Part 2

Review a pull request adding new Copilot for Fabric documentation. Identify content issues, validate cross-references, and provide constructive feedback.

**Content:** Workflow-created PR with intentional issues to discover

### Scenario 4: The Agent Arsenal
**Duration:** 20-25 minutes | **Covered in:** Part 2

Build a comprehensive agent ecosystem with specialized documentation agents that work together for enterprise-scale workflows.

**Content:** Advanced agent patterns and workflow orchestration

## Prerequisites

- **Git fundamentals**: Basic understanding of repositories, commits, branches, and pull requests
- **Markdown knowledge**: Familiarity with markdown syntax and documentation
- **GitHub Copilot**: Active GitHub Copilot subscription (individual, business, or enterprise)
- **Tools**: VS Code with GitHub Copilot extension, Git client, GitHub account

**Optional but helpful:**
- Experience with documentation systems (MkDocs, Jekyll, Docusaurus)
- Basic Python knowledge for understanding utility scripts
- Prior experience with code review processes

## Quest Format

This quest uses a **conceptual and interactive lab** format:

- **Conceptual sections** explain key GitHub Copilot features and best practices
- **Interactive labs** provide hands-on exercises with real repository scenarios
- **GitHub Copilot prompts** are provided for each task (copy-paste ready)
- **Solution guides** show expected Copilot interactions and outputs
- **Reflection prompts** encourage you to apply these skills to your work

## Getting Started

### Setup Requirements

1. **Install VS Code** - Download from https://code.visualstudio.com/
2. **Install GitHub Copilot extension** - From VS Code marketplace
3. **Activate GitHub Copilot** - Sign in with your GitHub account
4. **GitHub account** - Required for forking and running workflows

### Repository Setup

1. **Fork this repository** to your own GitHub account:
   - Click the "Fork" button at the top-right of this repository
   - Choose your account as the destination for the fork

2. **Clone your fork** (replace `[your-username]` with your GitHub username):
   ```bash
   git clone https://github.com/[your-username]/github-repo-management-quest.git
   cd github-repo-management-quest
   code .
   ```

3. **Create sample content** by running the setup workflows:

   **Option A: Using GitHub Web Interface (Recommended)**
   - Go to your forked repository on GitHub
   - Navigate to the **Actions** tab
   - You'll see two workflows: "Setup Quest Issues" and "Setup Quest PR"
   
   **To create sample issues for Scenario 3:**
   - Click on "Setup Quest Issues" workflow
   - Click "Run workflow" button
   - Select "scenario-3" from the dropdown
   - Click the green "Run workflow" button
   - Wait for the workflow to complete (creates 8 sample issues)

   **To create sample PR for Scenario 2:**
   - Click on "Setup Quest PR" workflow  
   - Click "Run workflow" button
   - Select your preferred PR size (small/medium/large)
   - Click the green "Run workflow" button
   - Wait for the workflow to complete (creates 1 sample pull request)

   **Option B: Using GitHub CLI (if you have it installed)**
   ```bash
   # Create sample issues
   gh workflow run setup-quest-issues.yml --field scenario=scenario-3

   # Create sample PR
   gh workflow run setup-quest-pr.yml --field pr_size=medium
   ```

4. **Verify setup**:
   - Check the **Issues** tab - you should see 8 sample issues labeled "quest-sample"
   - Check the **Pull requests** tab - you should see 1 sample PR labeled "quest-sample"

### Quest Workflow

1. **Open VS Code** with your forked repository
2. **Start with Scenario 1** in the `scenario-1-inheritance/` directory
3. **Open Copilot Chat** (Ctrl+Shift+I or Cmd+Shift+I)
4. **Follow task instructions** - use provided Copilot prompts
5. **Complete each task** using GitHub Copilot features
6. **Use your sample issues and PR** created by the workflows for Scenarios 2 & 3
7. **Check solution guides** to see expected approaches
8. **Progress through scenarios** at your own pace

### Important Notes

- **Scenario 1** uses the files in `scenario-1-inheritance/challenge-repo/` - no setup needed
- **Scenario 2** requires the sample PR created by running "Setup Quest PR" workflow
- **Scenario 3** requires the sample issues created by running "Setup Quest Issues" workflow
- All sample content is labeled with "quest-sample" for easy identification
- You can re-run the workflows anytime to create fresh sample content

### Troubleshooting

**Workflows not visible in Actions tab?**
- Make sure you're looking at your forked repository, not the original
- GitHub Actions should be enabled by default on forks

**Workflow run failed?**
- Check that your repository is public (required for GitHub Actions on free accounts)
- Ensure you have the latest version by syncing your fork with the original repository

**No sample issues or PRs created?**
- Check the Actions tab for workflow run details and any error messages
- Verify the workflows completed successfully (green checkmark)
- Issues appear in the "Issues" tab, PRs appear in "Pull requests" tab

**Need to start over?**
- You can delete the sample issues and PR, then re-run the workflows
- Or fork the repository again for a completely fresh start

## Repository Structure

```text
github-repo-management-quest/
├── README.md (this file)
├── part-1-fundamentals/
│   └── README.md (60-minute lab: Module 0.1 + Scenarios 1-2)
├── part-2-advanced/
│   └── README.md (60-minute lab: Module 0.2-0.4 + Scenarios 3-4)
├── learn-pr/
│   └── wwl/ (Microsoft Learn modules - your working content)
│       ├── get-started-lakehouses/
│       ├── describe-medallion-architecture/
│       ├── design-scalable-semantic-models/
│       └── ... (50+ Microsoft Fabric modules)
├── module-0-workspace-prep/
│   ├── README.md
│   └── tasks/ (agent and prompt configuration)
├── scenario-1-inheritance/
│   ├── README.md
│   ├── challenge-repo/ (legacy content for exploration)
│   ├── tasks/
│   └── solutions/
├── scenario-2-backlog-battle/
│   ├── README.md
│   ├── issues/ (created by workflow)
│   ├── tasks/
│   └── solutions/
├── scenario-3-big-merge/
│   ├── README.md
│   ├── pr-content/ (created by workflow)
│   ├── tasks/
│   └── solutions/
├── scenario-4-agent-arsenal/
│   ├── README.md
│   ├── tasks/
│   └── solutions/
└── resources/
    ├── copilot-prompts.md
    ├── best-practices.md
    └── copilot-features-guide.md
```

## Time Commitment

- **Part 1 (Fundamentals)**: ~60 minutes
- **Part 2 (Advanced)**: ~60 minutes
- **Complete quest**: ~2 hours total
- **Self-paced**: Complete parts independently on your own schedule
- **Requires**: Active VS Code session with GitHub Copilot

## Skills You'll Gain

### GitHub Copilot Mastery
- **@workspace agent** for repository-wide understanding
- **Copilot Chat** for analysis and content generation
- **Inline suggestions** for documentation improvements
- **PR summaries** for efficient code reviews
- **Issue-to-PR** automation workflows

### Repository Management
- Repository exploration with AI context awareness
- Content auditing and quality analysis
- Efficient pull request review strategies
- Issue triage and categorization at scale
- Automated template and standards generation
- Cross-reference validation with workspace intelligence

## Support and Feedback

- **Questions?** Open an issue in this repository
- **Stuck?** Check the solution guides in each scenario
- **Ideas for improvement?** We welcome contributions and feedback!

## Next Steps

Ready to begin? Choose your starting point:

- 🚀 **[Part 1: Fundamentals](part-1-fundamentals/README.md)** - Start here if you're new to GitHub Copilot or want to learn the core skills
- ⚡ **[Part 2: Advanced](part-2-advanced/README.md)** - Jump here if you're comfortable with Copilot basics and want advanced automation

Or dive into individual scenarios:
- [Scenario 1: The Inheritance](scenario-1-inheritance/README.md)
- [Scenario 2: The Backlog Battle](scenario-2-backlog-battle/README.md)
- [Scenario 3: The Big Merge](scenario-3-big-merge/README.md)
- [Scenario 4: The Agent Arsenal](scenario-4-agent-arsenal/README.md)

---

**Quest Version:** 2.0
**Last Updated:** 2025-12-04
**Content:** Microsoft Learn / Microsoft Fabric
**Estimated Completion Time:** 2 hours (1 hour per part)
**Difficulty Level:** Beginner to Advanced
