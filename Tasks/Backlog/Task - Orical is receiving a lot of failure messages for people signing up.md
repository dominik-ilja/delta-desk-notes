---
Complete: true
Tasks Complete: 4
Tasks: 4
Tasks Remaining: 0
Status: 0 - Not Started
State: 0 - Not Started
Priority: 0 - None
tags:
Due Date:
Start Date:
Date Completed: 2025-10-21
Date Created:
Last Updated: October 21, 2025, at 8:20 PM
Time Estimate:
Time Tracked:
Waiting On:
Docs:
GitHub:
Lists:
Related:
Sources:
ClickUp:
Type: Task
File Size: 2.58 KB
cssclasses:
  - full_width
---
# Task - Orical is receiving a lot of failure messages for people signing up

## Description

<span class="placeholder">No description</span>

## Task List

We're waiting for a response to our email.

### Completed

- [x] I need to get setup to receive error emails
    - [x] I need to get access to the info@deltadesk.com email
- [x] Get access to brevo
- [x] I need to get setup for Sanity [Completed:: 2025-10-21T16:29]

## Notes

These are some potential alternatives that we could use:

https://www.eventbrite.com/organizer/features/sell-tickets/
https://mailchimp.com/solutions/email-marketing-platform/

## Logs
### Tuesday, October 21, 2025

Ideas for resolving this issue:

- Remove the phone number
- Add a custom field for the phone number to prevent
- We look into a different solution that would be on an event-by-event basis

One of the things we can do for this is remove the phone number since that's causing the biggest issues. If they don't do SMS marketing, then this shouldn't be an issue. 

#### 18:21

Hello Madeline,

I've been personally looking into the issue. Here's what's happening. 

Brevo doesn't allow the same email and phone number to be used with multiple contacts.
When a user tries to sign-up with an email or phone number that's already in use, Brevo won't allow the contact to be created and you get the email about the sign-up failing.

After my research, I learned that Brevo isn't made to handle these kinds of event sign-ups. There's a couple of things we can do about this:

We could remove the phone number from the event sign-up. This is the simplest and most straightforward solution.
We could look into other services that are better suited for events. This would take time to research and implement but could allow us to get both an email and phone number.
We could keep things the way they are but have more descriptive emails sent to you. This could cause frustration for a user signing up when their phone number and email don't match. We'd miss more sign-ups.

I'm happy to jump on a call with you to go over these different options. I would recommend simply not requiring the phone number during sign-up unless you need it.

Thank you,


