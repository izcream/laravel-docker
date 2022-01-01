# Laravel + Docker  Compose
Example docker implements to old laravel version

## Installation
1. Clone this repo
2. `cp .env.example .env`
3. config your env file **(Important: required set `DB_HOST` to database)**
3. `docker compose up -d`
4. `docker exec -it ${APP_NAME}-app bash`
5. `composer install`
6. `php artisan key:generate`
7. Do anything you need to laravel ex: migrate, db:seed, passport:install
8. Visit [http://localhost](http://localhost) to view website

## Stack
- Laravel
- Docker Compose
- Mysql
- Nginx
