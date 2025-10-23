---
aliases:
cssclasses:
tags:
Related:
  - "[[Sushchnosti/National Student Debt Forgiveness Center/Customer Relationship Management/Customer Relationship Management|NSDFC - CRM]]"
Sources: []
Type: Documentation
---
# Application
## Global controls

The header and sidebar are global controls of the application.

**Header:**

- Breadcrumbs
- Create New Contact
- Global contact search
- Avatar

The "Create New Contact" modal allows you to create a new contact no matter where you're at within the system.

The "Create New Organization" modal allows you to create a new organization.

- **Organization Name** - Name of the organization
- **Organization Code** - 
- **Parent Organization** - 
- **Primary Contact First Name** - 
- **Primary Contact Last Name** - 
- **Phone** - 
- **Email** - 
- **Website** - 
- **Is Sponsor** - If checked, indicates that the organization is [[Sushchnosti/National Student Debt Forgiveness Center/Customer Relationship Management/Documentation/Concepts#Sponsors|sponsored]]. If this is checked, additional fields will be shown for the sponsor.
    - **Sponsor** - The sponsoring company
    - **Sponsor Starting Date** - When the sponsorship will began
    - **Sponsor Expiration Date** - When the sponsorship will end

## /dashboard

The dashboard contains an overview of the various [[Sushchnosti/National Student Debt Forgiveness Center/Customer Relationship Management/Documentation/Workflows and Statuses|workflows]] within the system. Each workflow is a step within NSDFC's pipeline to have someone purchase services. A workflow also has its own steps called "Statuses" that a person can be in. They represent where someone is at in the process of working with NSDFC. 

On the dashboard, you are able to filter out people by a specific workflow and status. There's also functionality to export the data to a CSV to be used in Excel or some other program.

## /dashboard/appointments

<span class="placeholder">No description</span>

## /dashboard/contacts

<span class="placeholder">No description</span>

## /dashboard/contacts/{id}

This is the details page of a specific contact. All the information relating to a contact is contained within this page. There's a tab bar for the different parts of the profile:

- Profile
- Workflow
- Loans
- Services
- Notes
- Appointments
- Forms
- Files
- History
- Tasks
- Recertification
- Accounting
- Communication

### Profile

This contains all the information of the contact. These various sections will be used to generate quotes for services that the contact qualifies for. The different sections are:

- Source Info
- General Info
- Family Info
- Identification Info
- Employment Info
- Income And Tax Info
- Forbearance
- References
- Servicers

#### Source Info

You can edit the file number from this page if you have the "Edit File Number" permission.

#### Identification Info

This pages requires permissions to edit the "Social Security Number" and "Driver's License Number". The required permissions are "Reveal SSN" and "Reveal Driver's License Number" respectively.

#### Income and Tax Info

- The "Is Public Service" field is required to be filled out before information can be saved. This was due to feedback from NSDFC of people not updating this field properly which would cause calculators to not function properly. If the value of this field is "Yes", then the header background color will be updated to green to reflect this.
- The "Current Monthly Payment" is the amount of money that the individual is currently paying for their student loans.
- The "New Monthly Payment" is the monthly payment that the individual will receive with a selected program. This field is required to generate forms properly. ==This should be revisited to work better==
- The "Application Total Fed Loans" is the total amount of student loans the individual has.

#### Forbearance

<span class="placeholder">What is forbearance?</span>

#### References

<span class="placeholder">What are these used for?</span>

#### Servicers

A servicer is a platform that the student loans are being paid through. The "Reveal Servicer Password" permission is required to see the servicer password.

### Workflow

The workflow tab contains all the different steps that a contact is currently in. Each workflow allows you to add a status for it.

==We're able to associate a service with a specific workflow status in some cases. What exactly does this mean?==

==An improvement to this page could be to not show the workflows that do not contain any statuses. This however could be an issue if you needed to add a status to a workflow that doesn't have any statuses. An alternative would be to show the number of statuses at the end of the workflow. The purpose of this is to quickly identify what a contact has statuses in.==

### Loans

- Loan Information
- Create Quote
- Saved Quotes

### Services

<span class="placeholder">No description</span>

## /dashboard/contact-statuses

<span class="placeholder">No description</span>

## /dashboard/estimated-payments

<span class="placeholder">No description</span>

## /dashboard/forms-library

<span class="placeholder">No description</span>

## /dashboard/organizations

<span class="placeholder">No description</span>

## /dashboard/organization/{id}

<span class="placeholder">No description</span>

## /dashboard/payments

<span class="placeholder">No description</span>

## /dashboard/reminders

<span class="placeholder">No description</span>

## /dashboard/reports

<span class="placeholder">No description</span>

## /dashboard/settings

<span class="placeholder">No description</span>

## /dashboard/sms-calls-inbox

<span class="placeholder">No description</span>

## /dashboard/uploaded-fsa

<span class="placeholder">No description</span>

