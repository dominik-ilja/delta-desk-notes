```base
views:
  - type: table
    name: Table
    filters:
      or:
        - Base.contains("[[" + this.file.name +"]]")

```