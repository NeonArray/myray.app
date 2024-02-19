---
title: Using Ray with Laravel
menuTitle: Installation
weight: 1
---

If you use Laravel, this is the way.

## Installing the package in single Laravel project

```bash
composer require spatie/laravel-ray
```

By installing Ray like this it will also be installed in your production environment. This way your application will not break if you forget to remove a `ray` call.  The package will not attempt to transmit information to Ray when the app environment is set to `production`.

You could opt to install `laravel-ray` as a dev dependency. If you go this route, make sure to remove every `ray` call in the code before deploying.

```bash
composer require spatie/laravel-ray --dev
```

## Use `ray()`, `dd()` and `dump()` in any file.

Head over to the [global installation instructions](/docs/php/vanilla-php/installation#global-installation) to learn how to enable `ray()`, `dd()` and `dump()` in any file.

## Creating a config file

Optionally, you can run an artisan command to publish [the config file](/docs/php/laravel/configuration) in to the project root.

```bash
php artisan ray:publish-config
```

You can also add an option for 'docker' or 'homestead' to give a base configuration for those dev environments.

```bash
php artisan ray:publish-config --docker
# or
php artisan ray:publish-config --homestead
```

## Using Ray in an Orchestra powered test suite

In order to use a Laravel specific functionality you must call Ray's service provider in your base test case.

```php
// add this to your base test case

protected function getPackageProviders($app)
{
    return [
        \Spatie\LaravelRay\RayServiceProvider::class,
    ];
}
```
