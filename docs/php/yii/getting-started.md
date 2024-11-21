---
title: Using Ray With Yii
weight: 1
---

You can use Ray with Yii via this third party package:

[spatie/yii-ray](https://github.com/spatie/yii-ray)

## Installing the package

```bash
composer require spatie/yii-ray
```

By installing Ray this way it will also be installed in your production environment. This way your application will not break if you forget to remove a `ray` call.  The package will not attempt to transmit information to Ray when the app environment is set to anything other than `dev`.

You could opt to install `yii-ray` as a dev dependency. If you go this route, make sure to remove every `ray` call in the code before deploying.

```bash
composer require spatie/yii-ray --dev
```

## Usage

Head over to the [global installation instructions](/docs/php/vanilla-php/installation#global-installation) to learn how to enable `ray()`, `dd()` and `dump()` in any file.
