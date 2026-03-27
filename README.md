# Manticore PHP Catalog Demo

Dedicated demo repository extracted from `manticoresearch-php`.

## Docker installation (recommended)

```bash
cd <repo-root>
docker compose up -d

cp app/.env.example app/.env
cd app
composer install
php bin/bootstrap-demo.php
php -S localhost:8081 -t public
```

This repository's `compose.yaml` starts the Manticore service in Docker.  
The PHP app itself is run locally via the built-in PHP server.

`php bin/bootstrap-demo.php` recreates the table and loads demo records from fixtures.

### Optional: Makefile shortcuts

If you prefer shorter commands, this repository also provides `Makefile` targets:

```bash
cd <repo-root>
make up
make install
make bootstrap
make serve
```

Open:

- http://localhost:8081/
- http://localhost:8081/admin/upload
- http://localhost:8081/admin/items
