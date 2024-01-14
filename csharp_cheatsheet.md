# Table of Contents
- [Data Types](#data_types)
- [Value Types](#value_types)
- [Reference Types](#reference_types)
- [Math Operations](#math_operations)
- [Operators](#operators)
- [Conditionals](#conditionals)
- [loops](#loops)
- [Ternary Operator](#ternary_operator)
- [Switch Statement](#switch_statement)
- [Working with Lists](#working_with_lists)
- [Jagged Arrays](#jagged_arrays)
- [2D Arrays](#2d_arrays)
- [List and Array Conversion](#list_and_array_conversion)
- [List Reversing](#list_reversing)
- [Adding Values into a New User Type](#adding_values_into_a_new_user_type)
- [Methods and Saving to a List via a Method](#methods_and_saving_to_a_list_via_a_method)
- [Overloading a Method](#overloading_a_method)
- [Method Sections in Program.cs](#method_sections_in_program.cs)
- [Method Section in User.cs](#method_section_in_user.cs)

_____
## Data_Types

- **Variable:** Stores some value (e.g., `var X`)
- **Literal:** Actual value (e.g., string `"This is the Literal Part"`)
- **Identifier:** What we call the variable
- **Expression:** Evaluates to a value (e.g., Math Equation)
- **Operator:** Works on operands (e.g., `+`, `-`, `*`, etc.)
- **Operand:** The things that the operator works on (e.g., parts of the equation)
- **Initialization:** Variables cannot be used without being declared first in C# (use `new` or give it a value to initiate)
- **Nullable Types:** Allows a variable to be passed through to the console without having a value (e.g., `int? x = null;`)

_____
### Value_Types

- Integers: Solid numbers that can be negative or positive (e.g., `int a = -5;`)
- Unsigned Integers: Solid numbers that cannot be negative (e.g., `uint b = 5;`)
- Characters: Single values such as letters or symbols (e.g., `char c = 'C';`)
- Floats: Store decimals up to 23 bits, i.e., less accurate (e.g., `float d = 5.5F;`)
- Doubles: Store decimals up to 52 bits and are more accurate (e.g., `double e = 5.5;`)
- Decimals: Can hold 38 digits at the cost of more memory (e.g., `decimal f = 5.5M;`)
- Booleans: Simple True (1) or False (0) variables (e.g., `bool g = true;`)

_____
### Reference_Types

- Strings: Datatypes that contain data (e.g., `string h = "Hello";`)
- Arrays: Store multiple values (e.g., `int[] a = { 3 };`)

_____
## Math_Operations

- **Round:** Allows us to round the value (e.g., `Math.Round(x, 0, MidpointRounding.AwayFromZero)`)
- **Floor/Ceiling:** Forces the round downwards or upwards (e.g., `Math.Ceiling(x);`)
- **Min/Max:** Returns the smaller/larger of two numbers (e.g., `Math.Max(y, x);`)
- **Abs:** Outputs the positive version of a number (e.g., `Math.Abs(x);`)
- **Sign:** Outputs a number indicating if a value is positive/negative or 0 (e.g., `Math.Sign(y);`)

_____
## Operators

- `<`: Less than
- `>`: Greater than
- `=`: Sets left operand equal to the right.
- `<=`: Less than or Equal to
- `>=`: Greater than or Equal to
- `==`: Equal to
- `&&`: AND parameter (e.g., `if (x == 1 && y == 1) { Console.WriteLine("x and y equal 1"); }`)
- `||`: OR parameter evaluates true if either operand is true (e.g., `if (x == 2 || y == 2) { Console.WriteLine("x or y == 2"); }`)
- `!=`: NOT Equal checks if operand is not equal to the input (e.g., `if (x != 2) { Console.WriteLine("x is not 2"); }`)

_____
## Conditionals

## if statement

- Test a condition
- Execute code block if condition is true

```csharp
if (condition) // If condition is true
{
    // Code to execute
}
```

### if...else statement

- Test a condition
- Execute first block if true, else execute second block

```csharp
if (condition) // If condition is true
{
    // Code to execute if condition is true
}
else // If condition is false
{
    // Code to execute if condition is false
}
```

### if...else if...else statement

- Test multiple conditions
- Execute only the first true condition's block

```csharp
if (condition1) // If first condition is true
{
    // Code to execute if condition1 is true
}
else if (condition2) // If second condition is true
{
    // Code to execute if condition2 is true
}
else // If no conditions are true
{
    // Code to execute if both conditions are false
}
```

## while loop

- Continue looping as long as a condition is true

```csharp
while (condition) // While condition is true
{
    // Code to execute during each iteration
}
```

### do...while loop

- Execute code once, then repeat loop as long as a condition is true

```csharp
do // Do at least once
{
    // Code to execute during each iteration
}
while (condition); // Continue if condition is true
```

### for loop

- Loop for a specified number of times

```csharp
for (int i = 0; i < 5; i++) // Initialize i; continue if i < 5; increment i each loop
{
    // Code to execute during each iteration
}
```

### foreach loop

- Loop through each item in a collection

```csharp
foreach (type item in collection) // For each item of type in collection
{
    // Code to execute during each iteration
}
```

### break statement

- Exit the loop immediately

```csharp
for (int i = 0; i < 10; i++) // Loop from i = 0 to i < 10
{
    if (i == 4) // If i equals 4
    {
        break; // Exit the loop
    }
}
```

### continue statement

- Skip the current iteration and continue with the next one

```csharp
for (int i = 0; i < 10; i++) // Loop from i = 0 to i < 10
{
    if (i == 4) // If i equals 4
    {
        continue; // Skip to the next iteration
    }
    // Code here will not execute when i equals 4
}
```

_____
## Ternary_Operator

- Like an if-else statement but with the syntax shown.

```csharp
// Define a boolean variable 'correct' and set its value to true
bool correct = true;

// Use the ternary conditional operator to determine the value of 'pointsEarned'.
// If 'correct' is true, 'pointsEarned' is set to 10. If 'correct' is false, it's set to 0.
int pointsEarned = correct ? 10 : 0;

// Output the value of 'pointsEarned' to the console.
// This will print '10' because 'correct' is true.
Console.WriteLine(pointsEarned);
```

_____
## Switch_Statement

- Like an if statement but with multiple conditions being checked.

```csharp
// Define an integer for age
int age = 18;

// Use a switch statement to execute code based on the value of 'age'
switch(age)
{
    case 17:
        // Case for when the age is exactly 17
        Console.WriteLine("One more year to adulthood.");
        // The 'break' statement exits the switch-case structure
        break;

    case 18:
        // Case for when the age is exactly 18
        Console.WriteLine("Congratulations on becoming an adult!");
        // Exit the switch-case structure
        break;

    default:
        // Default case for any age not specifically handled above
        Console.WriteLine("Enjoy the wisdom of your years!");
        // Exit the switch-case structure
        break;
}
```

_____
## Working_with_Lists

- Add, insert, remove, and clear list items.
- Compare lists for equality- (e.g., `if (grades.SequenceEqual(otherGrades)) { Console.WriteLine("Equal!"); }`)
- **Nested Lists:** Creating a nested list and iterating through it.

```csharp
// Define a nested list 'studentGrades' where each element is a List<int>.
List<List<int>> studentGrades = new List<List<int>>()
{
    // Each nested List<int> represents a student's grades.
    new List<int> { 1, 2, 3, 4, 5 },   // Grades for the first student
    new List<int> { 6, 7, 8, 9, 10 },  // Grades for the second student
    new List<int> { 11, 12, 13, 14, 15 } // Grades for the third student
};

// Iterate over each student's grades in the nested list.
foreach (List<int> grades in studentGrades)
{
    // Iterate over each grade in the current student's List<int> of grades.
    foreach (int grade in grades)
    {
        // Print the current grade followed by a tab space.
        Console.Write(grade + "\t");
    }
    // After printing all grades for the current student, output a newline.
    Console.WriteLine();
}
```

_____
## Jagged_Arrays

- Working with jagged arrays and iterating through them.

```csharp
// Define a jagged array 'studentGrades' with 3 inner arrays.
int[][] studentGrades =
{
    new int[] { 1, 2, 3, 4, 5 },     // First inner array
    new int[] { 6, 7, 8, 9, 10 },    // Second inner array
    new int[] { 11, 12, 13, 14, 15 } // Third inner array
};

// Iterate over each inner array in the jagged array 'studentGrades'.
foreach (int[] grades in studentGrades)
{
    // Iterate over each integer element in the current inner array 'grades'.
    foreach (int grade in grades)
    {
        // Print the current element followed by a tab space.
        Console.Write(grade + "\t");
    }
    // After printing all elements of the current inner array, print a new line.
    Console.WriteLine();
}
}
```

_____
## 2D_Arrays

- Working with 2D arrays and iterating through them.

```csharp
// Define a two-dimensional array 'grades' with 3 rows and 4 columns.
int[,] grades =
{
    { 7, 11, 13, 26},  // First row
    { 7, 11, 13, 26},  // Second row
    { 7, 11, 13, 26}   // Third row
};

// Outer loop iterates over each row (first dimension of the array).
for (int i = 0; i < grades.GetLength(0); i++)
{
    // Inner loop iterates over each column (second dimension of the array) for the current row.
    for (int k = 0; k < grades.GetLength(1); k++)
    {
        // Print the current element followed by a space.
        Console.Write(grades[i, k] + " ");
    }
    // After printing all columns for the current row, print a new line.
    Console.WriteLine();
}
```

_____
## List_and_Array_Conversion

- Converting a list to an array and vice versa.

```csharp
// Create a new list of integers with a single value
List<int> stuff = new List<int>() { 5 };

// Convert the list to an array
int[] myArr = stuff.ToArray();

// Convert the array back to a list
List<int> myList = myArr.ToList();
```

_____
## List_Reversing

- Working with lists to reverse the order or sort the elements.

```csharp
// Create a new list of integers with predefined values
List<int> stuff = new List<int>() { 5, 10, 20, 40, 80, 160 };

// Demonstrate reversing the list
Console.WriteLine("Original list:");
foreach (int s in stuff)
{
    Console.WriteLine(s); // This will print the numbers in the order they were added
}

// Reverse the order of the list and print the results
stuff.Reverse();
Console.WriteLine("\nList after reversing:");
foreach (int s in stuff)
{
    Console.WriteLine(s); // This will print the numbers in reverse order
}

// Reset the list to the original order
stuff.Reverse(); // This step is to undo the previous reverse so we can demonstrate sorting

// Demonstrate sorting the list in ascending order
stuff.Sort();
Console.WriteLine("\nList after sorting:");
foreach (int s in stuff)
{
    Console.WriteLine(s); // This will print the numbers in ascending order
}
````

_____
## Adding_Values_into_a_New_User_Type

- Creating instances of a User type and assigning values to properties.

```csharp
public class User
{
    // Auto-implemented properties for FirstName and LastName
    public string FirstName { get; set; }
    public string LastName { get; set; }

    // You can also include a FullName property if needed
    public string FullName => $"{FirstName} {LastName}";
}
// Create a new instance of User for 'me'
User me = new User();
// Set the FirstName property for 'me'
me.FirstName = "Cassius";
// Set the LastName property for 'me'
me.LastName = "Fragomeni";

// Create a new instance of User for 'you'
User you = new User();
// Set the FirstName property for 'you'
you.FirstName = "Emma";
// Set the LastName property for 'you'
you.LastName = "Watson";

// Initialize a new list to hold User objects
List<User> users = new List<User>();
// Add the previously created User 'me' to the list
users.Add(me);
// Add the previously created User 'you' to the list
users.Add(you);

// At this point, 'users' list contains two User objects, 'me' and 'you'
```

_____
## Methods_and_Saving_to_a_List_via_a_Method

- Demonstrates how to populate a list of Users using a method.

```csharp
public class Program
{
    // Method to create a list of User objects and perform actions on them
    public void doSomething()
    {
        // Initialize lists of first and last names
        List<string> firstNames = new List<string>() { "Cassius", "Emma", "Megan" };
        List<string> lastNames = new List<string>() { "Fragomeni", "Watson", "Fox" };

        // Create an empty list to hold User objects
        List<User> users = new List<User>();

        // Loop through the lists of names to create User objects
        for (int i = 0; i < firstNames.Count; i++)
        {
            // Create a new User object and set its properties
            User user = new User();
            user.FirstName = firstNames[i];
            user.LastName = lastNames[i];
            // Add the new User object to the list of users
            users.Add(user);
        }

        // Iterate over the list of User objects and print their full names
        foreach (User usr in users)
        {
            Console.WriteLine(usr.FullName);
        }

        // Modify the first name of the first User in the list
        takeUser(users[0]);

        // Print the updated full name of the first User
        Console.WriteLine(users[0].FullName);
    }

    // Method to modify the FirstName property of a User object
    public void takeUser(User user)
    {
        // Change the first name of the User to "Cae"
        user.FirstName = "Cae";
        // Print the full name after modification
        Console.WriteLine(user.FullName);
    }
}

public class User
{
    // Properties for the User's first and last names
    public string FirstName { get; set; }
    public string LastName { get; set; }

    // Property to get the full name by concatenating the first and last names
    public string FullName
    {
        get { return FirstName + " " + LastName; }
    }
}
```

_____
## Overloading_a_Method

- Create method overloads for different functionality with the same name.

```csharp
public class User
{
    // Method to output the user's full name in a simple sentence.
    // This is the non-overloaded version of the method.
    public string Output()
    {
        // Returns a string that includes the full name of the user.
        return "My name is " + FullName;
    }

    // Overloaded method to output the user's full name multiple times.
    // The 'times' parameter specifies how many times the full name should be repeated.
    // It has a default value of 5, so if no argument is provided, it will repeat 5 times.
    public string Output(int times)
    {
        // Initialize an empty string to build the repeated full name message.
        string message = "";

        // Loop 'times' number of times to concatenate the full name to the message.
        for (int i = 0; i < times; i++)
        {
            // Each time, add the first name, a space, the last name, followed by a line break.
            message += FirstName + " " + LastName + "\n";
        }

        // After the loop, return the constructed message.
        return message;
    }
}

```

- Use the created overloaded methods

```csharp
User user = new User
{
    FirstName = "Jane",
    LastName = "Doe"
};

Console.WriteLine(user.Output()); // Calls the first method and prints "My name is Jane Doe"
Console.WriteLine(user.Output(3)); // Calls the overloaded method and prints "Jane Doe" three times, each on a new line
```

_____
## Method_Sections_in_Program.cs

- Call methods from the main entry point of the program.

```csharp
public class Program
{
    // Method that demonstrates several operations with User objects
    public void DoSomething()
    {
        // Creating a new User object for 'me' and setting properties
        User me = new User();
        me.FirstName = "Caleb";
        me.LastName = "Curry";

        // Creating a new User object for 'you' and setting properties
        User you = new User();
        you.FirstName = "John";
        you.LastName = "Smith";

        // Initializing a list of User objects with the previously created users
        List<User> users = new List<User>() { me, you };

        // Creating a new User object to use for searching in the list
        User search = new User();
        search.FirstName = "John";
        search.LastName = "Smith";

        // Searching for the 'search' User in 'users' list and printing the result
        // If the user is not found, print "not found"
        Console.WriteLine(User.GetUserFromList(users, search)?.FullName ?? "not found");

        // Creating another new User object
        User user = new User();
        user.FirstName = "Sally";

        // Calling the Test method with the 'user' object
        Test(ref user);

        // After calling Test, printing the FirstName of 'user'
        // This will print "Samantha" because the Test method modifies the object passed to it by reference
        Console.WriteLine(user.FirstName);
    }

    // Method that modifies the User object passed to it by reference
    public void Test(ref User i)
    {
        // Since 'i' is passed by reference, modifying it will affect the original User object
        i.FirstName = "Samantha";
    }
}
```

_____
## Method_Section_in_User.cs

- Outlines various methods and properties within the User class to manage and search user data.

```csharp
public class User
{
    // Property that returns the full name by concatenating first and last names
    public string FullName
    {
        get { return FirstName + " " + LastName; }
    }

    // Auto-implemented property for the first name
    public string FirstName { get; set; }

    // Auto-implemented property for the last name
    public string LastName { get; set; }

    // Overriding the ToString method to return the FullName property
    public override string ToString()
    {
        return FullName;
    }

    // Overriding the GetHashCode method to get a hash code based on the FullName property
    public override int GetHashCode()
    {
        return FullName.GetHashCode();
    }

    // Overriding the Equals method to compare User objects based on the FullName property
    public override bool Equals(object obj)
    {
        return obj is User user && FullName == user.FullName;
    }

    // Static method to print all users in a list
    public static void PrintUsers(List<User> users)
    {
        foreach (User user in users)
        {
            Console.WriteLine(user);
        }
    }

    // Static method to print a single user's information
    public static void PrintUser(User user)
    {
        Console.WriteLine("Static method. Print User");
        Console.WriteLine(user);
    }

    // Static method to find the index of a user with a given full name in a list
    public static int Find(List<User> users, string fullName)
    {
        for (int i = 0; i < users.Count; i++)
        {
            if (users[i].FullName == fullName)
            {
                return i;
            }
        }
        return -1; // Return -1 if not found
    }

    // Static method to find the index of a User object in a list
    public static int Find(List<User> users, User user)
    {
        for (int i = 0; i < users.Count; i++)
        {
            if (users[i].Equals(user))
            {
                return i;
            }
        }
        return -1; // Return -1 if not found
    }

    // Static method to retrieve a User object from a list based on a match
    public static User GetUserFromList(List<User> users, User user)
    {
        // Using LINQ to find the first user that matches the given user, or return null if not found
        return users.FirstOrDefault(u => u.Equals(user));
    }
}
```

_____

*The following content was produced by Cassius Fragomeni*

SOURCE:
https://www.youtube.com/watch?v=qOruiBrXlAw&