Для того, чтобы привести какой-либо объект к JSON формату используется следующая конструкция.

Пример:
```JavaScript
const car = {
	model: 'BMW',
	power:500
}

carJson = JSON.stringify(car)
console.log(carJson) //{"model":"BMW","power":500}
```

Так же можно распарсить строку JSON формата.

Пример:
```JavaScript
const car = {
	model: 'BMW',
	power:500
}

const carJson = JSON.stringify(car)
const parsedCar = JSON.parse(carJson)

console.log(carJson)
console.log(parsedCar) //Выводим объект
```