Есть несколько способов перебрать JSON файл, либо объект JavaScript.

Для первого способа используем метод `.map()`.

Переберём объект `ways`.
![[Pasted image 20240411143823.png]]

Импортируем объект `ways`.
![[Pasted image 20240411143917.png]]

Далее в компоненте `App` в тэге `<ul>` напишем следующую конструкцию, где в `key` мы указываем уникальный параметр для элемента.
![[Pasted image 20240411144454.png]]

Где в `PrintDataInfo` находится следующий код, который в параметрах принимает `title` и `description`.
![[Pasted image 20240411144051.png]]

На выходе получаем следующий результат.
![[Pasted image 20240411144202.png]]