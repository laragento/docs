# Create a Console Command

- [Introduction](#introduction)
- [Example](#example)

<a name="introduction"></a>
## Introduction
If you want to know more about Laravel-Commands have a look at: https://laravel.com/docs/5.6/artisan 
To create a command for your module you can use:
```
php artisan module:make-command CreatePostCommand Blog
```

## Register a command
```php
<?php

namespace Vendorname\ClientImportExport;

use Illuminate\Console\Scheduling\Schedule;
use Illuminate\Support\ServiceProvider; 

class ProjectNameImportExportServiceProvider extends ServiceProvider
{
    protected $commands = [
        'VendorName\ProjectNameImportExport\Commands\ClientImportProducts',
    ];
    // [..]
 }       
```    