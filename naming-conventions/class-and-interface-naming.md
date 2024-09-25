## Naming Conventions: Classes and Interfaces

### Class Naming

A **class** serves as a blueprint for creating objects, so it's crucial to choose names that clearly communicate the purpose and role of the class within the application.

#### Key Guidelines for Class Names:

- **Use nouns**: Class names should be nouns (or noun phrases) as they typically represent things or entities (e.g., `User`, `Invoice`, `CustomerOrder`). **Do not use verbs** for class names, as classes are not actions but templates for objects.

- **Use capital letters**: Class names should always begin with a capital letter. This is a common convention across most programming languages (e.g., `Invoice`, `UserManager`).

- **Add adjectives when necessary**: Adjectives can be used to specify the type of the class. For example, `PremiumAccount` or `AdminUser` clarifies the specific role of the class.

- **Avoid vague or generic names**: Classes should be descriptive, not generic. Names like `Manager`, `Data`, or `Helper` lack context and can lead to confusion. Instead, aim for specific names like `AccountManager` or `OrderProcessor`.

#### Bad Class Naming Examples:

```plaintext
DoWork          // Incorrect; classes should not use verbs.
ThingProcessor  // Vague and lacks context. What is it processing?
Data            // Generic; doesn't explain what kind of data is handled.
```
#### Good Class Naming Examples:

```plaintext
Invoice         // Describes an object that represents an invoice.
CustomerOrder   // Clearly defines an order placed by a customer.
PremiumAccount  // Indicates a special type of account, specifying its purpose.
```

# Interface Naming

Interfaces define contracts for classes to implement, representing an abstraction that defines behavior. Therefore, the naming of interfaces should clearly communicate the role of that abstraction.

## Key Guidelines for Interface Names

- **Start with "I"**: In many programming languages like C#(Charp), it's common to prefix interface names with an "I" (e.g., `IUserRepository`, `IOrderProcessor`) to distinguish them from classes, although some modern conventions and in some languages like (Java, C++, Typescript) avoid this prefix in favor of context.
**NB:If you are not a Csharp Developer you can always ignore the `I` infront of interfaces.**

- **Use verbs or adjectives**: Since interfaces often define behavior, it’s acceptable to use verbs or adjectives in their names. For instance, interfaces like `ILogger`, `ISerializable`, or `IDisposable` clarify that the implementing class will have logging, serialization, or disposal behaviors, respectively.

- **Avoid "Impl" suffix**: Don’t name an interface by appending `Impl` (for "implementation") to it, as this limits flexibility. For example, `IProcessorImpl` suggests only one implementation, which can hinder future scalability.

## Bad Interface Naming Examples

```plaintext
ProcessImpl    // Not clear what kind of processing or behavior is intended.
Handler        // Too vague and doesn’t indicate what is being handled.
```

## Good Interface Naming Examples

```plaintext
ILogger                // Specifies that the interface defines logging behavior.
ICustomerRepository    // Clearly defines an interface for handling customer data storage and retrieval.
IOrderProcessor        // Defines a contract for processing orders.
```