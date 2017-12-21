# Console Comments

- [Introduction](#introduction)
- [Example](#example)

<a name="introduction"></a>
## Introduction

<a name="example"></a>
## Example

```php
<?php
use Illuminate\Console\Command;

class ImportClientProducts extends Command
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
        $this->info('End Product Data Import');
    }
}
```