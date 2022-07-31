# Laravel vite

Base installation of Laravel 9 with Jetsteam (Livewire) starter kit. Vite is now the frontend asset bundler.

This base site will allow a comparison with existing projects when a know working example is required.

## Local installation

### Requirements

This is a Laravel 9 project. The requirements are the same as a
new [Laravel 9 project](https://laravel.com/docs/9.x/installation).

- [PHP 8.0+](https://www.php.net/downloads.php)
- [Composer](https://getcomposer.org)
- [Nodejs 14.18.0+ || >=16.0.0](https://nodejs.org/en/download/) for vite

Recommended:

- [Git](https://git-scm.com/downloads)

### Clone

See [Cloning a repository](https://help.github.com/en/articles/cloning-a-repository) for details on how to create a
local copy of this project on your computer.

e.g.

```sh
clone git@github.com:Pen-y-Fan/laravel-vite.git
```

### Install

Install all the dependencies using composer

```sh
cd laravel-vite
composer install
```

### Create .env

Create an `.env` file from `.env.example`

```shell script
cp .env.example .env
```

### Generate APP_KEY

Generate an APP_KEY using the artisan command

```shell script
php artisan key:generate
```

### Configure Laravel

Laravel is compatible with different database servers, MySQL is given as an example setup here, but there should be no
reason why this app wouldn't work on other Laravel supported SQL servers. I have not tested with other SQL servers.

This app uses migrations to generate the tables for the database. Tests will use factories for data. Configure the
Laravel **.env** file with the **database**, updating **username** and **password** as per you local setup.

```text
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_vite
DB_USERNAME=YourDatabaseUserName
DB_PASSWORD=YourDatabaseUserPassword
```

### Create the database

The database will need to be manually created e.g. using MySQL:

```shell
mysql -u YourDatabaseUserName
CREATE DATABASE laravel_vite CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
exit
```

### Migrate

```shell
php artisan migrate
```

## Jetstream

The Laravel Jetstream starter package has been installed which includes Livewire and Tailwind. This provides the
authentication for this package.

### Initial install

The first time the project is cloned the node packages will need to be installed

```shell
npm install
```

### run dev

To develop the front end assets (blade / tailwind) using vite:

```shell
npm run dev
```

## Contributing

This is a **personal project**. Contributions are **not** required. Anyone interested in developing this project are
welcome to fork or clone for your own use.

## Credits

- [Michael Pritchard \(AKA Pen-y-Fan\)](https://github.com/pen-y-fan).

## License

MIT License (MIT). Please see [License File](LICENSE.md) for more information.
