## Lab01

Скачиваем библиотеку boost(***Задание1***):

`wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`

![Pic-1](акт 3.png)

Разархивируем(***Задание2***):
	
`tar -xvf boost_1_69_0.tar.gz`	
	
![Pic-2](Pic-2.png)
	
Считаем количество не включая вложенные директории(***Задание3***):

`tree ~/boost_1_69_0 -L 1`
	
![Pic-3](Pic-3.png)
	
Считаем Включая вложенные(***Задание4***):

`tree ~/boost_1_69_0`
	
![Pic-4](Pic-4.png)
	
Считаем файлы(***Задание5***):

`find ~/boost_1_69_0 -name "*.cpp" | wc -l`

	1).cpp  13774
	2).h  296
	3).hpp  14912
	
	4)остальные  37847
	
	
![Pic-5](Pic-5.png)
	
Пути к any.hpp(***Задание6***):

`find ~/boost_1_69_0 -name "any.hpp"`
	
![Pic-6](Pic-6.png)
	
Где есть какая-то часть текста(***Задание7***):

`find ~/boost_1_69_0 -type f | xargs grep -i boost::asio`
	
Переносим в другую директорию(***Задание9***):

`mv * ~/boost-libs`
	
![Pic-7](Pic-7.png)
	
Смотрим вес файлов(***Задание10***):

`ncdu ~/boost-libs`
	
![Pic-8](Pic-8.png)
	
10 самых тяжелых(***Задание11***):

`ls -lS`
	
