# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-10-16

### Added

* Добавлен файл сpnginx.conf
* Добавлена переменная для указания пути к cpnginx.conf
* Добавлена переменная для указания пути к default.conf
* Добавлена переменная для указания пути к linux-amd64_deb.tgz

### Changed

* Теперь хэндлер перезаускает cpnginx только через бинарник с помощью флага `-s reload`

## [1.0.2] - 2025-10-10

### Fixed

* Вместо проверки на среду виртуализации сделал поверку на существование systemd

## [1.0.1] - 2025-10-09

### Added

* Новые тесты Molecule для проверки содержимого тестовой странице

### Fixed

* Добавлен отдельный запуск nginx для докера, так как часто в пайплайне ломался systemd

## [1.0.0] - 2025-10-03

### Added

* Публикация первой версии роли cpnginx_install
