---
aliases: []
cssclasses: []
tags: []
Related:
  - "[[/Agenda/Daily/2025-09-24 - Wednesday]]"
---
# Wednesday, September 24, 2025

[[/Notes/Yearly/2025|2025]] ❯ [[/Notes/Quarterly/2025 - Q3|Q3]] ❯ [[/Notes/Monthly/2025 - September|September]] ❯ [[/Notes/Weekly/2025 - Week 39|Week 39]]

❮ [[/Notes/Daily/2025-09-23 - Tuesday|Tuesday, September 23, 2025]] · Wednesday, September 24, 2025 · [[/Notes/Daily/2025-09-25 - Thursday|Thursday, September 25, 2025]] ❯

<time>7:02</time>
Okay, I'm going to need to track my time today on different tasks. I'm thinking how I could potentially do this. Let's get this room cleaned up and then start discussing this.

<time>7:13</time>
Okay, so we should have categories that our time is going into. Let's be more broad then make the categories more narrow.

- Reviews - Internal Reviews
- Developer work
    - 
- Manager work
    - Checking on the developers
    - Making sure they're focusing on the highest priority items
    - Meetings
- Client work
    - Attend to emails, messages, etc. from the client
    - Meetings
- Task creation
    - Slack messages
- Documentation
    - High-level processes
    - Understanding the domain
- Improving processes
- Organizing work

<time>7:37</time>
The way that I'm handling our three main projects: FIN Searches, NSDFC, and OMS is  is moving the tasks I need you to focus on into sprints. If you need help seeing what tasks are in the sprints, please let me know. If there's other things that popup that you need to take care of, I'll let you know, so that we can shift priorities for a moment.

<time>7:45</time>
Finished up with Mostofa and Vu.

<time>8:14-8:45</time>
Call with Bao

![[Attachments/Pasted image 20250924083257.png]]
![[Attachments/Pasted image 20250924083327.png]]
![[Attachments/Pasted image 20250924083627.png]]

When will we post staging to production? Give him an update on what's going on with that.  - Bao

Has something to discuss with Josh

<time>8:45</time>

Break

<time>8:54</time>
**9:07** — Finished reviewing my email. Now, I'm going to go through NSDFC email.

## 9:35

Zul - Did the chat search

The testing part is the tricky part for him.

Research notes page he doesn't think is being visited very often.

Zulqarnain questions:
- Firm names
- NSDFC - Invoice preview - https://app.clickup.com/t/86abu7zvn

The from should be the person currently visiting it and the to is the contact itself

---

Multiple fields and filters. There's a lot of conditions that can be confusing to Zulqarnain.

## 10:00

- How could we create a system to allow the clients to see what we're currently working on?
- What are the different roles/permissions in the database?
- What are the different automations and where are they stored?
    - How can I see where this is happening?
---
- [86abr453v – Need to Implement Email Rules Based on Feedback From Staff | in progress | Bao Do Van, Dominik Kulak](https://app.clickup.com/t/86abr453v)
- [86abyhwrp – Reschedule payment for client | ready to start | Josh Jennings](https://app.clickup.com/t/86abyhwrp)
- [86abvhk8f – Figure out why amounts are zeros in Recertification tab | in progress | Josh Jennings, Mikhail](https://app.clickup.com/t/86abvhk8f)
- [86aby3czj – All files should have an account workflow | to do | Josh Jennings](https://app.clickup.com/t/86aby3czj)
- Cleaning up emails in NSDFC. How can I get access so, that I can start filtering out emails and creating rules?
- How can we stop the forwarding of NSDFC emails from Luke's account?


---

- Moving around teams meetings
    - a
- Colin
    - Figure out how we could make him useful.
- 5:30 - Making financial companies are more streamlined.
- OMS
    - He's allowed a hedge fund to scale without them having to hire more people
    - Carrick Lane - 2.5 billion w/ 700 people
    - Optimizing/streamlining and database stuff
- MS SQL Server version 1
- Daily Risk Assessment Report
- 11:00 - Options have other numbers that go with them
- 12:00 - Problem with things running very fragile things
- 13:00 - Being able to keep track of all of their different jobs
- 13:35 - NEOS gave a down payment for the work
- 15:30 - Look into ClickUp to see if we can give clients insight into our
- 19:00 - Import tool
- 21:00 - Permissions page for FIN / NSDFC
- 23:00 - Not to get sidetracked on something that isn't important and urgent. He doesn't think that the documentation is super important.
- 24:45 - Going through all the NSDFC
- 25:30 - Data only requests vs. things with functionality. What is the scope of the change?
- 26:10 - Demos from the users. He wants to know how they're using the system.
- 27:00 - Add Service
    - Hide Estimated Payments when there are no entries
    - 27:50 - Having a wizard for adding a service
- 28:00 - Depending on the program type you pick will alter what services they can choose from.
- 29:20 - Look into what services they can apply to program.
- 30:30 - Scheduled stuff is Azure functions. Some is triggered by the API.
- 31:45 - 
    - 32:15 - Ask Bao how the automations are happening?
- 33:15 - Not automated means it isn't being used?
- 33:45 - Hates double scrollbars
- 34:45 - Intake - Client not interested
- 36:30 - Destructive actions
- 38:00 - Wait a couple of days to stop Luke's emails. Maybe we could do this on Friday.
- 40:00 - 
- 50:00 - Inbox rules on a shared inbox

## 11:37

- 00:30 - Blocking Azure site
- 1:15 - Using a DNS alias
- 2:30 - MCP server wrapper
    - 3:45 - Most recent version of the data

![[Attachments/Pasted image 20250924115008.png]]

- 23:00 - Send everything in bulk
- 40:00 - Database only tasks

## 14:24

Okay, so this is what I want to do:

- Shared documentation
- Task management
    - Team
    - Personal
- Email management

## 19:05

```js
(async () => {
    async function timeout(milliseconds) {
        return new Promise((resolve) => {
            setTimeout(() => resolve(), milliseconds)
        })
    }

    const scrollContainer = document.querySelector('[data-test="dashboard-table__scroll"]')
    scrollContainer.scrollTo(0, 0);
    await timeout(1000)

    const rows = Array.from(scrollContainer.querySelectorAll("cu-task-row"))
    const items = [];
    
    for (const row of rows) {
        let name = row.querySelector("cu-task-row-main span");
        
        if (!name) {
            console.log('Name not found, scrolling to row...');
            row.scrollIntoView({ behavior: 'smooth', block: 'center' });
            await timeout(1000);
            name = row.querySelector("cu-task-row-main span");
            console.log('After scroll:', name);
        }
        
        // get remaining data from row
        items.push({name});
    }
    
    console.log(items);
})()
```

```js
(()=>{
    const scrollContainer = document.querySelector('[data-test="dashboard-table__scroll"]')
    const row = scrollContainer.querySelector("cu-task-row");
    const name = row.querySelector("cu-task-row-main span").innerText;
    const taskID = row.querySelector("cu-task-row-id").innerText.replace("# ", "");
    const sprints = Array.from(
        row.querySelector(`[data-test="task-row__sprint"]`)
           .querySelectorAll(".cu-multiple-lists-display__item-name")
    ).map(el => el.innerText);
    const requestors = Array.from(
        row.querySelector(`[aria-label*="Requestors Custom Field"]`)
            .querySelectorAll(".cu-custom-field-dropdown-labels__label-text")
    )
    const taskSources = Array.from(
        row.querySelector(`[aria-label*="Task Sources Custom Field"]`)
            .querySelectorAll(".cu-custom-field-dropdown-labels__label-text")
    )
    const status = row.querySelector("cu-task-row-status > div span").innerText;
    const state = row.querySelector(`[aria-label*="State Custom Field"]`).innerText;
    const assignee = Array.from(
        row.querySelector(`cu-task-row-assignee`)
            .querySelectorAll(`cu3-avatar > div`)
    ).map(el => {
        return el.getAttribute("aria-label")
            .split(",")
            .filter((el => el.trim() !== ""))
            .join(" ")
    })
    .sort()
    .join(", ");

    console.log({
        name,
        taskID,
        sprints,
        requestors,
        taskSources,
        status,
        state,
        assignee
    })
})()
```