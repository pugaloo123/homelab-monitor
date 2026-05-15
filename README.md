# Homelab Monitor

Мониторинг сервера в реальном времени на основе Prometheus + Grafana + Node Exporter. Весь стек поднимается одной командой через Docker Compose.

## Архитектура

Сервер → Node Exporter → Prometheus → Grafana

## Технологии

- **Prometheus** — сбор и хранение метрик
- **Grafana** — визуализация и дашборды
- **Node Exporter** — метрики сервера (CPU, память, диск, сеть)
- **Docker Compose** — оркестрация контейнеров

## Что мониторим

- Загрузка CPU
- Использование памяти
- Состояние диска
- Сетевой трафик
- Uptime сервера

## Быстрый старт

Клонируй репозиторий и запусти стек:

```bash
git clone https://github.com/pugaloo123/homelab-monitor.git
cd homelab-monitor
docker compose up -d
```

Открой в браузере:

| Сервис | Адрес |
|--------|-------|
| Grafana | http://YOUR_IP:3000 |
| Prometheus | http://YOUR_IP:9090 |
| Node Exporter | http://YOUR_IP:9100 |

## Дашборд

После запуска импортируй готовый дашборд в Grafana:

1. Перейди в **Dashboards → Import**
2. Введи ID: `1860`
3. Выбери Prometheus как datasource
4. Нажми **Import**

## Проверка статуса

```bash
docker compose ps
```