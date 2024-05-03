Для создания контейнера с PostgreSQL создадим файл `docker-compose.yml` в папке с проектом.
В image укажем версию postgres
В environment опишем пользователя базы данных, а также название базы данных.

Описание файла:
```yml
version: '3'  
  
services:  
  postgres:  
    container_name: postgres  
    image: postgres:16  
    environment:  
      POSTGRES_USER: admin  
      POSTGRES_PASSWORD: admin  
      POSTGRES_DB: gameshop  
    ports:  
      - "5432:5432"  
    restart: unless-stopped
```

После создания файла необходимо запустить контейнер. В терминале введите команду:
![[Pasted image 20240504004050.png]]
Далее с помощью следующей команды можно проверить статус запущенного контейнера.
![[Pasted image 20240504004155.png]]
![[Pasted image 20240504004218.png]]

Для подключения базы данных к [[Создание проекта]] необходимо зайти в [[settings.py]] и прописать следующие строки, предварительно установив `psycopg2`:
```python
DATABASES = {  
    'default': {  
        'ENGINE': 'django.db.backends.postgresql_psycopg2',  
        'NAME': 'gameshop',  
        'USER': 'admin',  
        'PASSWORD': 'admin',  
        'HOST': 'localhost',  
        'PORT': '5432 ',  
    }  
}
```