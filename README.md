#Example docker compose implements to laravel old version

## include
 - Laravel
 - Nginx
 - Mysql

- cp .env.example -> .env
- docker compose up -d
- docker exec -it ${APP_NAME}-app bash
- composer install
- php artisan key:generate
- php artisan passport:install / php artisan migrate
- visit http://localhost to see you site
