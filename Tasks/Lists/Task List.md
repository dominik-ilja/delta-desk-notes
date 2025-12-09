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

Project priority:

- NEOS
- OMS
- FIN Searches
- Our site
- NSDFC
- Aiden

## Due
### Tasks

```base
views:
  - type: table
    name: Table
    filters:
      and:
        - '!note["Due Date"].isEmpty()'
        - Complete != true
    order:
      - file.name
      - Due Date
      - Complete
    sort:
      - property: Due Date
        direction: ASC
    columnSize:
      file.name: 474
      note.Due Date: 202

```

### Individual Tasks
```dataviewjs
const tasks = dv.pages()
  .file.tasks
  .where(t => !t.completed && t.Due)
  .sort(t => t.Due, 'asc');

const today = dv.date("today");
const overdueTasks = tasks.where(t => t.Due < today);
const todayTasks = tasks.where(t => {
    console.log(t)
    return t.Due.equals(today)
});
const futureTasks = tasks.where(t => t.Due > today);
const headers = ["File", "Due Date", "Task"];
const headingLevel = 3;

console.log(overdueTasks, todayTasks, futureTasks)

function createRow(task) {
    return [
        task.blockId 
            ? dv.blockLink(task.path, task.blockId)
            : dv.fileLink(task.path),
        task.Due,
        task.text
            .replace(/\[Priority::\s*[^\]]+\]/g, '')
            .replace(/\[Due::\s*[^\]]+\]/g, '')
            .replace(/\s+/g, ' ')
            .trim(),
    ];
}

if (overdueTasks.length > 0) {
  dv.header(headingLevel, "Overdue");
  dv.table(
    headers,
    overdueTasks.map(createRow)
  );
}

if (todayTasks.length > 0) {
  dv.header(headingLevel, "Due Today");
  dv.table(
    headers,
    todayTasks.map(createRow)
  );
}

if (futureTasks.length > 0) {
  dv.header(headingLevel, "Upcoming");
  dv.table(
    headers,
    futureTasks.map(createRow)
  );
}

if (tasks.length === 0) {
  dv.paragraph("No tasks with due dates found.", {cls: "placeholder"});
}
```

## Agenda

```base
views:
  - type: table
    name: Table
    filters:
      and:
        - file.path.startsWith("Agenda/Daily")
    order:
      - file.name
      - Complete
      - Tasks Remaining
      - Tasks Complete
      - Tasks
      - File Size
    sort:
      - property: file.name
        direction: DESC
    limit: 7
    columnSize:
      file.name: 249
      note.File Size: 103

```

## Focus

```dataviewjs
const tasks = dv.pages()
    .file
    .tasks
    .where(t => !t.completed && t.text.includes("#Focus"))

dv.taskList(tasks)
```

## Priority

```dataviewjs
(() => {
// Get tasks from the current file
const file = app.workspace.getActiveFile();
if (!file) return;

const hideCompletedSubtasks = (task) => {
    return {
        ...task,
        children: task.children
            .filter((subtask) => subtask.task && !subtask.fullyCompleted)
            .map(hideCompletedSubtasks)
    }
}

const tasks = dv.page(file.path).file.tasks.where(task => !task.fullyCompleted);
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
})()
```

## General



- [ ] Create documentation about how the podcasts are being done for Passaic Partners: 

---

- [ ] Create templates for asking developers for updates
- [ ] Syncing developer work with ClickUp
- [ ] Project timelines and estimates
- [ ] Talk to developers about how they're using Git
- [ ] How to properly do different development environments
- [ ] Automate setting of custom fields
- [ ] I'm thinking that the "Ready for Deployment" status should be an "In Progress" status rather than a "Done". The reasoning is that there's still more work to be done.
- [ ] Get access to V0
- [ ] [86ac1fqtv – Subtotaling premiums on the website | to do | Josh Jennings](https://app.clickup.com/t/86ac1fqtv), [86ac1ft8x – Automate the price input process | to do | Josh Jennings](https://app.clickup.com/t/86ac1ft8x) - These tasks also apply to the OMS and Visdom not just Carrick Lane.

- [ ] Things to learn about:
    - [ ] Learn about options
        - [ ] XSP/SPX - Size of options
        - [ ] What are "futures" in regards to options?
    - [ ] What is an RIA? Is it a registered investment agent?
    - [ ] MCP Server
    - [ ] What is our process for doing security ratings?

- [ ] Standardize how we do components
    - [ ] Table
        - [ ] Table columns should have a min-width to show all controls
        - [ ] Remove pagination if all the rows are being shown

- [ ] [[Tasks/Backlog/Task - Create system for sharing work with clients]] [Priority:: High]
- [ ] Figure out how to answer these questions [Priority:: High]
    - [ ] "What are the developers working on?"
    - [ ] "What are the developers working on today?"
    - [ ] "What tasks need to be reviewed by me?"
    - [ ] "What are the overarching projects that we are working on?" 
- [ ] How am I going to keep track of the work completed in the week for a client? [Priority:: High]
- [ ] How will I keep track of what each individual developer is working on [Priority:: High]

- [ ] [[Tasks/Backlog/Task - Review Notion|Task - Review Notion]] [Priority:: Medium]
- [ ] [[Tasks/Backlog/Task - Figure out how to manage different schedules of each developer]] [Priority:: Medium]
- [ ] [[Tasks/Backlog/Task - Creating assets to share with clients for project progress]] [Priority:: Medium]
- [ ] How to see if ClickUp task is private or not? [Priority:: Medium]

- [ ] Josh will add me to his different subscriptions: Figma, V0, etc. [Priority:: Low]

- [ ] Create documentation on how email signature should be done [Priority:: None]

- [ ] Look into these shirts: https://www.charlestyrwhitt.com/us/mens-shirts/classic-fit+slim-fit/?prefn1=iron&prefv1=Yes&ppr=4&tib=TIB-text-shirts-ss23&isFiltersHidden=false
- [ ] Get professional headshots taken
- [ ] How could we sync GitHub commits with ClickUp tasks
- [ ] How could we start to standardize our components?
    - [ ] What makes a good table?
- [ ] Get access to the NSDFC Delta Desk Documents

## Groups
### Aiden



### Carrick Lane

- [ ] Go through the tickets that were added by Andrew [Priority:: High]

### Delta Desk

- [ ] Add notes about Zoom login and email [Priority:: Low]
- [ ] Bao would like me to review things another time when it is in production [Priority:: Low]

### FIN Searches

- [ ] [86adb3jyf - Form D automated report of new filings - to do (FIN Searches - External Issue Submissions)](https://app.clickup.com/t/86adb3jyf) - Get information for Bao and Mikhail on this task. [Priority:: Urgent]
- [ ] [86ade11z2 - remove about section from specific mandates - to do (FIN Searches - External Issue Submissions)](https://app.clickup.com/t/86ade11z2) - Get information for Mikhail on this task. [Priority:: Urgent]

---

- [ ] Look into how we can take advantage of screen spacing at smaller sizes
- [ ] Terms to learn:
    - [ ] Private equity
    - [ ] Private equity manager
    - [ ] Allocators
    - [ ] Basis points
    - [ ] Mandates
    - [ ] What is a firm?
    - [ ] Asset class
    - [ ] What is a plan?
    - [ ] What is a major/minor strategy?
    - [ ] What does AuM stand for? - Assets under Management
    - [ ] Institutional private wealth
- [ ] Documentation
    - [ ] RFP - Request for Proposal
- [ ] `consultant-details/{id}` not filtering properly when he searched for "Denver"
- [ ] Clearing chat/chat history/starting a new chat

### NSDFC

- Main focuses
    - Recertifications
    - Making the application have more guardrails to prevent bad data
    - Simplifying the user experience
    - Fixing existing data
    - Documenting how the software works
    - Data integrity
    - Data conversion issues
    - Allowing users to do things so we don't have do them

---
- [ ] Follow-up with NSDFC about this task: https://app.clickup.com/t/86acgv7pc?comment=90130179931669&threadedComment=90130181300273 [Priority:: High]
- [ ] If a salesperson is not assigned, then our team, Natalie, and Josef will get notified of the call. #Document
- [ ] Remove unneeded filters
- [ ] Adding hash for contact files page, so you can refresh and stay on the same tab you were on
- [ ] Contact ID 10066 has messed up balances
- [ ] Should a sponsor be the whole organization if it is just the department that is sponsored?
- [ ] What automations do we have happening within the system?
- [ ] Notifications for the Incoming calls should not disappear while the call is inbound. If a call is missed, then it should disappear after a couple minutes.
---
- [ ] Setup meetings with NSDFC for maintenance meetings [Priority:: High]
- [ ] Demo for application. Schedule for next week [Priority:: High]
- [ ] Do we need to add the permission to see the servicer password? Who should get these permissions? - Send to client #Todo  
- [ ] If a salesperson is not assigned, then our team, Natalie, and Josef will get notified of the call. #Document
- [ ] Task fix recertification Contact > Recertification tab

### Orical

<span class="placeholder">No tasks</span>

## ✓ Projects
### ✓ OMS

<span class="placeholder">No tasks</span>
