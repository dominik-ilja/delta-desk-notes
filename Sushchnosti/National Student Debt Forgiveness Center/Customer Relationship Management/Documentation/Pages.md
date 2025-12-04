---
aliases:
cssclasses:
  - full_width
tags:
Related: []
Sources: []
Type: Documentation
---
# Pages

```
{
    const container = document.querySelector(".Table-module__Box--KyMHK")
    const els = Array.from(container.querySelectorAll(`[aria-label*="(Directory)"]`))
    const items = Array.from(new Set(els.map(e => e.textContent)));
    const text = items.join("\n")
    console.log(items)
    console.log(text)
}
```

## Public Paths
### /
### /application
### /confirm-appointment
### /create-payment-profile
### /fsa-file
### /login
### /update-info
### /update-payment-profile
### /update-servicers

## Authenticated Paths
### /dashboard
### /dashboard/appointments-intake
### /dashboard/appointments-intake
### /dashboard/appointments-intake
### /dashboard/appointments-sales-rep1
### /dashboard/appointments-sales
### /dashboard/appointments
### /dashboard/audit-trail
### /dashboard/calculators
### /dashboard/campaigns
### /dashboard/contact-statuses
### /dashboard/contacts
### /dashboard/contacts/:id

This is where the majority of people will spend there time in the CRM. It is broken down by 13 tabs at the top. Each individual tab may have additional categories associated with it.

The header will change color based on the type of contact that it is. This is based on the selection of the "Is Public Service?" field that can be found in the "Profile > Income And Tax Info" section. If the value is "No", the header will be the default color. If the value is "Yes", the header will be green. This was done so that you could tell what type of contact they are at a glance.

#### Profile Tab
##### Income And Tax Info

The "Is Public Service?" field was placed first to give it more visibility. This was requested by Natalie. The value of "Is Public Service?" does not have a value set when the contact is initially created. This was done to force the user to make a selection rather than a default selection being done.

##### New Monthly Payment

This field is overwritten when a quote is selected in the "Loans" tab.

##### Applicant Total Fed Loans

This field is automatically filed out when a new FSA text file is selected.

#### Workflow Tab

This tab represents where a contact is within the NSDFC pipeline. A workflow typically corresponds to a specific department within NSDFC. The workflows are ordered in a specific way that given to us by the client.

Each workflow will contain it's own statuses. A status represents a step within the workflow. The statuses also have a defined ordering given to us by the client.

In each workflow, there is the "Add Status" button. This allows a user to add a status to the workflow. This changes where a contact is within the workflow. There can be automations and other side-effects that happen when adding a new status. Some of these side-effects require a service to be selected for the side-effect to occur properly. ==This is something that needs to have a guardrail around it.==

Related database tables are:

- Workflows
- WorkflowSteps

### /dashboard/documents
### /dashboard/estimated-payments
### /dashboard/forms-library
### /dashboard/invoicing
### /dashboard/list-imports
### /dashboard/organizations
### /dashboard/organizations/:id
### /dashboard/payments
### /dashboard/reminders
### /dashboard/reports
### /dashboard/settings
#### Email Template

This table contains the various email templates defined by NSDFC. In this table, we can see if the email will be sent out automatically for one of the following reasons:

- **Custom logic.** For example, reminder emails for payments.
- **Tied to a workflow status.** For example, when the "Client Unresponsive" status is set in the "Processing" workflow will be sent when the status is set.
- **A combination of both.** For example, the "Contract Received" status in the "Sales" workflow will be sent out 30 days after the status.

#### List Import
#### System Automations
### /dashboard/sms-calls-inbox
### /dashboard/sponsors
### /dashboard/sponsors/:id
### /dashboard/uploaded-fsa
