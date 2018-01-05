# Catalog Product

- [Introduction](#introduction)
- [Available Methods](#available-methods)
- [Method Listing](#method-listing)

<a name="introduction"></a>
## Introduction
The `Laragento\Catalog\Support\Facades\ProductFacade` provides a easy access point to common tasks related 
to catalog products. Below you see how you can use the Facade in your custom controller. The 4 newest 
products will be returned to your template.

```php
<?php

namespace App\Http\Controllers;
use Laragento\Catalog\Support\Facades\ProductFacade as Product;

class HomeController extends Controller
{
      public function index()
      {
            return view('laragento.home',
                  [
                        'newest' => Product::newest(4)
                  ]);
      }
}
```

<a name="available-methods"></a>
## Available Methods

<a name="method-listing"></a>
## Method Listing

<a name="method-first"></a>
#### `first()`

The `first` method returns formatted information about one product. Information about the 
products **categories**, **attributes** and **children** are automatically included.
The function accepts the productId or the productUrlKey.

```php
<?php 
      Product::first(12);
      // or
      Product::first('product-12-url-key');
```

<a name="method-getIdByUrlKey"></a>
#### `getIdByUrlKey()`

The `getIdByUrlKey` returns the product id by passing an urlKey
```php
<?php 
      Product::getIdByUrlKey('product-12-url-key');
      // 12
```

<a name="method-newest"></a>
#### `newest()`














