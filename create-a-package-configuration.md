# Package Config

- [Introduction](#introduction)
- [Naming](#naming)
- [Publish Configuration](#publish-configuration)

<a name="introduction"></a>
## Introduction

<a name="naming"></a>
## Naming

<a name="service-provider"></a>
## Service Provider

```php
<?php
use Illuminate\Support\ServiceProvider;

class PackageNameServiceProvider extends ServiceProvider
{
    /**
     * Bootstrap the application services.
     *
     * @return void
     */
    public function boot()
    {
        $this->publishes([
            __DIR__.'/../config/vendor_package-name.php' => config_path('vendor_package-name.php'),
        ]);
    }
}
```


<a name="publish-configuration"></a>
## Publish Configuration
- https://laravel.com/docs/5.5/packages
```
php artisan vendor:publish --force
```
