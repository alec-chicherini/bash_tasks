Задание:
 

Файлы:
task2_deb_creator - скрипт копирует файлы в корень пакета, раздаёт разрешения, запускает сборку и подчищает файлы.
conffiles  control  copyright  dirs  postinst  postrm  prerm - файлы для сборки

Использование:

cd task2

#создаём деб пакет и устанавливаем его
./task2_deb_creator
dpkg --install timebomb_0.1-1_all.deb

#проверка
service task1 status
ls -lah /var/log/time*

#удаляем пакет
apt remove timebomb
