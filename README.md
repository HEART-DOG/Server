
## Heart_dog-2019_sw_exhibition

# 1. 개발 내용

* `강아지의 심장박동을 측정하여 강아지의 심장 질환을 사전에 예방하고 건강 상태를 체크한다.' 

* `또한 GPS 모듈을 장착하여 강아지의 반경 1km 안에서 강아지의 위치가 어딘지 체크할 수 있으며 최대한 가벼운 무게를 위해 아두이노 NANO를 사용한다.' 

# 2. 개발 환경

# 아누이노 NANO
*        통신 모듈 : NRF24L01
*        블루투스 모듈 : HC-05 
*        GPS 모듈 : NEO-7M
*        심박 센서
*        Wemos D1 MINI PRO (for. ESP8266)
*        ArduinoJson : https://github.com/bblanchon/ArduinoJson
       
# 안드로이드 : Java
*        Google Map ( 아두이노에서 받은 GPS 위치 기반으로 위치 표시 )
*        User Management ( 회원가입, 로그인 )
*        Dog Management ( 강아지 등록 )
*        Open Weather Map API : https://openweathermap.org/api
*        Google Map API : https://cloud.google.com/maps-platform/?hl=ko

       

# 서버 : PHP, Slim Framework
*       Data Transfer ( 아두이노 / 안드로이드에서 받은 데이터 기반으로 저장 및 Transfer )
*       DB Communication
*       User Management ( 회원가입, 로그인 )
*       Dog Management ( 강아지 등록 )
*       Slim3 Framework : http://www.slimframework.com/
       

# DB : MySQL
*       Data Store
           =============================================================================================   
           # Slim 3 MVC Skeleton

This is a simple skeleton project for Slim 3 that includes FluentPDO, Twig and Monolog.

Base on https://github.com/vhchung/slim3-skeleton-mvc

## Prepare

1. Create your project:

       `$ composer create-project -n -s dev mrmoneyc/slim-mvc-skeleton YOUR_APP_NAME`

2. Create database: `$ cat sql/db.sql | sqlite3 storage/db/db.sqlite`

### Run it:

1. `$ cd YOUR_APP_NAME`
2. `$ php -S 0.0.0.0:8888 -t public/`
3. Browse to http://localhost:8888

### Run coding style check

1. Install [PHP_CodeSniffer] (https://github.com/squizlabs/PHP_CodeSniffer)
2. `$ cd YOUR_APP_NAME`
3. `$ phpcs`

### Run test

1. Install [PHPUnit] (https://phpunit.de/)
2. `$ cd YOUR_APP_NAME`
3. `$ phpunit`

### Notice

Set `storage/` folder permission to writable when deploy to production environment

## Key directories

* `app`: Application code
* `app/controllers`: Controller files
* `app/models`: Model files
* `app/templates`: Template files
* `storage/log`: Log files
* `storage/db`: SQLite DB files
* `public`: Webserver root
* `vendor`: Composer dependencies
* `sql`: sql dump file for sample database

## Key files

* `public/index.php`: Entry point to application
* `app/settings.php`: Configuration
* `app/dependencies.php`: Services for Pimple
* `app/middleware.php`: Application middleware
* `app/routes.php`: All application routes are here
* `app/controllers/IndexController.php`: Controller class for the home page
* `app/models/ConfigurationModel.php`: Model class for configurations table
* `app/templates/index.twig`: Template file for the home page
============
