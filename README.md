# Мониторинг энергообъектов Новосибирской области

![Стек](https://img.shields.io/badge/React%20%C2%B7%20Express%20%C2%B7%20PostgreSQL-334155?style=flat-square) ![Семестр](https://img.shields.io/badge/семестр-4-0f766e?style=flat-square) ![Статус](https://img.shields.io/badge/статус-%D0%A3%D1%87%D0%B5%D0%B1%D0%BD%D1%8B%D0%B9%20%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82-64748b?style=flat-square)

Учебное веб-приложение для работы с энергообъектами, инцидентами и отчётами. React-интерфейс обращается к Express API, данные хранятся в PostgreSQL.

## Состав приложения

| Каталог | Назначение |
|---|---|
| [frontend](frontend/) | React, Material UI, маршрутизация и страницы приложения |
| [backend/src](backend/src/) | Express, модели Sequelize, маршруты API и проверка JWT |
| [database/init.sql](database/init.sql) | Начальная схема и данные БД |
| [docker-compose.yml](docker-compose.yml) | Совместный запуск трёх сервисов |

## Запуск через Docker

Нужны Docker и Docker Compose.

```bash
git clone https://github.com/Assweg/4laba_4sem.git
cd 4laba_4sem
docker compose up --build -d
```

| Сервис | Адрес на компьютере |
|---|---|
| Интерфейс | http://localhost:3001 |
| Backend | http://localhost:5002 |
| PostgreSQL | `localhost:5434` |

Порты взяты из текущего `docker-compose.yml`. Для остановки: `docker compose down`.

## Разработка

Frontend:

```bash
cd frontend
npm install
npm start
```

Backend в отдельном терминале:

```bash
cd backend
npm ci
npm run dev
```

Для запуска вне Docker отдельно настройте подключение backend к PostgreSQL и адрес API frontend.

## Конфигурация и статус

Compose содержит демонстрационные реквизиты БД и значение JWT-секрета для учебного стенда. Перед внешним развёртыванием их нужно заменить. Исходники опубликованы как учебная работа; автоматический деплой, успешные тесты и готовность к промышленной эксплуатации здесь не заявляются.

## Связанные материалы

[Начальная версия интерфейса](https://github.com/Assweg/1laba_4sem) · [Локальные варианты проекта и отчёты](https://github.com/Assweg/nstu).

---

[Каталог учебных репозиториев](https://github.com/Assweg/nstu) · [Профиль Assweg](https://github.com/Assweg)

## Материалы из локальной папки

Исходники и документы этой работы собраны в этом репозитории.

Локальный вариант отличается от ранее опубликованного кода и сохранён в [local-version](local-version/). Основная версия остаётся в корне. Для запуска локального варианта сначала перейдите в его каталог.

[local-version](local-version/) · [reports](reports/) · [variants](variants/)

### Отчёты и документы

- [Отчет Лабораторная 4 БутаковНМ.docx](reports/%D0%9E%D1%82%D1%87%D0%B5%D1%82%20%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%204%20%D0%91%D1%83%D1%82%D0%B0%D0%BA%D0%BE%D0%B2%D0%9D%D0%9C.docx)
