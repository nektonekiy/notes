# React Компонент
## Создание
React компонент - функция,которая возврашает один элемет в JSX разметке:
```jsx
function Component() {
	return (
		<h1>Component Header</h1>
	)
}
```
## Несколько элементов в одном компоненте
Если же вы хотите вернуть несколько компонентов, то их нужно обернуть в контейнер, например `div`
```jsx
function TestComponent() {
	return (
		<div>
			<h1>TestComponent Header</h1>
			<p>TestComponent pargraph with <a href="https://react.dev/">TestComponent link</a></p>
		<div/>
	)
}
```
Однако также компоненты можно обернуть во `Fragment`
```jsx
function TestComponent() {
	return (
		<>
			<h1>TestComponent Header</h1>
			<p>TestComponent pargraph with <a href="https://react.dev/">TestComponent link</a></p>
		</>
	)
}
```
## CSS класс
Чтобы определить CSS-класс необходимо использовать атрирбут `className`
```jsx
<img className="avatar" />
```
## Отображение данных
Также можно компакто выводить разные компоненты в зависимости от условий:
```jsx
<div>  
	{isLoggedIn ? (  
		<AdminPanel />  
	) : (  
		<LoginForm />  
	)}  
</div>
```
ИЛИ:
```jsx
<div>  
	{isLoggedIn && <AdminPanel />}  
</div>
```
Так-же благодарая JSX можно удобно форматировать наборы данных.
К примеру массив
```jsx
const someData = [
	{"title":"First example title", "content":"First example content", "id":1},
	{"title":"Second example title", "content":"Second example content", "id":1}
]
```
С помощью JSX мы красиво размечаем данные.
```jsx
const someFormatedData = someData.map(artice => <div key={article.id}><h1>{artice.title}</h1><p>{artice.content}</p></div>)
return (
	<>
		{someFormatedData}
	</>
)
```

>[!warning] Обрати внимание, на то что мы должны передвавть уникальный интендификатор для кажого копонента в атрибуте `key`, он как правило, есть в базах данных на бэкэнде. Это нужно чтобы в последствие определять, с каким элементом производить операции.
## Обработка событий
Чтобы обрыбатывать нажатие кнопки вы можете создать функцию обработчик события для кнопки и передать её в атрибут:
```jsx
function ExampleButton() {
	function handleClick() {
		alert("You clicked me")
	}
	return (
		<button onClick={handleClick}>
		Click on me
		</button>
	)
}
```
## Обновление экрана
> Иногда ты можешь захотеть сохранить информацию и использовать её. К примеру кол-во нажатий на кнопу. Для этого нужно добавить `state` к компоненту

Для начала импортируем `useState` из React-а:
```jsx
import { useState } from 'react';
```
Теперь вы можете обьявить _переменную состояния_ (state variable) внутри вашего компонента
```jsx
function MyButton() { 
	const [count, setCount] = useState(0);
	// ...
```
`useState` возращает две вещи:
- текущий `state`
	в примере: `count`
- функия для обновления `state`
	в примере: `setCount`
Из примера мы видим что в хук `useState` передаётся `0`, это есть самое первый state который будет сохранен и выведен.
Когда вы захотите обновить `state`, вызовите функцию для обновления и передайте в неё новое значение

Пример простого счётчика кликов:
```jsx
function MyButton() {  
	const [count, setCount] = useState(0);
	function handleClick() {
		setCount(count + 1);  
	}  
	return (
		<button onClick={handleClick}>
			Clicked {count} times
		</button>  
	);
}
```
