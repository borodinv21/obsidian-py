[[BigInt]]
Number в JavaScript это любое число.

Пример:
```JavaScript
const a = 100
const b = 100.08
const c = 1_000_000_000
```

Для того, чтобы перевести СТРОКУ в число, воспользуемся функцией `Number()`.

Пример:
```JavaScript
const str = '100'
console.log(Number(str)) // 100
```

Ещё методы для преобразования СТРОК в число:

Пример:
```JavaScript
const _int = '20'
const _float = '20.20'

console.log(parseInt(_int)) // 20
console.log(parseInt(_float)) // 20

console.log(parseFloat(_int)) // 20
console.log(parseFloat(_float)) // 20.20

// parseInt приводит строку в целое число, отбрасывая дробную часть
// parseFloat приводит строку в число с плавающей точкой
------------------------------------------
const _int = '20'
const _float = '20.20'

console.log(+_int, +_float) // 20 20.20

// + переводит строку в число
```

Для того, чтобы указать количество символов после запятой используется метод `toFixed(количество цифр после запятой)`, при этом преобразует число в СТРОКУ.

Пример:
```JavaScript
const _float = 20.20134

console.log(+_float.toFixed(3)) // 20.201
```