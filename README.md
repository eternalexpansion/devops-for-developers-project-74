### Hexlet tests and linter status:
[![Actions Status](https://github.com/eternalexpansion/devops-for-developers-project-74/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/eternalexpansion/devops-for-developers-project-74/actions)


![CI](https://github.com/eternalexpansion/devops-for-developers-project-74/actions/workflows/push.yml/badge.svg)


## Требования к системе

- Docker (>= 20.10.0)
- Docker Compose (>= 1.27.0)
- Node.js (>= 18.x) — для локального запуска (необязательно, если всё через Docker)
- Git

## Запуск приложения

```bash
git clone https://github.com/eternalexpansion/devops-for-developers-project-74.git
cd devops-for-developers-project-74
docker-compose up
```

Приложение будет доступно по:

- `http://localhost:8080` — прямой доступ.
- `http://localhost` — через Caddy (HTTP).
- `https://localhost` — через Caddy (HTTPS).

## Запуск тестов

```bash
docker-compose -f docker-compose.yml up --abort-on-container-exit --exit-code-from app
```

## Docker Hub образ

- Официальный образ: `eternalexpansion/devops-for-developers-project-74:latest`
- Образ собирается и пушится в Docker Hub через GitHub Actions.
- Makefile содержит команды для подготовки и запуска проекта.