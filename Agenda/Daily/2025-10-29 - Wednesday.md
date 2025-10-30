---
Complete: false
Tasks: 27
Tasks Remaining: 18
Tasks Complete: 9
Date Completed:
Last Updated: October 29, 2025, at 10:54 AM
File Size: 5.88 KB
aliases: []
cssclasses:
  - full_width
tags: []
Related:
  - "[[/Notes/Daily/2025-10-29 - Wednesday]]"
---
# Wednesday, October 29, 2025

[[/Agenda/Yearly/2025|2025]] ❯ [[/Agenda/Quarterly/2025 - Q4|Q4]] ❯ [[/Agenda/Monthly/2025 - October|October]] ❯ [[/Agenda/Weekly/2025 - Week 44|Week 44]]

❮ [[/Agenda/Daily/2025-10-28 - Tuesday|Tuesday, October 28, 2025]] · Wednesday, October 29, 2025 · [[/Agenda/Daily/2025-10-30 - Thursday|Thursday, October 30, 2025]] ❯

## Tasks

[[Task List]] · [[Tasks/Lists/Question List|Question List]] · [[Sushchnosti/Delta Desk/Meetings/Josh Jennings Meetings|Josh Jennings Meetings]]

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

- [x] Reach out to girls at Orical [Priority:: Urgent] [Completed:: 2025-10-29T08:20]
- [x] Reach out to Vu about the Orical work [Priority:: Urgent] [Completed:: 2025-10-29T08:22]
- [ ] Review the tasks that are in internal review [Priority:: Urgent]

- [ ] Attend to ClickUp tasks
- [ ] Attend to Slack messages
- [ ] Attend to Slack saved messages
- [ ] Attend to email: 9 -> 
- [ ] Review tasks
- [ ] Create tasks
- [ ] Communicate with developers
    - [ ] Bao
    - [ ] Mikhail
    - [ ] Mostofa
    - [x] Vu
    - [ ] Zulqarnain

- [ ] Tasks to review: 7
    - [ ] [86acvtpdm – Frontend part | internal review | Zulqarnain Niazi](https://app.clickup.com/t/86acvtpdm)
    - [ ] [86acq5tdv – Improve Send For E-Signature logic | internal review | Zulqarnain Niazi](https://app.clickup.com/t/86acq5tdv)
    - [ ] [86actnyn3 – Send Recert payment email for recert payment instead of normal email | internal review | Bao Do Van](https://app.clickup.com/t/86actnyn3)
    - [ ] [86achu6me – Adjust Contract Received logic | internal review | Bao Do Van](https://app.clickup.com/t/86achu6me)
    - [ ] [86ace9164 – 3rd party authorization form (UFT004785  Tashawna Praddy) | internal review | Bao Do Van](https://app.clickup.com/t/86ace9164)
    - [x] [86acmdaw6 – Remove email automation that occurs after a new FSA text file is uploaded to the CRM | internal review | Bao Do Van](https://app.clickup.com/t/86acmdaw6) [Completed:: 2025-10-29T10:48]
    - [x] [86acq9w1k – Handle SSNs in database | internal review | Bao Do Van, Mikhail](https://app.clickup.com/t/86acq9w1k) [Completed:: 2025-10-29T09:07]

Event Title
Event Category
Description
Gallery of photos
Audio
Date with an optional time
Location
Tags

Data Dictionary is a spreadsheet which contains all the tables and fields for the tables. My number 1 job is to make sure the clients are being serviced at a high-level.

Josh found a bunch of payments in the Old CRM. He scheduled an extra 100 payments for tomorrow. How many of them got reminders?

### Complete

- [x] Attend to ClickUp notifications: 6-> 0
- [x] Attend to Teams messages
- [x] Setup tasks [Completed:: 2025-10-29T07:33]
- [x] Let the developers know I'm online in the morning