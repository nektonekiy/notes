# 🎯 Actions
# Next
${template.each(query[[
  from p = index.tag("actions")
  where table.includes(p.tags, "next") and table.includes(p.itags, "page")
  order by lastModified
  ]], templates.pageItem) }
# Waiting for
${template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "waitingFor") and table.includes(p.itags, "page")
  order by lastModified
  ]], templates.pageItem) }
# Someday Maybe
${template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "somedayMaybe") and table.includes(p.itags, "page")
  order by lastModified
  ]], templates.pageItem) }
# Scheduled
${template.each(query[[
  from p = tags.actions
  where table.includes(p.tags, "scheduled") and table.includes(p.itags, "page")
  order by p.date
  ]], templates.pageItem) }