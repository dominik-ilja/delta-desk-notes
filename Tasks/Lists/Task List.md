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



## General

- [ ] Create templates for asking developers for updates
- [ ] Review the project for Aiden
- [ ] Syncing developer work with ClickUp
- [ ] Project timelines and estimates
- [ ] Talk to developers about how they're using Git
- [ ] How to properly do different development environments
- [ ] Automate setting of custom fields
- [ ] I'm thinking that the "Ready for Deployment" status should be an "In Progress" status rather than a "Done". The reasoning is that there's still more work to be done.
- [ ] Get access to V0
- [ ] [86ac1fqtv – Subtotaling premiums on the website | to do | Josh Jennings](https://app.clickup.com/t/86ac1fqtv), [86ac1ft8x – Automate the price input process | to do | Josh Jennings](https://app.clickup.com/t/86ac1ft8x) - These tasks also apply to the OMS and Visdom not just Carrick Lane.
- [ ] Tell developers what the "Needs Internal Review" attribute means

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
- [x] How to filter out specific entries in ClickUp so that clients don't see them
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
- [ ] Reach out to Rob Regan about the Infinity search button


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

- [ ] Follow-up with NSDFC about this task: https://app.clickup.com/t/86acgv7pc?comment=90130179931669&threadedComment=90130181300273 [Priority:: High]
- [ ] If a salesperson is not assigned, then our team, Natalie, and Josef will get notified of the call. #Document
- [ ] Should the whole organization be considered sponsored if it is just the department that is sponsored.
- [ ] Get on a call with Josef to discuss this issue. Some of the entries in Josef's list were not found in the database. Asking Josef if these entries should be a department of an organization or an organization itself.
- [ ] He wants confirmation that the mapping is correct before committing to it: https://files.slack.com/files-pri/T05CBUR61FV-F09MKQDGTEU/image.png
- [ ] Remove unneeded filters
- [ ] Adding hash for contact files page, so you can refresh and stay on the same tab you were on
- [ ] Contact ID 10066 has messed up balances
- [ ] Should a sponsor be the whole organization if it is just the department that is sponsored?
- [ ] What automations do we have happening within the system?
- [ ] File type of "Student Loan File" should be "FSA Text File"
- [ ] Notifications for the Incoming calls should not disappear while the call is inbound. If a call is missed, then it should disappear after a couple minutes.
- [ ] [[Tasks/Completed/2025/Task - UI & UX enhancements]] ^cyvu77
---
- [ ] Setup meetings with NSDFC for maintenance meetings [Priority:: High]
- [ ] Demo for application. Schedule for next week [Priority:: High]
- [ ] Look into what Blue Rock is: https://app.clickup.com/t/86ac3x9qq [Priority:: High]
- [ ] Figure out what different services they provide [Priority:: Medium]
- [ ] Add process for sending update reports. Should be sent to Josef, Natalie, and Kathleen [Priority:: Low]
- [ ] Do we need to add the permission to see the servicer password? Who should get these permissions? - Send to client #Todo  
- [ ] If a salesperson is not assigned, then our team, Natalie, and Josef will get notified of the call. #Document
- [ ] Create task to specify that forms should not be edited if they are not in a status of "Generated"
- [ ] Task fix recertification Contact > Recertification tab

### Orical



## Projects
### OMS

- [ ] Column resizing is resizing every column
- [ ] Spell out "Electronic Communication Approved"
- [ ] Should be live by the end of October