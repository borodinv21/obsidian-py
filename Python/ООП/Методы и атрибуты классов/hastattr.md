Метод `hasattr` используется для проверки наличия какого-либо атрибута в классе.

Пример:
```python
class Cat:
	def __init__(self, name):
		self.name = name

cat1 = Cat('Барсик')
print(hasattr(cat1, 'name'))#True
#hasattr(ссылка на объект класса, атрибут класса)
```