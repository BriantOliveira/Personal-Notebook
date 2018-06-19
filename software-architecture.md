### Software Architecture for the Enterprise Architect

What is UML?

* Standard language for modeling software systems 
* Pictorial view
* Different Perspectives

3 Categories:

* Structural 
* Behavior
  * Interaction

What is Kruuchten's 4 + 1 model?

* A view model used to describe the architecture of software based systems.
* Multiple, concurent views 
* The view included in the model are:
  * Development view
  * Logical view 
  * Physical view
  * Process view
  * Scenarios

#### **Software Architecture Patterns**

* Defining characteristics of each pattern 
  * Benefits
  * Where it should be used. 
* Different patterns can be used in the same system. 
* Assignment: applying architecture patterns to different enterprise systems.

#### **Multi-Tired Architecture**

**Advantages**

* Separation of concerns 
* Easy to define roles and component scope
* Easier development and testing 
* Good general purpose pattern 

**Drawbacks **

* Sinkhole architecture anti-pattern 
* Ofter leads to monolithic applications 

#### **Client-Server Architecture Model**

* Servers provide a service which clients request
* Centralized
* Lite vs Fat Clients

**Advantages**

* Security. 
* Backup and recovery procedure is simplified. 
* Easier management and administration.
* Easier upgrading and scalability.

**Drawbacks **

* Single point of failure 
* More prone to network congestion issues
* Cost

#### **Service Oriented Architecture**

* Loosely coupled services. 
* A service can be defined as:
  * It logically represents a business activity with a specified outcome. 
  * self-contained. 
  * a black box for its consumers.
  * may consist of other underlying services. 

**Advantages **

* Low coupling 
* Code/Service reusability
* Easier to maintain and test
* Easier to scale 
* Promotes parallel development. 

**Drawbacks**

* Service management can become complex
* Increased complexity and cost especially at the setup phase
* Increased overheads. 
* Not suitable for GUI based application or applications which are standalone and short lived. 

#### **Microservice Architecture**

* Services are:
  * fine grained 
  * lightweight

**Advantages**

* Low coupling.
* Improves modularity.
* Promotes parallel development.
* Promotes scalability.

**Drawbacks**

* Infrastructure cost are usually higher. 
* Integration testing complexity
* Service management and deployment
* Nanoservice anti pattern 



