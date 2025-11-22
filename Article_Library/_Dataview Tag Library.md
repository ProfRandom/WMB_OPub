---
Aliases:
  - "#math"
title: Dataview Tag Library
date: 2025-11-19
---
```dataview
TABLE WITHOUT ID tag AS "Tag"
FROM ""
FLATTEN file.tags AS tag
GROUP BY tag
SORT tag ASC
```

