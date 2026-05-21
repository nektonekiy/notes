# 📥 Inbox
${template.each(query[[
  from j = index.tag("inbox")
  order by j.name desc
]], templates.pageItem)}