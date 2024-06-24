# Домашнее задание к занятию 2 «Работа с Playbook» - `Мурчин Артем`

## Подготовка к выполнению

1. * Необязательно. Изучите, что такое [ClickHouse](https://www.youtube.com/watch?v=fjTNS2zkeBs) и [Vector](https://www.youtube.com/watch?v=CgEhyffisLY).
2. Создайте свой публичный репозиторий на GitHub с произвольным именем или используйте старый.
3. Скачайте [Playbook](./playbook/) из репозитория с домашним заданием и перенесите его в свой репозиторий.
4. Подготовьте хосты в соответствии с группами из предподготовленного playbook.

## Основная часть

1. Подготовьте свой inventory-файл `prod.yml`.
2. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает [vector](https://vector.dev). Конфигурация vector должна деплоиться через template файл jinja2. От вас не требуется использовать все возможности шаблонизатора, просто вставьте стандартный конфиг в template файл. Информация по шаблонам по [ссылке](https://www.dmosk.ru/instruktions.php?object=ansible-nginx-install). не забудьте сделать handler на перезапуск vector в случае изменения конфигурации!
3. При создании tasks рекомендую использовать модули: `get_url`, `template`, `unarchive`, `file`.
4. Tasks должны: скачать дистрибутив нужной версии, выполнить распаковку в выбранную директорию, установить vector.
5. Запустите `ansible-lint site.yml` и исправьте ошибки, если они есть.
6. Попробуйте запустить playbook на этом окружении с флагом `--check`.
7. Запустите playbook на `prod.yml` окружении с флагом `--diff`. Убедитесь, что изменения на системе произведены.
8. Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.
9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги. Пример качественной документации ansible playbook по [ссылке](https://github.com/opensearch-project/ansible-playbook). Так же приложите скриншоты выполнения заданий №5-8
10. Готовый playbook выложите в свой репозиторий, поставьте тег `08-ansible-02-playbook` на фиксирующий коммит, в ответ предоставьте ссылку на него.

## Решение

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-01-01-hw.png)

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-01-02-hw.png)

## Доработка решения от 24.06.2024

Запустил `ansible-lint site.yml` и исправил ошибки:

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-05-01-hw.png)

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-05-02-hw.png)

Запустил playbook на этом окружении с флагом `--check`:

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-06-01-hw.png)

Запустил playbook на `prod.yml` окружении с флагом `--diff`:

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-07-01-hw.png)

Повторно запустил playbook с флагом `--diff` и убедился, что playbook идемпотентен:

![alt text](https://github.com/artmur1/18-02-hw/blob/main/img/18-02-08-01-hw.png)

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---
