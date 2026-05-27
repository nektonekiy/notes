# 📅 Journal
${template.each(query[[
  from p = index.tag("daily")
  where p.name != "Library/Page Templates/Daily"
  order by p.name desc
]], templates.pageItem)}