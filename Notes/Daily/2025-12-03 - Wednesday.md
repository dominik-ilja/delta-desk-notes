---
aliases: []
cssclasses: []
tags: []
Related:
  - "[[/Agenda/Daily/2025-12-03 - Wednesday]]"
---
# Wednesday, December 03, 2025

[[/Notes/Yearly/2025|2025]] ❯ [[/Notes/Quarterly/2025 - Q4|Q4]] ❯ [[/Notes/Monthly/2025 - December|December]] ❯ [[/Notes/Weekly/2025 - Week 49|Week 49]]

❮ [[/Notes/Daily/2025-12-02 - Tuesday|Tuesday, December 02, 2025]] · Wednesday, December 03, 2025 · [[/Notes/Daily/2025-12-04 - Thursday|Thursday, December 04, 2025]] ❯

"I think out of all of the tasks we have for NSDFC, we should have someone start on the new Contracts soon.  However, we're going to need to give the team very good requirements and probably put it in a new branch so we can test and it doesn't hold up other small tasks that need to get pushed"

We need to write the requirement based on the above.

These are the notes from the meeting:

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

---

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

**Name:** Updates to the Group Advantage Form

Natalie has sent us a new Group Advantage Form as a Word document. We need to do the following:

- Remove the "ACH Authorization" section from the form
- Turn the Word document into a fillable form
- Get confirmation on the mapping between the fields in the form and what's in the CRM
- Add the individual payment schedules for the different services

The form contains the following fields:

- Page 1
    - Representative - ==What is the mapping for this field?==
    - File - ==What is the mapping for this field?==
    - Initial (Footer) - **Filled by Xodo sign**
- Page 2
    - Initial (Footer) - **Filled by Xodo sign**
- Page 3
    - Initial (Footer) - **Filled by Xodo sign**
- Page 4
    - Executed On this Date - ==What is the mapping for this field? What is the date that should be used.==
    - Client Signature - **Filled by Xodo sign**
    - Client Name - ==What is the mapping for this field?==
    - Corp. Rep. Name - **Prefilled with the text "Josef Basmagy"**
    - Corp. Rep. Signature - **Prefilled with an image of Josef's signature**
    - Initial (Footer) - **Filled by Xodo sign**
- Page 5
    - Annual Gross Income - ==What is the mapping for this field?==
    - Married Status - ==What is the mapping for this field?==
    - Family Size, Including Yourself - ==What is the mapping for this field?==
    - Amount of Total Federal Student Loan Debt - ==What is the mapping for this field?==
    - Current Loan Monthly Payment - ==What is the mapping for this field?==
    - Estimated Interest Rate - ==What is the mapping for this field?==
    - Estimated Months to Repay - ==What is the mapping for this field?==
    - Estimated New Monthly Payment - ==What is the mapping for this field?==
    - Client's Total Debt Amount - ==What is the mapping for this field?==
    - Fee Directly Payable to Group Advantage Corp - ==What is the mapping for this field?==
    - Service Plan - ==What is the mapping for this field?==
    - Signature - **Filled by Xodo sign**
    - Initial (Footer) - **Filled by Xodo sign**
- Page 6
    - Client’s Service Fee for services rendered is $`{service fee amount}`, - ==What is the mapping for this field?==
    - Payment schedules for each program - **This will require us to replace what is currently in the word document and dynamically update it to include the payment schedules for the individual services. This requires further discussion on how this can be done.**
    - Client Signature - **Filled by Xodo sign**
    - Date - ==What is the mapping for this field?==
    - Initial (Footer) - **Filled by Xodo sign**
- Page 7
    - I, `{client name}`, hereby acknowledge... - ==What is the mapping for this field?==
    - Client signature - **Filled by Xodo sign**
    - Date - ==What is the mapping for this field?==
    - Initial (Footer) - **Filled by Xodo sign**
- Page 8
    - I `{client name}`, the Client... - ==What is the mapping for this field?==
    - The total Service Fee of $`{service fee}`US dollars... - ==What is the mapping for this field?==
    - Check the type of credit card - ==What is the mapping for this field?==
    - CC Number - ==What is the mapping for this field?==
    - Expiration Date (DD/MM/YYYY) - ==What is the mapping for this field?==
    - Security Code - ==What is the mapping for this field?==
    - Name of Credit Card Holder - ==What is the mapping for this field?==
    - Billing Address - ==What is the mapping for this field?==
    - Signature of Card Holder - **Filled by Xodo sign**
    - Initial (Footer) - **Filled by Xodo sign**
- Page 9 - ACH Authorization - This page will be removed

