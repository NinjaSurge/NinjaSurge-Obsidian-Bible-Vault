<% const word = await tp.system.prompt('Greek/Hebrew link') -%>
### [[<% word %>|<% tp.file.find_tfile('word').split(' ')[2] %>]]
![[<% word %>#Definition]]
```ad-note
```