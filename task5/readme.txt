Задание: 

Файлы:
task5_deb_creator - скрипт генерирует деб пакет из Qt5 .pro файла в указанной папке.

Использование:

cd task5

#создаём деб пакет и устанавливаем его
./task5_create_deb PATH/TO/PRO/FILE/FOLDER
dpkg --install PRO_FILE_NAME_0.1-1_all.deb

#запускаем
/opt/PRO_FILE_NAME

#удаляем пакет
apt remove PRO_FILE_NAME
