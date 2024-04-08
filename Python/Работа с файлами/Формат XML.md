![[Pasted image 20240408221831.png]]
![[Pasted image 20240408221356.png]]
![[Pasted image 20240408222206.png]]

Для того, чтобы считать xml файл воспользуемся следующим кодом.

Пример:
```Python
import xml.etree.ElementTree as ET  
  
parser = ET.XMLParser(encoding="utf-8")  
tree = ET.parse("files/filexml.xml")  
  
root = tree.getroot()  
  
print(root.tag)
```

Для вывода определенного элемента используем следующий код.

Пример:
```Python
import xml.etree.ElementTree as ET  
  
parser = ET.XMLParser(encoding="utf-8")  
tree = ET.parse("files/filexml.xml")  
  
root = tree.getroot()  
news_list = root.findall("channel/item")  
  
print(len(news_list))
```

Также элементы файла можно перебрать с помощью цикла for.

Пример:
```Python
import xml.etree.ElementTree as ET  
  
parser = ET.XMLParser(encoding="utf-8")  
tree = ET.parse("files/filexml.xml")  
  
root = tree.getroot()  
news_list = root.findall("channel/item")  
  
for row in news_list:  
    print(row.find('title').text)
```