---
cssclasses:
  - full_width
Related:
  - "[[Sushchnosti/FIN Searches/FIN Searches|FIN Searches]]"
---
# FIN Searches - Meetings
## Friday, October 31, 2025

- [86acq3b4v – Dropdown options are not being filtered for the "Investment Strategy" | complete | Mostofa Reza](https://app.clickup.com/t/86acq3b4v)
    - Fixed the bug where the investment strategies filter weren't getting narrowed down in the "/documents-search" page . This was a bug reported by Matt Poremba.
- [86aakpj54 – Add a toggle ON RIA firm Search | complete | Mostofa Reza, Bao Do Van](https://app.clickup.com/t/86aakpj54)
    - Added the "Any or All Firm Types" filter in the "/firm-search", "/firm-holding", and "/contact-search" pages. This was requested by Matt Poremba.
- [86acm7y7t – Make updates to "Firm Aliases and Affiliates" section in "/firm-details/{id}" page | complete | Vu Nguyen](https://app.clickup.com/t/86acm7y7t)
    - Renamed the "Firm Aliases and Affiliates" to "Teams and Affiliates". Renamed the "Alias Name" column to "Team/Affiliate Name". Prevent duplicate team/affiliate names to be created.


- [86abzqg5w – Add "Minority Owned" data to data.finsearches | complete | Vu Nguyen](https://app.clickup.com/t/86abzqg5w)
    - 
- [86abzqfv9 – Add "Acquired by..." to data.finsearches | complete | Vu Nguyen](https://app.clickup.com/t/86abzqfv9)
    - Added the "Acquired by" label to the left card in the "/manager-details\{id}" page.
- [86acj629z – Fix overlapping controls in the firm-details page | complete | Zulqarnain Niazi](https://app.clickup.com/t/86acj629z)
    - Fixed controls that were overlapping with the heading in the "Contacts" section in the "/firm-details/{id}" page.
- [86ac7pr1x – Infinity search button | complete | Mostofa Reza](https://app.clickup.com/t/86ac7pr1x)
    - Added the Infinity search button to the "/plan-details/{id}" page. This is only accessible by admins.
- [86acr2p84 – Add captcha for the forms at v1 | complete | Mikhail](https://app.clickup.com/t/86acr2p84)
    - Added the re-captcha to the finsearches.com website
- Thumbnails URL 
---
- Follow-up with Matt McCue

## Friday, October 17, 2025

- Moved different admin permissions to current site 
    - `/firm-details/{id}`
        - [86ac2x7au – Allow Add/Edit/Delete Firm Alias | complete | Vu Nguyen](https://app.clickup.com/t/86ac2x7au)
            - https://data.finsearches.com/firm-details/10587 - In the "Firm Aliases" section
        - [86ac3b870 – Allow Add/Edit/Delete Research Note on Firm Detail page | complete | Vu Nguyen](https://app.clickup.com/t/86ac3b870)  
            - https://data.finsearches.com/firm-details/10587 - In the "Research Overview" section
        - [86ac77m1r – Implement "Click the # of Employees in Offices grid" feature | complete | Vu Nguyen](https://app.clickup.com/t/86ac77m1r)  
            - Added feature where clicking on the number in the "Company Offices" section will scroll-up to the "Contacts" section and filter by that particular office.
        - [86ac8b48q – Allow Edit Clients section | complete | Vu Nguyen](https://app.clickup.com/t/86ac8b48q)  
            - Added the admin control to edit clients in the "Clients" section.
        - [86ac8dk6r – "Move Contacts to New Firm" feature | complete | Vu Nguyen](https://app.clickup.com/t/86ac8dk6r)  
            - Added the admin control to allow moving a contact to a new firm. There's some improvement that this needs to go through. There's a bug where the control will overlap with the text. There's a ticket to get this taken care of. I'm thinking that these could be reduced to just icons at smaller screens.
        - [86ac8b3j5 – Implement website section | complete | Vu Nguyen](https://app.clickup.com/t/86ac8b3j5)  
            - Added the website section to the firm details page. This includes the admin controls to manipulate the entries. Only non-primary websites can be deleted and only websites that were manually added can be edited.
        - [86ac77r32 – Allow Edit Services | complete | Vu Nguyen](https://app.clickup.com/t/86ac77r32)  
            - Added admin feature that allows editing the "Services" section in the firm-details page.
        - [86ac77qx0 – Allow Edit Compension | complete | Vu Nguyen](https://app.clickup.com/t/86ac77qx0)  
            - Added admin feature that allows editing the "Compensation" section in the firm-details page.
        - [86ac3b9ax – Implement CRUD for Service Provider | complete | Vu Nguyen](https://app.clickup.com/t/86ac3b9ax)  
            - In the "Service Providers" section, we've added the ability to create, edit, and delete service providers.
        - [86ac53uvg – Allow Add/Edit/Delete Firm Office | complete | Vu Nguyen](https://app.clickup.com/t/86ac53uvg) & [86ac53uzm – Implement "Merge Firm Office" feature | complete | Vu Nguyen](https://app.clickup.com/t/86ac53uzm)  
            - https://data.finsearches.com/firm-details/10587 - In the "Company Offices" section, we have the admin controls to merge firm offices and to create, edit, and delete offices. 
        - [86accqp42 – Add "Public" column to Research Note grid | complete | Vu Nguyen](https://app.clickup.com/t/86accqp42)  
            - https://data.finsearches.com/firm-details/9521#research-overview - (Not an admin control) A public column was added for the research notes
    - `/contact-details/{id}`
        - [86accqp07 – Allow Add/Edit/Delete Research Note on Contact Detail page | complete | Vu Nguyen](https://app.clickup.com/t/86accqp07)  
            - https://data.finsearches.com/contact-details/755111 - In the research section
        - [86ac53v00 – Implement CRUD for Contact Nickname | complete | Vu Nguyen](https://app.clickup.com/t/86ac53v00)  
            - https://data.finsearches.com/contact-details/755111 - In the "Nicknames" section, we can now add nicknames.
    - `/contacts/blocklist`
        - [86ac21201 – Contacts Blocklist Management | complete | Vu Nguyen, Mikhail](https://app.clickup.com/t/86ac21201)
            - https://data.finsearches.com/contacts-blocklist -  Added admin page at `/contacts/blocklist` that allows you to add exclusions to the LinkedIn import.
- General
    - [86abz5dt7 – Hide the firm name column by default in the firm details page | complete | Zulqarnain Niazi, Josh Jennings](https://app.clickup.com/t/86abz5dt7)  
        - We hide the 
    - [86ac9m255 – Update the URL for Infinity chat | complete | Vu Nguyen](https://app.clickup.com/t/86ac9m255) 
        - Changed the "universal-chat" route to "infinity-chat".
    - [86abzrf73 – Enhance Plan Dropdown Search Functionality | complete | Vu Nguyen](https://app.clickup.com/t/86abzrf73)  
        - https://data.finsearches.com/mandate-search - Enhanced the "Plan" dropdown menus across the site to pull relevant results for both aliases and full names. For example, "calpers" will return entries for "California Public Employees' Retirement System". Acronyms can be added on the V1 site when creating a new plan.
        - Acronyms to use: calpers, sfers, MWRDRF, and SAMCERA
    - Adding the ability to scroll within maps
- Bug fixes
    - [86abxxjq9 – Universal Search - Speech to Text | complete | Mostofa Reza, Mikhail, Bao Do Van](https://app.clickup.com/t/86abxxjq9)
        - Hitting the "X" before would clear the previous results. Now, it only clears the input
    - [86acb10ud – Video thumbnails are black on v1 & v3 site | complete | Bao Do Van](https://app.clickup.com/t/86acb10ud)  
        - We fixed the black thumbnails as you already know. We have a follow-up task that will allow you to app the URI of the thumbnail in the V1 site. Josh just needs to redeploy the site for this to be taken into effect.
    - [86acb8mbm – User activity search filters not running when hitting "Search" button | complete | Bao Do Van, Zulqarnain Niazi](https://app.clickup.com/t/86acb8mbm)  
        - https://data.finsearches.com/user-activity-search - Fixed search filters not running on the "/user-activity-search". Searching can now be performed
    - [86ac0wtjg – Controls for Firm Holdings overlap with text | complete | Zulqarnain Niazi](https://app.clickup.com/t/86ac0wtjg)
        - https://data.finsearches.com/firm-details/10587#firm-holdings - Fixed issue with the controls for the firm holdings section overlapping other parts of the UI when the left panel was closed.
        - ![[Attachments/Pasted image 20251017100733.png]]

## October 3, 2025

- What were the goals for the week?
- What extras did we get added?
- What problems did we solve?
- What ideas were created?

---

The main focus of this week has been:

- Bug fixes
- Improvements to the Universal Search
- Improvements to the Infinity Chat
- Progress on moving the site
    - Responsiveness
    - Cross-browser compatibility
    - Migration of the admin controls

---

- Date sorting is currently in developer review, but hasn't been merged yet — [86abxmbc6 – Fix date sorting across application | developer review | Zulqarnain Niazi](https://app.clickup.com/t/86abxmbc6)
- ["Terms & Conditions" and "Privacy" links in footer are not clickable](https://app.clickup.com/t/86ac6ctek) - The pages didn't exist in the new site

## September 26, 2025

- Show them what Bao has done for the AI chats: https://gentle-moss-01d780c0f-dev.eastus2.1.azurestaticapps.net/
    - https://gentle-moss-01d780c0f-dev.eastus2.1.azurestaticapps.net/plan-details/16377 - drawer with button in header
    - https://gentle-moss-01d780c0f-dev.eastus2.1.azurestaticapps.net/document/476563 - panel on the left
- Ask them how they'd like to have updates
    - ClickUp
    - CSV (Tab Delimited)
    - Excel
- [Bao saying what was pushed to production](https://deltadesk.slack.com/archives/C08JPKUC5M4/p1758857408807679)
    - [https://app.clickup.com/t/86abwhwd2](https://app.clickup.com/t/86abwhwd2) - Add the ability to filter for Security Type
    - [https://app.clickup.com/t/86abwj5xg](https://app.clickup.com/t/86abwj5xg) - Add filters to 13F search page
    - [https://app.clickup.com/t/86abz4qd2](https://app.clickup.com/t/86abz4qd2) - Universal Search - Version 2
        - Improved the universal search
    - [https://app.clickup.com/t/86ac3tn0a](https://app.clickup.com/t/86ac3tn0a) - Pagination on universal search page
        - Removed the pagination and limited the results to 
    - [https://app.clickup.com/t/86ac0wqy7](https://app.clickup.com/t/86ac0wqy7) - Enhance User Activity to add duration and add logs for Firm Holding search
        - 
    - [https://app.clickup.com/t/86abv66e2](https://app.clickup.com/t/86abv66e2) - Remove White Spacing Above and Below Placeholder Contact Photo
    - [https://app.clickup.com/t/86abvbr3b](https://app.clickup.com/t/86abvbr3b) - Inconsistencies with Area codes
- Big projects:
    - Moving of admin controls to new site
    - Responsiveness and browser consistency
- FIN Searches - Site Demo
    - [[Tasks/Completed/2025/Task - Get a demo of the FIN Searches platform#^tgwio0]]
- [86ac3tjah – Consultant data not loading when using chrome | to do | Josh Jennings, Bao Do Van](https://app.clickup.com/t/86ac3tjah)