# Guidelines Api

- [Introduction](#introduction)
- [Method Names](#method-names)
- [Responses](#responses)

<a name="introduction"></a>
## Introduction

<a name="method-names"></a>
## Method names
If you are creating an Api to your Laragento package please use the following method names 
and method-naming-conventions. It makes it a lot easier for an developer to access your data
if all api look the same.


#### first()

```php
<?php 
      /**
       * Returns the first occurrence in an data-list
       * The indentifier is either the id as integer, an object or the the most common and unique 
       * string representaion in the current entity. (like url_key with the product-entity)  
       * When the occurrence is inactive, hidden, not visible or something similar null will be returned  
       */
      public function first($identifier){};
```

#### fall()

```php
<?php 
      /**
       * Return the same result as first() but has some respect for inactive entities
       */
      public function fall($identifier){};
```


#### get()

```php
<?php 
      /**
       * Returns all entities commonly visible 
       */
      public function get(){};
```

#### all()

```php
<?php 
      /**
       * Returns all entities, even entities whom are deactivated
       */
      public function all(){};
```

#### find()

```php
<?php 
      /**
       * Used for complicated search and filter requests
       * returns a list of resources without complicated relation information
       */
      public function find(){};
```

#### store()
```php
<?php 
      /**
       * Store a newly created resource in storage.
       */
      public function store(){};
```

#### update()
```php
<?php 
      /**
       * Update the specified resource in storage.
       */
      public function update($id){};
```

#### destroy($id)
```php
<?php 
      /**
       * Remove the specified resource from storage.
       */
      public function destroy($id){};
```


#### children($id)
```php
<?php 
      /**
       * Returns children of the specified resource, you know like child-categories
       * or simple products in a group-product. 
       */
      public function children($id){};
```

#### allChildren($id)
```php
<?php 
      /**
       * Returns children of the specified resource, even deactivated ones
       */
      public function allChildren($id){};
```

#### parent($id)
```php
<?php 
      /**
       * Returns parent resource of the specified resource
       */
      public function parent($id){};
```

#### Relations
Returns a related property of an resource
The method name should be as readable and short as possible

Some possible Examples: 

```php
<?php 
      /**
       * Example: 
       * Laragento\Customer\Http\Controllers\CustomerApi
       * - Returns the customer group 
       */
      public function group($customerId){};
```

```php
<?php 
      /**
       * Example: 
       * Laragento\Catalog\Http\Controllers\ProductApi
       * - Returns attribute list for a given attribute set
       */
      public function attributesBySetId($attributeSetId){};
```

```php
<?php 
      /**
       * Example:
       * Laragento\Catalog\Http\Controllers\ProductApi
       * - Returns attributes with values for a given product.
       */
      public function attributesWithValues($productId){};
```

#### getXxxByYyy($Yyy)
```php
<?php 
      /**
       * Example:
       */
      public function getIdBySku($sku){};
```

#### allByYyy($Yyy)
```php
<?php 
      /**
       * Example:
       */
      public function allByYyy($yyy){};
```

#### getByYyy($Yyy)
```php
<?php 
      /**
       * Example:
       */
      public function getByYyy($yyy){};
```


<a name="responses"></a>
## Responses
- Api responses from core modules are all ways in json format. 
- When you request more details from an resource you will get the the resource back
according the requested detail information.

#### v1/category/33/children
```
{
  "data": {
    "id": 33,
    "category_id": 33,
    "name": "Küche",
    "parent_id": 2,
    "url_path": "kueche",
    "children": {
      "data": Array[11][
        {
          "id": 7,
          "category_id": 7,
          "name": "Gewürze",
          "url_path": "kueche/gewuerze"
        },
        {
          "id": 8,
          "category_id": 8,
          "name": "Geschenke/Sets",
          "url_path": "kueche/geschenke"
        }
      ]
    }
  }
}
```