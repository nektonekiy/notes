---
command: "Journal: Today"
key: "Ctrl-q t"
suggestedName: "${os.date('%Y-%m-%d')}"
confirmName: false
tags: meta/template/page
openIfExists: true
---
# Scheduled 
${"$"}{template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "scheduled") and p.date == editor.getCurrentPage()
  order by lastModified
  ]], templates.pageItem)}
# Notes
- |^| 
