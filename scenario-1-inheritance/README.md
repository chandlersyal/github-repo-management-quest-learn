# Scenario 1: The Inheritance

## The Story

It's Monday morning, and you've just received an urgent message from your manager:

> "Hey! The team that was managing our Microsoft Learn content for Fabric and related technologies has been reorganized. We need you to take over the `learn-pr/wwl` documentation repository. It's critical content for our customers learning Microsoft Fabric, Intune, and DevOps. The repository has been maintained by different writers over the years, and honestly, we're not sure what state it's in. Can you do a quick assessment and let us know what we're working with? Thanks!"

You navigate to the repository and see dozens of module folders, each with YAML metadata files, markdown includes, and media assets. There's no single overview of all the content, and you have no idea which modules might have outdated information, broken links, or inconsistencies.

**Your mission:** Understand what you've inherited, identify critical issues, and create an actionable plan to bring this repository up to standard.

## Scenario Overview

**Duration:** 30-45 minutes
**Difficulty:** Beginner to Intermediate
**Focus:** AI-assisted repository exploration and content auditing

## Learning Objectives

By completing this scenario, you will:

1. Learn to efficiently explore unfamiliar repositories using AI assistance
2. Identify documentation quality issues (broken links, outdated content, inconsistencies)
3. Create comprehensive content audit reports
4. Establish documentation standards and guidelines
5. Develop a systematic approach to repository takeover

## The Content Repository

The `learn-pr/wwl/` directory contains real Microsoft Learn training modules with:

- **50+ module folders** covering Microsoft Fabric, Intune, DevOps, and more
- **YAML metadata files** (index.yml, unit files) defining module structure
- **Markdown includes** with actual learning content
- **Media folders** containing images and diagrams
- **Various authors and dates** requiring consistency review
- **Cross-references** between modules that need validation
- **Mixed content types** (tutorials, conceptual, exercises, knowledge checks)

## Your Tasks

### Task 1.1: Repository Exploration and Mapping (15 minutes)
**File:** [tasks/task-1.1-explore.md](tasks/task-1.1-explore.md)

Use AI to quickly understand the Microsoft Learn module structure, content organization, and purpose of different folders. Create a visual map or outline of what exists.

**Key Questions to Answer:**
- What types of learning modules exist (conceptual, tutorial, exercise)?
- How are the modules organized by topic (Fabric, Intune, DevOps)?
- What are the main product areas covered?
- How is metadata structured in the YAML files?
- What's the overall content architecture?

### Task 1.2: Content Quality Audit (15 minutes)
**File:** [tasks/task-1.2-audit.md](tasks/task-1.2-audit.md)

Identify specific quality issues including outdated dates, inconsistent metadata, formatting issues, and technical accuracy problems.

**What to Look For:**
- Outdated `ms.date` values in YAML files
- Inconsistent author metadata patterns
- Missing or broken image references
- Inconsistent heading styles across modules
- Missing accessibility attributes
- Modules with TODO markers or incomplete sections

### Task 1.3: Generate Audit Report (10 minutes)
**File:** [tasks/task-1.3-report.md](tasks/task-1.3-report.md)

Create a comprehensive audit report summarizing your findings, prioritizing issues, and recommending next steps.

**Report Should Include:**
- Executive summary
- Issues categorized by severity (critical, high, medium, low)
- Quantitative metrics (modules by product, content freshness, etc.)
- Prioritized action plan
- Estimated effort for fixes

### Task 1.4: Documentation Standards Document (15 minutes)
**File:** [tasks/task-1.4-standards.md](tasks/task-1.4-standards.md)

Create or update a documentation standards file to ensure consistency across Microsoft Learn modules.

**Standards Should Cover:**
- YAML metadata requirements and formatting
- Markdown formatting conventions for Learn content
- Image and media asset requirements
- Module structure patterns
- Accessibility requirements
- Review and approval process

## How to Approach This Scenario

### Step 1: Set Up Your Environment

```bash
cd learn-pr/wwl
# Familiarize yourself with the module structure
ls -R
# Or use your file explorer
```

### Step 2: Use AI Strategically

Don't try to manually read every module. Instead, use AI to:
- Summarize module structure and metadata patterns quickly
- Identify patterns across multiple YAML and markdown files
- Find specific issues (outdated dates, inconsistencies)
- Generate reports from your findings

### Step 3: Work Through Tasks Sequentially

Each task builds on the previous one. Follow the instructions in the task files.

### Step 4: Document Your Process

Keep notes on:
- What prompts worked well with your AI assistant
- What patterns you discovered across modules
- What would you do differently next time

### Step 5: Check Solutions

When you're done, review the solution guides to see alternative approaches and best practices.

## Success Criteria

You've successfully completed this scenario when you can:

- ✅ Explain the Microsoft Learn module structure and content organization
- ✅ Identify at least 10 specific quality issues across the modules
- ✅ Categorize issues by type and severity
- ✅ Create a professional audit report
- ✅ Draft comprehensive documentation standards for Learn content
- ✅ Estimate effort required for remediation
- ✅ Articulate a clear plan for repository improvement

## Tips for Success

1. **Think like an auditor**: Be systematic and thorough
2. **Use AI for speed**: Let AI handle repetitive analysis tasks
3. **Validate AI findings**: Spot-check AI recommendations for accuracy
4. **Prioritize ruthlessly**: Focus on high-impact issues first
5. **Be specific**: Vague findings aren't actionable
6. **Consider the audience**: Who will use this documentation (learners, trainers)?

## Time Management

- **Task 1.1 (Explore)**: 15 minutes - Don't get lost in details
- **Task 1.2 (Audit)**: 15 minutes - Focus on finding issues
- **Task 1.3 (Report)**: 10 minutes - Be concise and actionable
- **Task 1.4 (Standards)**: 15 minutes - Create reusable templates
- **Buffer**: 10 minutes for review and reflection

## What's Next?

After completing this scenario, you'll be ready to:

- Apply these exploration techniques to any unfamiliar repository
- Conduct professional content audits on Microsoft Learn content
- Establish quality standards for documentation teams
- Move on to **Scenario 2: The Big Merge** where you'll review a complex PR updating Fabric modules

## Need Help?

- **Stuck on a task?** Check the hints section in each task file
- **Want to see solutions?** Review the solution guides in `solutions/`
- **Questions about AI prompts?** See `../../resources/ai-prompts.md`

---

**Ready to begin?** Start with [Task 1.1: Repository Exploration](tasks/task-1.1-explore.md)
