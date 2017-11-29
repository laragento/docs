# Catalog Product

- [Introduction](#introduction)
- [Available Methods](#available-methods)
- [Method Listing](#method-listing)

<a name="introduction"></a>
## Introduction
The `Laragento\Catalog\Support\Facades\ProductFacade` provides an easy access point to common tasks related 
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
<style>
    #product-method-list > p {
        column-count: 3; -moz-column-count: 3; -webkit-column-count: 3;
        column-gap: 2em; -moz-column-gap: 2em; -webkit-column-gap: 2em;
    }
    #product-method-list a {
        display: block;
    }
</style>

<div id="product-method-list" markdown="1">
    [get](#method-get)
    [getIdByUrlKey](#method-getIdByUrlKey)
    [newest](#method-newest)
</div>

<a name="method-listing"></a>
## Method Listing

<style>
    #product-method code {
        font-size: 14px;
    }
    #product-method:not(.first-product-method) {
        margin-top: 50px;
    }
</style>

<a name="method-first"></a>
#### `first()` {#product-method .first-product-method}

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
#### `getIdByUrlKey()` {#product-method}

The `getIdByUrlKey` returns the product id by passing an urlKey
```php
<?php 
      Product::getIdByUrlKey('product-12-url-key');
      // 12
```

<a name="method-newest"></a>
#### `newest()` {#product-method}














