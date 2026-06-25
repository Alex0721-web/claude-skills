---
name: find-skills
description: Helps users discover and install agent skills when they ask questions like "how do I do X", "find a skill for X", "is there a skill that can...", or express interest in extending capabilities. This skill should be used when the user is looking for functionality that might exist as an installable skill.
---

# Find Skills

This skill helps you discover and install skills from the open agent skills ecosystem.

## When to Use This Skill

Use this skill when the user:

- Asks "how do I do X" where X might be a common task with an existing skill
- Says "find a skill for X" or "is there a skill for X"
- Asks "can you do X" where X is a specialized capability
- Expresses interest in extending agent capabilities
- Wants to search for tools, templates, or workflows
- Mentions they wish they had help with a specific domain (design, testing, deployment, etc.)

## What is the Skills CLI?

The Skills CLI (`npx skills`) is the package manager for the open agent skills ecosystem.

**Key commands:**
- `npx skills find [query]` - Search for skills
- `npx skills add <package>` - Install a skill
- `npx skills check` - Check for updates
- `npx skills update` - Update all skills

**Browse skills at:** https://skills.sh/

## How to Help Users Find Skills

### Step 1: Understand What They Need
Identify domain, specific task, and whether a skill likely exists.

### Step 2: Check the Leaderboard First
Check https://skills.sh/ for popular skills. Top sources: `vercel-labs/agent-skills`, `anthropics/skills`.

### Step 3: Search for Skills
```bash
npx skills find [query]
```

### Step 4: Verify Quality
1. Install count — prefer 1K+. Be cautious under 100.
2. Source reputation — vercel-labs, anthropics, microsoft are trustworthy.
3. GitHub stars — <100 stars is a red flag.

### Step 5: Present Options
Show skill name, what it does, install count, source, and install command.

### Step 6: Offer to Install
```bash
npx skills add <owner/repo@skill> -g -y
```

## Common Skill Categories
| Category | Queries |
|---|---|
| Web Development | react, nextjs, typescript, tailwind |
| Testing | jest, playwright, e2e |
| DevOps | deploy, docker, kubernetes |
| Documentation | docs, readme, changelog |
| Code Quality | review, lint, refactor |
| Design | ui, ux, design-system |
| Productivity | workflow, automation, git |

## When No Skills Are Found
Offer to help directly, suggest `npx skills init`.
