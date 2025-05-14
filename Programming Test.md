Programming Test

---

### Question 1: Iteration Program

Write a Python program that iterates from 1 to 100. In each iteration, generate a random number between 1 and 100. If the number is divisible by 7, print "Lucky number!" after the number. Also, print a separator line "---" every 5 iterations.

```python
import random

for i in range(1, 101):
    number = random.randint(1, 100)
    print(f"{i}: {number}", end=" ")
    if number % 7 == 0:
        print("Lucky number!")
    else:
        print()
    if i % 5 == 0:
        print("---")
```

---

### Question 2: Design Patterns

#### a) What is your understanding of the term “Design Patterns”?

Design patterns are reusable solutions to common software development problems. They offer a standard way of designing software structures to solve recurring challenges, improve readability, and promote maintainability and scalability.

#### b) Explain the MVC Pattern.

MVC stands for Model–View–Controller. It is a design architecture that separates an application into three main logical components:

- **Model**: Handles the data, logic, and rules of the application.
- **View**: Displays the data (UI layer).
- **Controller**: Acts as an interface between Model and View, handling user input and updating the view.

**Use Cases:**  
MVC is widely used in frameworks such as Django (Python), Spring (Java), ASP.NET (C#), and Angular (JavaScript) for building modular and scalable web applications.

#### c) List three other design patterns and describe them.

- **Singleton Pattern**  
  Ensures a class has only one instance and provides a global access point.  
  *Use Case:* Logging systems, configuration managers, and driver objects.

- **Factory Pattern**  
  Provides an interface for creating objects in a superclass but allows subclasses to alter the type of objects that will be created.  
  *Use Case:* Object creation involving complex logic that shouldn't be exposed to the client.

- **Observer Pattern**  
  Defines a dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.  
  *Use Case:* GUIs and event-driven systems (e.g., UI updates when the model changes).

---

### Question 3: Class Implementation and OOP Concepts

Implement the following Python code:

```python
from abc import ABC, abstractmethod

class A(ABC):
    def __init__(self, name):
        self._name = name

    @abstractmethod
    def PrintName(self):
        pass

class B(A):
    def __PrintName(self, message):
        print(f"{message}: {self._name}")

class C(B):
    def PrintName(self, message):
        print(f"{message}: {self._name}")
```

#### a) Are you able to directly create a new instance of class A?

No, because class `A` is an abstract class and contains an abstract method. Abstract classes cannot be instantiated directly.

#### b) Given an instance of class `C`, are you able to call the method `PrintName` defined in class `B`?

Yes, class `C` inherits from class `B`, so it can override and access methods from `B`. In this implementation, the method is overridden and made public in `C`.

#### c) What Object-Oriented Programming (OOP) features are demonstrated in this example?

- **Abstraction**: Class `A` is abstract.
- **Encapsulation**: `_name` is a protected attribute.
- **Inheritance**: Classes `B` and `C` inherit from `A` and `B`.
- **Polymorphism**: Method overriding in class `C`.

---

### Question 4: Working with Existing Code

#### a) How would you approach understanding and contributing to an existing code base with minimal disruption?

- Read through documentation, comments, and README files.
- Explore the code structure and understand module interactions.
- Run the software and debug it to observe the flow.
- Use tools like breakpoints and call tracing.
- Communicate with existing team members to clarify unclear logic.

#### b) What practices would you follow to ensure your changes integrate well with the current structure?

- Follow existing naming conventions and code style.
- Write modular, well-tested code.
- Keep functions/classes focused on a single responsibility.
- Use version control with meaningful commit messages.
- Review and test code before pushing changes.

#### c) What techniques would you use to keep the code base clean, modular, and easy to maintain?

- Apply SOLID principles.
- Use design patterns when applicable.
- Write unit and integration tests.
- Refactor code regularly to reduce technical debt.
- Maintain updated documentation and API references.

#### d) How would you design or refactor software to be flexible for future changes while keeping existing features stable?

- Use abstraction and interfaces to separate concerns.
- Apply dependency injection to decouple components.
- Follow the Open-Closed Principle (open to extension, closed to modification).
- Implement versioned APIs and clear module boundaries.
- Apply patterns like Strategy, Adapter, or Facade when needed.
