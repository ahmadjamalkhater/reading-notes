# Reading Notes - Memory Management in C#

Classes
Classes are fundamental building blocks in object-oriented programming.
They encapsulate data and behavior into a single unit.
Classes serve as blueprints for creating objects.
They define the structure and behavior of objects of that class.
Constructors
Constructors are special methods used to initialize objects of a class.
They have the same name as the class and are called when an object is created.
Constructors can set the initial state of the object by assigning values to its properties or fields.
Constructors can be overloaded, allowing for different ways to create objects with varying parameter lists.
Constructors are not explicitly inherited, but derived classes can invoke the base class constructors using the base keyword.
Properties
Properties provide a way to access and manipulate the state of an object.
They encapsulate fields and provide controlled access to them.
Properties have get and set accessors, which define how the value is retrieved or modified.
Get accessors return the value of the property, while set accessors assign a value to it.
Properties can have different access levels (public, private, etc.) to control their visibility.
They can also have additional logic, such as validation or calculations, in the get and set accessors.
What's the difference between a static and an instance constructor?
A static constructor is used to initialize static members of a class and is called once per class.
It is invoked automatically before any static member is accessed or any instance is created.
A static constructor does not take any parameters and cannot be called explicitly.
An instance constructor, on the other hand, is used to initialize instance members of a class.
It is called each time an instance of the class is created using the new keyword.
An instance constructor can take parameters to initialize instance members based on the provided values.
The main difference lies in their purpose and when they are called. Static constructors are for static members, while instance constructors are for instance members.
How does the use of a static constructor differ from setting properties/values?
A static constructor is used for one-time initialization of static members of a class.
It is called automatically before accessing any static member or creating an instance.
The static constructor is useful for performing initialization tasks or setting up shared resources.
Setting properties or values, on the other hand, can be done in both static and instance contexts.
Properties can be set multiple times during the lifetime of an object.
The use of a static constructor focuses on the initialization of the class as a whole, whereas setting properties/values allows for more granular control over the state of individual instances.
Stack and Heap
The stack and the heap are two areas of memory used in program execution.
The stack is used for storing local variables, method calls, and other data during runtime.
It operates in a Last-In-First-Out (LIFO) order, meaning the last item pushed is the first to be popped.
Variables allocated on the stack have a fixed size and are automatically deallocated when they go out of scope.
The heap is used for dynamically allocating and deallocating memory during runtime.
Objects allocated on the heap have a variable size and are managed by the garbage collector.
The heap memory needs to be explicitly allocated and deallocated using keywords like new and delete (in some programming languages).
Rethinking memory usage with stack and heap
Understanding the stack and heap can help optimize memory usage in projects.
To make more efficient use of memory:
Minimize the usage of large objects or data structures on the stack.
Consider using references to objects stored on the heap instead of duplicating them on the stack.
Properly manage the allocation and deallocation of objects on the heap to avoid unnecessary memory usage.
Dispose or release resources as soon as they are no longer needed.
Avoid unnecessary object creation or retaining objects longer than necessary.
Minimize the usage of large collections or data structures on the stack and consider using heap-based alternatives when dealing with large amounts of data.
Garbage Collection Fundamentals
Garbage collection is an automatic memory management mechanism in C#.
It is responsible for reclaiming memory occupied by objects that are no longer in use.
The garbage collector periodically identifies and collects objects that are no longer reachable.
It releases the memory occupied by those objects, making it available for future allocations.
Garbage collection helps prevent memory leaks and simplifies memory management for developers.
The exact mechanism and algorithms used by the garbage collector may vary across different implementations and versions of the .NET framework.
Compare "Garbage Collection" in C# with the lifecycle of normal household items
Garbage collection in C# can be compared to the lifecycle of normal household items as follows:

Acquisition: When you bring a new household item into your home, you acquire it. Similarly, in C#, when you create a new object using the new keyword, memory is allocated to store that object.

Usage: You use household items for a certain period until they fulfill their purpose or are no longer needed. Similarly, in C#, objects are used in your program to perform specific tasks.

Disposal: When a household item is no longer useful or needed, you dispose of it by throwing it away or recycling it. Similarly, in C#, when an object is no longer needed or goes out of scope, the garbage collector identifies it as eligible for garbage collection.

Garbage Collection: Just as you rely on waste management systems to collect and dispose of your household waste, in C#, the garbage collector periodically identifies objects that are no longer reachable or referenced by the program and releases the memory occupied by those objects.

Reclamation: In garbage collection, the memory occupied by the disposed objects is reclaimed and made available for future use. Similarly, in waste management, the items you disposed of are recycled or the space is freed up for other purposes.

The comparison highlights the similarities between the lifecycle of household items and the garbage collection process in C#. Objects are created, used, identified as no longer needed, and their memory is reclaimed for efficient memory management.

Things I want to know more about
How different programming languages handle memory management?
Advanced memory management techniques, such as object pooling and manual memory allocation.
Performance implications of using stack vs. heap memory.
Optimization strategies for minimizing memory usage in large-scale projects.
Note: The above notes are based on my understanding and knowledge of the topic. No direct content has been quoted from any external sources