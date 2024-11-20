# Nova Setting Tool

A Laravel Nova package that can change the basic admin panel settings, i.e app title, copyright texts, app version and etc by overriding the default Laravel Nova template which hopefully could help developer when starting their projects without having doing simple stuff over and over again.

## Installation

You can install the package into a Laravel app that uses [Nova](https://nova.laravel.com) via composer:

```bash
composer require schuetzenlust/nova-setting-tool
```

And you need to publish the migration file (this come from unisharp/laravel-settings):

```bash
php artisan vendor:publish --tag=settings
```

Next up, you must register the tool with Nova. This is typically done in the `tools` method of the `NovaServiceProvider`.

```php
// in app/Providers/NovaServiceProvider.php

// ...

public function tools()
{
    return [
        // ...
        new \Schuetzenlust\SettingTool\SettingTool,
    ];
}
```

## Usage

Click on the "Settings" menu item in your Nova app to see the tool provided by this package.


## Todo :

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Security


## Support



## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
