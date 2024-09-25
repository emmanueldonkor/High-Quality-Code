## Naming Conventions: Identifier Naming

When naming an identifier, it's essential to ensure that the name clearly reflects its purpose. This improves readability and maintainability. To do this, ask yourself:
- **What does this class do?**
- **What is the purpose of this variable?**
- **What is this method doing?**
- **What information does this parameter hold?**

By doing so, you'll avoid cryptic or vague names that confuse others and instead create identifiers that convey their function at a glance.

### Bad Examples of Naming Identifiers

```plaintext
move2bed()      // What does this method do? Is it moving something to a bed?
nameitem        // What kind of item? What's the purpose of this variable?
proc1()         // Vague; what is being processed?
k3              // why not k4 instead?🤔
btn1            // Button for what? What is it doing?
``` 

### Good Examples of Naming Identifiers

```plaintext
printReport()       // Clearly describes that a report will be printed
processOrder()      // Indicates the method processes an order
customerName        // Explicitly identifies the variable holds a customer’s name
submitButton        // Clearly indicates this button is for submitting
```

### Avoid Unclear Abbreviations in Naming an Identifier

While abbreviations are tempting, avoid using them unless they are universally recognized. Using abbreviations like `htmlParser`,`uriDecoder` is acceptable because it's widely understood, but cryptic abbreviations like `grpbxtn`, `btn` (for group box button) should be avoided.

#### Bad Example

```plaintext
grpbxtn    // Cryptic; hard to understand without context.
```

#### Good Example
``plaintext
groupBoxButton // more easier to understand
``

### Name Identifiers within Business Domain

Naming should always reflect the domain or functionality within the business context. Using general terms like `data`, `item`, or `obj` doesn't provide enough insight into what a variable represents or how it’s used within the specific domain.
For example, in an application related to e-commerce, using `order`, `customerAccount`, or `inventory` is more appropriate.