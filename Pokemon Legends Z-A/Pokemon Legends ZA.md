
# Summary

## Colorful Screws

### Screws

```base
summaries:
  "% Complete": (((values.filter(value == true).length) / values.filter(!value.isType("null")).length) * 100).round(2)
views:
  - type: table
    name: Table
    filters:
      and:
        - file.hasTag("ColorfulScrews")
    order:
      - file.name
      - Obtained
    sort:
      - property: file.name
        direction: ASC
    summaries:
      Obtained: "% Complete"
```

### Canari Plushs

```base
summaries:
  Obtained: values.(filter(value == true).length)/filter.length*100
  Upgraded: values.filter(value == true).length
  Maxed: values.filter(value == true).length
  Checked: values.filter(value == true).length
  "% Complete": |
    (((values.filter(value == true).length) / values.filter(!value.isType("null")).length) * 100).round(2)
properties:
  file.name:
    displayName: Plush
views:
  - type: table
    name: Table
    filters:
      and:
        - file.hasTag("CanariPlush")
    order:
      - file.name
      - Obtained
    sort:
      - property: Lvl1
        direction: DESC
      - property: file.name
        direction: ASC
    summaries:
      Lvl1: Obtained
      Lvl2: Checked
      Lvl3: Maxed
      Obtained: "% Complete"
    columnSize:
      note.Lvl1: 155
      note.Lvl2: 174
    markers: number
    indentProperties: true

```

