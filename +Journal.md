# 📅 Journal
${template.each(query[[
  from p = index.tag("daily")
  order by p.name desc
]], templates.pageItem)}
 where p.name != "Library/Page Templates/Daily"