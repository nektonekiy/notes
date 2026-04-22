---
pageDecoration: 
  prefix: "🏠 "
  disableTOC: true
---
# [[+Study|Study]] [[+IT|IT]] [[+Routine|Routine]] [[+Strategy|Strategy]] [[+Brain|Brain]] | [[+Library|Library]]
## Pins 
* [[_learnReact]]
- [[_learningGerman]]
#### Switching to SilverBullet from Obsidian Checklist
- [x] Change index page
- [ ] Setup Git
- [x] Setup journaling
- [ ] Rebuild Templates
- [x] Customize
## Journal
${template.each(query[[
  from j = index.tag("daily")
  order by j.name desc
  limit 7
]], templates.pageItem)}


