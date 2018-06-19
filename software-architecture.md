### Software Architecture for the Enterprise Architect

#### Enterprise Architect - The role

**Key Responsibilities and Challenges**

* Ensure that a company's IT strategy and business goals are aligned. 
* Actively involved with the design, maintenance and continual improvement of the company's architecture and continual improvement of the company's architecture at an enterprise level.
* Development of IT standards and policies within the company. 
* Risk management & impact assessment of the architecture. 
* Identifying Disruptive Technology. 

#### Understanding Business Requirements

* Requirements state what the stakeholders want the system to achieve. 
* We can classify requirements into three different types:
  1 - Vision: requirements for the future direction for a system.
  2 - Functional Requirements: what a system needs to be able to 'do'.
  3 - Performance Requirements: the performance levels that the stakeholders want the system to achieve.



**What is UML?**

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

#### Domain Driven Design

**Characteristics **

* Software experts work with domain experts, to build a ubiquitous language which describes the system. 
* The **ubiquitous language** will help from the structure of the object oriented design of the software and guides you in a dividing the objects into:
  * Value objects 
  * Entities 
  * Aggregate roots

**Drawbacks**

* Requires very good knowledge of the domain driven process to implement correctly. 
* Initial investment is costly. 
* Not suitable for systems that do not have a complex domain model, or which are not going to be used for a long time.

#### Event Driven Architecture

**Advantages **

* Decoupling between consumers and procedures, and between the consumers themselves. 
* Allow for scalability and distribution.



