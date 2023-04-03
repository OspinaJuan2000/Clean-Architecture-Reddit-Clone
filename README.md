# Reddit Clone using Clean Architecture in both sides, backend & frontend

## The clean architecture

![clean architecture](https://blog.cleancoder.com/uncle-bob/images/2012-08-13-the-clean-architecture/CleanArchitecture.jpg)

### The Dependency Rule that Makes Clean Architecture Work.

The **Dependency Rule** means that the core business logic of the system should not depend on the implementation details of lower-level modules, such as databases, frameworks, or external services. Instead, it should depend on interfaces or contracts that define the behavior and expectations of these dependencies.

<hr>

### Entities

An entity represents a **core concept or object in the domain** of the software system. Entities encapsulate the business logic and rules that govern the behavior and state of these objects.

**Entities should be designed with a clear understanding of the business requirements and domain knowledge, and they should be modeled in a way that reflects the real-world concepts they represent.**

#### Example

The User object represents a specify user inside the application.

### Use Cases

Use cases represent the **application business** rules and represent the ways in which the system's entities can be used to fulfill specific goals or requirements of the users or stakeholders.

#### Example

Create a user in the application or fetch a specify user by its username.

**Use cases define the interactions between the actors (users or external systems) and the system, and describe the steps and actions required to achieve a specific outcome or goal.**

### Interface Adapters

The Interface Adapter layer **provides the mechanism for communicating between the outer layers** (frameworks and drivers) and the inner layers (entities, use cases, and infrastructure).

**The Interface Adapter layer acts as a bridge between the domain-specific logic and the external systems and devices.**

#### Example

An interface that has all the operations that the database will do when the use case needs persistence.

### Frameworks & Drivers

The "Framework & Drivers" layer is responsible for providing **concrete implementations** of the "Interface Adapters" and for interacting with external systems using specific frameworks or libraries.

**This component includes code that is specific to the chosen technology stack, such as web frameworks, database drivers, or messaging clients.**

#### Example

The implementation of the interface adapter to perform database operations. The implementation may be JPA, JDBC, etc.
