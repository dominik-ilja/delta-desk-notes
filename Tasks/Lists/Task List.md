---
aliases:
cssclasses:
  - full_width
tags:
Related:
  - "[[Completed List]]"
  - "[[Main Dashboard]]"
Sources: []
Type: Dashboard
No Task Update: true
Complete: false
Tasks: 159
Tasks Remaining: 159
Tasks Complete: 0
Date Completed:
---
# Task List
## Focus

```dataviewjs
const tasks = dv.pages()
    .file
    .tasks
    .where(t => !t.completed && t.text.includes("#Focus"))

dv.taskList(tasks)
```

## Priority
### Urgent

<span class="placeholder">No tasks</span>

### High

<span class="placeholder">No tasks</span>

### Medium

<span class="placeholder">No tasks</span>

### Low

<span class="placeholder">No tasks</span>

### None

<span class="placeholder">No tasks</span>

### Queued

<span class="placeholder">No tasks</span>

## Spillover

<span class="placeholder">No tasks</span>

## Tasks

<span class="placeholder">No tasks</span>

