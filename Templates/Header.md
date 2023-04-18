---
 Created: <% tp.file.creation_date() %>
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [<%* tR += tp.file.tags.map(function(x){ return x.replace(/#/g,"") }); %>]
---

