---
alias: 
---
<%* const topic = await tp.system.prompt('Topic') -%>

````ad-info
title: Files with tags:
```dataviewjs
let list = []
let tags = [...dv.current().file.aliases.map((i) => i.toLowerCase()), dv.current().file.name.toLowerCase()]
for (let i = 0; i < tags.length; i++) {
	dv.pages(`#${tags[i]}`).map( i => {
	  list.push(i.file.link)
 })
}
dv.list(list)
```
````
%% There might still be a problem with the file name and the tag search… %%
<% tp.file.rename(topic) -%>
<% tp.file.move("/Studies/Topical/" + topic) -%>