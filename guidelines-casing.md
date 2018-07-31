# Casing Guidelines

- [Introduction](#introduction)

<a name="introduction"></a>
## Introduction

Here is defined how you should name your methods, variables, classes and tests.

### Methods/Variables/Parameters
Methods and Parameters have to be in camelCase (in blade templates as well)

```php
<?php 
      protected $productId;
      
      public function setProductId($productId){
            $this->productId = $productId;
      }
```

### Classes and Interfaces 
Should be UpperCamelCase

```php
<?php 
      class ProductApi extends ProductApiInterface{}
```

### DB Attributes
Are separated by underscores and are lowercase (like they are in the database).
```php
<?php 
      $product = Product::first(1);
      $productId = $product->entity_id;
```

### Array Keys
Are separated by underscores and are lowercase
```php
<?php 
      $customer = 
      [
            'address_firstname' => 'Arthur',    
            'address_lastname' => 'Dent',    
      ];
```

> Exception!
```php
<?php 
        return view('catalog.product', [
            'productQty' => $productQty,
            'storeId' => $storeId,
        ]);
```


### Tests 
Should be separated by underscores. Best write a short sentence. 
Don't add test to the method name. 
Add @test to the comment

```php
<?php 
      class CustomerApiTest extends BaseTestCase
      {
            /**
            * @test
            */
            public function get_default_billing_address_by_customer_id()
            {
                  // [..]
            }
      }
```

