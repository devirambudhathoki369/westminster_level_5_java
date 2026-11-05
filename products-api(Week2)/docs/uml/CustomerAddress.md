# Customer and Address — UML Class Diagram

```mermaid
classDiagram
    direction LR

    class Customer {
        -id : Long
        -name : String
        -email : String
        -address : Address
        +Customer()
        +Customer(id : Long, name : String, email : String, address : Address)
        +getId() : Long
        +setId(id : Long) : void
        +getName() : String
        +setName(name : String) : void
        +getEmail() : String
        +setEmail(email : String) : void
        +getAddress() : Address
        +setAddress(address : Address) : void
    }

    class Address {
        -street : String
        -city : String
        -postcode : String
        +Address()
        +Address(street : String, city : String, postcode : String)
        +getStreet() : String
        +setStreet(street : String) : void
        +getCity() : String
        +setCity(city : String) : void
        +getPostcode() : String
        +setPostcode(postcode : String) : void
    }

    class CustomerController {
        +getById(id : Long) : Customer
    }

    Customer --> Address : has
    CustomerController --> Customer
```
