---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# Documentation

- What are the high level concepts we need to understand about the organization/project?

NSDFC makes money through performing various services for people. These services being offered is essentially them doing the paperwork for people to get into these programs.

## Automations

- [List of what Bao created](https://docs.google.com/spreadsheets/d/1_pr02AbDeXAwz5F7z2ew5fKFrIQCfshKqcXYpnW41f8/edit?gid=0#gid=0)
- Documents from Luke:
    - https://deltadesk.sharepoint.com/:x:/s/SoftwareDevelopment/EenEBkj4sT1AqyUXspKweSgBi-7FcJC4QdyauEM1EP3w-g?e=ycFq53 
    - https://deltadesk.sharepoint.com/:x:/s/NSDFC-DeltaDesk/EdYF1wbOfmBAnKBpnVKCt-EBwCwdEJ1qT4KrLTV2uKCs9g?rtime=8jFML4b13Ug 

## Permissions

```sql
SELECT * FROM dbo.[Permissions];
```

| IdPermission | Permission Name              | Description                                                                                                                                                                   |
| ------------ | ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1            | View Calendars               | We don't use this permission                                                                                                                                                  |
| 2            | Edit Payment                 | Only users that has this role can edit a payment, mark a payment from actual to estimated                                                                                     |
| 3            | Edit Payment Plan            | Only users that has this role can edit payment plans                                                                                                                          |
| 4            | Process Payment              | Only users that has this role can process a payment                                                                                                                           |
| 5            | Issue Refund                 | Only users that has this role can issue to refund a Cleared payment                                                                                                           |
| 6            | Reveal Driver License Number | Only users that has this role can view the full driver license number. By default we show the partial driver license number value                                             |
| 7            | Reveal SSN                   | Only users that has this role can view the full SSN. By default we show the partial SSN value                                                                                 |
| 8            | Void Payment                 | Only users that has this role can issue to void a Approved payment                                                                                                            |
| 9            | Reveal Servicer Password     | Only users that has this role can view the full Sevicer Password. By default we show the partial Sevicer Password value (Contact Details -> Profile tab -> Servicers section) |
| 10           | Edit Payment Profile         | Only users that has this role can create/edit the payment profile for Contact (Contact details -> Accounting tab)                                                             |
| 11           | Edit Email Template          | Only users that has this role can edit email templates on Settings page                                                                                                       |
| 12           | Edit Contact Note            | Contact Note can be edited by the creator or the users that have this permission                                                                                              |
| 13           | Delete Contact               | Only users that has this role can delete a Contact                                                                                                                            |
| 14           | Listen To Calls              | Only users that has this role can listen to the Call Recordings (Contact detail -> Communications tab -> Call recording tab)                                                  |
| 15           | Edit FileNumber              | Only users that has this role can edit the FileNumber for a Contact                                                                                                           |

## Archive

A "Notice of Cancellation" must have two pages. This is a compliance rule.

---

**From Bao:**
I'll try to answer as much as possible, based on my knowledge. but I believe these are related to business logic mostly, right? Luke should have more detailed views for you  

- What is a sponsor in relation to an Organization?
    - in our system, we only know which person is a sponsor of an Organization. we don't use it anywhere. so it's just kind of information
- What is a contact within our system?
- What is a "File"?
    - Contact and File are the same, I believe. basically, NSDFC is a system related to consulting / assistance services for people with student loans, helping them understand and apply for **student loan forgiveness, repayment plans, consolidations.** when a person applies to any programs, we'll create a Contact record ("File") for him/her and the client (NSDFC staff) will do some processes for that Contact - "File"
- What is forbearance?
    - Forbearance is a temporary pause or reduction in required payments that the system allows a Contact, usually because the Contact is experiencing financial hardship.
- What is a servicer?
    - the company that manages Contact's loan on a day-to-day basis
- What is the dummy contact ID we use?
    - here is my dummy contact: 17214
    - Luke's dummy contact 17179
    - you probably can create a dummy for your own. but let's confirm with Luke
- What is a workflow?
    - firstly, I think you should know NSDFC has some departments and each department will be responsible for some processes that I mentioned above. a workflow is a step that reflects what is going on with a Contact (File). for example, when a Contact is created, the Intake department will have an appointment with that Contact to discuss something and in our system, there is a status that will be created under Intake workflow to help us know that progress. when Intake finishs the appoitment, they will request a FSAFile, a new status will be created - FSA request, etc.
- What is a recertification?
    - we have some concepts that are related to "Recertification" - recertification services, recertifications, etc.. but I'm not really familiar with them. sorry I can't provide more information for this question
- What does the number for "Age of Status" represent?
    - it's the number of days between the Date Created of a status and today

---

#Todo 

The task this was pulled from: https://app.clickup.com/t/86abz6255 ^sljeuh 

I created this file. I'll write down the automation information
[https://docs.google.com/spreadsheets/d/1_pr02AbDeXAwz5F7z2ew5fKFrIQCfshKqcXYpnW41f8/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1_pr02AbDeXAwz5F7z2ew5fKFrIQCfshKqcXYpnW41f8/edit?usp=sharing)

Luke had some documents for the automation logic

[https://deltadesk.sharepoint.com/:x:/s/SoftwareDevelopment/EenEBkj4sT1AqyUXspKweSgBi-7FcJC4QdyauEM1EP3w-g?e=ycFq53](https://deltadesk.sharepoint.com/:x:/s/SoftwareDevelopment/EenEBkj4sT1AqyUXspKweSgBi-7FcJC4QdyauEM1EP3w-g?e=ycFq53)

[https://deltadesk.sharepoint.com/:x:/s/NSDFC-DeltaDesk/EdYF1wbOfmBAnKBpnVKCt-EBwCwdEJ1qT4KrLTV2uKCs9g?rtime=8jFML4b13Ug](https://deltadesk.sharepoint.com/:x:/s/NSDFC-DeltaDesk/EdYF1wbOfmBAnKBpnVKCt-EBwCwdEJ1qT4KrLTV2uKCs9g?rtime=8jFML4b13Ug)

---

https://app.clickup.com/t/86aby3j1e?comment=90130170825602&threadedComment=90130171317290
