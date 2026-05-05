```space-lua
config.set{
  plugs = {
    "ghr:deepkn/silverbullet-graphview"
  },
  graphview = {
    ignoredPrefixes = {
      "Library",
    },
    enableDecorations = true,
    position = "rhs",
    colormap = {
      tag = {
        services = "01017a",
        notes = "02bdb6"
      }
    }
  }
}

actionButton.define {
  icon = "calendar",
  priority = 3, -- or whatever order puts it in the spot you like
  run = function()
    editor.invokeCommand "Journal: Today"
  end
}
```

```space-style
html[data-theme="dark"] {
  --ui-accent-color: #e8e8e8;
  --top-background-color: #161616;
  --modal-selected-option-background-color: #3f3f3f;
}

html[data-theme="dark"] .cm-editor {
  background: #161616 !important;
}

/* Типографика */
html {
  --editor-font: "Inter", system-ui, sans-serif;
  --editor-width: 75%;
}

html[data-theme="dark"] .cm-content {
  color: #dde1ec;
  line-height: 1.8;
}

/* Заголовки */
html[data-theme="dark"] h1 { font-size: 2em; font-weight: 700; color: #eef0f8; }
html[data-theme="dark"] h2 { font-size: 1.4em; font-weight: 600; color: #dde1ec; }
html[data-theme="dark"] h3 { font-size: 1.1em; font-weight: 600; color: #b8bdd0; }

/* Ссылки */
html[data-theme="dark"] a {
  color: #dde1ec;
  text-decoration: none;
}
html[data-theme="dark"] a:hover { color: #bbc0ca }

/* Теги */
html[data-theme="dark"] .hashtag {
  background: #22252f;
  color: #6b7080;
  border-radius: 3px;
  padding: 1px 5px;
  font-size: 0.85em;
}

/* Код */
html[data-theme="dark"] code {
  background: #252525;
  color: #b8bdd0;
  border-radius: 3px;
  padding: 1px 5px;
}

html[data-theme="dark"] .cm-fenced-code {
  background: #1c1f28 !important;
  border-radius: 6px;
  border: 1px solid #2a2d38;
}

/* Разделитель */
html[data-theme="dark"] hr { border-color: #2a2d38; }

/* Скроллбар */
::-webkit-scrollbar { width: 0px; }

/* ═══════════════════════════════
   FRONTMATTER — тихий и ненавязчивый
   Схлопнут по умолчанию, видна
   только первая строка (---) бледно.
   Раскрывается при клике внутрь.
═══════════════════════════════ */

.sb-frontmatter.sb-line-frontmatter-outside:has(+ .sb-frontmatter) ~ .sb-frontmatter {
  display: none;
}

/* Сама строка --- почти невидима */
.sb-frontmatter-outside {
  opacity: 0.18;
  font-size: 0.75em;
  transition: opacity 0.2s ease;
}

/* При наведении чуть проявляется — намекает что там что-то есть */
.sb-frontmatter-outside:hover {
  opacity: 0.45;
}

/* При фокусе внутри — полностью показываем всё */
.sb-frontmatter-outside:focus-within {
  opacity: 1;
}

.sb-frontmatter-outside:focus-within ~ .sb-frontmatter,
.sb-frontmatter-outside:has(+ .sb-frontmatter:focus-within) ~ .sb-frontmatter {
  display: block;
}

/* Убрать обводку вокруг виджетов */
.sb-lua-directive-block, .sb-lua-directive-inline {
  border: none !important;
  outline: none !important;
}
```
```