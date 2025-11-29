---

---



```dataview
TABLE file.link AS "Untagged Notes"
FROM ""
WHERE length(file.tags) = 0
SORT file.name ASC
```


```dataview
TABLE file.link AS "YAML but No Tags"
FROM ""
WHERE file.frontmatter AND length(file.tags) = 0
SORT file.name ASC
```

```dataview
TABLE file.link AS "Orphan Notes (No YAML, No Tags)"
FROM ""
WHERE !file.frontmatter AND length(file.tags) = 0
SORT file.name ASC
```
