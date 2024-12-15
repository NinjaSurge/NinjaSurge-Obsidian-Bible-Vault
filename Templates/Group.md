<%* let name = await tp.system.prompt("Group Name") -%>
---
tags:
aliases:
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

<% tp.file.move("/People/Groups/" + name) -%>
