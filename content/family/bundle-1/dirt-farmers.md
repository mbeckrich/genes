---
title: Dirt Farmers
summary: |
  Some Laura Ingalls Wilder type shit.
date: "2011-11-11"
individuals:
  - 02-003
  - 02-002
  - 02-i
---

Life on the range. Ma [02-003] and Pa [02-002] and ol' Aunt Susan Jane [02-i] were dirt farmers in Potato, Idaho.

### Ideas

- Include full name + ID under people kind
  - Ma [02-003]
    - Should result in .com/people/ma-02-003
- Include full name under people kind
  ```yaml
  people:
    - Ma Mommersen
  ```
  Loop through people to match use in text and append ID from reference-lists file?
  - Loop
    - Find Ma Mommersen
      - Append [02-002] in post. 'Ma Mommersen[02-002] and Pa...'.
