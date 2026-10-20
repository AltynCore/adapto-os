# Adapto OS

Сборки Adapto OS — системы для проектов, договоров, мероприятий, закупок, имущества и обращений организации. Сайт: [adapto.kz](https://adapto.kz).

## Установка

На сервере с Linux x86_64 и интернетом:

```
curl -fsSL https://adapto.kz/install.sh | sudo bash
```

Скрипт скачивает последнюю сборку из [релизов](https://github.com/AltynCore/adapto-os/releases), сверяет контрольную сумму и ставит систему в `/opt/adapto`. Повторный запуск обновляет систему, настройки и данные остаются.

Параметры передаются через окружение:

```
curl -fsSL https://adapto.kz/install.sh | sudo BOX_HOST=box.center.kz bash
```

| Переменная | Что задаёт | По умолчанию |
|---|---|---|
| `BOX_HOST` | имя сервера, которое сотрудники набирают в браузере | первый IP-адрес сервера |
| `BOX_PORT` | порт | 80 |
| `ADAPTO_VERSION` | версия, например `0.26.0` | последняя |
| `ADAPTO_DIR` | папка установки | `/opt/adapto` |

Сервер: 2 ядра, 4 ГБ памяти, 30 ГБ диска; Debian 12–13 или Ubuntu 22.04 и новее. Docker ставится из сборки, если его нет.

## Без интернета

Скачайте `adapto-os-<версия>.tar` из релиза, перенесите на сервер и выполните:

```
tar -xf adapto-os-<версия>.tar
cd box-package-<версия>
sudo ./install.sh
```

Руководство администратора — `guide.html` в той же папке, требования и обслуживание — на [adapto.kz/install](https://adapto.kz/install).

## Лицензия

Бесплатная бессрочная лицензия ТОО «AltynCore» — [LICENSE.md](LICENSE.md). Компоненты третьих лиц — [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

Вопросы: info@altyncore.kz, +7 775 898 54 54.
