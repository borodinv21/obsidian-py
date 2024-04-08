![[Pasted image 20240408213121.png]]

Для того, чтобы работать с файлом формата JSON используем библиотеку `json`, далее в примере будет показано считывание данных из файла.

Пример:
```Python
import json  
  
with open('files/filejson.json', 'r') as file:  
    json_data = json.load(file)  
  
print(json_data)
```

С JSON файлом мы можем работать точно так же как и с обычным списком, обращаться к элементам по ключам. В примере будет вывод всех новостей.

Пример:
```Python
import json  
  
with open('files/filejson.json', 'r') as file:  
    json_data = json.load(file)  
    json_items = json_data['rss']['channel']['items']  
  
    print(json_items)
```

Для записи в JSON файл используется метод `dump`, для того, чтобы символы в файл записались корректно аргумент `ensure_ascii` ставим в значение False.

Пример:
```Python
import json  
  
with open('files/filejson.json', 'r') as file:  
    json_data = json.load(file)  
    json_items = json_data['rss']['channel']['items']  
  
    print(json_items)  
  
  
with open('files/result.json', 'w') as file:  
    json.dump(json_items[0], file, ensure_ascii=False)
```

Для красивого вывода в консоль данных из JSON файла воспользуемся библиотекой `pprint`.

Пример:
```Python
import json  
from pprint import pprint  
  
with open('files/filejson.json', 'r') as file:  
    json_data = json.load(file)  
    json_items = json_data['rss']['channel']['items']  
  
    pprint(json_items)
```

Для сохранения одной записи из файла JSON используется метод `dumps`.

Пример:
```Python
import json  
  
with open('files/filejson.json', 'r') as file:  
    json_data = json.load(file)  
    json_items = json_data['rss']['channel']['items']  
  
json_str = json.dumps(json_items[3], ensure_ascii=False)  
  
print(json_str)
```

Для загрузки определённо строки используется метод `loads`.

Пример:
```Python
import json  
  
with open('files/filejson.json', 'r') as file:  
    json_data = json.load(file)  
    json_items = json_data['rss']['channel']['items']  
  
json_str = json.dumps(json_items[3], ensure_ascii=False)  
json_str_2 = json.loads(json_str)  
  
print(json_str_2)
```