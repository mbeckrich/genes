---
# (To remove these comments from future posts, delete #comment
# lines from the `archetypes/default.md` file.)
# Docs: https://gohugo.io/content-management/front-matter/
# How the frontmatter works:
# Run `hugo new foldernamehere/post-name-here.md`
# Docs: https://gohugo.io/getting-started/quick-start/
# Creates a title using the name you chose above in folder
# you selected above:
title: '{{ replace .Name "-" " " | title }}'
# Auto populates with date:
date: {{ .Date }}
# Post goes live when site is updated:
draft: false
# The individuals `taxonomy`. For adults, use the ID format of:
# id-00-000 where 00 is the generation number and 000 
# is the person's number. For offspring, use the format of: 
# id-00-ivx where 00 is the mother's generation number and ivx is
# the Roman numeral corresponding to child birth order (e.g., the
# oldest child is id-00-i). Both adults and children must be 
# listed with a for each hyphen as shown below. Do not indent.
individuals:
-
# The series `taxonomy`. For ongoing or planned series on
# a given topic. They can be called anything, but make sure
# the same name for a topic is always used.
series:
- 
# The tags `taxonomy` for miscellaneous topics.
tags:
- 
# A brief description of the content:
description:
# Link to image files (by default in the `assets/images` folder)
images:
- 
---

[//]: # (The squiggly brackets denote a shortcode. Any text placed inside will be searched for a family member's name in the database and turned into a link to their page, provided it has been created in the site's `content/individuals` folder. The name must be written the same as the database's name to be found. The database is located in `data/dar.json`. For example, if his name is written as "Superwholock, Larry" in the database, it will need to be written as "Superwholock, Larry" any time you want it to be turned into a link in the post.)

{{< individual >}}

{{</ individual >}}