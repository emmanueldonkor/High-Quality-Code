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