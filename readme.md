<p align="center">
    <br>
    <img src="https://raw.githubusercontent.com/cnvs/art/master/github-header.png" width="500">
</p>

<p align="center">
	<a href="https://travis-ci.org/cnvs/canvas"><img src="https://travis-ci.org/cnvs/canvas.svg?branch=master"></a>
	<a href="https://packagist.org/packages/cnvs/canvas"><img src="https://poser.pugx.org/cnvs/canvas/downloads"></a>
	<a href="https://packagist.org/packages/cnvs/canvas"><img src="https://poser.pugx.org/cnvs/canvas/v/stable"></a>
	<a href="https://packagist.org/packages/cnvs/canvas"><img src="https://poser.pugx.org/cnvs/canvas/license"></a>
    <br>
</p>

## Introduction

A [Laravel](https://laravel.com) publishing platform. Canvas is a fully open source package to extend your 
application and get you up-and-running with a blog in just a few minutes. In addition to a distraction-free 
writing experience, you can view monthly trends on your content, get insights into reader traffic and more!

<img src="https://cnvs.io/img/zDTOCfMeOf2pr1sHax9KqNzWsnF8KOa55CPPyppc.png">

## Installation

> **Note:** Canvas requires you to have user authentication in place prior to installation. You may run the `make:auth` Artisan command to satisfy this requirement.

You may use composer to install Canvas into your Laravel project:

```bash
composer require cnvs/canvas
```

Publish the assets and primary configuration file using the `canvas:install` Artisan command:

```bash
php artisan canvas:install
```

Create a symbolic link to ensure file uploads are publicly accessible from the web using the `storage:link` Artisan command:

```bash
php artisan storage:link
```

## Configuration

> **Note:** You are not required to complete the following steps. You have complete design freedom when integrating the content into your application.

Generate a default controller, blog routes and views to get up and running as quickly as possible:

```bash
php artisan canvas:setup
```

If you want to include [Unsplash](https://unsplash.com) images in your posts, set up a new application at [https://unsplash.com/oauth/applications](https://unsplash.com/oauth/applications). Grab your access key and update `config/canvas.php`:

```php
'unsplash' => [
    'access_key' => env('CANVAS_UNSPLASH_ACCESS_KEY'),
],
```

## Updates

You may update your Canvas installation using composer:

```bash
composer update
```

Run any new migrations using the `migrate` Artisan command:

```bash
php artisan migrate
```

You may also want to run this command to re-publish the assets:

```bash
php artisan vendor:publish --tag=canvas-assets --force
```

## Testing

Run the tests with:

```bash
composer test
```

## License

Canvas is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).