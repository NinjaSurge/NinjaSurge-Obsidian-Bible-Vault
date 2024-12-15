# General 

## Songs
1. 
2. 
<%* if (tp.date.now("dddd") != "Thursday") { -%>
3. 
4. 
5. 
6. 
<%* } -%>

## Announcements
```meta-bind
INPUT[list:Announcements#announcements]
```
```meta-bind
INPUT[list:Announcements#events]
```

# Class

<%* if (tp.date.now("dddd") === "Sunday") { -%>
#Rog/Reuben
<%* } else if (tp.date.now("dddd") === "Wednesday") { -%>
#Tarrel/Joe 
<%* } else { -%>
#Stubblefield/Brant
<%* } -%>

> [!info]- Last Week
> <%*
tR+="![[Studies/" + tp.date.now("dddd") + "/" + app.vault.fileMap["Studies/" + tp.date.now("dddd")].children.sort((a,b) => b.stat.ctime - a.stat.ctime).map(f => f.basename)[0] + "#Class]]"
%>

<%* if (tp.date.now("dddd") === "Sunday") { -%>
# Sermon

#Rog/Reuben 


<%* } -%>
<%* if (tp.date.now("dddd") === "Thursday") { -%>
# Class 2

#Stubblefield/Brant


> [!info]- Last Week
> <%*
tR+="![[Studies/" + tp.date.now("dddd") + "/" + app.vault.fileMap["Studies/" + tp.date.now("dddd")].children.sort((a,b) => b.stat.ctime - a.stat.ctime).map(f => f.basename)[0] + "#Class 2]]"
%>

<%* } -%>
# Information

> [!info] Passages
> ```dataview
> LIST FROM outgoing([[]]) AND "bible"
> ```

> [!info] People
> ```dataview
> LIST FROM outgoing([[]]) AND "People"
> ```

> [!info] Places
> ```dataview
> LIST FROM outgoing([[]]) AND "Places"
> ```

> [!info] Things
> ```dataview
> LIST FROM outgoing([[]]) AND "Misc"
> ```

> [!word]+ Words
> > [!english]
> > ```dataview
> > LIST FROM outgoing([[]]) AND "dictionary"
> > ```
> 
> > [!greek]
> > ```dataview
> > LIST FROM outgoing([[]]) AND "lexicon/greek"
> > ```
> 
> > [!hebrew]
> > ```dataview
> > LIST FROM outgoing([[]]) AND "lexicon/hebrew"
> > ```


<%* let name =  tp.date.now("dddd") + " " + tp.date.now("YY_MM_DD") -%>
<% tp.file.rename(name) -%>
<% tp.file.move("/Studies/"+tp.date.now("dddd") + "/" + name) -%>