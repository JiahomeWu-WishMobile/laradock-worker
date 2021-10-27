# PHP-Worker-Simple-Deploy

This project is for deploying simplify project that only remain container for PHP-Worker functionality in [laradock](https://laradock.io/introduction/).
PHP-Worker is using [Supervisor: A Process Control System](http://supervisord.org/) to run php schedule processes (ex : [Laravel Scheduler](https://laravel.com/docs/8.x/scheduling)) automatically

## How to use it

First
```
cp .env.example .env
cp php-worker/supervisord.d/laravel-scheduler.conf.example laravel-scheduler.conf
```
After change  `APP_CODE_PATH_HOST={your laravel project location}` in `.env`
Run follow command and there you go
```
docker-compose up -d
```


