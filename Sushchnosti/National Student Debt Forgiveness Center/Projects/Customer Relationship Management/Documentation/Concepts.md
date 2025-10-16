---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# Concepts
## Contacts

A contact is an individual who is in the NSDFC pipeline. A contact can also be referred to as a "file" meaning "the contact's file". There's a lot of information associated with a contact.

## FSA File

==What is the actual format of this file?==
==What is this file?==
==What does it stand for?==

<span class="placeholder">No description</span>

## Organizations

An organization represents an entity that has employees. 

### Organization Sub-Categories

<span class="placeholder">No description</span>

## Permissions

There are different permissions or rules that dictate what a person can and cannot do within the system. A lot of the permissions are pretty self-explanatory. It is understanding where the areas are within the system.

- **Edit Payment** - 
- **Edit Payment Plan** - 
- **Process Payment** - 
- **Issue Refund** - 
- **Reveal Driver's License Number** - 
- **Reveal SSN** - 
- **Void Payment** - 
- **Reveal Servicer Password** - 
- **Edit Payment Profile** - 
- **Edit Email Template** - 
- **Delete Contact** - 
- **Listen To Calls** - 
- **Edit File Number** - 
- **Edit Contact Note (Not used)** - We no longer use this permission since only the original user can edit/delete their own notes now.
- **View Calendars (Not used)** - 

Developers can view the permissions table with:

```sql
SELECT * FROM dbo.[Permissions];
```

## Programs

These are the different programs that NSDFC offers. Note that online there are different types of programs that are offered through the government.

- An IDR is an "Income Driven Plan" and is a type of categorization. The following IDR plans are:
    - IBR - Income-Based Repayment
    - ICR - Income-Contingent Repayment
    - PAYE - Pay As You Earn
    - SAVE - Saving on A Valuable Education
- PSLF stands for "Public Service Loan Forgiveness"
- PAYE and ICR will be phased out on July 1, 2028. Student borrowers enrolled in those plans at that time can transfer to IBR or RAP. - https://www.edcapny.org/resources-for-borrowers/idr-calculator/
- https://www.studentloanplanner.com/repayment-assistance-plan-rap/

### Extended Fixed Program

<span class="placeholder">No description</span>

### Extended Graduated Program

<span class="placeholder">No description</span>

### Graduated Program

<span class="placeholder">No description</span>

### IBR Program

<span class="placeholder">No description</span>

### ICR Program

ICR stands for "Income-Contingent Repayment".

https://edfinancial.studentaid.gov/income-driven-repaymentinformation-center/icr

### New IBR Program

IBR stands for "Income Based Repayment".

<span class="placeholder">No description</span>

### Old IBR Program

==What is the difference between the old and new IBR plan?==

<span class="placeholder">No description</span>

### PAYE Program

PAYE stands for "Pay As You Earn".

<span class="placeholder">No description</span>

### REPAYE Program

<span class="placeholder">No description</span>

### SAVE Program

SAVE stands for "Saving on A Valuable Education". This was formerly known as REPAYE.

<span class="placeholder">No description</span>

### Standard Program

<span class="placeholder">No description</span>

### Standard Program (30 Year)

<span class="placeholder">No description</span>

## Services
### Annual Recertification - IDR Only

<span class="placeholder">No description</span>

### Annual Recertification with PSLF

<span class="placeholder">No description</span>

### Consolidation

<span class="placeholder">No description</span>

### Consultation

<span class="placeholder">No description</span>

### Double Consolidation

<span class="placeholder">No description</span>

### IDR Backtracking

<span class="placeholder">No description</span>

### IDR Recalculation

<span class="placeholder">No description</span>

### PSLF Backtracking

<span class="placeholder">No description</span>

### Rehabilitation

<span class="placeholder">No description</span>

### Title 1 Forgiveness

<span class="placeholder">No description</span>

## Sponsors

A sponsor is a company that has an agreement with NSDFC to give them some benefits to their members. Currently, there's only two sponsor companies NSDFC themselves and FKM.

## Workflows & Statuses

We can think of the CRM as a pipeline or production line. New leads are generated and are at the being of the pipeline. Leads will then go through different steps as their specific service needs are established. This idea is represented by what we call "Workflows" and "Statuses". A workflow represents a specific step within the pipeline. A status is a step within a specific workflow. All they represent is where someone is at within the pipeline.

There's 15 workflows each containing different amounts of statuses. The workflows are ordered in how someone will typically go through the pipeline:

1. Intake
2. Sales
3. Welcome Packet
4. Processing
5. Forbearance
6. Online Servicer Account
7. Submission
8. Consolidation Approval
9. Non-IDR/IDR Approval
10. Accounting
11. Public Service Loan Forgiveness
12. Teacher Loan Forgiveness
13. Recertification
14. Rehab
15. Disability Discharge

There's some behind the scene automations that happen with workflows and statuses. Certain workflows and statuses will trigger an automation to happen. This is something that we need to document.