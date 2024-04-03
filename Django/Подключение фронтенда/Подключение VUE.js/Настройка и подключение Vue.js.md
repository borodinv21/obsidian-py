Для подключения фронтенда к нашему приложению создадим новый html файл. И в *head* укажем некоторые ссылки.
![[Pasted image 20240403162919.png]]
Bootstrap - https://getbootstrap.com/
Vue.js - https://ru.vuejs.org/guide/quick-start.html
Axios.js - https://cdnjs.com/libraries/axios

Создаем представление.
![[Pasted image 20240403163228.png]]

И подключаем его в *urls.py*
![[Pasted image 20240403163305.png]]

Создаём директорию *static* и файл *app.js*.
![[Pasted image 20240403163656.png]]

Подключаем статические файлы в файле [[settings.py]].
![[Pasted image 20240403165209.png]]

В html документ добавляем ссылку на файл *app.js*.
![[Pasted image 20240403165450.png]]