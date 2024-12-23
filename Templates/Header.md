---
 Created: <% tp.file.creation_date() %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [<%* tR += tp.file.folder(true).split('/').map(function(x){ return x.toLowerCase().replace(/ /g, '-') }); %><%* tR += tp.file.tags.map(function(x){ return x.replace(/#/g,"") }); %>]
---

<% tp.file.cursor(0) %>