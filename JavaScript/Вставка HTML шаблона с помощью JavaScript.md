Для того, чтобы вставить шаблон в HTML воспользуемся следующей конструкцией.

Пример:
```JavaScript
const div = document.getElementById('div')

function addHtml () {
	div.innerHTML = `<h1>Hello, world!</h1>`
}
```

Метод [insertAdjacentHTML](https://developer.mozilla.org/en/DOM/element.insertAdjacentHTML) позволяет вставлять произвольный HTML в любое место документа, в том числе _и между узлами_!

Пример:
```JavaScript
const div = document.getElementById('div')

function addHtml () {
	div.insertAdjacentHTML('where', '<h1>Hello, world!</h1>')
}
```
Там где `where` необходимо указать куда вставить HTML элемент.
```JavaScript
1. `beforeBegin` – перед элементом.
2. `afterBegin` – внутрь элемента, в самое начало.
3. `beforeEnd` – внутрь элемента, в конец.
4. `afterEnd` – после элемента.
```