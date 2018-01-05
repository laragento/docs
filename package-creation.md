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
	- <em style="color:olive;">Take care of tasks not related to the data layer, like file handling</em>
- Http
	- <em style="color:olive;">Api, Controllers, Middleware and Requests</em>
- Models
	- <em style="color:olive;">Direct access to database tables</em>
- Repositories
	- <em style="color:olive;">Get information from internal data storage or store data to storage</em>
- Managers
	- <em style="color:olive;">Junction point between data-provider and data-storage/services @see call-stack diagrams below</em>
- Traits
    - <em style="color:olive;">Traits</em>
- Transformers
	- <em style="color:olive;">Data-Mapping</em>
- Support
	- <em style="color:olive;">Facades, Helpers and Stuff</em>  
- views
	- <em style="color:olive;">Presentation Layer</em>
  
#### **tests**
- Browser
	- <em style="color:olive;">Laravel Dusk tests in browser</em>
- Integration
	- <em style="color:olive;">Tests to integrate with other systems</em>  
- Feature
	- <em style="color:olive;">Tests with existing framwork</em>
- Unit
	- <em style="color:olive;">Tests without framework</em>

#### **vendor**

<a name="used-packages"></a>
## Used Packages
- https://fractal.thephpleague.com/transformers/

<a name="search"></a>
## Search
- https://laracasts.com/series/whatcha-working-on/episodes/16 ?

<a name="call-stack"></a>
## Call Stack
![Call Stack General](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackGeneral_v0.1.jpg)
![Call Stack Packages](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackPackages_v0.1.jpg)
![Call Stack Packages](https://raw.githubusercontent.com/laragento/docs/develop/images/CallStackNotAllowed_v0.1.jpg)