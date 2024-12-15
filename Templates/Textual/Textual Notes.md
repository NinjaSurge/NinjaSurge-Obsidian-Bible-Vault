
<%*
const book_ch = await tp.system.prompt('Book and Chapter') 
folder_name = isNaN(parseInt(book_ch.split(' ')[0])) ? book_ch.split(' ')[0] : book_ch.split(' ')[0] + ' ' + book_ch.split(' ')[1]
-%>
[[<% book_ch %> Word Study|Word Study]] • [[<% book_ch %>]]

## Verses

### Verse 1

## Notes

> [!info] References to the Book 
> ```dataview
> LIST FROM [[<% book_ch %>]] AND !"bible" AND !"lexicon" AND !"dictionary"
> ```

---
[[<% book_ch %> Word Study|Word Study]] • [[<% book_ch %>]]
<% tp.file.rename(book_ch + ' Notes') -%>
<% tp.file.move("/Studies/Textual/" + folder_name + '/' + book_ch + ' Notes') -%>