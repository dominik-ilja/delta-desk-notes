---
Complete: false
Tasks: 59
Tasks Remaining: 1
Tasks Complete: 58
Date Completed:
---

# Josh Jennings meetings

- [ ] This question comes from Bao. He was wanting to know how we should proceed with migrating the child pages of admin features:
      ![[Attachments/Pasted image 20250930080955.png]]

## Wednesday, October 22, 2025



## Tuesday, October 21, 2025

- [x] Bao - https://app.clickup.com/t/86ace9164?comment=90130181119842
- [x] Vu - https://app.clickup.com/t/86acj1vvb?comment=90130179294475
- [x] Get access to Sanity [Completed:: 2025-10-21T13:38]
- [x] Mikhail says that the button click automation is ready #Focus
- [x] This is ready for you to review - [86acg44xp - Automate Recons - developer review (Carrick Lane)](https://app.clickup.com/t/86acg44xp)
- [x] Mikhail is unsure of if this is working or not and wanted to check in with you. [86abv6dt2 - Fix Document Export and Check Other Exports - ready to start (FIN Searches - Backlog)](https://app.clickup.com/t/86abv6dt2)

## Monday, October 20, 2025

- [x] tell him about the OB appointment

## Friday, October 17, 2025

- [x] [86acg3b3q – Populating agreements - Mapping | ready to start | Vu Nguyen](https://app.clickup.com/t/86acg3b3q)
    - [x] I'm waiting for confirmation on the New Monthly Payment logic from Josh.
    - [x] Do you mean that whenever the New Monthly Payment is 0, we don't allow adding a new form—or just don't allow adding a new Group Advantage Agreement form, or any form that has a New Monthly Payment field in it?

## Wednesday, October 15, 2025

### 12:30

- [x] I need him to run SQL query to fix Kathleen's issue
- [x] I need him to run SQL query to finish the workflow adjustments
- [x] Guys, can we add a button on the payment profile that says request credit card information? It will send an email to the client with a link to the authorized net form for them to fill out. - Should it be shown if they already have a payment profile. --- ==Yes we should show this no matter what==
- [x] 3rd party authorizations
  - [x] I need him to answer the questions for Bao to do the 3rd party authorization forms
  - [x] How do we get the total amount due for a third party payer form?
  - [x] To populate the 3rd party payer form, we would use the name from the payment profile or is this incorrect?
- [x] Let's talk about the field mappings for the form - A user has different quotes that they qualify for. When Natalie set the "Change of Repayment" and "Annual Recertification with PSLF" amounts to $0, they're charging $0 for their that service. It looks like they would pay this amount for the service. Would NSDFC be in charge of the loan then and make money off of the interest? I'm trying to understand their business model better. When we generate a form, it should be pulling the information of their debt, previous monthly payments, and the updated amounts. The updated amounts would be determined by the quote, correct? I guess how do the services and the programs work together?
      ![[Attachments/Pasted image 20251015102740.png|300]]
- [x] For the "Fee Directly Payable to Group Advantage Corp", this should be $0 based on Natalie overriding the amount. ==The only field to fix the "Estimated New Monthly Payment"==
      ![[Attachments/Pasted image 20251015103232.png]]
- [x] https://outlook.office365.com/mail/nsdfc@deltadesk.com/inbox/id/AAQkADcxZTE1NjdmLTM4OTYtNDIwMy1iMjJkLWRjZmQzMDM1YWE4NAAQALPQkB%2BmUETbnLkUTEzGtJE%3D
- [x] https://outlook.office365.com/mail/nsdfc@deltadesk.com/
- [x] Can we talk about the recertification page
- [x] Mention that Zulqarnain is doing a good job
- [x] Bring up Orical and the issues that come with Brevo.

## Monday, October 13, 2025

### Next

- [x] Could you ask for NSDFC to send a PDF that can be filled out for the 3rd party authorization form - I'll ask Bao if Luke was doing this sort of thing
- [x] Tell him about how I'm planning on laying out my day: [[Daily Outline]]
- [x] How does a payment go from estimated to actual
- [x] What is a sponsor within the NSDFC system?
- [x] After talking with Bao, I learned that a third party payer form is generated for: "UTF Service Agreement", "Group Advantage Agreement", "NSDFC Loan Watch Agreement", and "Credit Card Authorization" when the payment profile is a third party payer. I also learned that they only send forms to the contact profile not the third party payer. For example, if the profile is
- [x] What's left to be done for NEOS?

- The new third party authorization form has ACH as an option, but we don't currently support ACH.

### Covered

Okay, so let's summarize our report for Josh:

- The service price has been set to $0 which is the reason for the form populating as $0.

## Friday, October 3, 2025

**Overdue tasks of Josh to Review:**

- [86a9q6e8k – Proc_No_47_QBO_Customers.xlsx | to do | Josh Jennings](https://app.clickup.com/t/86a9q6e8k)
- [86a9q6f50 – Proc_No_47_QBO_Invoices.xlsx. | to do | Josh Jennings](https://app.clickup.com/t/86a9q6f50)
- [86a9q6gz9 – Proc_No_47_QBO_Receive_Pmt.xlsx | to do | Josh Jennings](https://app.clickup.com/t/86a9q6gz9)
- [86aa9mtbu – Create Proposal for David Chau | to do | Josh Jennings](https://app.clickup.com/t/86aa9mtbu)

**Tasks Josh needs to review:**

- [x] [86ac3x9qq – Improve Bluerock Call Record Mapping | internal review | Bao Do Van, Mikhail](https://app.clickup.com/t/86ac3x9qq)
- [x] [86ac6k1t7 – ETF page | internal review | Zulqarnain Niazi](https://app.clickup.com/t/86ac6k1t7)
- [x] [86abzwf5t – Get rid of [UserToChatServUser] table | internal review | Mikhail, Bao Do Van](https://app.clickup.com/t/86abzwf5t)
- [x] [86ac6auq4 – Upload New Data page | internal review | Zulqarnain Niazi, Bao Do Van](https://app.clickup.com/t/86ac6auq4)
- [x] [86ac6auv6 – Upload Data section | internal review | Zulqarnain Niazi](https://app.clickup.com/t/86ac6auv6)
- [x] [86abxxjq9 – Universal Search - Speech to Text | internal review | Mostofa Reza, Mikhail, Bao Do Van](https://app.clickup.com/t/86abxxjq9)

**Developer Questions:**

- [x] [86abvbr3b – Inconsistencies with Area codes | in progress | Mostofa Reza, Zulqarnain Niazi](https://app.clickup.com/t/86abvbr3b)

## Thursday, October 2, 2025

- NSDFC
  - Email from John: "LeTip0018191206 Mary Perez"
- [x] FIN Searches
  - [x] How to spell Gene Dilinsky's name
  - [x] Testing:
    - [x] [Universal Search - Speech to Text](https://app.clickup.com/t/86abxxjq9) - I've found bugs where this includes noises. Also, I wanted to discuss with you the behavior of pressing the "X" in the search. It clears out the previous search results altogether. I think the old results should stay until a new search is performed.
    - [x] I can run this query, but would need to be given the information to connect to the DB. Else, you could do the testing - https://app.clickup.com/t/86ac1157m?comment=90130172901109&threadedComment=90130172994487
    - [x] [86abz40vq – Have FIN Searches subscriptions expire the day after rather than the day of | internal review | Mikhail](https://app.clickup.com/t/86abz40vq) - Mikhail responded, but I'm not sure it answers your question

### 10:24

3:00 -
12:00 -

## Wednesday, October 1, 2025

- [x] Developer Updates
  - [x] Vu
    - [x] Vu has made the changes for Chart National. We're now waiting on to hear if Mohamed is added to their team or not. In the [ticket](https://app.clickup.com/t/86ac6ycqj), I requested Vu to make two branches, so if Mohamed is joining we can deploy that branch immediately. I've reviewed both and they look good.
    - [x] Vu also added the check dropdown item for NSDFC. I tested it and found that the option doesn't show up in the edit functionality. ~~He needs to make additional changes to that.~~ He made the changes and this is good to be merged to production.
  - [x] Mostofa
    - [x] He's implementing the feedback I gave him for OMS
    - [x] I checked his spreadsheet and it looked like there's 13 pages that need worked on. I wanted to get confirmation from him about this. Maybe he didn't update the spreadsheet yet. There's 8 pages left: Mandate changes, Add Client, Close/Reduce PUTS, Performance, Billing - Actual, Billing - Estimated, Add Order, Allocations
  - [x] Bao
    - [x] Working on NEOS. Wants me to make sure Mostofa is understanding the logic for the OMS.
  - [x] Zulqarnain
    - [x] He's feeling good. He's working on multiple pages of the NEOS project. He's done the upload data and ETF page. Bao will test what he's done
- [x] Comments
  - [x] On the sites that we make, we have these "slide-in" animations. This animation should only happen once, but every time a section goes out of view it'll redo the animation again.
- [x] Admin on computer: https://support.lenovo.com/us/en/solutions/ht513708-how-to-set-administrators-account-in-windows-11

- [x] ![[Attachments/Pasted image 20251001112726.png|200]] I'm seeing these emails in NSDFC. Did you setup an automation to tell them about the payments being run for the day?

## Tuesday, September 30, 2025

- I've gone through and captured all the tasks that were in slack
- This question comes from Bao. He was wanting to know how we should proceed with migrating the child pages of admin features:
- ![[Attachments/Pasted image 20250930080955.png]]
- [86abvbr3b – Inconsistencies with Area codes | in progress | Mostofa Reza, Zulqarnain Niazi](https://app.clickup.com/t/86abvbr3b)
