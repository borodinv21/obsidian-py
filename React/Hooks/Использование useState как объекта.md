Для того, чтобы не создавать множество useState есть возможность создать один useState и использовать его как объект, свойствами которого будут являться нужные нам состояния.

Пример того как можно отрефакторить код. Снизу старый код, сверху новый измененный код.
![[Pasted image 20240417231753.png]]

Используем новое состояние следующим образом.
![[Pasted image 20240417232140.png]]

Также, если нам необходимо изменить значение не для всех полей, то используем следующий код, так как в ином случае в других полях ничего не будет храниться.
![[Pasted image 20240417234242.png]]

Для обращения к свойствам объекта используем следующий синтаксис.
![[Pasted image 20240417232229.png]]
![[Pasted image 20240417232243.png]]

