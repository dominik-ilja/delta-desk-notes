# Git Branch and Commit Guidelines
## Overview

This guide establishes our team's standards for Git branch naming and commit messages to maintain clear traceability between code changes and project requirements.

## Branch Naming Convention

We use two types of branch naming schemes depending on whether the work is tied to a ClickUp task.

### ClickUp Task Branches

Branches that relate to a specific task within ClickUp consist of four parts:

```
<type>/clickup/<clickup-id>/<description>
```

**Parts:**

1. **Type** - The nature of the change (bug, fix, feat, refactor, docs, etc.)
2. **Segment** - Always "clickup" to identify task-related branches
3. **ClickUp ID** - The ID of the ClickUp item
4. **Description** - Short description of the task (can be the task name itself)

**Examples:**

```
fix/clickup/8babxmbcb/fix-date-sorting-across-application
feat/clickup/9xyzmn123/add-payment-gateway-integration
bug/clickup/7abcdef45/resolve-login-timeout-issue
refactor/clickup/6mnopqr78/optimize-database-queries
```

### Non-ClickUp Branches

Any other branch that isn't tied to a ClickUp task uses a simpler format:

```
<type>/<description>
```

**Examples:**

```
feat/implement-crud-employee
fix/update-dependencies
refactor/clean-up-util-functions
docs/update-api-documentation
```

### Environment Branches

The following branches are exceptions and relate to specific deployment environments:

- `main` - Production environment
- `staging` - Staging environment
- `dev` - Development environment

**These branches should never be deleted and follow direct deployment workflows.**

## Branch Types

Use these standardized types for consistency:

- `feat` - New features or enhancements
- `fix` - Bug fixes
- `bug` - Bug fixes (alternative to fix)
- `hotfix` - Urgent production fixes
- `refactor` - Code refactoring without functional changes
- `docs` - Documentation updates
- `test` - Adding or updating tests
- `chore` - Maintenance tasks, dependency updates, etc.

## Commit Messages

### Individual Commits

Individual commits on feature branches should be clear and descriptive. Focus on explaining **what** changed and **why**, not how.

**Good commit messages:**

```
Add Stripe SDK integration

Integrate Stripe payment processing library to support
credit card transactions. Configured with API keys from
environment variables.
```

```
Fix null pointer exception in user service

Added null check before accessing user.email property
to prevent crashes when user data is incomplete.
```

**Tips for good commits:**

- Use the imperative mood ("Add feature" not "Added feature")
- Keep the first line under 50 characters
- Add a blank line, then a more detailed description if needed
- Explain the "why" behind the change, not just the "what"

### Pull Request Titles

When creating a pull request, always include the ClickUp ID (if applicable) in the title:

```
[clickup-<id>] Brief description of the change
```

**Examples:**

- `[clickup-8babxmbcb] Fix date sorting across application`
- `[clickup-9xyzmn123] Add payment gateway integration`
- `Implement CRUD operations for employee management` (non-ClickUp task)

The PR title will become the merge commit message, automatically linking the code changes to the ClickUp task.

## Complete Workflow Example

### For ClickUp Tasks:

1. **Create a branch from the ClickUp task:**
```bash
git checkout -b feat/clickup/9xyzmn123/add-payment-gateway
```

2. **Make commits with clear messages:**
```bash
git commit -m "Add Stripe SDK integration"
git commit -m "Create payment service class"
git commit -m "Add unit tests for payment flow"
```

3. **Create a pull request with ClickUp ID in title:**
```
Title: [clickup-9xyzmn123] Add payment gateway integration
```

4. **Merge to the appropriate environment branch** (dev → staging → main)

### For Non-ClickUp Work:

1. **Create a descriptive branch:**
```bash
git checkout -b refactor/optimize-user-queries
```

2. **Make clear commits:**
```bash
git commit -m "Add indexes to user table for faster lookups"
git commit -m "Refactor user query to use prepared statements"
```

3. **Create a pull request with descriptive title:**
```
Title: Optimize user database queries
```

## Benefits

- **Easy tracking**: Quickly find all code changes related to a ClickUp task
- **Clean history**: Individual commits stay focused on technical details while merge commits provide project context
- **Consistent workflow**: Clear conventions reduce confusion and improve team collaboration
- **Environment safety**: Protected environment branches prevent accidental deployments

## Summary

- **Always use the ClickUp branch format** when working on a ClickUp task
- **Include the ClickUp ID in PR titles** for task-related work
- **Write clear, descriptive commit messages** that explain the why
- **Never delete environment branches** (main, staging, dev)
- **Follow the type conventions** for consistency across the team
