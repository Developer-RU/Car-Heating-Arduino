## Arduino-Car-Heating

http://shop-avr.ru/

Автопрогрев авто ОКА (класики и подобных авто) на карбюратор, вместо ручки подсоса.
Данный скетч управляет шаговым двигателем "28BYj-48" с помощью Ардуино платы. 

#### Используемые компоненты

1) Ардуино (Atmega 328).

2) шаговый двигатель 28BYj-48 с драйвером на ULN2003.

3) Преобразователь напряжения 12V -> 5V запитанный напрямую с зажигания.


#### Алгоритм работы
    
При включении зажигания шаговый двигатель включает возвращение в нейтральную точку (в шапке скетча указывается колличество шагов), с максимальной скоростью вращения.

Перемещает пластину на двигателе на заданное колличество шагов, для максимального закрытия заслонки с максимальной скоростью вращения.

В течении установленного времени и установленной скорости вращения плавно вращает шаговый двигатель, который в свою очередь приоткрывает заслонку (подсос). 

По прошествии заданного времени, либо достижении нейтральной точку (концевика) отключает двигатель.

Программа завершается до перезагрузки, либо отключения питания (выключение зажигания). 

#### Ручное управление

В любое время при нажатии на одну из двух клавиш, либо тумблера без фиксации (типа джойстика) включается ручной режим, также до перезагрузки либо отключения питания бортовой сети.

В ручном режиме можно приоткрывать, закрывать заслонку с помощью тумблера (кнопок).

При срабатывании концевика в любом режиме присутствует блокировка максимального открытия (закрытия).

*Ручной режим полезен при сильных морозах, если машина плохо прогрета но надо уже ехать, можно слегка закрыть заслонку и проехать немного, затем вывести в нейтраль также тумблером после полного прогрева.
