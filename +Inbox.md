# 📥 Inbox
${template.each(query[[
  from p = index.tag("inbox")
  where table.includes(p.itags, "page")
  order by p.name desc
]], templates.pageItem)}