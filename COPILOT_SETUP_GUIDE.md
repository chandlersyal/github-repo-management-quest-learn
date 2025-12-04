# GitHub Copilot Setup Guide

Quick guide to get GitHub Copilot set up for this quest.

## Prerequisites

- GitHub account (free)
- VS Code installed
- Internet connection

## Step 1: Get GitHub Copilot Access

### Option A: Individual Subscription ($10/month)
1. Go to https://github.com/features/copilot
2. Click "Start free trial" or "Buy now"
3. Complete payment setup
4. You get 30-day free trial!

### Option B: Student/Teacher (Free!)
1. Verify student/teacher status: https://education.github.com/
2. GitHub Copilot is FREE for verified students and teachers
3. Apply for GitHub Student Developer Pack

### Option C: Use Organization License
If your company has GitHub Copilot Business or Enterprise:
1. Ask your GitHub admin to add you
2. Accept the invitation
3. You're ready to go!

## Step 2: Install VS Code Extension

1. **Open VS Code**

2. **Open Extensions** (Ctrl+Shift+X or Cmd+Shift+X)

3. **Search for "GitHub Copilot"**

4. **Install TWO extensions:**
   - **GitHub Copilot** (the main extension)
   - **GitHub Copilot Chat** (for chat features)

5. **Reload VS Code** when prompted

## Step 3: Sign In

1. **VS Code will prompt you to sign in**
   - Click "Sign in to GitHub"
   - Browser will open

2. **Authorize the extension**
   - Click "Authorize Visual Studio Code"
   - Complete authentication

3. **Return to VS Code**
   - You should see Copilot icon in status bar

## Step 4: Verify It's Working

### Test 1: Inline Suggestions

1. Create a new file: `test.md`
2. Type: `# How to`
3. Wait a second - you should see gray suggestion text
4. Press `Tab` to accept, or keep typing to ignore

✅ If you see suggestions, inline Copilot works!

### Test 2: Copilot Chat

1. Press `Ctrl+Shift+I` (Windows/Linux) or `Cmd+Shift+I` (Mac)
2. Chat panel should open on the side
3. Type: `hello`
4. Copilot should respond

✅ If you get a response, Copilot Chat works!

### Test 3: @workspace Agent

1. In Copilot Chat, type: `@workspace`
2. You should see it autocomplete with a workspace icon
3. Complete the prompt: `@workspace what is in this repository?`
4. Copilot should analyze your workspace

✅ If Copilot describes files/folders, @workspace works!

## Step 5: Learn the Basics

### Essential Keyboard Shortcuts

| Action | Windows/Linux | Mac |
|--------|---------------|-----|
| Open Copilot Chat | Ctrl+Shift+I | Cmd+Shift+I |
| Inline Copilot | Ctrl+I | Cmd+I |
| Trigger suggestion | Alt+\ | Alt+\ |
| Accept suggestion | Tab | Tab |
| Reject suggestion | Esc | Esc |
| Next suggestion | Alt+] | Alt+] |
| Previous suggestion | Alt+[ | Alt+[ |

### Chat Agents

- **@workspace** - Ask about files/folders in your workspace
- **@terminal** - Get help with terminal commands
- **@vscode** - Get help with VS Code features

### Basic Prompts

Try these in Copilot Chat:

```
@workspace what files are in this project?
```

```
@workspace explain what this file does [filename]
```

```
@workspace find all markdown files
```

## Common Issues & Solutions

### Issue: No suggestions appearing

**Solutions:**
1. Check Copilot icon in status bar (bottom right)
   - Should show "Copilot" not "Copilot (disabled)"
2. Try: Ctrl+Shift+P → "GitHub Copilot: Enable"
3. Restart VS Code
4. Check your subscription is active

### Issue: @workspace doesn't work

**Solutions:**
1. Make sure you opened a **folder**, not just a file
   - File → Open Folder...
2. Check you have GitHub Copilot Chat extension installed
3. Update VS Code to latest version
4. Restart VS Code

### Issue: "Copilot isn't available"

**Solutions:**
1. Verify your subscription at https://github.com/settings/copilot
2. Check payment method is valid
3. Wait 5 minutes after subscribing (propagation time)
4. Sign out and sign back in to VS Code

### Issue: Slow or no responses

**Solutions:**
1. Check internet connection
2. GitHub Copilot might be experiencing issues
   - Check https://www.githubstatus.com/
3. Try simpler prompts first
4. Restart VS Code

## Quest-Specific Setup

### For This Quest

1. **Clone the repository:**
   ```bash
   git clone https://github.com/hrasheed-msft/github-repo-management-quest.git
   cd github-repo-management-quest
   ```

2. **Open in VS Code:**
   ```bash
   code .
   ```

3. **Verify @workspace sees the files:**
   - Open Copilot Chat (Ctrl+Shift+I)
   - Type: `@workspace what scenarios are in this repository?`
   - Copilot should list: Scenario 1, 2, and 3

4. **Navigate to Scenario 1:**
   ```bash
   cd scenario-1-inheritance/challenge-repo
   code .
   ```

5. **Start Task 1.1:**
   - Open `tasks/task-1.1-explore-COPILOT.md`
   - Follow the instructions
   - Use the provided Copilot prompts

## Tips for Success

### Do:
✅ Use `@workspace` for repository-wide questions
✅ Be specific in your prompts
✅ Ask follow-up questions
✅ Accept suggestions with Tab
✅ Experiment - Copilot is a learning tool

### Don't:
❌ Expect perfection (always validate)
❌ Share sensitive code (if using public Copilot)
❌ Forget to use @workspace for context
❌ Give up if first prompt doesn't work (rephrase!)

## Getting Help

### During the Quest

- Check task instructions for specific Copilot prompts
- Review solution guides for expected outputs
- Try rephrasing prompts if not getting good results

### General Copilot Help

- **Documentation:** https://docs.github.com/copilot
- **Community:** https://github.com/community
- **Support:** https://support.github.com

### Quest-Specific Help

- Open an issue: https://github.com/hrasheed-msft/github-repo-management-quest/issues
- Check existing issues for solutions

## Next Steps

Once Copilot is working:

1. ✅ Complete the verification tests above
2. ✅ Read the main [README.md](README.md)
3. ✅ Start [Scenario 1: The Inheritance](scenario-1-inheritance/README.md)
4. ✅ Use provided Copilot prompts in each task
5. ✅ Experiment and learn!

---

## Quick Reference Card

Print or bookmark this page:

```
GitHub Copilot for Repository Management Quest

Setup:
1. Get Copilot subscription (https://github.com/features/copilot)
2. Install extensions: GitHub Copilot + GitHub Copilot Chat
3. Sign in to GitHub in VS Code
4. Open quest folder: code .

Shortcuts:
- Copilot Chat: Ctrl+Shift+I (Cmd+Shift+I on Mac)
- Inline: Ctrl+I (Cmd+I on Mac)
- Accept: Tab
- Reject: Esc

Essential:
- Use @workspace for repository questions
- Be specific in prompts
- Validate outputs
- Ask follow-up questions

Help:
- Docs: https://docs.github.com/copilot
- Quest Issues: github.com/hrasheed-msft/github-repo-management-quest/issues
```

---

**Ready to start? Go to the [README.md](README.md) to begin your quest!**
