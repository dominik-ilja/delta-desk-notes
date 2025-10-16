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

## To Review



## Spillover

<span class="placeholder">No tasks</span>

## General

**Urgent:**

<span class="placeholder">No tasks</span>

**High:**

- [ ] [[Tasks/Backlog/Task - Create system for sharing work with clients]] [Priority:: High]
- [ ] Figure out how to answer these questions [Priority:: High]
    - [ ] "What are the developers working on?"
    - [ ] "What are the developers working on today?"
    - [ ] "What tasks need to be reviewed by me?"
    - [ ] "What are the overarching projects that we are working on?" 
- [ ] How am I going to keep track of the work completed in the week for a client? [Priority:: High]
- [ ] How will I keep track of what each individual developer is working on [Priority:: High]

**Medium:**

- [ ] [[Tasks/Backlog/Task - Review Notion|Task - Review Notion]] [Priority:: Medium]
- [ ] [[Tasks/Backlog/Task - Figure out how to manage different schedules of each developer]] [Priority:: Medium]
- [ ] [[Tasks/Backlog/Task - Creating assets to share with clients for project progress]] [Priority:: Medium]
- [ ] How to see if ClickUp task is private or not? [Priority:: Medium]

**Low:**

- [ ] Josh will add me to his different subscriptions: Figma, V0, etc. [Priority:: Low]

**None:**

- [ ] Create documentation on how email signature should be done
- [ ] Move documentation from ClickUp into Obsidian
    - [x] Dominik's space [Completed:: 2025-09-30T19:25]
    - [x] Delta Desk [Completed:: 2025-09-30]
        - [x] Delta Desk - Wiki [Completed:: 2025-09-30]
        - [x] Project Management [Completed:: 2025-09-30T19:45]
        - [x] Software [Completed:: 2025-09-30T19:45]
    - [x] FIN Searches - Wiki [Completed:: 2025-09-30T19:50]
    - [ ] NSDFC - Wiki
- [ ] We need to figure out a way to see what ClickUp items
- [ ] Look into these shirts: https://www.charlestyrwhitt.com/us/mens-shirts/classic-fit+slim-fit/?prefn1=iron&prefv1=Yes&ppr=4&tib=TIB-text-shirts-ss23&isFiltersHidden=false
- [ ] Get professional headshots taken
- [ ] How could we sync GitHub commits with ClickUp tasks
- [ ] How could we start to standardize our components?
    - [ ] What makes a good table?
- [ ] Access to Fireflies
- [ ] Updates to healthcare plan
- [ ] Generate templates for ClickUp
    - [ ] List View
    - [ ] List
    - [ ] Folder
    - [ ] Space
- [ ] How to filter out specific entries in ClickUp so that clients don't see them
- [ ] Get access to the NSDFC Delta Desk Documents

## Groups
### Carrick Lane

<span class="placeholder">No tasks</span>

### Delta Desk

**Urgent:**

<span class="placeholder">No tasks</span>

**High:**

<span class="placeholder">No tasks</span>


**Medium:**

<span class="placeholder">No tasks</span>

**Low:**

- [ ] Add notes about Zoom login and email [Priority:: Low]
- [ ] Bao would like me to review things another time when it is in production [Priority:: Low]

**None:**

<span class="placeholder">No tasks</span>

### FIN Searches

- [ ] Look into how we can take advantage of screen spacing at smaller sizes


**Urgent:**

<span class="placeholder">No tasks</span>


**High:**

<span class="placeholder">No tasks</span>

**Medium:**

<span class="placeholder">No tasks</span>

**Low:**
- [ ] Add process for sending update reports. Should be sent to Gar Chung, Gene Dilinsky, and Rob Regan [Priority:: Low]

**None:**

<span class="placeholder">No tasks</span>


### NEOS

**Urgent:**

<span class="placeholder">No tasks</span>

**High:**

<span class="placeholder">No tasks</span>

**Medium:**

<span class="placeholder">No tasks</span>

**Low:**

<span class="placeholder">No tasks</span>

**None:**

<span class="placeholder">No tasks</span>


### NSDFC

**Urgent:**

<span class="placeholder">No tasks</span>

**High:**

- [ ] Setup meetings with NSDFC for maintenance meetings [Priority:: High]
- [ ] Demo for application. Schedule for next week [Priority:: High]
- [ ] Look into what Blue Rock is: https://app.clickup.com/t/86ac3x9qq [Priority:: High]

**Medium:**

- [ ] [[Tasks/Backlog/Task - UI & UX enhancements]] ^cyvu77
- [ ] Figure out what different services they provide [Priority:: Medium]

**Low:**

- [ ] Add process for sending update reports. Should be sent to Josef, Natalie, and Kathleen [Priority:: Low]

**None:**

- [ ] Add info about dropdowns that need added: https://app.clickup.com/t/86aby8dwn [Priority:: High]
### Orical

**Urgent:**

<span class="placeholder">No tasks</span>

**High:**

<span class="placeholder">No tasks</span>

**Medium:**

<span class="placeholder">No tasks</span>

**Low:**

<span class="placeholder">No tasks</span>

**None:**

<span class="placeholder">No tasks</span>

## Projects
### OMS

**Urgent:**

<span class="placeholder">No tasks</span>

**High:**

<span class="placeholder">No tasks</span>

**Medium:**

<span class="placeholder">No tasks</span>

**Low:**

<span class="placeholder">No tasks</span>

**None:**

<span class="placeholder">No tasks</span>