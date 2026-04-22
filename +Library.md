# Library

# Obsidian Base
```base
filters:
  and:
    - file.hasTag("media")
    - '!file.path.contains("meta")'
formulas:
  precent: precent * 100 + "%"
properties:
  formula.precent read:
    displayName: precent read
views:
  - type: cards
    name: in progress
    filters:
      and:
        - precent != 1
        - status == false
    order:
      - title
      - author
      - genre
      - tags
      - formula.precent
    image: note.image
    imageFit: contain
    imageAspectRatio: 1.1
  - type: cards
    name: to accumalate
    filters:
      and:
        - precent == 0
        - status == false
    order:
      - title
      - author
      - genre
    image: note.image
    imageFit: contain
    imageAspectRatio: 1.1
  - type: cards
    name: done
    filters:
      and:
        - precent == 1
        - status == true
    order:
      - title
      - author
      - genre
      - tags
      - rating
    image: note.image
    imageFit: contain
    imageAspectRatio: 1.1
  - type: cards
    name: droppped
    filters:
      and:
        - precent != 1
        - status == true
    order:
      - title
      - author
      - genre
      - tags
      - formula.precent
      - rating
    image: note.image
    imageFit: contain
    imageAspectRatio: 1.1
  - type: cards
    name: all
    order:
      - title
      - author
      - genre
      - formula.precent read
      - rating
    image: note.image
    imageFit: contain
    imageAspectRatio: 1.1

```