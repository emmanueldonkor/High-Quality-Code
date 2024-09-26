# Method and Property Naming

## Method Names

Method names are crucial for clarity and understanding. They should convey what the method does and follow a clear pattern:

- **Format**: `<verb> + <object>`  
- **Style**: Each separate word starts with an uppercase letter depending of the language you are using.

### Good Examples
- **C#**: 
    ```csharp
    public void PrintReport() 
    {
        // Implementation to print a report
        Console.WriteLine("Report printed.");
    }

    public void LoadSettings() 
    {
        // Implementation to load user settings
        Console.WriteLine("Settings loaded.");
    }
    ```
- **Python**:
    ```python
    def print_report():
        # Implementation to print a report
        print("Report printed.")

    def load_settings():
        # Implementation to load user settings
        print("Settings loaded.")
    ```
- **TypeScript**:
    ```typescript
    function printReport(): void {
        // Implementation to print a report
        console.log("Report printed.");
    }

    function loadSettings(): void {
        // Implementation to load user settings
        console.log("Settings loaded.");
    }
    ```

### Bad Examples
- **C#**:
    ```csharp
    public void DoWork() 
    {
        // Vague method, does not describe work done
    }

    public void Printer() 
    {
        // No verb, unclear what this does
    }
    ```
- **Python**:
    ```python
    def do_work():
        pass  # Vague method, does not describe work done

    def printer(): 
        pass  # No verb, unclear what this does
    ```
- **TypeScript**:
    ```typescript
    function doWork(): void { 
        // Vague method, does not describe work done
    }  

    function printer(): void { 
        // No verb, unclear what this does
    }
    ```

## Returning Values
For methods that return values, the name should reflect the returned value clearly.

### Good Examples
- **C#**:
    ```csharp
    public int GetNumberOfProcessors() 
    {
        // Implementation to return the number of processors
        return Environment.ProcessorCount;
    }
    ```
- **Python**:
    ```python
    def get_number_of_processors():
        # Implementation to return the number of processors
        return os.cpu_count()
    ```
- **TypeScript**:
    ```typescript
    function getNumberOfProcessors(): number {
        // Implementation to return the number of processors
        return navigator.hardwareConcurrency || 1; // Fallback to 1
    }
    ```

### Bad Examples
- **C#**:
    ```csharp
    public void ShowReport() 
    {
        // Not clear what it returns
    }
    ```
- **Python**:
    ```python
    def show_report():
        pass  # Not clear what it returns
    ```
- **TypeScript**:
    ```typescript
    function showReport(): void { 
        // Not clear what it returns
    }
    ```

## Cohesion
Methods should focus on a single task. If a method does more than one thing, it should be split into multiple methods.

### Example of Poor Cohesion
- **C#**:
    ```csharp
    public void CreateAnnualReportAndSendEmail() 
    {
        // Too many tasks: creating a report and sending an email
    }
    ```
- **Python**:
    ```python
    def create_annual_report_and_send_email():
        # Too many tasks: creating a report and sending an email
        pass
    ```
- **TypeScript**:
    ```typescript
    function createAnnualReportAndSendEmail(): void { 
        // Too many tasks: creating a report and sending an email
    }
    ```

## Property Names

Property names should consist of a noun, or sometimes an adjective followed by a noun when necessary. They should be descriptive of the data they hold.

### Good Examples
- **C#**:
    ```csharp
    public string Name { get; set;}
    ```
- **Python**:
    ```python
    class User:
        def __init__(self, user_name):
            self._user_name = user_name
            
        @property
        def user_name(self):
            return self._user_name
    ```
- **TypeScript**:
    ```typescript
    class User {
        private name: string;

        constructor(name: string) {
            this.name = name;
        }

        get userName(): string {
            return this.name;
        }
    }
    ```


