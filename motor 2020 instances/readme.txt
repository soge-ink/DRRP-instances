-customers.csv
Latitude: широта (gps координаты)
Longitude: долгота (gps координаты)
Boreholes Number: число скважин на объекте
Earliest: наиболее раннее время начала работ
Latest: наиболее позднее время окончания работ
Rig Types: типы буровых установок, которые могут обслуживать данный объект (в данных примерах не используется)

-vehicles.csv
Latitude: широта (gps координаты)
Longitude: долгота (gps координаты)
Type: тип буровой установки (в данных примерах не используется)

-distances.txt
Двумерная матрица времен переезда (в целых днях) от одной вершины к другой (t_ij). В начале списка вершин идут все объекты в порядке, соответствующем файлу 'customers.csv', затем идут буровые установки в порядке, соответствующем файлу 'vehicles.csv'. То есть матрица имеет размер (#объектов + #БУ) * (#объектов + #БУ). В файле она записана в виде одномерного массива с разделителем ' ' (индексом для элемента t_ij будет i * (#объектов + #БУ) + j).

Примеры 11-20 соответствуют сокращению временных окон вдвое в примерах 1-10.

Расстояния по gps координатам рассчитывались как здесь:
https://ru.wikipedia.org/wiki/Ортодромия#Расчёт_ортодромии
с коэффициентом 40. Скорость передвижения задавалась равной 50 км/ч. Расстояние в днях (не целых) округлялось вверх, если дробная часть > 0.1 дней, иначе округление производилось вниз.