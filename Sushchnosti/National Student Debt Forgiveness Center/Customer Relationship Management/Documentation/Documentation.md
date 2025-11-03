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

## Database
### bluerock.RequestLog

<span class="placeholder">No Description</span>

### dbo_.EFMigrationsHistory

This table is created by the .NET Entity Framework package.

### dbo.ActivityLogs

This table is the "History" tab within the `/dashboard/contacts/{id}` page.

### dbo.AGIPercentFactors

<span class="placeholder">No Description</span>

### dbo.Appointments

<span class="placeholder">No Description</span>

### dbo.Appointments_Backup250617

<span class="placeholder">No Description</span>

### dbo.ApptOriginTypeOptions

<span class="placeholder">No Description</span>

### dbo.AutomationLogs

<span class="placeholder">No Description</span>

### dbo.AutomationRequests

<span class="placeholder">No Description</span>

### dbo.AutomationRules

<span class="placeholder">No Description</span>

### dbo.BoroughTypeOptions

<span class="placeholder">No Description</span>

### dbo.CallHistory

<span class="placeholder">No Description</span>

### dbo.ChatServUsers

<span class="placeholder">No Description</span>

### ==dbo.client==

I'm not sure where this came from.

### dbo.ConsolidationLoans

<span class="placeholder">No Description</span>

### dbo.ContactCallRecordings

<span class="placeholder">No Description</span>

### dbo.ContactEmployers

<span class="placeholder">No Description</span>

### dbo.ContactEmployers_250625

<span class="placeholder">No Description</span>

### dbo.ContactFiles

<span class="placeholder">No Description</span>

### dbo.ContactForms

<span class="placeholder">No Description</span>

### dbo.ContactHistory

<span class="placeholder">No Description</span>

### dbo.ContactLoanServicers

<span class="placeholder">No Description</span>

### dbo.ContactLoanServicersTmp

<span class="placeholder">No Description</span>

### dbo.ContactNotes

<span class="placeholder">No Description</span>

### dbo.ContactReferrals

<span class="placeholder">No Description</span>

### dbo.Contacts

This is the main contacts table. It is basically a 1-to-1 mapping of the `/dashboard/contacts/{id}` profile tab.

I noticed that they have an `OrganizationCode` column. This should be in the `Organizations` table.

### dbo.Contacts_Backup250627

<span class="placeholder">No Description</span>

### dbo.ContactServices

<span class="placeholder">No Description</span>

### dbo.ContactStatuses

<span class="placeholder">No Description</span>

### dbo.ContactStatuses_250826

<span class="placeholder">No Description</span>

### dbo.ContactStatuses_Backup

<span class="placeholder">No Description</span>

### dbo.ContactTypeOptions

<span class="placeholder">No Description</span>

### dbo.ContractReceivedClients_Temp

<span class="placeholder">No Description</span>

### dbo.Departments

<span class="placeholder">No Description</span>

### dbo.DevContactFiles

<span class="placeholder">No Description</span>

### dbo.devPaymentProfiles

<span class="placeholder">No Description</span>

### dbo.draft_plan

<span class="placeholder">No Description</span>

### dbo.EmailJobs

<span class="placeholder">No Description</span>

### dbo.EmailSignatures

This contains the different email signatures. This was a table for a feature that was later dropped according to Bao.

### dbo.EmailTemplates

This contains the various email templates that can be sent out. This is edited on the `/dashboard/settings` page.

### dbo.EmailTemplates_Backup250617

<span class="placeholder">No Description</span>

### dbo.Employers

<span class="placeholder">No Description</span>

### dbo.Forbearance

<span class="placeholder">No Description</span>

### dbo.Forms

<span class="placeholder">No Description</span>

### dbo.FormsToConvert

<span class="placeholder">No Description</span>

### dbo.FSAFiles

<span class="placeholder">No Description</span>

### dbo.FSALoans

<span class="placeholder">No Description</span>

### dbo.FSAUploads

<span class="placeholder">No Description</span>

### dbo.FSAUploadsTest

<span class="placeholder">No Description</span>

### dbo.GlobalSettings

<span class="placeholder">No Description</span>

### dbo.LeadtracAppointmentFix

<span class="placeholder">No Description</span>

### dbo.ListImports

<span class="placeholder">No Description</span>

### dbo.LoanServicerOptions

<span class="placeholder">No Description</span>

### dbo.mapped_workflow_history

<span class="placeholder">No Description</span>

### dbo.MissingDocuments

<span class="placeholder">No Description</span>

### dbo.NoteCategories

<span class="placeholder">No Description</span>

### dbo.NoteCategoriesNorm

<span class="placeholder">No Description</span>

### dbo.NoteTemplates

<span class="placeholder">No Description</span>

### dbo.OrganizationDepartments

<span class="placeholder">No Description</span>

### dbo.Organizations

<span class="placeholder">No Description</span>

### dbo.PaymentPlans

<span class="placeholder">No Description</span>

### dbo.PaymentPlansBackup250617

<span class="placeholder">No Description</span>

### dbo.PaymentProfiles

<span class="placeholder">No Description</span>

### dbo.Payments

<span class="placeholder">No Description</span>

### dbo.PaymentsBackup250617

<span class="placeholder">No Description</span>

### dbo.Permissions

<span class="placeholder">No Description</span>

### dbo.PersonalReferences

<span class="placeholder">No Description</span>

### dbo.PovertyTable

<span class="placeholder">No Description</span>

### dbo.ProcessPaymentLogItems

<span class="placeholder">No Description</span>

### dbo.ProcessPaymentLogs

<span class="placeholder">No Description</span>

### dbo.ProgramTypes

<span class="placeholder">No Description</span>

### dbo.Recertifications

<span class="placeholder">No Description</span>

### dbo.reference

<span class="placeholder">No Description</span>

### dbo.ReferralTypeOptions

<span class="placeholder">No Description</span>

### dbo.Reminders

<span class="placeholder">No Description</span>

### dbo.Services

<span class="placeholder">No Description</span>

### dbo.ServiceWorkflows

<span class="placeholder">No Description</span>

### dbo.SignDocument

<span class="placeholder">No Description</span>

### dbo.SmsHistory

<span class="placeholder">No Description</span>

### dbo.SmsJobs

<span class="placeholder">No Description</span>

### dbo.SponsorTypes

<span class="placeholder">No Description</span>

### dbo.StandardRepaymentPeriod

<span class="placeholder">No Description</span>

### dbo.StatusJobs

<span class="placeholder">No Description</span>

### dbo.sysdiagrams

<span class="placeholder">No Description</span>

### dbo.TableSettings

<span class="placeholder">No Description</span>

### dbo.TempOrg

<span class="placeholder">No Description</span>

### dbo.TempQuote

<span class="placeholder">No Description</span>

### dbo.tmpWorkflowStepMap

<span class="placeholder">No Description</span>

### dbo.TriggerRules

<span class="placeholder">No Description</span>

### dbo.UFTFormSubmissions

<span class="placeholder">No Description</span>

### dbo.UserDepartments

<span class="placeholder">No Description</span>

### dbo.UserPermissions

<span class="placeholder">No Description</span>

### dbo.Users

<span class="placeholder">No Description</span>

### dbo.UserToChatServUser

<span class="placeholder">No Description</span>

### dbo.Workflows

This table correlates to the workflows of the system. A workflow is a top-level categorization within the CRM.

### dbo.WorkflowSteps

<span class="placeholder">No Description</span>

### dbo.ZipToCity

This table is for mapping a Zip code to a city and state. This is for a feature that auto-fills inputs.

### dbo.zz_tmpWorkflowStepMap

<span class="placeholder">No Description</span>

### dbo.zzzCampaigns

<span class="placeholder">No Description</span>

### dbo.zzzLoanServicerOptionsLuke

<span class="placeholder">No Description</span>

### dbo.zzzOrganizations

<span class="placeholder">No Description</span>

### dbo.zzzSponsorDepartments

<span class="placeholder">No Description</span>

### dbo.zzzSponsorMembers

<span class="placeholder">No Description</span>

### dbo.zzzSponsors

<span class="placeholder">No Description</span>

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

---

Where did he get the formulas from?

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
