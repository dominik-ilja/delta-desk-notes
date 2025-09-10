---
cssclasses:
  - full_width
Address:
Phone Numbers:
Type: Organization
---
# Delta Desk

This is a company that was started by [[Josh Jennings]].

## Employees

```base
formulas:
  Current: |-
    if(
    note["Company"].containsAny("Delta Desk", link("Sushchnosti/Organisasjon/Delta Desk", "Delta Desk")),"Yes", "No"
    )
  Positions: Positions.filter(value.toString().contains("Delta Desk")).map(value.toString().replace("Delta Desk · ", ""))
properties:
  formula.Current:
    displayName: Current
views:
  - type: table
    name: Current
    filters:
      or:
        - Company.containsAny("Delta Desk", link("Sushchnosti/Organisasjon/Delta Desk", "Delta Desk"))
    order:
      - file.name
      - formula.Current
      - formula.Positions
      - GitHub
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 244
      formula.Positions: 272
    cardSize: 250
  - type: table
    name: Previous
    filters:
      and:
        - note["Previous Companies"].containsAny("Delta Desk", link("Sushchnosti/Organisasjon/Delta Desk", "Delta Desk"))
    order:
      - file.name
      - formula.Current
      - formula.Positions
      - GitHub
    columnSize:
      file.name: 244
      formula.Positions: 202

```

- Mikhail
- Quang Khuat
- Zulqarnain Niazi
- Khurram Abbasi
- Mostofa Reza
- Colin

Eagles?