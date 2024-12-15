<%* let name = await tp.system.prompt("Place's Name") -%>
---
tags:
aliases: 
---

# Bio

## History

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
<% tp.file.move("/Places/" + name) -%>