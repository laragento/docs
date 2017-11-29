# Guidelines Blade

- [Introduction](#introduction)
- [Controller Method Names](#controller-method-names)

<a name="introduction"></a>
## Introduction

<a name="controller-method-names"></a>
## Controller Method Names

> **Look at the guidelines-api for more information/methodes. The method names should be the same**

Source: https://scotch.io/tutorials/simple-laravel-crud-with-resource-controllers

#### edit()

```php
<?php 
    /**
     * Show the form for editing the specified resource.
     *
     * @param  int  $id
     * @return Response
     */
    public function edit($id)
    {
        //
    }
```

#### show()

```php
<?php 
    /**
     * Display the specified resource.
     *
     * @param  int  $id
     * @return Response
     */
    public function show($id)
    {
        //
    }
```

#### index()

```php
<?php 
  /**
     * Display a listing of the resource.
     *
     * @return Response
     */
    public function index()
    {
        //
    }
```    