```base
filters:
  or:
    - Base.contains("[[" + this.file.name + "]]")
    - and:
        - file.name.startsWith("Git -")
        - Type == "Tutorial"
views:
  - type: table
    name: All
    order:
      - file.name
      - Topics
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 395
      note.Topics: 290
  - type: table
    name: Filtered
    filters:
      and:
        - Topics.contains("tag")
    order:
      - file.name
      - Topics
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 460
      note.Topics: 290

```
