---
cssclasses:
  - bible
---

```dataviewjs
let pageName = app.workspace.lastActiveFile.name
//let pageName = dv.current().pageName
let links = dv.page(pageName).file.outlinks
links = links.where(l => l.embed == false && l.path.contains("bible"))
dv.header(1, pageName)
if (links.length > 0) {
  let lastLink = links[links.length-1]
  dv.paragraph(dv.fileLink(lastLink.path))
  dv.paragraph(dv.fileLink(lastLink.path, true))
  dv.paragraph(dv.fileLink(lastLink.path))
} else {
  dv.paragraph(`No Bible links in ${pageName}`)
}
```
