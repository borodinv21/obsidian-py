self в классах используется для указания ссылки на экземпляр класса.

Для примера воспользуемся классом `Cat()` из [[Классы]].

Пример:
```python
class Cat:
	name = 'default'

	def set_name(self, name):
		self.name = name

	def get_name(self):
		return self.name
```

Для вызова методов класса воспользуемся следующей конструкцией.

Пример:
```python
cat1 = Cat()

cat.set_name('Барсик')

print(cat.get_name) #Барсик
```

В данном примере мы не передаем в метод параметр `self` потому что этот параметр заполняется автоматически ссылкой на экземпляр `cat1` класса `Cat()`.

Если при написании метода класса не указать параметр `self`, то использовать такой метод в экземплярах этого класса не получится.

Также в `python` вызывать метод класса можно следующей конструкцией, в данном примере демонстрируется работа атрибута `self`.

Пример:
```python
class Passport:  
    pages = 20  
  
    def __init__(self, first_name, last_name, date_of_birth):  
        self.first_name = first_name  
        self.last_name = last_name  
        self.date_of_birth = date_of_birth  
        print('Добавлен новый паспорт')  
  
    def add_visa(self, visa_name):  
        if not hasattr(self, 'visas'):  
            self.visas = [visa_name]  
        else:  
            self.visas.append(visa_name)  
  
    def get_visas(self):  
        if not hasattr(self, 'visas'):  
            print('Виз нет')  
        else:  
            print(f"Список всех виз: {', '.join(self.visas)}")  
  
    def show_info(self):  
        print(f'First Name: {self.first_name} | Last Name: {self.last_name}')

passport_1 = Passport('Vaycheslav', 'Borodin', '11.03.2002')  
Passport.show_info(passport_1) #Вызов метода с передачей в него ссылки на объект класса
```