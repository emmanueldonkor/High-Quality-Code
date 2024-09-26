# Naming Conventions for Variables, Booleans, Constants, and Enums

 This guide outlines how to name variables, constants, boolean identifiers, and enumerations in your code. 

## Variable Names

### General Guidelines:
- Variable names should be descriptive and immediately understandable.
- Use **camelCase** for variable names except in some languages like python that mostly uses snake case(all words except the first should start with an uppercase letter).
- Names should reflect **what** the variable represents, not **how** it will be used.
- Avoid abbreviations and meaningless names (e.g., `r18pq`, `val1`, `rcfd`).
- Use terms from the **business domain** rather than technical terms (e.g., `customerList` instead of `stringArray`).

### Examples:

#### Good Naming:
- **C#**:
    ```csharp
    int customerAge = 30;
    double totalPrice = 199.99;
    string customerName = "John Doe";
    ```
- **Python**:
    ```python
    customer_age = 30
    total_price = 199.99
    customer_name = "John Doe"
    ```
- **TypeScript**:
    ```typescript
    let customerAge: number = 30;
    let totalPrice: number = 199.99;
    let customerName: string = "John Doe";
    ```

#### Bad Naming:
- **C#**:
    ```csharp
    int a = 30;  // Not descriptive
    double tp = 199.99;  // Too abbreviated
    string name = "John Doe";  // Vague
    ```
- **Python**:
    ```python
    a = 30  # Not descriptive
    tp = 199.99  # Too abbreviated
    name = "John Doe"  # Vague
    ```
- **TypeScript**:
    ```typescript
    let a: number = 30;  // Not descriptive
    let tp: number = 199.99;  // Too abbreviated
    let name: string = "John Doe";  // Vague
    ```

### Optimal Name Length:
Variables with a wider scope should have more descriptive names, while those with narrower scopes (like loop counters) can be shorter.

#### Examples:
- **C#**:
    ```csharp
    for (int i = 0; i < customerList.Length; i++) { ... }
    ```
- **Python**:
    ```python
    for i in range(len(customer_list)):
        ...
    ```
- **TypeScript**:
    ```typescript
    for (let i = 0; i < customerList.length; i++) {
        ...
    }
    ```

## Boolean Identifiers

Boolean variables, properties, and parameters should indicate a **truth** or **falsehood**. The name should clearly reflect the condition it checks.

### Guidelines:
- Use **is**, **has**, or **can** as prefixes when necessary for clarity (e.g., `isAvailable`, `hasAccess`, `canRead`).
- Avoid negated names (e.g., avoid using `notValid`, use `isValid` instead).

#### Good Examples:
- **C#**:
    ```csharp
    bool isAvailable = true;
    bool hasPendingPayment = false;
    ```
- **Python**:
    ```python
    is_available = True
    has_pending_payment = False
    ```
- **TypeScript**:
    ```typescript
    let isAvailable: boolean = true;
    let hasPendingPayment: boolean = false;
    ```

#### Bad Examples:
- **C#**:
    ```csharp
    bool notFound = false;  // Negated name
    bool valid = true;  // Not very descriptive
    ```
- **Python**:
    ```python
    not_found = False  # Negated name
    valid = True  # Not very descriptive
    ```
- **TypeScript**:
    ```typescript
    let notFound: boolean = false;  // Negated name
    let valid: boolean = true;  // Not very descriptive
    ```

## Constants

Constants are used to store values that should not change during the program's execution. The names of constants should be descriptive and represent **what** the value signifies, not just the value itself.

### Guidelines:
- Constants can either be written in **PascalCase** or **ALL_CAPS** with underscores (`_`) separating the words.
- Avoid meaningless or confusing constant names.

### Examples:

#### Good Naming:
- **C#**:
    ```csharp
    public const double PI = 3.14159265359;
    public const int MAX_USERS = 100;
    ```
- **Python**:
    ```python
    PI = 3.14159265359
    MAX_USERS = 100
    ```
- **TypeScript**:
    ```typescript
    const PI: number = 3.14159265359;
    const MAX_USERS: number = 100;
    ```

#### Bad Naming:
- **C#**:
    ```csharp
    public const double number314159 = 3.14159265359;  // Not descriptive
    ```
- **Python**:
    ```python
    number_314159 = 3.14159265359  # Not descriptive
    ```
- **TypeScript**:
    ```typescript
    const number314159: number = 3.14159265359;  // Not descriptive
    ```

## Enumeration (Enums)

Enums represent a set of named values. These values should reflect clear states or categories relevant to the business domain. Consistency in naming is key across all enum members.

### Guidelines:
- Enum names can be **singular** or **plural** depending on the context.
- Enum values should clearly describe the different states or options they represent.

### Examples:

#### Good Naming:
- **C#**:
    ```csharp
    public enum Days
    {
        Sunday,
        Monday,
        Tuesday,
        Wednesday,
        Thursday,
        Friday,
        Saturday
    }

    public enum Color
    {
        Red,
        Green,
        Blue,
        Yellow
    }
    ```
- **Python**:
    ```python
    from enum import Enum

    class Days(Enum):
        Sunday = 1
        Monday = 2
        Tuesday = 3
        Wednesday = 4
        Thursday = 5
        Friday = 6
        Saturday = 7

    class Color(Enum):
        Red = 1
        Green = 2
        Blue = 3
        Yellow = 4
    ```
- **TypeScript**:
    ```typescript
    enum Days {
        Sunday,
        Monday,
        Tuesday,
        Wednesday,
        Thursday,
        Friday,
        Saturday
    }

    enum Color {
        Red,
        Green,
        Blue,
        Yellow
    }
    ```

#### Bad Naming:
- **C#**:
    ```csharp
    public enum DayEnum
    {
        DAY1,
        DAY2,
        DAY3
    }
    ```
- **Python**:
    ```python
    class DayEnum(Enum):
        Day1 = 1
        Day2 = 2
        Day3 = 3
    ```
- **TypeScript**:
    ```typescript
    enum DayEnum {
        Day1,
        Day2,
        Day3
    }
    ```


