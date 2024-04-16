1 На странице сервиса подключения авторизации https://id.vk.com/about/business/go/accounts/83175/apps нажмите на кнопку «Добавить приложение»
2 Придумайте название приложению. Выберите тип платформы — Web
![[Pasted image 20240414161936.png]]
3 Нажимаем «Далее» для создания приложения  
4 Вставляем в поле «Базовый домен» и «Доверенный Redirect URL» ссылку  
и нажимаем готово `https://example.com/callback`
5 Поздравляем! Приложение создано  
6 Теперь из поля «Информация о приложении» запоминаем или копируем в текстовый редактор «ID  
приложения» (только цифры без букв)  
7 В редактор копируем ссылку: `https://oauth.vk.com/authorize?client_id={client_id}&display=page&redirect_uri=https://example.com/callback&scope=friends,photos&response_type=token&v=5.131&state=123456`  ГЛАВНОЕ В redirect_uri ИСПОЛЬЗОВАТЬ https, а не http!!!
8 И вместо {client_id} вставляем «ID приложения» из пункта 6 (без фигурных скобок, только цифры)  
9 Вставляем в браузер ссылку и нажимаем «Enter»  
10 Появится окно:  
![[Pasted image 20240414162103.png]]
11 Нажимаем «Продолжить»  
12 Браузер перекинет на другую ссылку:
![[Pasted image 20240414162117.png]]
Из этой ссылки нужно скопировать access_token. Это весь набор символов от access_token=  до &expires_in  
14 Именно он нужен для отправки запросов из Python. Если вы всё правильно сделали, то код ниже должен заработать. Проверьте себя  
```Python
import requests  


class VK:  
	def __init__(self, access_token, user_id, version='5.131'):  
		self.token = access_token  
		self.id = user_id  
		self.version = version  
		self.params = {'access_token': self.token, 'v': self.version}  
	
	def users_info(self):  
		url = 'https://api.vk.com/method/users.get'  
		params = {'user_ids': self.id}  
		response = requests.get(url, params={**self.params, **params}) 
		 
		return response.json()    
		
access_token = 'access_token'  
user_id = 'user_id'  
vk = VK(access_token, user_id)  
print(vk.users_info())  
```
15 Идентификатор пользователя VK вы можете найти на странице `https://vk.com/settings` в блоке «Адрес страницы»