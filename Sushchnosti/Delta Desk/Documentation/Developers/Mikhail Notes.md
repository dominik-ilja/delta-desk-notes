---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
Complete: true
Tasks: 0
Tasks Remaining: 0
Tasks Complete: 0
Date Completed:
---
# Mikhail Notes
## Tuesday, October 21, 2025
### Tasks

FIN Security and Login [86acbbfbu]
Create\review a list of steps to do for login [86acp8ttp]

### Logs

I wanted to follow-up on these tasks:  

- [86abv32pq – Create a script to click a button | ready for deployment | Mikhail](https://app.clickup.com/t/86abv32pq)
- [86acg44xp – Automate Recons | developer review | Mikhail](https://app.clickup.com/t/86acg44xp)  

I know for the first task you were waiting on Josh. The second task who are you waiting on to review it?

These are also some other high priority tasks:  

This was due in September, but doesn't look like it was worked on. Can you take a look for me.

- [86abv6dt2 – Fix Document Export and Check Other Exports | ready to start | Josh Jennings, Mikhail](https://app.clickup.com/t/86abv6dt2)  

All of these are relating to loading issues:  

- [86abz555v – Firm Holding page can take 15+ seconds to load | in progress | Mikhail, Josh Jennings](https://app.clickup.com/t/86abz555v)
- [86acm7r19 – Look at "/firm-details/10587" for loading issues | in progress | Bao Do Van, Mikhail](https://app.clickup.com/t/86acm7r19)
- [86ac7mx5g – Excessive loading times for "/people-moves-search" page | to do | Josh Jennings, Mikhail, Bao Do Van](https://app.clickup.com/t/86ac7mx5g)


## Monday, October 20, 2025
### Tasks

- Manage Terminated crd Firms [86accvkk9]
- Look at "/firm-details/10587" for loading issues [86acm7r19]
- FIN Security and Login [86acbbfbu]
- aapryl issues

### Logs

Hello, hope you had a good weekend! Did you get to do anything fun on the break?

---

How is this coming along? Do you have an idea of when this will be done?
- 86accvkk9 - Manage Terminated crd Firms - In Progress

---

How is this coming along? Josh has those seven steps he requested you to follow. What step are you currently on
- 86acbbfbu - FIN Security and Login - To Do

These are the seven steps for reference:
1. Research current situation, interview me to learn more details and discuss – provide small documentation
2. Research different options and approaches – provide small documentation
3. Present the findings to me, together we decide which plan to take (give me at least 2 options with pros and cons)
4. Based on the decision, create a detailed migration plan
5. Present the migration plan to me for approval
6. Notify and educate the client on the migration plan for client approval
7. Manage and execute the migration plan

---

How will you go about identifying the loading issues in this page?
- 86acm7r19 - Look at "/firm-details/10587" for loading issues - To Do

If there isn't a task linked to this, could you create one please. If there is, could you send it to me:
-  aapryl issues

## Friday, October 17, 2025
### Tasks

- FIN Security and Login [86acbbfbu]
- Move the universal search description generator into the Fin API MYSQL part [86acar692]
- Manage Terminated crd Firms [86accvkk9]
- (add fields and the process to production)

### Logs


## Thursday, October 16, 2025
### Tasks

FIN Security and Login [86acbbfbu]
Move the universal search description generator into the Fin API MYSQL part [86acar692] - May be done today or tomorrow. Will be alpha beta version ready on Monday.

### Log
#### 8:00 AM - Meeting

He's having some issue on architecture

---

- Move MySQL to MS SQL
- Stored procedures
- Has not started on the approach

Organization sponsors

---

- Should the whole organization be considered sponsored if it is just the department that is sponsored.
- Get on a call with Josef to discuss this issue. Some of the entries in Josef's list were not found in the database. Asking Josef if these entries should be a department of an organization or an organization itself.
- He wants confirmation that the mapping is correct before committing to it: https://files.slack.com/files-pri/T05CBUR61FV-F09MKQDGTEU/image.png

## Wednesday, October 15, 2025
### Tasks

List for Gar
Update database with list sent from Josef[86acgav8c]
Move the universal search description generator into the Fin API MSSQL part [86acar692]
FIN Security and Login [86acbbfbu]

## Tuesday, October 14, 2025
### Tasks

- Move the universal search description generator into the Fin API [86acar692]
- Manage Terminated firms [86accvkpp]

### Logs

first 103 records from this file, I'm not sure how this file was created, it seems to me someone of nsdfc approved it

I found some departments with the names they provided

```
ASSCR - FKM  select * from Organizations where OrganizationName like '%ASSCR%'  
ATU 1342 - FKM  
SBA – FKM  
BUGS – NSDFC select * from OrganizationDepartments where DepartmentName like '%BUGS%'  
Dream Charter – NSDFC select * from OrganizationDepartments where DepartmentName like '%Dream%'  
National Health and Law Program (NHeLP) – NSDFC  
Nuasin Charter – NSDFC select * from OrganizationDepartments where DepartmentName like '%Nuasin%'
```

Can you use db ?

---

**8:48** — I need a linqpad script for the cliker, and I need Josh to review the current result of this task and tell me what to do next

- https://app.clickup.com/t/86acg44xp
- https://app.clickup.com/t/86acgav8c

#### 10:13

Okay, the meeting we got clarification on things that were blocking him. I also checked on his task. We need to go through and check these things out.

## Monday, October 13, 2025
### Tasks

- Review Notify the user about an incoming call [86acd2jvf]
- Automate Recons [86acg44xp]
- Update database with list sent from Josef [86acgav8c]  
