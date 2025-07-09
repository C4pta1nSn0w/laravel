<p align="center">
    <a href="#" target="_blank">
        <img src="https://www.docker.com/app/uploads/2023/08/logo-guide-logos-1.svg" width="400" alt="Docker Logo" style="border-radius: 10px;">
        <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo" style="border-radius: 10px;margin-bottom:3rem">
    </a>
</p>
<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>



## Prerequisites

Run the code below when fresh installing the software.


* Build & Start the project
    ```
    docker-compose up -d
    ```

* Set the .ENV File Passwords
  * MYSQL_DATABASE=laravel
  * MYSQL_USERNAME=root
  * MYSQL_PASSWORD=secret
  * MYSQL_ROOT_PASSWORD=secret


* Generate the Key
  ```
  docker-compose exec app php artisan key:generate
  ```
* Run artisan and Migrate the project
  ```
  docker-compose exec app php artisan migrate
  ```
  * laravel: http://localhost:8000
  * phpmyadmin: http://localhost:8080
* Any Issues
  ```
  docker-compose exec app php artisan config:clear  
  ```
  ```
  docker-compose exec app php artisan cache:clear
  ```
* Access Mysql 
  ```
  docker-compose exec db mysql -u root -p
  ```
* Build Docker Image
  ```
  docker build -t username/laravel:latest .
  ```
* Push Docker Image to Hub
  ```
  docker push username/laravel:latest
  ```
  








## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.



## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

