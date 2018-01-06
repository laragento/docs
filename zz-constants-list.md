# List of constants

## Laragento Core Packages

*./laragento/catalog/src/Repositories/Catalog/CatalogAttributeRepository.php:*

`const ENTITY_TYPE_ID = 4;`

---
*./laragento/catalog/src/Repositories/Product/ProductAttributeRepository.php:*

`const IN_DELIMITER = '|';`

*./laragento/catalog/src/Repositories/Product/ProductAttributeRepository.php:*

`const STORE_DELIMITER = ',';`

*./laragento/catalog/src/Repositories/Product/ProductLinkRepositoryInterface.php:*

```
const DEFAULT_PRODUCTLINK_ATTRIBUTE_TYPES = [
        'varchar',
        'decimal',
        'int'
 ];
 ```

*./laragento/catalog/src/Repositories/Product/ProductRepository.php:*

```
const DEFAULT_FRONTEND_CONFIG = [
        'visibility' => [self::VISIBILITY_CATALOG, self::VISIBILITY_CATALOG_SEARCH],
        'status' => ['1'],
        'child_config' => ['status' => ['1']],
 ];
 ```

*./laragento/catalog/src/Repositories/Product/ProductRepositoryInterface.php:*

`const VISIBILITY_NOT_VISIBLE_INDIVIDUALLY = 1;`

*./laragento/catalog/src/Repositories/Product/ProductRepositoryInterface.php:*

`const VISIBILITY_CATALOG = 2;`

*./laragento/catalog/src/Repositories/Product/ProductRepositoryInterface.php:*

`const VISIBILITY_SEARCH = 3;`

*./laragento/catalog/src/Repositories/Product/ProductRepositoryInterface.php:*

`const VISIBILITY_CATALOG_SEARCH = 4;`

---
*./laragento/catalog-import-export/src/Repositories/ProductImportRepository.php:*

`const REFERENCE_ID = 'sku';`

*./laragento/catalog-import-export/src/Repositories/ProductImportRepositoryInterface.php:*

`const LINK_TYPE_ID = 3;`

---
*./laragento/eav/src/Models/Contracts/ScopedAttributeInterface.php:*

`const SCOPE_STORE = 0;`

*./laragento/eav/src/Models/Contracts/ScopedAttributeInterface.php:*

`const SCOPE_GLOBAL = 1;`

*./laragento/eav/src/Models/Contracts/ScopedAttributeInterface.php:*

`const SCOPE_WEBSITE = 2;`

*./laragento/eav/src/Repositories/AttributeRepository.php:*

`const ENTITY_TYPE_ID = 4;`

---
*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const BEHAVIOR_APPEND = 'append';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const BEHAVIOR_ADD_UPDATE = 'add_update';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const BEHAVIOR_UPDATE = 'update';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const BEHAVIOR_REPLACE = 'replace';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const BEHAVIOR_DELETE = 'delete';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const BEHAVIOR_CUSTOM = 'custom';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const IGNORE_STOCK = false;`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const CONFIG_IGNORE_STOCK = 'ignore_stock';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const CONFIG_BEHAVIOR = 'behavior';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const CONFIG_ARCHIVE_ON_IMPORT = 'archive';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const CONFIG_IMPORT_BASE_PATH = 'import-base-path';`

*./laragento/import-export/src/Managers/Import/ImportInterface.php:*

`const CONFIG_IMPORT_SUB_PATH = 'import-sub-path';`

---
*./laragento/media-storage/src/Managers/Image.php:*

`const MODE = '0777';`

---
*./laragento/review/src/Repositories/ReviewRepositoryInterface.php:*

`const REVIEW_ENTITY_ID_PRODUCT = 1;`

*./laragento/review/src/Repositories/ReviewRepositoryInterface.php:*

`const REVIEW_STATUS_ID_APPROVED = 1;`

*./laragento/review/src/Repositories/ReviewRepositoryInterface.php:*

`const REVIEW_STATUS_ID_PENDING = 2;`

*./laragento/review/src/Repositories/ReviewRepositoryInterface.php:*

`const REVIEW_STATUS_ID_NOT_APPROVED = 3;`

---
*./laragento/store/src/Repositories/StoreRepositoryInterface.php:*

`const ADMIN_STORE_ID = 0;`

*./laragento/store/src/Repositories/StoreRepositoryInterface.php:*

`const DEFAULT_STORE_ID = 1;`

*./laragento/store/src/Repositories/StoreRepositoryInterface.php:*

`const ADMIN_WEBSITE_ID = 0;`

*./laragento/store/src/Repositories/StoreRepositoryInterface.php:*

`const DEFAULT_WEBSITE_ID = 1;`

---
## Mexan XmlImportExport Package

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_ID = 0;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_SHORT_DESCRIPTION = 1;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_DESCRIPTION = 2;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_INGREDIENTS = 3;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_PREPARATION = 4;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_COPIOUSNESS = 5; // Ausgiebigkeit`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_TIPS = 6;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_SKU = 7;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_FOLIC_ACID = 8;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_LACTOSE_FREE = 9;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_VEGAN = 10;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_GLUTEN_FREE = 11;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialAttributesImportTransformer.php:*

`const COL_FAT_FREE = 12;`

---
*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialNutritionImportTransformer.php:*

`const COL_ID = 0;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialNutritionImportTransformer.php:*

`const COL_NAME = 1;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialNutritionImportTransformer.php:*

`const COL_ATTRIBUTE_REAL_NAME = 2;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialNutritionImportTransformer.php:*

`const COL_ATTRIBUTE_VALUE = 4;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvInitialNutritionImportTransformer.php:*

`const COL_SKU = 5;`

---
*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_SKU = 0;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_META_TITLE = 1;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_META_DESCRIPTION = 2;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_USP_1 = 3;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_USP_2 = 4;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_USP_3 = 5;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_USP_4 = 6;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_USP_5 = 7;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvMetaAttributesImportTransformer.php:*

`const COL_LANGUAGE = 8;`

---
*./mexan/xml-import-export/src/Transformers/Initial/CsvReviewImportTransformer.php:*

`const COL_SKU = 1;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvReviewImportTransformer.php:*

`const COL_TITLE = 0;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvReviewImportTransformer.php:*

`const COL_DETAIL = 3;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvReviewImportTransformer.php:*

`const COL_NICKNAME = 5;`

*./mexan/xml-import-export/src/Transformers/Initial/CsvReviewImportTransformer.php:*

`const COL_DATETIME = 4;`

---
*./mexan/xml-import-export/src/Transformers/XmlCustomerImportTransformer.php:*

`const STORE_ID_DE = 1;`

*./mexan/xml-import-export/src/Transformers/XmlCustomerImportTransformer.php:*

`const STORE_ID_FR = 2;`

*./mexan/xml-import-export/src/Transformers/XmlCustomerImportTransformer.php:*

`const STORE_ID_IT = 3;`

*./mexan/xml-import-export/src/Transformers/XmlCustomerImportTransformer.php:*

`const DEFAULT_GROUP_ID = 1;`

*./mexan/xml-import-export/src/Transformers/XmlCustomerImportTransformer.php:*

`const DEFAULT_WEBSITE_ID = 1;`
