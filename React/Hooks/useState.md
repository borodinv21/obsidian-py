Отвечает за работу с состоянием внутри компонента.
Для того, чтобы использовать `useState` его необходимо импортировать.
![[Pasted image 20240411125230.png]]
Далее **СТРОГО** в начале компонента инициализируем наш `useState` такой конструкцией, где `content` это содержимое, а `setContent` это функция для изменения содержимого.
![[Pasted image 20240411125424.png]]
Будем вызывать `content` в отдельном элементе `<p>`. А изменять с помощью `setContent` в обработчике события кнопки `handleClick`.
![[Pasted image 20240411125540.png]]
![[Pasted image 20240411125552.png]]
В результате при нажатии на кнопку будет показано то содержимое параметра `text`, которое мы указали.

Нажатие кнопки `Текст1`.
![[Pasted image 20240411125644.png]]

Нажатие кнопки `Текст2`.
![[Pasted image 20240411125651.png]]

Нажатие кнопки `Текст3`.
![[Pasted image 20240411125706.png]]

Также можно выводить информацию с помощью тернарного оператора, если по-умолчанию установить значение `useState` в `null`.
![[Pasted image 20240411141036.png]]
![[Pasted image 20240411141054.png]]
 