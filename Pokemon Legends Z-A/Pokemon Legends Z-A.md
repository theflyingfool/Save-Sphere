---
tags:
  - Game
Owned: true
Cover: "[[Pokemon_Legends_ZA_Cover.png]]"
Systems:
  - Switch
ReleaseDate: 2025-10-16
---
# Summary

## Pokedex

## TMs


```base
summaries:
  "% Complete": (((values.filter(value == true).length) / values.filter(!value.isType("null")).length) * 100).round(2)
views:
  - type: table
    name: Table
    filters:
      and:
        - file.hasTag("TM")
    order:
      - file.name
      - Obtained
      - Location
    summaries:
      Obtained: "% Complete"

```

## Clothing

## Colorful Screws

### Screws

#### Rouge District

```base
views:
  - type: cards
    name: Table
    filters:
      and:
        - file.hasTag("ColorfulScrews/RougeDistrict")
    order:
      - file.name
      - Obtained
    image: note.Map

```
#### Jaune District

#### Vert District

#### Bleu District

#### Magenta District

#### All Screws
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
      - Location
    sort: []
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


## Quests