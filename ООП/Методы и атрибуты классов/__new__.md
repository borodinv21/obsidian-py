Методы __new__ вызывается при создании экземпляра класса.

Пример:
```python
class Cat:
	def __init__(cls, *args, **kwargs):
		print('Создание экземпляра класса Cat')
		return super().__new__(cls) #Возвращаем адрес созданного класса
```