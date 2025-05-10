## Assets used

```dataview
LIST WITHOUT ID
elink(url, default(aliases, file.name) + choice(contains(url, "renderotica"), " 🔞", ""))
FROM outgoing([[#]]) AND #ds-asset 
WHERE url AND contains(this.assets, file.link)
SORT file.name ASC
```
