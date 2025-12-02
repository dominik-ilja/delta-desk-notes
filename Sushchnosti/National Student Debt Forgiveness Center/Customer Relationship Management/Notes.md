---
aliases:
  - NSDFC - CRM Notes
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# NSDFC - CRM Notes
## Monday, December 1, 2025
### Stagnant Leads - 2:00 PM

- Intake complete is not autocompleted
    - Look for anyone who is in Intake complete without an FSA text file
- What email statuses trigger what emails
- 

### Meeting with Natalie - 10:00 AM

- 4:00 - 
- 10:00 - Contact ID: 4453
    - Should not be estimated. Should have been flagged as actual and consolidation approved
- 12:30 - The approved on date for the service and what's in the "Contact Status" sidebar should match
- 14:30 - Recertification
    - We need to have on the top of the recertification page to have the recertification amounts on top and on the bottom to have the recertification payments that are scheduled.
    - 15:44 - Recertification totals at the top and scheduled recertification payments on the bottom. Get it done by Wednesday
- 17:00 - Group Advantage Agreement (Start of discussion)
    - 19:00 - The Corp Rep. Name and Corp Rep. Signature will be pre-filled with Joe's signature. I'm assuming that Joe is referring to Josef. This is on page 4.
    - 21:30 - ACH won't be done until the end of January.
    - 22:30 - Needing a payment schedule for the different services. For example, if I have the service "IDR Recalculation", it should be:
        - IDR Recalculation
            - Payment 1 | 11/06/2025 | $278.50
            - Payment 2 | 11/22/2025 | $278.50
    - 24:30 - 1% discount if a person pays in full. This is to avoid legal issues, to be compliant.
    - 52:00 - Current loan monthly payment is being pulled from the loan page
    - 1:05:00 - Hide the ACH part of the form
- 35:15 - Assigned sales rep should be showing in the sidebar
- 38:10 - Kanako shouldn't be able to cancel a file until it is at least 10 business days have passed. There is a $25 re-instating fee.
    - 39:00 - What if we just email someone each time a file is canceled with a link to the file that was cancelled. This should be emailed to Kathleen.
    - 41:00 - It must be 10 days from the sold on date
- 44:00 - No services are available. Due to leadtrac data. The contact ID is 8760.
- 45:30 - date of 01/01/1900
- 47:00 - If a file has been cancelled, then moves out of a cancelled status a $25 "reactivation" fee needs to be added
- 50:00 - If Kanako sets a file in processing to "Cancelled", then it moves out of the status an email should go out notifying John and Kathy to add a $25 "reactivation" fee.
- 54:00 - The "New Monthly Payment" should be allowed to be null.
    - 55:30 - When selecting a new monthly, payment in the loan page it should auto-populate the "New Monthly Payment"
- 57:00 - The error for their being no new monthly payment in the group advantage form should be shown differently. For example, a banner in the modal so that it is front and center.
- 1:00:00 - Initial monthly payment should auto-populate the "New Monthly Payment"
- 1:01:00 - ACH pricing and credit pricing for the services
    - 1:02:20 - How will we know if they'll be paying with a credit card versus an ACH
- 1:06:00 - Andrew - Fluid something???
- 1:06:10 - Implement the new form
- 1:07:00 - New report for Natalie that does the following: Of all the people that owe them money that have been approved. There's going to be an email that will be sent out.
- 1:08:00 - Natalie won't be in on Friday. She's going to Puerto Rico for a week.
- 1:10:00 - The different pricing don't seem to be working properly.
- 1:21:00 - The different employers I feel like should be it's own list for them to edit and update. Currently, this is something that Natalie and her team is working on.
- 1:33:00
    - PSLF credits can be pulled from the FSA text file. The most recent Anniversary date and PSLF credits should be auto-populated in the Recertification tab.

---

- Contact ID: 4453 - When things are approved, they need to be linked to a service. The reason approved on wasn't set was because they didn't select a service.
- Recertification tab
    - We need to have on the top of the recertification page the recertification amounts on top and on the bottom the recertification payments that are scheduled. Due Wednesday.
- Group Advantage Agreement
    - We need to create a new fillable form for it.
    - The Corp Rep. Name and Corp Rep. Signature will be pre-filled with Joe's signature. I'm assuming that Joe is referring to Josef. This is on page 4.
    - ACH won't be done until the end of January.
    - Needing a payment schedule for the different services. For example, if I have the service "IDR Recalculation", it should be:
        - IDR Recalculation
            - Payment 1 | 11/06/2025 | $278.50
            - Payment 2 | 11/22/2025 | $278.50
    - 1% discount if a person pays in full. This is to avoid legal issues, to be compliant.
    - Current loan monthly payment is being pulled from the loan page
    - Hide ACH part of the form
- Status Quick View
    - Assigned sales rep should be showing in the sidebar
- Cancellation of files
    - Kanako shouldn't be able to cancel a file until it is at least 10 business days have passed. If a file is cancelled, an email is sent to Kathleen.
    - If a file is moved out of cancelled, there is a $25 reactivation fee. This is something that should be emailed to John and Kathy to add the fee.
- New report for Natalie that does the following: Of all the people that owe them money that have been approved. There's going to be an email that will be sent out.
- Bugs
    - New Monthly Payment should be allowed to be empty (`null`)
    - The different pricing don't seem to be working properly in the services. They all seem to show the unsponsored price.
- Improvements
    - The error for their being no new monthly payment in the group advantage form should be shown differently. For example, a banner in the modal so that it is front and center.
    - Initial monthly payment should auto-populate the "New Monthly Payment" when a quote is selected.
    - PSLF credits can be pulled from the FSA text file. The most recent Anniversary date and PSLF credits should be auto-populated in the Recertification tab.
- Discussion
    - How should ACH pricing and credit pricing be handled in the services?
    - The different employers I feel like should be it's own list for them to edit and update. Currently, this is something that Natalie and her team is working on.