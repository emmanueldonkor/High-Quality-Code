# Code Formatting and Documenting Best Practices

Proper formatting and documentation are essential for writing maintainable, readable, and efficient code. 

## Code Formatting

### Why Formatting is Important:
- Consistent formatting ensures that your code is easy to read and understand.
- Properly formatted code helps developers quickly spot mistakes or follow logic.
- Different languages and teams may have slightly different conventions, but the key is **consistency**.

### General Formatting Rules:
1. **Indentation**: Use consistent indentation (spaces or tabs) across your project. Common practices include:
   - **4 spaces** per indentation level in languages like Python, C#, and TypeScript.
   - Avoid mixing spaces and tabs in the same project.
   
2. **Line Length**: Keep lines of code to a maximum of **80–100 characters** to avoid horizontal scrolling and improve readability.

3. **Curly Braces**: Always use curly braces for control structures (if, else, for, while) even if there is only one statement. This avoids bugs caused by adding a second line without braces.
   - **TypeScript, Java**: Opening brace on the same line and **C#** differ a bit by always the next line.
   - **Python**: Uses indentation instead of braces.

4. **White Space**: Use blank lines to separate blocks of code logically (e.g., between method definitions) and within methods to separate logical sections of code.

### Example of a Bad Formatted Code

 ```csharp
    using System;
public class Student{
public string name;
public int age;
public string grade;
public Student(string n,int a,string g){name=n;age=a;grade=g;}
public void Study(){Console.WriteLine("Studying...");}
public void DisplayInfo(){Console.WriteLine("Name: "+name+", Age: "+age+", Grade: "+grade);}
public void UpdateGrade(string newGrade){grade=newGrade;Console.WriteLine("Grade updated to: "+grade);}
public void CelebrateBirthday(){age++;Console.WriteLine("Happy Birthday! You are now "+age+" years old!");}
public string GetStudentDetails(){return "Student Name: "+name+", Age: "+age+", Grade: "+grade;}
public void Reset(){name="";age=0;grade="";Console.WriteLine("Student details reset.");}}
```

### Example of a Good Formatted Code

```csharp
using System;

public class Student
{
    public string Name { get; set; }
    public int Age { get; set; }
    public string Grade { get; set; }

    public Student(string name, int age, string grade)
    {
        Name = name;
        Age = age;
        Grade = grade;
    }

    public void Study()
    {
        Console.WriteLine("Studying...");
    }

    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}, Grade: {Grade}");
    }

    public void UpdateGrade(string newGrade)
    {
        Grade = newGrade;
        Console.WriteLine($"Grade updated to: {Grade}");
    }

    public void CelebrateBirthday()
    {
        Age++;
        Console.WriteLine($"Happy Birthday! You are now {Age} years old!");
    }

    public string GetStudentDetails()
    {
        return $"Student Name: {Name}, Age: {Age}, Grade: {Grade}";
    }

    public void Reset()
    {
        Name = string.Empty;
        Age = 0;
        Grade = string.Empty;
        Console.WriteLine("Student details reset.");
    }
}
```

## Code Documentation

## Why Over-Commenting Each Line of Code is Bad

Over-commenting refers to writing comments for every line or block of code, if you are to do that then you should be worried about the quality of the code you are writing. Comment is only us to complement a good code not to explain each line of code. This approach clutters the code and makes it harder to maintain. Instead, write self documenting code,and use documenting tools like XML (C#), PyDoc (Python), or JSDoc (JavaScript/TypeScript) to complement it, provides a much cleaner and maintainable solution.

### Bad Example of Code Commenting 

```csharp
// This is a method to add two numbers
public int AddNumbers(int number1, int number2)
{
    // Adding number1 and number2
    int result = number1 + number2;
    // Return the result of addition
    return result;
}
```

```python
# This is a function to add two numbers
def add_numbers(number1, number2):
    # Add number1 and number2
    result = number1 + number2
    # Return the result
    return result
```

```typescript
// This function adds two numbers
function addNumbers(number1: number, number2: number): number {
    // Add number1 and number2
    const result = number1 + number2;
    // Return the result
    return result;
}
```

### Good Example of Code Commenting 

```csharp
/// <summary>
/// Adds two integers and returns the result.
/// </summary>
/// <param name="number1">The first number to add.</param>
/// <param name="number2">The second number to add.</param>
/// <returns>The sum of the two numbers.</returns>
public int AddNumbers(int number1, int number2)
{
    int result = number1 + number2;
    return result;
}
```

```python
def add_numbers(number1, number2):
    """
    Adds two numbers and returns the result.

    Args:
        number1 (int): The first number to add.
        number2 (int): The second number to add.

    Returns:
        int: The sum of the two numbers.
    """
    result = number1 + number2
    return result
```

```typescript
/**
 * Adds two numbers and returns the result.
 *
 * @param {number} number1 - The first number to add.
 * @param {number} number2 - The second number to add.
 * @returns {number} The sum of the two numbers.
 */
function addNumbers(number1: number, number2: number): number {
    const result = number1 + number2;
    return result;
}
```