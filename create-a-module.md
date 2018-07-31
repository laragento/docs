# Module Creation

- [Introduction](#introduction)
- [Additional Folders](#additional-folders)
- [Used External Packages](#used-external-packages)
- [Search](#search)
- [Call Stack](#call-stack)

<a name="introduction"></a>
## Introduction
A module in Laragento represent a group of classes and functionalities that belonging together. (Like Customer and Addresses or Products and Categories)
Ideally a module is like a service witch can be consumed by other parts of the program in a simple and well structured manner.

Laragento-Modules are made with https://nwidart.com/laravel-modules/v3/introduction


<a name="additional-folders"></a>
## Additional folders
- Handlers
	- Take care of tasks not related to the data layer, like file handling
- Managers
	- Facades point to Managers
	- Handle data validation and authorisation by using Requests	
- Models
	- Laravel Models
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

**Not used folders**
These folders are not used and can be deleted:
- Entities
    - Replaced with Models

**Additional folders**
Try to avoid adding new folders to a module
	
  
<a name="used-external-packages"></a>
## Used External Packages
- https://fractal.thephpleague.com/transformers/

<a name="search"></a>
## Search
- https://laracasts.com/series/whatcha-working-on/episodes/16 ?

<a name="call-stack"></a>
## Call Stack
- Circular dependencies between modules are not allowed!