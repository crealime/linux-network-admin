## Yum

`yum help` `man yam` — отображение команд и опций

`yum list` — список названий пакетов из репозитория

`yum list available` — список всех доступных пакетов

`yum list installed` — список всех установленных пакетов


`yum list installed httpd` — установлен ли указанный пакет

`yum list all` — список установленных и доступных пакетов

`yum list kernel` — список пакетов, относящихся к ядру

`yum info httpd` — отображение информации о пакете

`yum deplist httpd` — список зависимостей и необходимых пакетов

`yum provides "*bin/top"` — найти пакет, который содержит файл

`yum search httpd` — поиск пакета по имени и описанию

получить информацию о доступных обновлениях безопасности
#yum updateinfo list security

вывести список групп
#yum grouplist

вывести описание и содержимое группы
#yum groupinfo "Basic Web Server"

установка группы пакетов «Basic Web Server»
#yum groupinstall "Basic Web Server"

удаление группы
#yum groupremove "Basic Web Server"

Проверка на доступные обновления
#yum check-update

список подключенных репозиториев
#yum repolist

информация об определенном репозитории
#yum repoinfo epel

информация о пакетах в указанном репозитории
#yum repo-pkgs epel list

установить все пакеты из репозитория
#yum repo-pkgs reponame install

удалить пакеты установленные из репозитория
#yum repo-pkgs reponame remove

создать кэш
#yum makecache

проверить локальную базу rpm (поддерживаются параметры dependencies, duplicates, obsoletes, provides)
#yum check

#yum check dependencies

просмотр yum истории (вывод списка транзакций)
#yum history list

просмотр информации определенной транзакции (установленные пакеты, установленные зависимости)
#yum history info 9

отмена транзакции
#yum history undo 9

повторить
#yum history redo 9

дополнительно можно просмотреть лог
#cat /var/log/yum.log

удалить пакеты сохраненные в кэше
#yum clean packages

удалить все пакеты и метаданные
#yum clean all

установить пакет
#yum install httpd

удаление пакета
#yum remove httpd

обновить пакет
#yum update httpd

обновить все пакеты
#yum update

обновить до определенной версии
#yum update-to

установить из локальной директории (поиск/установка зависимостей будут произведены из подключенных репозиториев)
#yum localinstall httpd.rpm

или
#yum install httpd.rpm

установить с http
#yum localinstall http://server/repo/httpd.rpm

откатиться к предыдущей версии пакета
#yum downgrade

переустановка пакета (восстановление удаленных файлов)
#yum reinstall httpd

удаление ненужных более пакетов
#yum autoremove

создание локальных репозиториев (createrepo ставится отдельно)
#createrepo

установка обновлений по расписанию (yum-cron устанавливается отдельно)
#yum-cron



Опции Yum

ответить «yes» при запросе,
-y

#yum update -y

ответить «no» при запросе
--assumeno

использовать Yum без плагинов
--noplugins

или отключить определенный плагин
--disableplugin=fastestmirror

включить плагины, которые установлены, но отключены
#yum --enableplugin=ps

включить отключенный репозиторий
#yum update -y --enablerepo=epel

отключить репозиторий
#yum update -y --disablerepo=epel

скачать пакеты, но не устанавливать
(на Centos 7 x86_64 будут скачаны в '/var/cache/yum/x86_64/7/base/packages/')
#yum install httpd --downloadonly


Cледующие команды доступны после установки пакета yum-utils

найти из какого репозитория установлен пакет
#find-repos-of-install httpd

найти процессы, пакеты которых обновлены и требуют рестарта
#needs-restarting

запрос к репозиторию, узнать зависимости пакета, не устанавливая его
#repoquery  --requires --resolve httpd

синхронизировать yum репозиторий updates в локальную директорию repo1
#reposync -p repo1 --repoid=updates

проверить локальный репозиторий на целостность
#verifytree URL

завершить транзакции
#yum-complete-transaction

установить необходимые зависимости для сборки RPM пакета
#yum-builddep

управление конфигурационными опциями и репозиториями yum
#yum-config-manager

запрос к локальной базе yum, отображение информации о пакете
(использованная команда, контрольная сумма, URL с которого был установлен и другое)
#yumdb info httpd

скачать rpm пакеты из репозитория
#yumdownloader

скачать src.rpm пакет из репозитория
(должен быть подключен соответствующий репозиторий, например в '/etc/yum.repos.d/CentOS-Sources.repo' в CentOS)
yumdownloader --source php


Конфигурационные файлы Yum и их расположение

Основной конфигурационный файл
/etc/yum.conf

директория, с конфигурациями (например, yum плагины)
/etc/yum/

директория, содержащая информацию о репозиториях
/etc/yum.repos.d/


Некоторые опции yum.conf:

Директория, где yum хранит кэш и файлы базы (по умолчанию '/var/cache/yum')
cachedir=/var/cache/yum/$basearch/$releasever

Определяет должен или нет Yum хранить кэш заголовков и пакетов после успешной установки. Значения: 0 или 1. (по умолчанию 1)
keepcache=1

уровень вывода отладочных сообщений. Значения: 1-10 (по умолчанию 2)
debuglevel=2

лог файл (по умолчанию '/var/log/yum.log')
logfile=/var/log/yum.log

обновлять устаревшие пакеты
obsoletes=1

проверка подписи пакетов. Значения: 0 или 1 (по умолчанию 1)
gpgcheck=1

включение плагинов. Значения: 0 или 1 (по умолчанию 1)
plugins=1



Некоторые полезные плагины

Добавляет опцию командной строки для просмотра ченжлога перед/после обновлениями
yum-plugin-changelog

выбирает более быстрые репозитории из списка зеркал
yum-plugin-fastestmirror

добавляет команды keys, keys-info, keys-data, keys-remove, которые позволяют работать с ключами.
yum-plugin-keys

блокировать указанные пакеты от обновления, команда yum versionlock
yum-plugin-versionlock

добавление команд yum verify-all, verify-multilib, verify-rpm для проверки контрольных сумм пакетов
yum-plugin-verify


Работа Yum через прокси сервер

Для всех пользователей:
добавить в секцию [main] в /etc/yum.conf
proxy="http://server:3128"

при необходимости указать пароль, добавить
proxy_proxy_username=user
proxy_password=pass

указать прокси для отдельного пользователя
#export http_proxy="http://server:3128"



---
[Home](../README.md) -> [CLI](cli.md)
