```JavaScript
const list = document.querySelector('#list') //получаем элемент с айди list
const filter = document.querySelector('#filter') //получаем элемент с айди filter
let USERS = [] //создаем массив 

//В данной функции фильтруем имена пользователей относительно того, что вписано в инпут
filter.addEventListener('input', (event) => { 
	const value = event.target.value.toLowerCase()
	const filteredUsers = USERS.filter((user) => {
		return user.name.toLowerCase().includes(value)
	})
	render(filteredUsers)
})

//Функция запуска программы, получает ссылку с JSON данными
async function start(){
	try {
		list.innerHTML = 'Loading...'
		const response = await fetch('https://jsonplaceholder.typicode.com/users')
		const data = await response.json()
		setTimeout(() => {
			USERS = data
			render(data)
		}, 2000)
	} catch (err) {
		list.innerHTML = `Error ${err}`
	}
}

  
//Функция отображения пользователей
function render(users = []){
	if (users.length === 0) {
		list.innerHTML = 'Такого пользователя не существует'
	}else{
		const html = users.map(toHTML).join('')
		list.innerHTML = html
	}
}

  
//Генератор html 
function toHTML(user) {
	return `
	<li>${user.name}</li>
	`
}

start()
```