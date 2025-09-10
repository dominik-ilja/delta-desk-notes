---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# <% tp.file.title %>

<!--
A description of the technology:

- What it is typically used for?
- Why is it helpful? 
-->

## Resources

<!-- This section is used for commands, resources, etc. that can be used to access the documentation. -->

- <!-- add link or command that can take us to documentation -->

## Versioning

<!--
- When was the technology released?
- What is the current version of the technology? (Add timestamp of when this was added by us)
- Has there been any changes to how this technology used? Is it deprecated?
-->

**Introduced:** Unknown
**Current:** v0.0.0 <span class="placeholder">as of {date}</span>

## Documentation

<!--
Contains an overview of how to use the technology if it isn't straight forward. This can also be for making things more clear that aren't readily available in the source documentation.
-->

```

```

## Lessons

<!-- This section is used to link lessons related to the technology. This section can be replaced by the "Documentation" section if necessary. -->

## Tutorials

<!-- This table is used to collect tutorials that are related to the technology. This shows you how to do specific things with the technology. -->

```base
views:
  - type: table
    name: Table
    filters:
      and:
        - file.name.startsWith("Git -")
        - Topics.containsAny("branch")
        - Type == "Tutorial"
    order:
      - file.name
      - Topics
    columnSize:
      file.name: 410

```

