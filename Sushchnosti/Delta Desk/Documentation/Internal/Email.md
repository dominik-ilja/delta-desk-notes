# Email

Emails should be responded to as quick as possible. If you cannot answer a clients question in that moment, then simply let them know that you’ll be getting back to them. Add a tag to the email to let yourself know that you have an email to attend to.

## Categories

Outlook is the email client we use at Delta Desk. We use different “Categories” to know the state that an email is in. Most categories are grouped into pairs. One tag indicates an action needs to be taken while the other says the action has been completed. For example, “To Respond” and “Responded”.

Currently, we have the following categories:

- **To Review:** Email needs to be read.
- **Reviewed:** Email has been looked at.
- **To Respond:** Need to send an email response.
- **Responded:** Sent an email response.
- **Awaiting Response:** Waiting for an email response. Communication isn't finished.
- **Add to ClickUp:** Email contains task that need to be added to ClickUp.
- **Added to ClickUp:** Task from email was added to ClickUp.
- **To Document:** There's information in the email that needs to be added to documentation.
- **Documented:** The information in the email has been documented.
- **Incomplete:** Some things relating to the email have not been completed. For example, the ClickUp task hasn't been finished
- **Completed:** Everything from the email has been completed
- **Important:** The email is of high importance.
- **ClickUp - `{n}`:** The related ClickUp ID. This always keeps the ID number visible. For example, "ClickUp - 86abwcdcx"

An example flow would look like this:

1. Email is received. Apply the “To Review” category. **Current Categories**: To Review
2. Read the email. Apply the “Reviewed” and “To Respond” categories and remove the “To Review” category. Current Categories: Reviewed, To Respond
3. Respond to the email. Apply the “Awaiting Response” category and remove the “To Respond” category. Current Categories: Reviewed, Awaiting Response
4. Receive a response. Apply the “To Review” category and remove the “Awaiting Response” and “Reviewed” categories. Current Categories: To Review
5. Review the email. You found that there’s something that should be added to ClickUp and needs to be documented. Apply the “Add to ClickUp” and “To Document” categories and remove the “To Review” category. Current Categories: Add to ClickUp, To Document
6. You add the ClickUp item and the document. You also see there’s nothing else to do. Apply the “Added to ClickUp”, “Documented”, and “Complete” categories and remove the “Add to ClickUp” and “To Document” categories. **Current Categories**: Added to ClickUp, Complete, Documented

## Rules

#Todo 

## Including ticket numbers in email

When responding to a client that a ticket has been created, we should also tell them the specific task ID. For example, in ClickUp, a task will have an ID that looks like this: “86ac1g1bu”.

An example email could have the subject line: “86ac1g1bu - Task was created” and the body could look like this:

```
Hi John,

Our developers are looking into this. The ID is "86ac1g1bu".

Thank you,
```

In Outlook, we could then use the search feature to find the task ID. The task ID can be found in the email itself as well as the subject line.

### Forwarding

You can forward emails to yourself, so that you can include the ClickUp ID in the subject line or email body. If you do this, remember to only include emails within Delta Desk. Let’s say you have a shared email like “nsdfc@deltadesk.com”. You’d want to the “To” portion of the email be “nsdfc@deltadesk.com” and the subject line could be “ClickUp ID - 86ac1enx9”.

```
Subject: ClickUp ID - 86ac1enx9
To: nsdfc@deltadesk.com
---
ClickUp ID - 86ac1enx9
```