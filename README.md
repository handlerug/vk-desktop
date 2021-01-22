# VK Desktop

## Скачать VK Desktop

Скачать последнюю версию приложения всегда можно [здесь](https://github.com/danyadev/vk-desktop/releases).

## Сборка приложения

У вас должен быть установлен [Node.js](http://nodejs.org) **версии минимум 10.13.0** и [Git](https://git-scm.com/downloads).

Для установки пакетов используется yarn, который можно установить с помощью npm:
```bash
npm i -g yarn
```

```bash
$ git clone https://github.com/danyadev/vk-desktop.git # Клонирование репозитория
$ cd vk-desktop # Переход в папку приложения
$ yarn # Установка всех зависимостей в проекте
$ yarn build # Сборка клиента
# Только для Windows:
# Здесь можно указать 32, 64 или ничего, чтобы собрать под все разрядности
$ yarn win-setup[32|64] # Сборка установщика
```

После сборки все файлы будут находиться в папке `build`.

## Получение логов

Для исправления некоторых ошибок разработчику могут понадобиться логи,
которые можно найти по соответствующему пути для каждой системы:

* **Windows**: `%appdata%/vk-desktop/logs/`
* **macOS**: `~/Library/Logs/vk-desktop/`
* **Linux**: `~/.config/vk-desktop/logs/`

## Возможная проблема при разработке на Windows

Если у вас вдруг при обновлении страницы приложения перестал отображаться контент, то необходимо
открыть папку `AppData/Roaming` (открывается с помощью комбинации клавиш `Win+R` и вводе в открывшемся окне `%appdata%`)
и удалить оттуда папку `Electron`. В данной папке находится кеш приложения, поэтому
после удаления приложение полностью сбросится и необходимо будет заново войти в аккаунт.
