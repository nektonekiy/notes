# 🎯 Actions
# Next
${template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "next")
  order by lastModified
  ]], templates.pageItem) }
# Waiting for
${template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "waitingFor")
  order by lastModified
  ]], templates.pageItem) }
# Someday Maybe
${template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "somedayMaybe")
  order by lastModified
  ]], templates.pageItem) }