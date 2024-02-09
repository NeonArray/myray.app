---
title: Using Ray with Craft CMS
weight: 1
---
# Using Ray with Craft CMS
If you use Craft CMS, this is the way.

## Installing the package

You can install Ray through the plugin store, or opt to install through composer.

```bash
composer require spatie/craft-ray
```

By installing Ray this way it will also be installed in your production environment. This way your application will not break if you forget to remove a `ray` call.  The package will not attempt to transmit information to Ray when the app environment is set to anything other than `dev`.

You could opt to install `craft-ray` as a dev dependency. If you go this route, make sure to remove every `ray` call in the code before deploying.

```bash
composer require spatie/craft-ray --dev
```

## Usage

Head over to the [global installation instructions](https://spatie.be/docs/ray/v1/configuration/framework-agnostic-php#global-installation) to learn how to enable `ray()`, `dd()` and `dump()` in any file.
