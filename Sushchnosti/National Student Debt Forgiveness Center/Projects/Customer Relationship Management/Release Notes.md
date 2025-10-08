---
aliases:
cssclasses:
  - full_width
tags:
Related:
  - "[[Sushchnosti/National Student Debt Forgiveness Center/National Student Debt Forgiveness Center|NSDFC]]"
Sources: []
Type: Documentation
---
# Release Notes
## Monday, October 6, 2025

**Tasks Completed:**

86aby3j1e – Updated recertification workflow statuses and assigned the “Recert Pending Review Email” to the “Recertification Pending Review” status.
86a9dux23 – Fixed task statuses not updating
86abhmcpj – Added payment process options on contact details -> accounting tab
86abju181 – Added payment type column and edit capabilities
86abjwbt5 – Added employer numbers to employer cards
86abpbynb – City and state can be auto-populated from zip code
86abpbzg7 – Added ability to manually enter date On all date pickers
86abre3rw – Added new statuses for payments by service report
86abt0bqc – Added green banner to contacts who are a public service
86abrnk7m – Fixed overflow of long menu item in /contact/id > workflow
86abt6k2u – Fixed error creating email template
86abu7zvn – Add send invoice button and PDF preview to "Generate Invoice" flow
86abv7qvb – Reordered the workflows on the dashboard page
86abv7ujj – Added 3rd Party Payer CC Authorization Form
86abvbrth – Added ability to update status while maintaining date
86abw05pp – Improved the UX of the SMS message filtering
86abw0tb3 – Re-enabled ability to edit "File Number" prefix
86abw9rjb – Updated the default date range filter on tasks page to today
86abw9t2u – Added Organization to Contract Received Report
86abwjkcq – Updated Layout On Profile -> Income and Tax Info Section
86abwm0fx – Removed "In Reminder" status from the dropdown
86abxwt87, 86abt10yv – Added a "User Assigned" filter to the pipeline report. This used to be "Salesperson".
86abwrnrt – Fixed payment reminder email even though a contract wasn't signed
86aby445m – Added report called "Upcoming Payments" to the Reports page
86aby8dwn – Made every dropdown alphabetical unless there's a good reason for it not to be
86abyj59q – Added "Check" as a document type option
86ac1enx9 – Reverted "Is Public Service" to default to "No"
86ac1eyuv – Fixed "Request Missing Document" modal not closing when hitting "Cancel" button
86ac1fg3k – Removed support link in the profile menu. Fixed the "Settings" link to go to settings page
86ac3q8xr – Fixed issue with estimated payments showing on accounting page
86ac3qart – Updated and added buttons to header for email and SMS
86ac3u3d6 – Fixed overflow on Dashboard
86ac55ex1 – Made all dropdown options were made consistent throughout the website
86ac88txe – Added automation for "Not Interested" Intake status
86ac8akmw – Fixed breadcrumbs turning into light/dark mode toggle at smaller screen sizes

**Known Issues:**

86ac9tm83 - In the communications tab of the contact profile, the date range will sometimes not filter properly
86ac62f0z - Clicking the "lightbulb" in the "Add Form" modal will causes all inputs to error
86ac88r5c - Bad debt issues showing up in upcoming payment report despite no scheduled payment
86ac9u5ry - Recert Pending Review Email will still run even if "Submitted to Servicer" workflow step is deleted

**Other:**

Payment profiles have been created for contacts that have unexpired credit card numbers.
Every week at 9 AM Monday, an email will be sent that contains information about email failures.
Daily email to Kathleen on the number of payments run and how many succeeded and failed.

## Friday, October 3, 2025

- Added a "User Assigned" filter to the "Pipeline Report". This was originally called "Salesperson"  (86abt10yv, 86abxwt87)
- Added the ability to manually enter dates in date pickers (86abpbzg7)
- Added the ability to change a status within a workflow step will maintaining the creation date (86abvbrth)
- Added auto-population of city and state fields. This happens when you enter a zip code (86abpbynb)
- Added "Upcoming Payments" report to the reports page (86aby445m)
- Fixed issue with manual dates on synchronizing with date picker (86abwp3wy)
- Fixed issue with not being able to create email templates (86abt6k2u)
- Improved SMS messages in contact profile. The "direction" dropdown now has an "All" option by default for seeing both inbound and outbound message types (86abw05pp)
- Removed estimated payments from accounting tab
- Added banner changed based on the "Is Public Service" of a contact. If it is a public service, then the application header will be green. (86abt0bqc)
- Added an "Organization Name" column to the "Contract Received Report" (86abw9t2u)
- Reverted the default value of "Is Public Service" to "No" (86abrvpgf, 86ac1enx9)
- Updated the ordering of the workflows on the dashboard (86abwm0fx)
- Added numbers to employer cards in the contact profile (86abjwbt5)
- Added filters for the different statuses in the "Payments By Service Report" (86abre3rw)
- Updated dropdowns to be sorted in alphabetical order (86aby8dwn)
- Updated layout of the contact profile's "Income And Tax Info" (86abwjkcq)
- Fixed issue with payment reminder being sent for estimated payments (86abwrnrt)
- Added payment type column to appropriate tables and the ability to edit (86abju181)

---

Keeping these, but won't use them

- September 30, 2025
    - Removed estimated payments from accounting tab
- September 26, 2025
    - [86ac42f0h](https://app.clickup.com/t/86ac42f0h) - Payments page fixes
        - Fixed date picker controls
        - Set new defaults to filters
            - Default to only showing scheduled payments
            - Sort by scheduled date
            - Show last seven days
- September 24, 2025
    - [86ac23edg](https://app.clickup.com/t/86ac23edg) - Fixed issue where future payments couldn't be selected in the "Upcoming Payments Report"
    - [86aby8dwn](https://app.clickup.com/t/86aby8dwn) - Made dropdowns alphabetical unless there's a reason it shouldn't be
    - [86ac1g1bu](https://app.clickup.com/t/86ac1g1bu) - Fixed bug where payment profile information couldn't be updated
- September 19, 2025
    - [86abvbrth](https://app.clickup.com/t/86abvbrth)
