Функция в JS описывают какую-либо логику программы отдельно от основной программы и выносится в отдельный блок кода, который можно вызывать множество раз в разных местах основной программы.

Объявлять функции в JavaScript можно двумя способами. Отличие этих способов является в вызове функции до её инициализации, Function Declaration можно вызвать до её инициализации, но с Function Expression так не выйдет.

Пример:
```JavaScript
greeting()

// Function Declaration
function greeting () {
	console.log('Hello, world!')
}

//Function Expression
const greeting2 = function () {
	console.low('Hello, world!')
}

greeting2()
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

Ключевое слово `return` возвращает результат функции.

Пример:
```JavaScript
function square(val) {
	return val**2
}

console.log(square(3)) // 9

--------------------------------------

const arrow = (val) => val**2
console.log(arrow(3)) // 9
```

Дефолтные значения параметров.

Пример:
```JavaScript
function pow(a, b = 2) {
	console.log(a ** b)
}

pow(10)
```

Передача в функцию нескольких параметров.

Пример:
```JavaScript
function allNumbersSum(... numbers){
	let sum = 0
	for (let i of numbers) sum += i
	return sum
}

console.log(allNumbersSum(1, 2, 3, 4, 5)) // 15
```