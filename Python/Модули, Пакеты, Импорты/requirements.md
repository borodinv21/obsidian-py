Для создания файла зависимостей в консоли используем следующую команду:
```python
pip freeze > requirements.txt
```

Файл создан:
![[Pasted image 20240705205109.png]]

Для установки библиотек из файла `requirements.txt` в терминал пишем следующее:
```python
pip install -r requirements.txt
```