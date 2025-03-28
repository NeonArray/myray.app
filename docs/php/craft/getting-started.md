---
title: Using Ray With Craft CMS
weight: 1
---

You can use Ray with Craft CMS via this third party package:

[spatie/craft-ray](https://github.com/spatie/craft-ray)

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

## Install the plugin

```bash
craft plugin/install craft-ray
```

## Usage

Head over to the [global installation instructions](/docs/php/vanilla-php/installation#global-installation) to learn how to enable `ray()`, `dd()` and `dump()` in any file.

