---
Complete: false
Tasks: 34
Tasks Remaining: 14
Tasks Complete: 20
Date Completed:
Last Updated: October 22, 2025, at 4:35 PM
File Size: 5.97 KB
aliases: []
cssclasses:
  - full_width
tags: []
Related:
  - "[[/Notes/Daily/2025-10-22 - Wednesday]]"
---
# Wednesday, October 22, 2025

[[/Agenda/Yearly/2025|2025]] ❯ [[/Agenda/Quarterly/2025 - Q4|Q4]] ❯ [[/Agenda/Monthly/2025 - October|October]] ❯ [[/Agenda/Weekly/2025 - Week 43|Week 43]]

❮ [[/Agenda/Daily/2025-10-21 - Tuesday|Tuesday, October 21, 2025]] · Wednesday, October 22, 2025 · [[/Agenda/Daily/2025-10-23 - Thursday|Thursday, October 23, 2025]] ❯

## Priority List

```dataviewjs
// Get tasks from the current file
const hideCompletedSubtasks = (task) => {
    return {
        ...task,
        children: task.children
            .filter((subtask) => subtask.task && !subtask.fullyCompleted)
            .map(hideCompletedSubtasks)
    }
}

const tasks = dv.current().file.tasks.where(task => !task.fullyCompleted);
tasks.values = tasks.values.map(hideCompletedSubtasks)

// Define priority order (lower number = higher priority)
const priorityOrder = {
    "Urgent": 1,
    "High": 2,
    "Medium": 3,
    "Low": 4,
    "None": 5,
    "": 5  // Default for tasks without priority
};

// Function to extract priority from task text
function getPriority(task) {
    const priorityMatch = task.text.match(/\[Priority::\s*([^\]]+)\]/);
    return priorityMatch ? priorityMatch[1].trim() : "";
}

// Function to extract due date from task text
function getDueDate(task) {
    const dueDateMatch = task.text.match(/\[Due::\s*([^\]]+)\]/);
    if (dueDateMatch) {
        return dv.date(dueDateMatch[1].trim());
    }
    return null;
}

// Function to clean task text by removing dataview tags
function cleanTaskText(task) {
    return task.text
        .replace(/\[Priority::\s*[^\]]+\]/g, '')  // Remove priority tags
        .replace(/\[Due::\s*[^\]]+\]/g, '')       // Remove due date tags
        .replace(/\s+/g, ' ')                     // Replace multiple spaces with single space
        .trim();                                  // Remove leading/trailing whitespace
}

// Create a custom comparator function for sorting
function taskComparator(a, b) {
    const dateA = getDueDate(a);
    const dateB = getDueDate(b);
    const priorityA = getPriority(a);
    const priorityB = getPriority(b);
    
    // First sort by date
    if (dateA && dateB) {
        const dateComparison = dateA.ts - dateB.ts;
        if (dateComparison !== 0) return dateComparison;
    } else if (dateA && !dateB) {
        return -1; // Tasks with dates come first
    } else if (!dateA && dateB) {
        return 1; // Tasks with dates come first
    }
    
    // Then sort by priority
    const priorityOrderA = priorityOrder[priorityA] || priorityOrder[""];
    const priorityOrderB = priorityOrder[priorityB] || priorityOrder[""];
    
    return priorityOrderA - priorityOrderB;
}

// Sort tasks using Dataview's sort method with custom comparator
const sortedTasks = tasks.sort(t => t, "asc", taskComparator);

// Display the sorted tasks in a table format
const tableData = sortedTasks.map((task, index) => {
    return [
        index + 1,                           // Index (1-based)
        cleanTaskText(task),                 // Task text (cleaned)
        getPriority(task) || "None",         // Priority
        getDueDate(task) || ""               // Due Date
    ];
});

dv.table(["Index", "Task", "Priority", "Due Date"], tableData);
```

## Tasks

- [ ] Get on a call with Josef to discuss the following: [Priority:: Urgent] [Due:: 2025-10-22]
    - [ ] Write out what we want to discuss in the meeting [Priority:: Urgent] #Focus 
    - [ ] Should the whole organization be considered sponsored if it is just the department that is sponsored.
    - [ ] Get on a call with Josef to discuss this issue. Some of the entries in Josef's list were not found in the database. Asking Josef if these entries should be a department of an organization or an organization itself.
    - [ ] He wants confirmation that the mapping is correct before committing to it: ![[Attachments/Pasted image 20251022140943.png]]
- [ ] Create task for ensuring that Omnicia deployment is successful
- [ ] Double check the notes and send bulk email about the notes https://deltadesk.slack.com/archives/C08A20K9M4H/p1761148282210199
    - [ ] Double check
    - [ ] Send email

---

- [ ] Perform reviews [Priority:: High]
- [ ] ClickUp Notifications
    - [x] 1-4
    - [x] Complete 2 notifications [Completed:: 2025-10-22T13:36]
- [ ] Emails
    - [x] Complete 6 emails [Completed:: 2025-10-22T12:11]
    - [x] Create tickets like Josh requested [Completed:: 2025-10-22T13:59]
        - [x] Lakeshore | DDOS/DLIT spx options trading: | Visdom ref: 20251022 1236.1
        - [x] 2
        - [x] 3
- [ ] Slack
    - [ ] 7
        - [x] Complete 1-4 [Completed:: 2025-10-22T13:35]

### Closed

- [x] Meeting with Madeline and Zabelle [Due:: 2025-10-22T15:00] [Priority:: High]
    - [x] Prep materials for meeting  [Priority:: Urgent] [Completed:: 2025-10-22T14:43]
- [x] Respond to Omnicia [Priority:: High]
- [x] Have call with Kevin [Completed:: 2025-10-22]
- [x] Send Kevin email about the API key [Completed:: 2025-10-22T16:35]
- [x] Add NSDFC database username and password to 1Password -> Dominik Read Only SQL User [Priority:: Low] [Completed:: 2025-10-22T15:48]
- [x] Get other examples for Zulqarnain and Bao for the note reply UI [Priority:: Medium] 
- [x] Visit the "SnapShooter" site to see if backups have been made [Completed:: 2025-10-22T11:52]
- [x] Close tasks for backing up data [Completed:: 2025-10-22T11:52]
- [x] Close the ClickUp task related to Omnicia [Completed:: 2025-10-22T11:43]
- [x] Send email to Omnicia about the files [Due:: 2025-10-22] [Priority:: Urgent] [Completed:: 2025-10-22T11:41]

- [x] Add info about dropdowns that need added: https://app.clickup.com/t/86aby8dwn [Priority:: High]