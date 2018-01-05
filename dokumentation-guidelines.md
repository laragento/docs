# Dokumentation Guidelines

- [Introduction](#introduction)
- [List](#list)

<a name="introduction"></a>
## Introduction

<a name="list"></a>
## List
Here is how you should comment your code.

#### in an interface
```php
<?php 
interface CategoryApiInterface
{
      /**
       * Finds a category by an identifier, products and children will be included in the response
       *
       * @param $identifier
       * @return string json
       */
      public function first($identifier);
}      
```
      
#### in a class      
```php
<?php 
class CategoryApi extends Controller implements CategoryApiInterface
{
      /**
       * @var CategoryRepositoryInterface
       */
      protected $categoryRepository;

      /**
       * CategoryApi constructor.
       * @param CategoryRepositoryInterface $categoryRepository
       */
      public function __construct(
            CategoryRepositoryInterface $categoryRepository
      )
      {
            $this->categoryRepository = $categoryRepository;
      }

      /**
       * {@inheritDoc}
       */
      public function first($identifier)
      {
            return Fractal::create(
                  $this->categoryRepository->first($identifier),
                  new CategoryTransformer()
            )
                  ->parseIncludes('products,children')
                  ->toJson();
      }
}     
```

#### in a test
