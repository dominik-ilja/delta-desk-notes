# Bugs
## Bug-1 (Added)

**Description:**  

Multiple pages have white sections with white background in dark mode. They should match the dark mode background color.

**Tags:**  

- Bug
- Frontend
- UI

**Tasks:**  

- Update the mis-matched backgrounds in the following pages:
    - `/dashboard/contacts/{id}` - [[Attachments/Pasted image 20250910195014.png]]
    - `/dashboard/sms-calls-inbox` - [[Attachments/Pasted image 20250910204626.png]]

## Bug-2 (Added)

**Description:**  

When the navigation item "Public Service Loan Forgiveness" in `/dashboard/contact/{id} > Worflow` is selected, it is clear that the padding is not the same between the left and right sides. This is being caused by the section having a fixed width.

**Tags:**  

- Bug
- Frontend
- UI

**Tasks:**  

- Increase the width of the sidebar within the `/dashboard/contact/{id}` page. It should be wide enough that the "Public Service Loan Forgiveness" item doesn't overflow.

[[Attachments/Pasted image 20250910205415.png]]

## Bug-3 (Added)

**Title:** 

<span class="placeholder">No title</span>

**Description:**  

The "Snooze Date" field is still visible despite switching the status to something other than "Snooze".

**Steps to Reproduce:**  

1. Edit a task
2. Select "Status" of "Snooze"
3. Set "Snooze Time" to "Custom"
4. Switch "Status" to something other than "Snooze"

**Expected Result:**  

<span class="placeholder">No description</span>

**Actual Result:**

<span class="placeholder">No description</span>

**Tasks:**

- <span class="placeholder">Task 1</span>
- <span class="placeholder">Task 2</span>
- <span class="placeholder">Task 3</span>

**Tags:**  

- <span class="placeholder">Tag 1</span>
- <span class="placeholder">Tag 2</span>
- <span class="placeholder">Tag 3</span>

![[Attachments/NSDFC - Bug - Snooze Date input remains even when status is changed.mp4]]

## Bug-4 (Added)

**Title:** 

Sidebar cannot be scrolled if the screen height is too short

**Description:**  

If the screen height is too short, the sidebar cannot be scrolled. This cuts off navigation like the settings in the attached image.

**Steps to Reproduce:**  

1. Reduce the window height of the browser

**Expected Result:**  

I expect a scrollbar to be rendered, so I can interact with all of my navigation items.

**Actual Result:**

Navigation items are being hidden and I cannot interact with them.

**Tasks:**

- Update the sidebar to allow scrolling

**Tags:**  

- frontend
