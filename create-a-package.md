# Package Creation

- [Introduction](#introduction)
- [Register a package in Laragento](#register)
- [First Level](#first-level)
- [Second Level](#second-level)
- [Used External Packages](#used-external-packages)
- [Search](#search)
- [Call Stack](#call-stack)

<a name="introduction"></a>
## Introduction
A package in Laragento represent a group of classes and functionalities witch are belonging together. (Like Customer and Addresses or Products and Categories)
Ideally a package is like a service witch can be consumed by other parts of the program in a simple and well structured fashion.

https://laravel.com/docs/5.5/packages

<a name="register"></a>
## Register a package in Laragento

#### Add Service Provider
config/app.php
```
/*
 * Laragento Service Providers...
 */
Laragento\Rating\RatingServiceProvider::class,

/*
 * Client Service Providers...
 */
Vendor\ClientImportExport\ClientImportExportServiceProvider::class,
```

#### Add Package to composer.json psr-4
```
"Laragento\\Rating\\": "packages/laragento/rating/src",
```

<a name="first-level"></a>
## First Level
- **database**
- **src**
- **tests**

<a name="second-level"></a>
## Second Level
#### **database**
- factories, migrations, seeder

#### **src**
- Handlers
	- Take care of tasks not related to the data layer, like file handling
- Http
	- Api, Controllers, Middleware and Requests
- Managers
	- Junction point between data-provider and data-storage/services. See [Call Stack](#call-stack) diagrams below
	- Are used by Internal Calls, Controllers, Api Calls, Cron Jobs, Console Commands
	- Package Facades point to Managers
	- Handle data validation and authorisation by using Requests	
- Models
	- Direct access to database tables
- Repositories
	- Get information from internal data storage or store data to storage
- Traits
    - Traits
- Transformers
	- Data-Mapping
- Services
	- Connect to needed webservices like payment provider, delivery, tracking, exchange rates	
- Support
	- Facades, Helpers and Stuff  
- views
	- Presentation Layer
  
#### **tests**
@todo improve concept!

- Browser
	- Laravel Dusk tests in browser
- Integration
	- Tests to integrate with other systems  
- Feature
	- Tests with existing framwork
- Unit
	- Tests without framework

<a name="used-external-packages"></a>
## Used External Packages
- https://fractal.thephpleague.com/transformers/

<a name="search"></a>
## Search
- https://laracasts.com/series/whatcha-working-on/episodes/16 ?

<a name="call-stack"></a>
## Call Stack
#### **Call Stack Layers**
![Call Stack Layers](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackLayers_v0.1.jpg)

#### **Call Stack General**
![Call Stack General](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackGeneral_v0.2.jpg)
- Managers work as junction point between the **date provider layer** and the **data storage layer**

#### **Call Stack Packages**
- It's allowed to call a Manager or an Facade from another Package
- Models can be directly connected (Eloquent)
![Call Stack Packages](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackPackages_v0.1.jpg)

#### **Call Stack NotAllowed**
- The following calls between packages are not allowed
    - Repository A1 calls Repository B1 directly
    - Model ca repository 
    - Circular dependencies between packages are not allowed
![Call Stack NotAllowed](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackNotAllowed_v0.1.jpg)