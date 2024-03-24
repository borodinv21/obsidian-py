Функция в JS описывают какую-либо логику программы отдельно от основной программы и выносится в отдельный блок кода, который можно вызывать множество раз в разных местах основной программы.

Пример:
```JavaScript
function greeting () {
	console.log('Hello, world!')
}
```

Аргументы функции нужны для передачи в функцию какой-либо информации для её последующей обработки.

Пример:
```JavaScript
let a = 10
let b = 100

sum(a, b)

function sum (firstValue, secondValue) {
	console.log(firstValue + secondValue)
}
```