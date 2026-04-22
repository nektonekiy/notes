# useEffect
React хук, который позволяет синхронизировать компонент с сторонней системой
```jsx
useEffect(setup, dependencies?)
```
`setup` - Функция с логикой эффекта. Ваш `setup` может также возвращать `cleanup` функцию, которую React может запускать после ре-рендера или удаления объекта, для очистки. 
	 Пример `cleanup` из примера ниже
	 `return () => {connection.disconnect();};`
`dependencies` - 

Пример:
```jsx
import { useState, useEffect } from 'react';
import { createConnection } from './chat.js';
function ChatRoom({ roomId }) {  
	const [serverUrl, setServerUrl] = useState('https://localhost:1234');  
	useEffect(() => {const connection = createConnection(serverUrl, roomId);
		connection.connect();   
		return () => {connection.disconnect();};  
	}, [serverUrl, roomId]);  
	// ...
```