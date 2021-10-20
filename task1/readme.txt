Задание:
Чтобы сразу увидеть результат демон запускает скрипт каждую секунду(вместо минуты) и дописывает 1-2 Mb(а не 1-2Gb) 

Файлы:
task1 - Скрипт для запуска демона используя init.d
task1.service - ini файл для systemd
task1_script - Скрипт демон запускающий каждую минуту скрипт из task0
task1_script task1_cleanup - Скрипты копируют/удаляют файлы и запускают демонов соответствующим образом.

Использование:

cd task1

#запуск демона через init.d
#инициализация
./task1_init using initd
#проверка
service task1 status
ls -lah /var/log/time*
#очистка
./task1_cleanup

#запуск демона через systemd
#инициализация
./task1_init using systemd
#проверка
systemctl status task1.service
ls -lah /var/log/time*
#очистка
./task1_cleanup
