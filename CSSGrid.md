---
media: https://www.youtube.com/watch?v=b_cc3Blez9I
created: 2025-05-24 15:52
typeOfContent: doc
related: "[[_learningFrontendTools]]"
---
# CSS Grid
[02:42](https://www.youtube.com/watch?t=162&v=b_cc3Blez9I)
## Категории свойств grid:
- Записываться в род. блок
- Записываться в дочер. блок
- Работают в тандеме

[02:57](https://www.youtube.com/watch?t=177&v=b_cc3Blez9I)
## Разметка CSS Grid:
```html
<div class="box"> <!-- Родительский блок -->
	<!-- Дочерние элементы -->
	<div class="item"> 
	<!-- НЕ дочерний элемент >> --> <h1></h1> 
	</div>
	<div class="item"></div>
	<div class="item"></div>
	<div class="item"></div>
	<div class="item"></div>
	<div class="item"></div> 
</div>
```

[04:11](https://www.youtube.com/watch?t=251&v=b_cc3Blez9I)
## Свойства:
### Для родительского блока:
- `display: grid;`
	Свойство которое необходимо указать род. элементу, при желании использовать CSS Grid 
- `display: inline-grid;`
	Тоже самое что и `display: grid;`, но сетка является строчным элементом, а не строчным
- `grid-template-rows: <размер 1-ой строки> <размер 2-ой строки> ..`
	Задаёт кол-во и размер строк
- `grid-template-columns: <размер 1-ого столбца> <размер 2-ого столбца> ..`
	Задаёт кол-во и размер столбцов
- `grid-template: <значение grid-template-rows> / <значение grid-template-columns>`
	Объединяет `grid-template-rows` и `grid-template-columns`