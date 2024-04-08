![[Pasted image 20240408220117.png]]
![[Pasted image 20240408220333.png]]![[Pasted image 20240408220507.png]]

Ввод и вывод данных в файле YAML.

Пример:
```Python
import yaml  
from pprint import pprint  
  
data = {"channel" : {"title": "Новость номер 1", "link": "Ссылка номер 1"}}  
  
with open('files/fileyaml.yml', 'w') as file:  
    yaml.dump(data, file, allow_unicode=True, default_flow_style=False)  
  
with open('files/fileyaml.yml', 'r') as file:  
    data = yaml.load(file, Loader=yaml.FullLoader)  
    pprint(data)
```