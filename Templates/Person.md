<%* let name = await tp.system.prompt("Person's Name") -%>
---
tags:
aliases:
father:
mother:
siblings:
spouse:
children:
---

# Bio

## Timeline

# Links

> [!info] Bible Chapters
> ```dataview
> LIST FROM [[]] AND "bible"
> ```

> [!info] Studies
> ```dataview
> LIST FROM [[]] AND "Studies"
> ```

> [!info] Other References
> ```dataview
> LIST FROM [[]] AND !"Studies" AND !"bible"
> ```

<% tp.file.rename(name) -%>
<% tp.file.move("/People/" + name) -%>
