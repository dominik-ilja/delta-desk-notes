---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# Git
## Naming branches

There's two types of naming schemes that we use for branches. ClickUp tasks are branches that relate to a specific task within ClickUp. It consists of four parts:

1. Type - This could be bug, fix, feat, etc.
2. Segment named "clickup"
3. ID of the ClickUp item
4. Description - Short description of the task. This could be the task name itself

**ClickUp tasks:**
```
# Syntax
<type>/clickup/<clickup-id>/<description>

# Example
fix/clickup/8babxmbcb/fix-date-sorting-across-application
```

Any other branch will only use the type and description as described above.

**Other branches:**
```
# Syntax
<type>/<description>

# Example
feat/implement-crud-employee
```

There's some outliers to this. However, these branches relate to a specific environment. These branches are:

- `dev` - Development environment
- `staging` - Staging environment
- `main` - Production environment

## Commit Messages

Commit messages should focus on having clear descriptive messages.

When doing a pull request, 
## Summary

Branches should always follow that are for a ClickUp item should always follow the above 
