# Bugs
## Bug-1

**Description:**  

A double scrollbar is occurring in the `/universal-search` page. A `max-height` is being set on a `<div>` within the `<main>`. The `max-height` is being set with the `calc` function. There's too much height which is causing the overflow.

We can manually adjust this for now, but should look into having the height set without `calc`. Attached is a screenshot of the problematic `<div>`.

You can use the following search term for a result: "private equity fund in frisco texas"

![[Attachments/Pasted image 20250911080552.png]]

**Tags:**  

- Bug
- Frontend
- UI

**Tasks:**  

- Update the `calc` functions to prevent double scrollbars in medium to large screens. We won't worry about mobile right now.
- Look into how we could remove the usage of `calc` altogether