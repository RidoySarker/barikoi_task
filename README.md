### Barikoi Task

## Installation

```shell
   cp .env.example .env
```

#### Put Your Nginx Port and phpmyadmin port in .env and set username and password for database

```dockerfile
   sudo docker-compose up -d --build
   sudo docker exec -it barikoi-app bash
   composer install
   npm install
   php artisan key:generate
   php artisan jwt:secret
   php artisan migrate
   php artisan websocket:serve
```

### Endpoints

```shell
   POST /api/login [email:required,password:required]
   POST /api/logout [Bearer `token`]
   POST /api/user-profile [Bearer `token`]
   GET  /api/refresh [Bearer `token`]
   POST /api/users [Bearer `token`]
```

### Websockets

```shell
   /laravel-websockets
```
