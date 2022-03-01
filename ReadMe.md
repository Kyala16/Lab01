## Lab01

Скачиваем библиотеку boost:

`wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`

![This is an image](/assets/images/Pic-1.png)

Разархивируем:
	
	pic-2
	
Считаем количество не включая вложенные директории:
	tree ~/boost_1_69_0 -L 1
	
	pic-3
	
Считаем Включая вложенные:
	tree ~/boost_1_69_0
	
	pic-4
	
Считаем файлы:
	-.cpp  13774
	-.h  296
	-.hpp  14912
	
	-остаьные  37847
	
	find ~/boost_1_69_0 -name "*.cpp" | wc -l
	
	pic-5
	
Пути к any.hpp
	find ~/boost_1_69_0 -name "any.hpp"
	
	pic-6
	
Где есть какая-то часть текста:
	find ~/boost_1_69_0 -type f | xargs grep -i boost::asio
	
Переносим в другую директорию:
	mv * ~/boost-libs
	
	pic-7
	
Смотрим вес файлов:
	ncdu ~/boost-libs
	
	pic-8
	
10 самых тяжелых:
	find ~/boost-libs -type f -exec du -h {} +|sort -rh | head -n 10
	
	pic-9
	
Лабораторная 01 завершина, мною были изучены новые для меня утилиты ОС linux
