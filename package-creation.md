# Package Creation

- [Introduction](#introduction)
- [First Level](#first-level)
- [Second Level](#second-level)
- [Used Packages](#used-packages)
- [Search](#search)
- [Call Stack](#call-stack)

<a name="introduction"></a>
## Introduction

<a name="first-level"></a>
## First Level
- **database**
- **src**
- **tests**
- **vendor**

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
	- Junction point between data-provider and data-storage/services @see call-stack diagrams below
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
- Browser
	- Laravel Dusk tests in browser
- Integration
	- Tests to integrate with other systems  
- Feature
	- Tests with existing framwork
- Unit
	- Tests without framework

#### **vendor**

<a name="used-packages"></a>
## Used Packages
- https://fractal.thephpleague.com/transformers/

<a name="search"></a>
## Search
- https://laracasts.com/series/whatcha-working-on/episodes/16 ?

<a name="call-stack"></a>
## Call Stack
![Call Stack Layers](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackLayers_v0.1.jpg)
![Call Stack General](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackGeneral_v0.1.jpg)
![Call Stack Packages](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackPackages_v0.1.jpg)
![Call Stack NotAllowed](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackNotAllowed_v0.1.jpg)