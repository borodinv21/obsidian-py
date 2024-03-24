Для того, чтобы в JavaScript получить доступ к элементу HTML необходимо присвоить элементу значение `id`.

Пример:
```HTML
<input type="text" name="" id="firstValue" value="100">
```

В данном примере для элемента `input` в поле `id` я присвоил значение `firstValue`.
Для того, чтобы получить значение `value` элемента `input` воспользуемся следующей конструкцией.

Пример:
```JavaScript
const firstValueInput = document.getElementById('firstValue')
console.log(firstValueInput.value)
```

В консоли получим вывод:
![[Pasted image 20240324122155.png]]