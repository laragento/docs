# Create a Console Command

- [Introduction](#introduction)
- [Example](#example)

<a name="introduction"></a>
## Introduction
https://laravel.com/docs/5.5/artisan


## Path in package
packages/vendor/client-import-export/src/Commands/ClientImportProducts.php

## Register
```php
<?php

namespace Vendorname\ClientImportExport;

use Illuminate\Console\Scheduling\Schedule;
use Illuminate\Support\ServiceProvider; 

class ClientImportExportServiceProvider extends ServiceProvider
{

    protected $commands = [
        'Vendorname\ClientImportExport\Commands\ClientImportProducts',
    ];
    // [..]
    
```    

<a name="example"></a>
## Example

```php
<?php
use Illuminate\Console\Command;

class ClientImportProducts extends Command
{
    protected $clientProductImport;
    /**
     * The name and signature of the console command.
     *
     * @var string
     */
    protected $signature = 'client:import-products 
                            {--F|files : Whether the source files should be imported (default: false)} 
                            {--A|archive : Whether to archive the imported SourceFiles after Import (default: false)}'; 

    /**
     * The console command description.
     *
     * @var string
     */
    protected $description = 'Import products from that file in that place';

    /**
     * Execute the console command.
     *
     * @return mixed
     */
    public function handle()
    {
        $this->info('Start Importing Product Data');
        // Do the magic
        // [..]
        $this->info('End Product Data Import');
    }
}
```