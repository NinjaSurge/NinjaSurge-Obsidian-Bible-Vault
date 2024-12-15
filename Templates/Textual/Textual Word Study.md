<%* const book_ch = await tp.system.prompt('Book and Chapter') -%>
# [[<% book_ch %>]]
[[<% book_ch %> Notes|Notes]] • [[<% book_ch %>]]
## v1
![[<% book_ch %>#1]]
### (Greek/Hebrew Word)
English Definition/Equivalent
This word could also be written as
- English words…
### Summary
```ad-quote
title: Rephrase

```

---
[[<% book_ch %> Notes|Notes]] • [[<% book_ch %>]]

<% tp.file.rename(book_ch + ' Word Study') -%>
<% tp.file.move("/Studies/Textual/"+book_ch.split(' ')[0] + '/' + book_ch + ' Word Study') -%>