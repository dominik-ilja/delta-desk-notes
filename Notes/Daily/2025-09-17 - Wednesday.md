---
aliases: []
cssclasses: []
tags: []
Related:
  - "[[/Agenda/Daily/2025-09-17 - Wednesday]]"
Complete: true
Tasks: 2
Tasks Remaining: 0
Tasks Complete: 2
Date Completed: 2025-09-18
---
# Wednesday, September 17, 2025

[[/Notes/Yearly/2025|2025]] ❯ [[/Notes/Quarterly/2025 - Q3|Q3]] ❯ [[/Notes/Monthly/2025 - September|September]] ❯ [[/Notes/Weekly/2025 - Week 38|Week 38]]

❮ [[/Notes/Daily/2025-09-16 - Tuesday|Tuesday, September 16, 2025]] · Wednesday, September 17, 2025 · [[/Notes/Daily/2025-09-18 - Thursday|Thursday, September 18, 2025]] ❯

<time>6:50</time>
Okay, so my main tasks right now are:

- Go through email
    - Respond to emails
    - Add requirements
    - Check if there's any tasks we moved to Tasks
    - Check emails with "Task" tag
- Go through Slack
    - Respond to messages
    - Go through saved messages
    - Check client channels
- Go through Teams
    - Respond to messages
    - Look for meetings
- Go through ClickUp
    - Respond to comments
    - Review tasks that are in "Internal QA"
    - Create additional tasks
- Assign tasks to developers
- Think of how we can improve are project management

<time>6:55</time>
Okay, let's go ahead and work through these tasks. Let me spend 30 minutes responding to the developers. We'll move onto other tasks at 7:30 AM.

==During meetings we can record and I can make references to timestamps during the meeting==

<time>7:00</time>
Actually, I'm going to go through emails first.

- [x] [[Agenda/Daily/2025-09-17 - Wednesday#^u30fcr]]

<time>7:09</time>
Here are some template rules for clients: ^oqj9d3

- {{Client}} - Move emails sent to {{Receiver}} to matching folder
    - Add a condition:
        - Recipient address includes: @{{Client Extension}}
    - Add an action:
        - Move to: {{Client Folder}}
- {{Client}} - Move emails received from {{Sender}} to matching folder
    - Add a condition:
        - Sender address includes: @{{Client Extension}}
    - Add an action:
        - Move to: {{Client Folder}}

<time>7:30</time>
Okay, there's still a lot of shit that needs to get done with this. We're going to do this:

- Go through all of the emails currently in tasks
- Make a ClickUp task if it hasn't already been added

<time>7:39</time>
Okay, I've gone through and cleaned up the emails. Now, I just need to add the tasks to ClickUp.

The following is from an email from Luke:

---

**TASKS**  
A) Deleting old Leadtrac “Appointments” that were actually just tasks and reminders to themselves  
[https://app.clickup.com/t/86abw9nb3](https://app.clickup.com/t/86abw9nb3 "https://app.clickup.com/t/86abw9nb3")  
I think this one will need a little planning to decide which records from Appointments table to delete. I have made my suggestion in the ClickUp task.  
B) Default to showing tasks due today on Tasks page  
[https://app.clickup.com/t/86abw9rjb](https://app.clickup.com/t/86abw9rjb "https://app.clickup.com/t/86abw9rjb")   ^uyailx
  
**CONTRACT RECEIVED REPORT**  
Add Organization to Contract Received Report  
[https://app.clickup.com/t/86abw9t2u](https://app.clickup.com/t/86abw9t2u "https://app.clickup.com/t/86abw9t2u")  
  
**GRADUATED PAYMENT PLAN  
**Added to Needs Planning (unassigned)  
[https://app.clickup.com/t/86abv6bkm](https://app.clickup.com/t/86abv6bkm "https://app.clickup.com/t/86abv6bkm")  
  
**APPOINTMENT SCHEDULING**  
Added to Needs Planning (unassigned)  
[https://app.clickup.com/t/86abw9w7m](https://app.clickup.com/t/86abw9w7m "https://app.clickup.com/t/86abw9w7m")  
  
**PIPELINE REPORTS**  
Adding the SalesPerson filter. Currently assigned to Vu.  
[https://app.clickup.com/t/86abt10yv](https://app.clickup.com/t/86abt10yv "https://app.clickup.com/t/86abt10yv")

---

<time>8:08</time>
Okay, I've gotten most of the email taken care of.

<time>8:22</time>
From Mr. Jennings

- Vu - NSDFC
- Bao/Mostofa - OMS and NEOS
- Zulqurnain - FIN Searches
- Mikhail - Josh will work with him directly

## 9:36

Okay, so this is what I want to focus on currently:

- [x] [[Agenda/Daily/2025-09-17 - Wednesday#^wcqadb]]

<time>10:29</time>
I'm still currently working on the above task. Lots of different things are going on.

<time>10:50</time>
Okay, I got through slack items.

<time>10:53</time>
I want to again look at all the tasks that the developers currently have assigned.

Let's focus on going through Bao, Vu, Mostofa, and Zulqarnain.

- Bao - 27
    - Dev Needs Info - 3
    - Blocked - 2
    - Internal QA - 12
    - In Progress - 3
    - Needs Planning - 4
    - To do - 1
    - New Issue - 2
- Vu - 20
    - Internal QA - 6
    - Dev QA - 1
    - In Progress - 2
    - Needs Planning - 1
    - Ready to Start - 3
    - To do - 1
    - New Issue - 6
- Mostofa - 17
    - Dev Needs Info - 1
    - Blocked - 2
    - Internal QA - 7
    - In Progress - 2
    - Needs Planning - 3
    - Internal Review - 1
    - To do - 1
- Zulqarnain - 19
    - Dev Needs Info - 1
    - Internal QA - 9
    - Dev QA - 1
    - In Progress - 2
    - Needs Planning - 1
    - Ready to Start - 1
    - Backlog - 1
    - To do - 1
    - New Issue - 2

<time>11:07</time>
Okay, how am I going to differentiate between the different lists. I'm going to add a prefix of the client to the list. This means for NSDFC we will have list like this, "NSDFC - Backlog".

<time>11:12</time>
Now, the next thing to do is figure out a way to capture what items have been done. To also show clients, what is being done.

```js
document.querySelectorAll("cu-task-row")
```

These rows have an `id` that are prefixed with `task-`. We can look into 

- `cu-task-row-id` - If we use `innerText`, we will get back something like this: `"# 86aarc4vz"`

We'll need to go through more of this, but I think this will be fine for now.

- Task
    - Name of the task
    - What does it belong to

<time>11:40</time>
Okay, we're going to do some of the Internal QA

Holdings refer to the investments that a firm (entity) currently have. 13F is a form that comes from the SEC. Entities are required to fill out and file. This information is publicly available.

13F search is the `/firm-holding` page.

Luke explained the 13F and holdings to me.

<time>11:52</time>
Okay, we've got a lot of things to go through.

<time>13:13</time>
I'm still going through the QA items.

<time>13:28</time>
Okay, I'm done with the QA stuff for now. It is getting really close to 2:30 PM, so I think I could just keep trucking along. My hope will be to leave a bit earlier.

<time>13:52</time>
The pages in the email were referring to the forms.

The 3rd party payer is accessed in the "Accounting > Payment Profile". We can confirm this in the "Forms" tab. We need to select a form that allows for a 3rd party payer. These forms are the:

- Group Advantage Agreement
- Credit Card Authorization
- UFT Service Agreement (NSDFC Sponsor)
- NSDFC Loan Watch Agreement

![[Attachments/Pasted image 20250917135759.png]]

- Would it be better to leave the credit card authorization empty for the 3rd party payer.

- Send form is digital

![[Attachments/Pasted image 20250917140357.png]]

- Confirm with the developers that the "Send Form" action is sending to the correct email address. In production, test the action with a dummy account.

<time>16:01</time>
Okay, I'm back at it. 