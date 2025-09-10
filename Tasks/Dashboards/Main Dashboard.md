---
aliases:
cssclasses:
  - full_width
tags:
Related:
  - "[[Complete Dashboard]]"
  - "[[Task List]]"
Sources: []
Type: Dashboard
---
# Main Dashboard
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
const todayTasks = tasks.where(t => t.Due.equals(today));
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
        task.text.replace(/\[[^\]]+\]\s*/gi, ""),
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
  dv.paragraph("No tasks with due dates found.");
}
```

### To Contact

```base
formulas:
  Last Contacted: |-
    (today() - note["Last Contacted"])
        .days
        .floor()
        .toString() +
    if(
      (note["Next Contact"] - today()).days < 0, 
      " (" + 
      (note["Next Contact"] - today())
          .days
          .abs()
          .toString() + 
      " days overdue)",
      ""
    )
properties:
  formula.Last Contacted:
    displayName: Days Since
views:
  - type: table
    name: Table
    filters:
      and:
        - note["Next Contact"] <= now()
    order:
      - file.name
      - Next Contact
      - Last Contacted
      - Last Response
      - formula.Last Contacted
      - Contact Frequency
    sort:
      - property: formula.Last Contacted
        direction: DESC
      - property: Next Contact
        direction: ASC
    columnSize:
      file.name: 178

```

## Tasks

[[Task List]]

```base
filters:
  and:
    - '!file.path.startsWith("Templates")'
formulas:
  Untitled: ""
properties:
  file.name:
    displayName: Name
  file.ctime:
    displayName: Created Time
views:
  - type: table
    name: Focus
    filters:
      and:
        - "!Tasks.isEmpty()"
        - '!note["Tasks Complete"].isEmpty()'
        - '!note["Tasks Remaining"].isEmpty()'
        - Complete == false
        - tags.contains("Focus")
    order:
      - file.name
      - Order
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Tasks Remaining
      - Tasks Complete
      - Tasks
      - Type
      - tags
    sort:
      - property: Priority
        direction: DESC
      - property: Order
        direction: ASC
    columnSize:
      file.name: 453
      note.Status: 108
      note.State: 114
      note.Priority: 103
      note.Life Category: 378
  - type: table
    name: All
    filters:
      and:
        - "!Tasks.isEmpty()"
        - '!note["Tasks Complete"].isEmpty()'
        - '!note["Tasks Remaining"].isEmpty()'
        - Complete == false
        - '!file.path.startsWith("RuneScape")'
    order:
      - file.name
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Tasks Remaining
      - Tasks Complete
      - Tasks
      - Order
      - tags
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: file.name
        direction: ASC
      - property: Priority
        direction: DESC
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    columnSize:
      file.name: 451
      note.Status: 108
      note.State: 114
      note.Priority: 103
      note.Life Category: 210
  - type: table
    name: Agenda
    filters:
      and:
        - "!Tasks.isEmpty()"
        - '!note["Tasks Complete"].isEmpty()'
        - '!note["Tasks Remaining"].isEmpty()'
        - Complete == false
        - file.path.startsWith("Agenda")
    order:
      - file.name
      - Complete
      - Tasks Remaining
      - Tasks Complete
      - Tasks
      - Order
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: file.name
        direction: DESC
      - property: Order
        direction: ASC
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    columnSize:
      file.name: 234
      note.Status: 108
      note.State: 114
      note.Priority: 103
      note.Life Category: 210
```

### Agenda

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
    limit: 14
    columnSize:
      file.name: 249
      note.File Size: 103

```

### Archived

```base
views:
  - type: table
    name: Archived
    filters:
      or:
        - Status == "3 - Archived"
        - file.path.startsWith("Tasks/Archive")
    order:
      - file.name
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Order
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: Complete
        direction: ASC
      - property: file.name
        direction: ASC
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    limit: 10
    columnSize: {}

```

### Completed

```base
filters:
  and:
    - Complete == true
    - Status != "4 - Dismissed"
    - '!note["Date Completed"].isEmpty()'
views:
  - type: table
    name: Complete
    order:
      - file.name
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Order
      - Date Completed
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: Date Completed
        direction: DESC
    limit: 10
    columnSize: {}
  - type: table
    name: "2025"
    filters:
      and:
        - Complete == true
        - '!note["Date Completed"].isEmpty()'
    order:
      - file.name
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Order
      - Date Completed
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    columnSize: {}
  - type: table
    name: "2024"
    filters:
      and:
        - Complete == true
        - note["Date Completed"] <= "2024-12-31"
        - note["Date Completed"] >= "2024-01-01"
    order:
      - file.name
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Order
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    columnSize: {}
  - type: table
    name: "2023"
    filters:
      and:
        - note["Date Completed"] == "2025-06-12"
    order:
      - file.name
      - Date Completed
      - Life Category
      - Complete
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: file.folder
        direction: DESC
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    columnSize:
      note.Type: 103

```

### Dismissed

```base
views:
  - type: table
    name: Dismissed
    filters:
      and:
        - Status == "4 - Dismissed"
    order:
      - file.name
      - Status
      - State
      - Priority
      - Life Category
      - Complete
      - Order
      - file.size
      - file.mtime
      - file.ctime
      - file.folder
      - Type
    sort:
      - property: file.name
        direction: ASC
      - property: property.Status
        direction: DESC
      - property: property.Priority
        direction: DESC
    limit: 10
    columnSize: {}

```

## Contacts

![[Contacts.base]]

## Last Updated

```base
views:
  - type: table
    name: Table
    order:
      - file.name
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
    limit: 30
    columnSize:
      file.name: 416

```

