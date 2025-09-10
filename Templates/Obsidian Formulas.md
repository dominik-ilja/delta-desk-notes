---
cssclasses:
  - full_width
---
# Obsidian Formulas
## Last Contacted

This uses the `"Last Contacted"` and `"Next Contact"` of a note and does the following:

1. Get the difference between today and when we last contacted the person. This will give us the total number of days since last contact.
2. If today is after are scheduled "Next Contact", then we render the text `({days} days overdue)`

```js
(today() - note["Last Contacted"])
    .days
    .floor()
    .toString() +
if(
  (note["Next Contact"] - today()).days < 0, 
  " (" + 
  (note["Next Contact"] - today())
      .days
      .abs()
      .toString() + 
  " days overdue)",
  ""
)
```
