---
Complete:
Status: 0 - Not Started
State: 0 - Not Started
Priority: 0 - None
Life Category:
tags:
Due Date:
Start Date:
Date Completed:
Date Created:
Last Updated: September 10, 2025, at 10:27 AM
Time Estimate:
Time Tracked:
Waiting On:
Docs:
GitHub:
Lists:
Related:
Sources:
Type: Task
File Size: 806.00 Bytes
cssclasses:
  - full_width
---
# <% tp.file.title %>

<%*
try {
    console.log("Running")
    if (!tp.file.path().includes("Tasks/Backlog")) {
        await tp.file.move(`/Tasks/Backlog/${tp.file.title}`)
    }
} catch(e) {
    console.log(e);
}
_%>

## Description

<span class="placeholder">No description</span>

## Task List

<span class="placeholder">No tasks</span>

### Completed

<span class="placeholder">No completed tasks</span>

## Logs

<span class="placeholder">No logs</span>
