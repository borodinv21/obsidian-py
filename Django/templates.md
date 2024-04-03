Шаблоны в Django хранятся в отдельной папке под названием *templates*, создадим эту папку в корневом каталоге нашего приложения.

Для подключения шаблонов необходимо зайти в [[settings.py]] и найти список *TEMPLATES*

![[Pasted image 20240403120929.png]]

Далее в словаре в список ключа *DIRS*  добавим название папки *templates*.
![[Pasted image 20240403121049.png]]

Шаблоны подключены.