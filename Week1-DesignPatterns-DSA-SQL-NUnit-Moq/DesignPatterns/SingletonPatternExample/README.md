# Exercise 1: Implementing the Singleton Pattern

## Objective

Implement the Singleton Design Pattern to ensure that a logging utility class has only one instance throughout the application lifecycle.

---

## Question

![Singleton Pattern Question](Screenshots/01_Singleton_Question.png)

---

## Scenario

A logging utility should maintain a single instance across the entire application to ensure consistent logging behavior.

---

## Implementation

### Logger Class

The `Logger` class is implemented as a Singleton by:

* Declaring a private static instance variable.
* Making the constructor private.
* Providing a public static `GetInstance()` method to access the single instance.

### Program Execution

The application:

1. Requests a Logger instance.
2. Logs application startup information.
3. Requests the Logger instance again.
4. Verifies that both references point to the same object.

---

## Expected Output

```text
Logger Instance Created
[LOG] Application Started
[LOG] Application Running
Only one Logger instance exists.
```

---

## Explanation

The Singleton Pattern is a Creational Design Pattern that restricts the instantiation of a class to a single object.

### Key Features

* Only one object of the class is created.
* Provides a global access point to the instance.
* Prevents unnecessary object creation.
* Improves consistency for shared resources like loggers and configuration managers.

### Verification

```csharp
Logger logger1 = Logger.GetInstance();
Logger logger2 = Logger.GetInstance();
```

Both variables reference the same Logger object, confirming that the Singleton Pattern is correctly implemented.

---

## Conclusion

The Logger class successfully implements the Singleton Design Pattern by ensuring that only one instance exists and is reused throughout the application lifecycle.
