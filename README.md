# ansible-role-cpnginx_install

Ansible-роль установки и базовой настройки КриптоПро Nginx.
Лабораторный прототип ВКР.

## Установка роли

```bash
ansible-galaxy role install git+https://github.com/paulitoop/ansible-role-cpnginx_install.git,main,cryptogates.cpnginx_install
```

Готовые playbook-файлы и inventory: https://github.com/paulitoop/cpnginx/tree/main/automation

## Подготовка

По умолчанию роль берёт `files/linux-amd64_deb.tgz` из своей локальной копии.
Поместите туда ранее скачанный дистрибутив либо задайте абсолютный путь
через `cpnginx_install_deb_packet`. Архив исключён из Git. Для текущей
локальной демонстрации он уже добавлен в `files`.
Лицензию при необходимости задавайте через `cpnginx_install_csp_license`
из закрытого источника.

Параметры роли описаны в `defaults/main.yml`, `vars/main.yml` и
`meta/argument_specs.yml`. Проверки Molecule находятся в `molecule/default`.
Для их выполнения также нужен локальный дистрибутив и подготовленный образ.

Корпоративные CI-настройки и привязки к внутренней инфраструктуре исключены.
Переносной Docker lab запускает чистые Ubuntu-шлюзы и вызывает эту роль командой `lab.sh install`.
Роль установки предназначена для отдельных подготовленных Linux-узлов.
Перезагрузка выполняется только после успешного `cpnginx -t`.
Лицензия на распространение исходного кода пока не выбрана.
