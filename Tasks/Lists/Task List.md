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

## Spillover

<span class="placeholder">No tasks</span>

## General

- [x] Add everything to our task list [Priority:: Urgent] [Completed:: 2025-09-25T14:18]
- [ ] Go through remaining notes and capture anything else we might need #Focus
- [ ] Go through and update the "Internal review needed" attributes before developers really start looking at them [Priority:: Urgent] #ClickUp 
---
- [ ] Create system for sharing work with clients [Priority:: High]
- [ ] Review Figma designs and give Josh feedback [Priority:: High] [Due:: 2025-09-26] #ClickUp 
- [ ] Review what Zulqarnain sent [Priority:: High]
- [ ] Add tasks to Vu's task for the admin permissions to show him how I'd like it done [Priority:: High]
- [ ] Figure out how to answer these questions [Priority:: High]
    - [ ] "What are the developers working on?"
    - [ ] "What are the developers working on today?"
    - [ ] "What tasks need to be reviewed by me?"
    - [ ] "What are the overarching projects that we are working on?" 
- [ ] How am I going to keep track of the work completed in the week for a client? [Priority:: High]
- [ ] How will I keep track of what each individual developer is working on [Priority:: High]
---
- [ ] [[Tasks/Backlog/Task - Look into having an attribute for determining who should review the code|Task - Look into having an attribute for determining who should review the code]] [Priority:: Medium]
- [ ] [[Tasks/Backlog/Task - Review Notion|Task - Review Notion]] [Priority:: Medium] #ClickUp 
- [ ] Figure out how to manage different schedules of each developer [Priority:: Medium]
- [ ] Create a Dataview script for displaying the tasks in this file sorted by due date then priority [Priority:: Medium]
- [ ] [[Tasks/Backlog/Task - Creating assets to share with clients for project progress]] [Priority:: Medium] #ClickUp 
- [ ] How to see if ClickUp task is private or not? [Priority:: Medium]
- [ ] Get OBS on computer for recording meetings [Priority:: Medium]
- [x] Create additional templates for Low, Medium, High, and Urgent priorities [Priority:: Medium] [Completed:: 2025-09-25T11:52]
---
- [ ] Josh will add me to his different subscriptions: Figma, V0, etc. [Priority:: Low]
---
- [ ] Create documentation on how email signature should be done [Priority:: None]

## Groups
### Carrick Lane

- [ ] Luke's spreadsheet for Carrick Lane? [Priority:: Medium] #ClickUp 

### Delta Desk

- [ ] Remove Luke from admin on SendGrid [Priority:: Urgent] #ClickUp 
- [ ] Figure out what the difference is between private/blob in the azure [Priority:: Urgent]
---
- [ ] We currently have two Google Accounts. One is the corporate account and the other is under "support@deltadesk.com". There's things tied to the support account which Luke made. We need to make sure that is taken care of. Josh would like this done before he gets Luke's laptop. [Priority:: High]
---
- [ ] Josh mentioned getting a credit card for me [Priority:: Low]
- [ ] General phone number for Delta Desk. We could potentially get a virtual PBX and calls can be routed between Josh and I depending on the hours [Priority:: Low]
- [ ] Create website to monitor different jobs we have. We would have an internal site that would contain all the jobs across all the different projects and sites for the jobs of individuals clients or projects [Priority:: Low]
- [ ] Create list of Delta Desk expectations. Include this in our daily tasks [Priority:: Low]
- [ ] Need to give Mikhail another Virtual Machine for automating button clicks for client [Priority:: High] #ClickUp 
    - [ ] What client also needs automated? I believe the two clients are Carrick Lane and Visdom #Question
---


### FIN Searches

- [ ] Need to do internal reviews, so that deployment can be pushed [Priority:: Urgent]
- [ ] Get the development environment from Bao to show them during our meeting [Priority:: Urgent] [Due:: 2025-09-26]
- [ ] Adjust meeting time for FIN on Friday [Priority:: Urgent] [Due:: 2025-09-25]
    - [ ] Who should have control of the reoccurring meeting.
    - [ ] Re
- [ ] Demo for application. Schedule for next week [Priority:: High]

### NEOS

- [ ] Make sure NEOS files are private  [Priority:: Urgent] #ClickUp 

### NSDFC

- [ ] In the notifications page, if we don't have a start or end date, the filter doesn't display anything [Priority:: High] #ClickUp 
- [ ] Setup meetings with NSDFC for maintenance meetings [Priority:: High]
- [ ] Need to document how the different plans should be done. For example, consolidations can't be charged until the work is done while recertifications can be charged immediately. [Priority:: High] #ClickUp 
- [ ] Demo for application. Schedule for next week [Priority:: High]
---
- [ ] Add task for UI enhancements
    - [ ] Hide estimated payments if there are none [Priority:: Medium]
    - [ ] Add cards for recertifications to show outstanding balances [Priority:: Medium] #ClickUp 
    - [ ] When sending an email, keep the action buttons always visible and only add a scrollbar once you've hit the full height #ClickUp 
    - [ ] Add two action buttons in header: #ClickUp 
        - [ ] Send email with email icon #ClickUp 
        - [ ] Send SMS with icon #ClickUp 
- [ ] Create task for adding permissions page for NSDFC if it doesn't exist [Priority:: Medium]
---
- [ ] Ask Zulqarnain what would need to be done to add highlighting to sending emails [Priority:: Low]

### Orical

<span class="placeholder">No tasks</span>

## Projects
### OMS

<span class="placeholder">No tasks</span>