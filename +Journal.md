# 📅 Journal
${template.each(query[[
  from j = index.tag("daily")
  order by j.name desc
]], templates.pageItem)}
