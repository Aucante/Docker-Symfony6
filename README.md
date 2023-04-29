# DOCKER SYMFONY PHP NGINX POSTGRE

## Installation

### Clone project
```bash
git clone https://github.com/Aucante/Docker-Symfony6.git
```
OR
```bash
git clone git@github.com:Aucante/Docker-Symfony6.git
```

### Build 

```bash
docker compose build
```

### Start containers

```bash
docker compose up -d
```

### Stop containers

```bash
docker compose down
```

## Init DB

##### Enter in container php

```bash
docker exec -it {FOLDER-NAME}-{PHP-CONTAINER-NAME} sh
```

##### Install orm-pack bundle

```bash
composer require symfony/orm-pack
```

##### Check postgre

```bash
php bin/console doctrine:query:sql 'select * FROM pg_catalog.pg_tables;'
```

Don't forget to set your database informations.

##### Allow rights

```bash
sudo chown -R {YOUR_USER_NAME} src/
```

```bash
sudo chmod 777 src/
```
