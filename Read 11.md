# Inheritance
Inheritance involves deriving new classes that benefit from the behavior and properties defined in other classes. The base class contains members that are inherited by the derived class. The derived class specializes the base class and adds additional behavior.

# Interfaces
Interfaces define a set of members that must be implemented by the classes that use them. Classes can support specific capabilities defined by interfaces regardless of the genetic relationship. Classes can implement multiple interfaces even if they can only derive from a single direct base class.

# Abstract Base Classes
Abstract classes prevent direct instantiation and serve as templates for derived classes. They contain abstract method signatures that must be implemented by non-abstract classes directly derived from them. Non-abstract derived classes must provide implementations for any abstract methods from an abstract base class.

# Abstract and Virtual Methods
Virtual methods can be overridden by derived classes with their own implementations. Abstract methods must be implemented in non-abstract classes that directly inherit from the abstract class. Abstract and virtual methods provide the foundation for polymorphism.

#Preventing Further Derivation
A class can prevent other classes from inheriting from it by declaring itself or its members as "sealed".

# Derived Class Hiding of Base Class Members
A derived class can hide base class members by declaring members with the same name and signature. The "new" modifier can be used to explicitly indicate that the member is not intended to override the base member.

# Abstract and Sealed Classes and Class Members (C# Programming Guide)
The abstract keyword enables you to create classes and class members that are incomplete and must be implemented in a derived class.

The sealed keyword enables you to prevent the inheritance of a class or certain class members that were previously marked virtual.

# Abstract Classes and Class Members
Classes can be declared as abstract by putting the keyword abstract before the class definition. An abstract class cannot be instantiated but provides a common definition of a base class that multiple derived classes can share.

Abstract classes may also define abstract methods by adding the keyword abstract before the return type of the method. Abstract methods have no implementation and must be implemented by derived classes.

When an abstract class inherits a virtual method from a base class, it can override the virtual method with an abstract method. Abstract classes can force derived classes to provide new method implementations for virtual methods.

# Sealed Classes and Class Members
Classes can be declared as sealed by putting the keyword sealed before the class definition. A sealed class cannot be used as a base class and prevents derivation. Sealed classes offer some run-time optimizations and make calling sealed class members slightly faster.

In a derived class, a method, indexer, property, or event that is overriding a virtual member of the base class can be declared as sealed. This prevents any further derived class from overriding that member.

# Polymorphism 

Polymorphism is the third pillar of object-oriented programming, after encapsulation and inheritance. It refers to the ability of objects to take on different forms and behave differently based on their actual types at runtime.

Polymorphism allows objects of derived classes to be treated as objects of their base class. This means that a derived class object can be passed as a parameter to a method that expects a base class object. This flexibility enables code reusability and simplifies program design.

Base classes can define virtual methods that can be overridden by derived classes. This means that the derived classes can provide their own implementation of the virtual method, which will be invoked at runtime instead of the base class implementation. This allows for specialization and customization of behavior in derived classes.

Polymorphism enables working with groups of related objects in a uniform way. For example, in a drawing application, you can have a base class called "Shape" and derived classes like "Rectangle," "Circle," and "Triangle." By treating all these objects as instances of the base class, you can invoke the same method on each object and have the appropriate implementation executed based on the actual type of the object.

In C#, every type is polymorphic because all types inherit from the base class "Object." This means that you can use polymorphism with both built-in types and user-defined types.

Overall, polymorphism allows for flexibility, extensibility, and code reuse in object-oriented programming by enabling objects to exhibit different behaviors based on their actual types at runtime.
