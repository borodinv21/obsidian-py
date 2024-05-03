Связь один к одному может использоваться к примеру для связи Счёта и Пользователя и т.д.

Пример:
```Python
from django.db import models

class User(models.Model):
    name = models.CharField(max_length=50)
    balance = models.OneToOneField(
        Place,
        on_delete=models.CASCADE,
    )

class Balance(models.Model):
    amount = models.IntegerField()
```

Теперь у каждого счёта есть один отдельный пользователь и наоборот.