# ansible-role-cpnginx_install

Ansible-роль установки и базовой настройки КриптоПро Nginx.
Лабораторный прототип ВКР.

## Установка роли

```bash
ansible-galaxy role install git+https://github.com/paulitoop/ansible-role-cpnginx_install.git,main,cryptogates.cpnginx_install
```

Готовые playbook-файлы и inventory: https://github.com/paulitoop/cpnginx/tree/main/automation

## Подготовка

Получите дистрибутив КриптоПро самостоятельно и передайте абсолютный путь
к `linux-amd64_deb.tgz` через переменную `cpnginx_install_deb_packet`.
Лицензию при необходимости задавайте переменной `cpnginx_install_csp_license`
из закрытого источника. Архив и лицензионные значения не публикуются.

Параметры роли описаны в `defaults/main.yml`, `vars/main.yml` и
`meta/argument_specs.yml`. Проверки Molecule находятся в `molecule/default`.
Для их выполнения также нужен локальный дистрибутив и подготовленный образ.

Корпоративные CI-настройки и привязки к внутренней инфраструктуре исключены.
Сквозные испытания этой публикационной копии не проводились.
Лицензия на распространение исходного кода пока не выбрана.
