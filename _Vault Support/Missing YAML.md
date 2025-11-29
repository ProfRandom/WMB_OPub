---
title: Missing YAML
---
```dataview
TABLE file.link AS "Notes Missing YAML"
FROM ""
WHERE !file.frontmatter
SORT file.name ASC
```
