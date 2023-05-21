# HomeWork-5
Домашняя работа, целью которой являлось создание модели мобильного робота с дифференциальным приводом при помощи ROS2 Galactic Geochelone.

## Состав работы
В результате работы было создано два пакета:
* sus - пакет типа ament-cmake для создания собственного системного сообщения;
* snarbot - пакет типа ament-python который принимает ввод с клавиатуры, выполняет необходимые преобразования и создаёт сообщения для узла визуализации rviz.

## Инструкция по запуску
### Шаг 1: Установка пакетов
1. Создать папку рабочего пространства
```
mkdir ros_ws
cd ./ros_ws
```
2. Склонировать содержимое репозитория
```
git clone https://github.com/Neltarionko/HomeWork-5
```
3. Меняем командную оболочку с Bash на ROS2
```
```
4. Необходимо собрать проект
```
colcon build
```
### Шаг 2: Запуск

1 термирминал запуск ноды
source /opt/ros/galactic/setup.bash
colcon build
. install/local_setup.bash 
ros2 run snarbot publisher 

2 терминал запус rviz
source /opt/ros/galactic/setup.bash
export TURTLEBOT3_MODEL=waffle
ros2 launch turtlebot3_bringup rviz2.launch.py 

3 терминал запус клавиатуры
source /opt/ros/galactic/setup.bash
export TURTLEBOT3_MODEL=waffle
ros2 run turtlebot3_teleop teleop_keyboard 
