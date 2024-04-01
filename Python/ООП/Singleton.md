Шаблон проектирования Singleton используется, когда для определенного класса может быть только один экземпляр, имеющий глобальную точку доступа.

Пример:
```python
class DataBase:  
    __instance = None  
  
    def __new__(cls, *args, **kwargs):  
        if cls.__instance is None:  
            cls.__instance = super().__new__(cls)  
  
        return cls.__instance  
  
    def __del__(self):  
        DataBase.__instance = None
```