<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Table Of Contents

[[_TOC_]]

## Requirements
- Laravel 9.x (PHP 8.1)
- NodeJS > 14
- Composer

## How to install

### Clone Repository
open your terminal, go to the directory that you will install this project, then run the following command:

```bash
git clone http://demo.te.net.id:8001/yyusronwirawan/base-laravel.git

cd base-laravel 
```

### Install packages
Install vendor using composer

```bash
composer update
```

Install node module using npm

```bash
npm install
```

### Configure .env
Copy .env.example file

```bash
cp .env.example .env
```

Then run the following command :

```php
php artisan key:generate
```

### Migrate Data
create an empty database with mysql 8.x version, then setup that fresh db at your .env file, then run the following command to generate all tables and seeding dummy data:

```php
php artisan migrate:fresh --seed
```
### Public Disk
To make these files accessible from the web, you should create a symbolic link from public/storage to storage/app/public.
To create the symbolic link, you may use the storage:link Artisan command:

```php
php artisan storage:link
```

### Running Application
To serve the laravel app, you need to run the following command in the project director (This will serve your app, and give you an adress with port number 8000 or etc)
- **Note: You need run the following command into new terminal tab**

```php
php artisan serve
```

Running vite
- **Note: You need run the following command into new terminal tab**

```bash
npm run dev
```

Access from public not found 404
```bash
sudo a2enmod rewrite
sudo service apache2 restart
AllowOverride All
```

## Email Test

MailHog is an email testing tool for developers.
- Inbox : 202.91.14.2:8025(http://202.91.14.2:8025)
- SMTP : 202.91.14.2:8125

## Integrate a Template
- Unzip in resource/template/name_template
- Add base css to resources/css/app.css
- Make main.js and add base js to resources/js/main.js (for production, see example)
- Make main-dev.js and add base js to resources/js/main-dev.js (for dev, see example)
- Edit vite.config.js

## Make API Documentation
### Swagger UI
- Manual write yaml/json
> - Edit resource/js/swagger.js
> - change url of json/yaml
- Using Postman Collection JSON
> - export collection to json
> - convert postman json to openapi json/yaml using [apimatic.io](http://apimatic.io) (Login / Signup Free)
> - Transform API
> - Convert and download
> - do as manual write

## VS Code Extension
- code --list-extensions | xargs -L 1 echo code --install-extension (UNIX)
- code --list-extensions | % { "code --install-extension $_" } (Windows)

> - code --install-extension ahinkle.laravel-model-snippets
> - code --install-extension amiralizadeh9480.laravel-extra-intellisense
> - code --install-extension austenc.laravel-blade-spacer
> - code --install-extension bmewburn.vscode-intelephense-client
> - code --install-extension calebporzio.better-phpunit
> - code --install-extension codingyu.laravel-goto-view
> - code --install-extension formulahendry.auto-close-tag
> - code --install-extension MehediDracula.php-namespace-resolver
> - code --install-extension ms-vscode.sublime-keybindings
> - code --install-extension neilbrayfield.php-docblocker
> - code --install-extension onecentlin.laravel-blade
> - code --install-extension onecentlin.laravel5-snippets
> - code --install-extension SonarSource.sonarlint-vscode
> - code --install-extension Codeium.codeium

## Usefull Links

- [Laravel 10 Documentations](https://laravel.com/docs/10.x/)
- [Spatie Laravel Permission](https://spatie.be/docs/laravel-permission/v5/introduction/)
- [AdminLTE](https://adminlte.io/)
- [Check Coding Standard](https://github.com/squizlabs/PHP_CodeSniffer)
- [PHP code style fixer - Laravel Pint](https://laravel.com/docs/9.x/pint)
- [Package yang berisi data Provinsi, Kabupaten/Kota, dan Kecamatan/Desa di seluruh Indonesia](https://github.com/laravolt/indonesia)

## FAQ
#### Apakah itu laravel pint?
Alat untuk merapihkan penulisan PHP, cara penggunaan ./vendor/bin/pint
#### Bagaimana cara mengubah template?
Template berada di folder storage/app.public/. Daftarkan url js dan css ke table preference. ubah THEME="default" di environment (.env)
#### Arsitektur apa yang digunakan?
Minimal dengan arsitektur MVC, bisa juga menambahkan service pattern, dan memungkinkan juga memakai repository jika diperlukan.
#### Apakah wajib mengunakan service dan repository ini?
Penggunaan service dan repository adalah optional.
#### Kapan penggunaan service pattern itu?
Penggunaan service pattern ketika banyak logic yang bisa dipanggil ulang.
#### Apa isi dari service pattern itu?
Isi service pattern adalah logic.
#### Kapan penggunaan repository pattern itu?
Penggunaan repository pattern ketika mengakses data selain database atau ketika query manual.
#### Apa isi dari repository pattern itu?
Isi repository pattern adalah query bisa juga logic untuk ambil data selain database semisal dari API.
#### Apakah boleh memanggil model di service?
Boleh
#### Apakah boleh memanggil model di repository?
Boleh
#### Bisakah service menggunakan service lainnya?
Bisa


## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
