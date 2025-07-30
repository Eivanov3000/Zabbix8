# Zabbix 8.0 Docker Compose

Этот проект содержит docker-compose конфигурацию для развёртывания Zabbix 8.0 (*trunk* версии) с PostgreSQL.

## 📦 Состав
- `zabbix/zabbix-server-pgsql:ubuntu-trunk`
- `zabbix/zabbix-web-nginx-pgsql:ubuntu-trunk`
- `zabbix/zabbix-agent:ubuntu-trunk`
- `postgres:16`

## 🚀 Быстрый старт

```bash
git clone https://github.com/Eivanov3000/zabbix8.git
cd zabbix8

# Создай .env файл
nano .env
# Пример содержимого:
# POSTGRES_USER=zabbix
# POSTGRES_PASSWORD=StrongPassword123!
# POSTGRES_DB=zabbix

docker compose up -d
```

## 🔗 Интерфейс
- Zabbix Web: [http://localhost:8080](http://localhost:8080)
- Логин: `Admin`
- Пароль: `zabbix`

## 📂 Volumes
- PostgreSQL хранит данные в `./postgres-data`

## ⚠️ Предупреждение
- trunk-образы Zabbix 8.0 не предназначены для продакшена
- Используются экспериментальные теги `ubuntu-trunk`

## 🧹 Остановка и очистка
```bash
docker compose down -v
```

---

Автор: [Eivanov3000](https://github.com/Eivanov3000)
