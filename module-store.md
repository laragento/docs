# Store

- [Introduction](#introduction)

<a name="introduction"></a>
## Introduction
The Store module is responsible for accessing StoreViews, StoreGroups and Websites.

#### Websites 
Multiple websites can be set up that use the same Magento/Laragento installation. The websites can be set up to use the same domain, or different domains.

#### StoreGroups
Currently no support in Laragento. See: http://docs.magento.com/m2/ce/user_guide/stores/stores-all-create-store.html
for more information.

#### StoreViews
Store views are typically used to make the store available in different locales. Shoppers can use the 
language chooser in the header of the store to change the store view.


## Whats the difference between ADMIN_STORE_ID and DEFAULT_STORE_ID?
Keep in mind that information shall be saved in the AdminStore and not in the default language. The default
languages information mustn't be touched.

