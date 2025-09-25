---
cssclasses:
  - full_width
---

This is meant to be run in the Chrome Developer Tools console:

```js
let container = document.querySelector(".ListView-module__ul--A_8jF");
let anchors = Array.from(container.querySelectorAll(".Title-module__container--XD9YG a"));
let links = anchors.map((anchor) => {
	return `[${anchor.innerText}](${anchor.href})`
}).join("\n")
copy(links)
```