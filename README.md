# Домашнее задание к занятию "08.02 Работа с Playbook"

Комманда для запуска playbook в своем окружении с установкой на хост elkib - java, elastic и kibana и запросом пароля root на удаленном хосте:

ansible-playbook site.yml -i inventory/prod.yml --ask-pass

9.  Подготовьте README.md файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.
10. Готовый playbook выложите в свой репозиторий, в ответ предоставьте ссылку на него.

Данный playbook выполняет следующие действия:

- первым разделом задач устанавливаем java 11 (копируем бинарники, распаковываем)
- вторым разделом задач устанавливаем elasticsearch (скачиваем, распаковываем в указанный каталог, генерируем конфигурацию с параметрами)
- третьим разделом задач устанавливаем kibana (скачиваем, распаковываем в указанный каталог, генерируем конфигурацию с параметрами)


В параметрах указываем:

- версии приложений
- домашние директории приложений

Для задач добавлены теги, если нужно установить отдельное приложение.
Нужные задачи запускаются с помощью опции -t, которой передаётся название тега.
В данном playbook 3 тега: java, elastic, kibana
