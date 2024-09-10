

## Screenshots


![art/screenshot-home.png](art/screenshot-home.png)

![art/screenshot-settings.png](art/screenshot-settings.png)


## Testing

PHPunit is ready setup to test the API side. Tested are all Sanctum and Fortify features cause there are heavily based on there original tests. Thats a good starting point to add tests for your next project. To run the tests you can call phpunit like this:

```bash
php artisan test
```


## explaining

.env.prod for production with nginx php fpm nodejs servers / .env.develop for developing on sail 

>docker compose up //develop

>docker compose -f ./docker-compose-prod.yml up //production



## Run on local

>composer install //install composer

>cp .env.develop .env //copy your env

>npm install

>php artisan key:generate //generate key for your app

>docker compose build

>docker compose up 

>php artisan migrate:refresh

>npm run dev



## Deploy on production server

>Clone your project on server 

>composer install //install composer

>cp .env.prod .env //copy your env don't forget to insert domain ofyour server in env and database password

>put your server adress in /docker/nginx/sites/laravel.conf //server_name [adress] 

>php artisan key:generate //generate key for your app

>sudo npm install // nstall js packages

>docker compose -f ./docker-compose-prod.yml build //build containers every time when you change something in yourproject

>docker compose -f ./docker-compose-prod.yml start //start your app

>docker ps //find your php fpm container and copy ID of this

>sudo docker exec -it [container id]  bash //jump into php-fpm container shell

>chmod o-r www-data:www-data . //give permissions to user something like this

>cd laravel/current/ // Open root directory

>php artisan migrate:refresh // Run migrations 

>read a prayer

>open your app



## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).    
The Vue framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).    
This repository is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).    
