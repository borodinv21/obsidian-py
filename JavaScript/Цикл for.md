Цикл for применяется, когда нам необходимо перебрать какую-либо последовательность элементов.

Пример:
```JavaScript
const myArr = [1, 2, 3]

for (let i = 0; i < myArr.length; i++) {
	console.log(myArr[i])
}

for (let elem of myArr){
	console.log(elem)
}
```