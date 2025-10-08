---
cssclasses:
  - full_width
Address:
Phone Numbers:
Type: Organization
---
# Delta Desk

This is a company that was started by [[Sushchnosti/Delta Desk/People/Josh Jennings]].

Around 900k in revenue

Josh has worked with FIN Searches for 10~ years and Carrick Lane and Visdom for 13~ years.

Developer who did the v1 version of FIN Searches was friends with Josh for 15~ years. There's jobs that run to keep the documents in sync between the old and new site.

OCR is the process of extracting text from a PDF

[Repositories](https://github.com/orgs/delta-desk/repositories)
[Virtual Backgrounds](https://deltadesk.sharepoint.com/:f:/s/MSP/EnQv-YQtlSVDoZ3v-jmzvUMBoO9JiiV8LZWA3rvymKCiBA?e=0gHFHi)
[Software Development - Documents - All Documents](https://deltadesk.sharepoint.com/sites/SoftwareDevelopment/Shared%20Documents/Forms/AllItems.aspx)

## Services

- IT Support Business

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

## Events

- Start of FIN Searches conference [Event:: 2025-09-15]
- [[Sushchnosti/Delta Desk/People/Luke Lancaster|Luke Lancaster]]'s last day [Event:: 2025-09-17T12:00:00]
- End of FIN Searches conference [Event:: 2025-09-19]