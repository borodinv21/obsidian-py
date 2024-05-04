Для использования фильтров в DRF установим `django-filter`.
![[Pasted image 20240504130914.png]]
Далее для корректного отображения отфильтрованного JSON файла в [[settings.py]] пропишем следующий код:
```python
REST_FRAMEWORK = {  
    'DEFAULT_RENDERER_CLASSES': (  
        'rest_framework.renderers.JSONRenderer',  
    ),  
    'DEFAULT_PARSER_CLASSES': (  
        'rest_framework.parsers.JSONParser',  
    )  
}
```

В качестве примера будем фильтровать записи по цене.
Для работы с фильтрами в представлении добавим два поля:
```python
filter_backends = [DjangoFilterBackend]  
filter_fields = ['price']
```
И для корректной работы подключим следующий модуль:
```python
from django_filters.rest_framework import DjangoFilterBackend
```

Готовый код выглядит так:![[Pasted image 20240504131218.png]]
Затем в браузере создаём запрос.
Выводим все игры с ценой = 1000.
![[Pasted image 20240504131254.png]]
