# Recipe: Laravel

>laravel recipe to working in development

**Containers**

- php 8.1
- postgres 14.4
- node:18
- mailhog

### Start development

Up containers
```
docker compose up -d
```

Creating new project
```
docker exec lv-php composer create-project laravel/laravel .
```

Install npm deps
```
docker exec lv-node npm install
```

Fix permissions
```
sudo chown -R ${USER}:${USER} project
```

Connect database in ```.env```

```
DB_CONNECTION=pgsql
DB_HOST=postgres
DB_PORT=5432
DB_DATABASE=dev_db
DB_USERNAME=dev_user
DB_PASSWORD=dev_pass
```

### Possible problems

permission to storage folder
```
chmod -R 777 storage
```