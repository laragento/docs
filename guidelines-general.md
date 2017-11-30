# Guidelines General

- [Introduction](#introduction)
- [Cases](#cases)

<a name="introduction"></a>
## Introduction

<a name="cases"></a>
## Cases
Here is how you should name your methods, variables, classes and tests.

#### Methods/Variables/Parameters
Methods and Parameters have to be in camelCase

```php
<?php 
      protected $productId;
      
      public function setProductId($productId){
            $this->productId = $productId;
      }
```

#### Classes and interfaces 
Should be UpperCamelCase

```php
<?php 
      class ProductApi extends ProductApiInterface{}
```

#### DB Attributes
Are separated by underscores and are lowercase (like they are in the database).
```php
<?php 
      $product = Product::first(1);
      $productId = $product->entity_id;
```

#### Tests 
Should be separated by underscores. Best write a short sentence 

```php
<?php 
      class CustomerApiTest extends BaseTestCase
      {
            /**
            * @test
            */
            public function get_default_billing_address_of_an_customer()
            {
                  
            }
      }
```

