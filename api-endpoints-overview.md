# Api Endpoints Overview

- [Introduction](#introduction)
- [Endpoints](#endpoints)

<a name="introduction"></a>
## Introduction

<a name="endpoints"></a>
## Endpoints

#### Catalog
```
v1/product/{product_id}
v1/product/{product_slug}
v1/product/attribute-list/{attribute_set}
v1/product/{product_id}/attribute-list
v1/product/{product_id}/parent
v1/product/{product_id}/children
v1/product/{product_id}/price
v1/product/{product_id}/special-price
```

```
v1/category/get
v1/category/all
v1/category/base/{website_id}
v1/category/{category_id}
v1/category/{category_slug}
v1/category/{category_id}/parent
v1/category/{category_id}/children
v1/category/{category_id}/products
```

#### Customer
```
v1/customer/get
v1/customer/all
v1/customer/{customer_id}
v1/customer/{customer_email}
v1/customer/{customer_id}/addresses
v1/customer/{customer_id}/group
v1/customer/{customer_id}/shipping
v1/customer/{customer_id}/billing
v1/customer/{customer_id}/addresses/{address_id}
```

```
v1/address/{address_id}
```



