# NSDFC Report (October 9, 2025 to November 3, 2025)

**86acyxp73 - Link to update Credit Card Info - complete**

Removed the option to select a bank account for the create payment profile page since the systen currently only supports credit cards.

**86acyttqr - Your Payment Is Due In 7 Days - REF0012897837 - How did this client receive a payment reminder? - complete**

Resolved issue with contact receiving a reminder email when they shouldn't have.

**86acx84kn - Insert and Send reminders for new Recert payments - complete**

Added and sent reminders for recertification payments.

**86acq0dc6 - Remove N/A status from the "Welcome Packet" and "Rehab" workflows - complete**

Removed all "N/A" statuses from the "Welcome Packet" and "Rehab" workflows.

**86acnk69w - The "Unresponsive" status is being set over and over for the "Welcome Packet" workflow - complete**

Fixed the issue where the "Unresponsive" status was being set over and over in the "Welcome Packet" workflow. Requested by Kanako Lino.

**86acnk0wc - Remove "Cancelled" status from disability workflow - complete**

Removed the "Cancelled" status from the disability workflow. There was already a status named "Canceled". The spelling with one "l" is used throughout the application.

**86acn6677 - Add Request payment profile feature - complete**

Added feature that requests a contact to provide payment information. This is in the "Accounting" tab of the contact profile. If a contact doesn't have information, it'll be added. Else, it'll update the information.

**86acmf2kx - Need to add a payment Brittany Licitra DOE0018171718 - complete**

Added and scheduled a payment of $447.00 for February 16, 2026 for Brittany Licitra. Requested by Kathleen Kenney.

**86acmdbv8 - Update organization page - ready for deployment**

Updated the organization listing page by adding an "Organization Acronym" column. Updated inputs to use this new name. This allows you to filter by an organization's acronym.

**86acmdaw6 - Remove email automation that occurs after a new FSA text file is uploaded to the CRM - ready for deployment**

Removed the automation that tells a contact that it is time to schedule an appointment. Requested by Josef Basmagy.

**86acjrdna - Check logic to log out the user when the token is expired - ready for deployment**

Updated logic to log out users after an idle period of two hours.

**86acjrcvb - Investigate the files without extension - complete**

Investigated and resolved issues relating to files uploaded without extensions.

**86acjrcg9 - Update color for Estimated tag - complete**

Updated the color of the estimated tags to be red. This was done to differentiate the payments that are estimated versus actual at a glance.

**86acjq0t2 - Client unable to download files - complete**

Resolved issue where files where unable to be downloaded.

**86acj47zn - If status is cancelled, highlight the card in red - complete**

Added red highlight to all cards that have a status of "Canceled" in the "Status Quick View" sidebar.

**86acj4693 - Reschedule Kathleen's payment - complete**

Rescheduled Kathleen's payment for Victoria Pucci.

**86acj1ztz - Payment Amount doesn't seem to be saving - complete**

Fixed issue where the payment amount was disappearing after saving and returning to the profile tab in the contact profile.

**86acj1k91 - Give Kathleen access to SMS - complete**

Fixed issue with Kathleen not having access to the SMS feature.

**86achju5g - Add a "Sales Application" document type - complete**

Added the "Sales Application" document type to the "File" tab in the contact profile.

**86achgkkt - Only show forms for the department of the user - ready for deployment**

Updated the forms dropdown to add labels for the forms of each department. Originally, it was suggested to not show forms outside of someone's department. However, this caused issue with some people not seeing any forms.

**86ach2mqx - Update inputs to reflect the permissions they have - complete**

Updated inputs to have a light gray background for inputs that a user doesn't have the permissions to interact with. Also updated the text "Drivers" to "Driver's".

**86acgvagy - Add a tag next to the payment profile that says "3rd Party Payer" - complete**

Added a tag next to the payment profile so you can see if it is setup to use a 3rd party payer at a glance.

**86acgv9yc - Add columns to the dashboard - complete**

Added the following columns to the dashboard: Email, Phone Number, and Salesperson.

**86acgv913 - Show all future tasks by default - complete**

Updated default filtering to show all future tasks by default.

**86acek93f - Update the "Send Form" action to "Send for E-Signature" - complete**

Updated the "Send Form" action to be "Send for E-Signature" in the "Forms" tab of the contact profile.

**86acek88a - Specify that the age of an item is days - complete**

Added label to show that "Age" is the number of days since a date.

**86acejxth - Format numbers with a comma between groups of three - complete**

Updated how numbers are formatted. Numbers will now have commas in them.

**86acejwkm - Update the "Delete" action in action menus - complete**

Updated the "Delete" action in menus to always be at the bottom and to have red text. Hovering the button will show a red background.

**86acejvgd - Change the text of "InTake" to "Intake" - complete**

Corrected the spelling of the word "InTake" to "Intake".

**86acejtrx - Sort workflow statuses on dashboard in alphabetical order - complete**

All workflow statuses are now ordered alphabetically on the dashboard.

**86acea821 - Add "Billing Invoice" file category - complete**

Added "Billing Invoice" to the "File Category" dropdown in the "Files" tab of the contact profile.

**86ace6y3d - Updates to Income and Tax Info and "Is Public Service?" field - complete**

Moved the "Is Public Service?" input to the first row in the contact profile. Updated how the "Is Public Field?" works. It will no longer have a default value which forces users to make a conscious decision on what type of contact it is.

**86acd2jvf - Notify the user about an incoming call. - complete**

Added notifications that appear in the bottom right corner when a user is receiving a call from a client. This notification allows a user to go to the contact's profile. If the call is missed, the notification will say that the call was missed.

**86acb8vmu - Workflow adjustments - complete**

Added a "Canceled" status to every workflow. Removed the ability to select "N/A" as a status for all workflows. Removed all "N/A" statuses from the "Accounting" workflow. Requested by Natalie Luongo.

**86acb7g9e - Changes to how editing notes is handled - complete**

Changed how note editing is handled. Notes can now only be edited by the person who originally created the note. Other users can respond to a note and edit their own responses. The UI has been updated to show replies in the table.

**86acb6q6a - Email overkill - complete**

Changed functionality when sending out a UTF agreement. Originally, two emails were sent out. One for the Xodo sign document and a second reminder email. The reminder email is now delayed. It won't be be sent until three days after and will be sent every three days until thirty days have passed.

**86ac89p4p - Remove some categories from "Create New Note" dropdown - complete**

Removed the following categories from the "Create New Note" modal: "BlueRock", "Client Portal", "Google Review", and "PROCESSING NOTE".

**86ac62f0z - Clicking "lightbulb" causes form modal to display everything errored - complete**

In the "Add Form" modal, clicking the lightbulb icon next to the "Pages To Send" input would cause the whole form to error. This bug has been fixed.

**86ac61ndk - Payment plan can be deleted, but the estimated payment plans do not automatically disappear - ready for deployment**

Originally, if a payment plan was deleted and it was an estimated payment plan, the estimated payment plan wouldn't disappear. Now, the estimated payment plan will also be removed.

**86ac1e85p - Add entries to "Missing Documents" dropdown - complete**

Added "Date of Birth" and "Social Security Number" as options to the "Missing Documents" dropdown in the contact profile. Requested by Kanako Lino.
