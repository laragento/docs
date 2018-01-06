# Method Names Guidelines

- [Introduction](#introduction)
- [Method Names](#method-names)
- [More Examples](#more-examples)

<a name="introduction"></a>
## Introduction
If you are creating an Manager, Api or Controller to your Laragento package, please use the following method names 
and method-naming-conventions. It makes it a lot easier for a developer to access your data
if all method-names look the same.

<a name="method-names"></a>
## Method names
#### first()

```php
<?php 
      /**
       * Returns the first occurrence in a data-list
       * The indentifier is either the id as integer, an object or the the most common and unique 
       * string representaion in the current entity. (like url_key with the product-entity)  
       * When the occurrence is inactive, hidden, not visible or something similar null will be returned  
       */
      public function first($identifier){};
```

#### forceFirst()

```php
<?php 
      /**
       * Return the same result as first() but has some respect for inactive entities
       */
      public function forceFirst($identifier){};
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
Returns a related property of a resource
The method name should be as readable and short as possible

Some possible Examples: 

#### xxx($yyyZZ)
When you want to access relation information
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
       * Laragento\Customer\Http\Controllers\CustomerApi
       * - Returns addresses for a customer
       */
      public function addresses($customerId){};
```

#### xxxWithYyy($yyy)
When you want to access additional relation information

```php
<?php 
      /**
       * Example:
       * Laragento\Catalog\Http\Controllers\ProductApi
       * - Returns attributes with values for a given product.
       */
      public function attributesWithValues($productId){};
```

#### xxxByYyy($yyy)
```php
<?php 
      /**
       * Example: 
       * Laragento\Catalog\Http\Controllers\ProductApi
       * - Returns attribute list for a given attribute set id
       */
      public function attributesBySetId($attributeSetId){};
```

#### getXxxByYyy($yyy)
You can use get if the method is badly readable like *idBySku()*
Keep in mind that short and clean method names are more readable.
```php
<?php 
      /**
       * Example:
       */
      public function getIdBySku($sku){};
```

#### getByYyy($Yyy)
```php
<?php 
      /**
       * Example:
       */
      public function getByYyy($yyy){};
```

#### allByYyy($yyy)
```php
<?php 
      /**
       * Example:
       */
      public function allByYyy($yyy){};
```

<a name="more-examples"></a>
## More Examples
