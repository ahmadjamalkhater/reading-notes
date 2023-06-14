# Exception Handling

## Debugging for absolute beginners

## Summary:

This article discusses the importance of using a debugger in software development to identify and fix coding errors. It emphasizes the need to clarify the problem before starting the debugging process and suggests asking specific questions about the expected behavior of the code and the actual outcome. It also encourages developers to examine their assumptions and consider potential mistakes, such as using the wrong API or making typos in the code.

The article explains the concept of debugging mode, where the debugger actively monitors the program's execution and allows developers to pause and inspect the code's state. It highlights the use of breakpoints to pause the program at specific points for detailed examination. The Visual Studio IDE is recommended as a debugging tool, and the article provides step-by-step instructions on debugging a sample application with bugs.

The sample code demonstrates a scenario where the output does not match the expected result. By using breakpoints and examining the code during debugging, the developer identifies the issue with the GalaxyType property, which was incorrectly defined as an object instead of the intended GType class. The article concludes by emphasizing the importance of understanding code intent and starting with small, working code snippets when debugging.

Overall, the article provides an introduction to debugging principles and offers practical tips for effective debugging using Visual Studio as the debugging tool.

## Name one major benefit of being able to trace the call stack.

One major benefit of being able to trace the call stack is that it allows developers to understand the flow of execution in their code. By tracing the call stack, developers can see the sequence of function or method calls that led to the current point in the code. This information is valuable for debugging purposes as it helps identify the sequence of events that led to a particular error or unexpected behavior.

## Try/Catch Blocks
## summary:
To catch exceptions using the try/catch block, follow these steps:

Place the code statements that might raise an exception inside a try block.
Write one or more catch blocks below the try block to handle the exception(s). Each catch block specifies the type of exception it can handle.
Inside each catch block, write the necessary statements to handle the specific exception type.

##1. If you could use try/catch in your day to day life, name an exception you’d like to ‘catch’ and handle.

If I were to use try/catch in my day-to-day life, one exception I would like to catch and handle is a network connection error.
In today's digital age, we heavily rely on network connectivity for various tasks, such as accessing online services, communicating with others, or retrieving information. However, network connections can sometimes be unreliable or encounter issues. By using try/catch, I could handle network connection exceptions and provide a better user experience or take necessary actions to mitigate the impact of a network failure.


## 2.From an efficiency standpoint, are there downsides to try/catch blocks?

Code Execution Flow: When an exception is thrown within a try block, the normal flow of execution is interrupted, and the control transfers to the corresponding catch block. This flow disruption can impact the overall efficiency of the code, especially if exceptions occur frequently. In performance-critical scenarios, it's important to carefully consider the placement of try/catch blocks and minimize their impact on the critical code paths.


## Exception Handling

Imagine you are baking a cake using a recipe. While following the recipe, you may encounter unexpected situations like running out of an ingredient or accidentally burning the cake. In programming, these unexpected situations are called exceptions.
The .NET framework, which is a set of tools and libraries for building software, provides a built-in mechanism to handle exceptions effectively. It's like having a safety net in your code. When an exception occurs during the execution of a program, instead of crashing and displaying confusing error messages, .NET allows you to catch and handle those exceptions gracefully.
Think of the try-catch block as your safety net. You enclose the code that might cause exceptions within the try block, just like putting the cake batter in the oven. If an exception occurs, it's caught by the catch block, which acts as your backup plan. Inside the catch block, you can specify what actions to take when an exception happens, such as displaying a friendly error message or trying an alternative approach.
The .NET framework also provides different types of exceptions, just like different types of problems you may encounter while baking. For example, there could be an exception for a missing file, similar to missing ingredients for a recipe. By catching specific types of exceptions, you can handle them differently based on their nature.
Overall, the .NET approach to exception handling is about being prepared for unexpected situations in your code and having a mechanism to handle them in a controlled and organized manner, similar to how you handle unexpected situations while baking a cake.



## Several glaring mistakes were made during the production of the Therac-25 and its predecessors, which contributed to the accidents and failures of the system. Here are some notable mistakes:

1.Insufficient testing: The software for the Therac-25 was developed by a single programmer over several years using assembly language. The lack of a robust testing process and independent code review meant that critical software flaws went undetected.

2.Lack of proper safety mechanisms: Previous models of the Therac series had hardware interlocks to prevent certain errors, but the Therac-25 relied primarily on software checks for safety. The removal of these hardware interlocks increased the risk of accidents caused by software failures.

3.Inadequate error messages and feedback: The error messages displayed by the Therac-25 were often cryptic and did not provide clear guidance to operators when errors occurred. This lack of informative feedback made it difficult for operators to identify and rectify problems.

4.Overconfidence and lack of responsiveness: The engineers and manufacturers of the Therac-25 displayed overconfidence in the system's safety and failed to promptly address reports of software bugs and user complaints. This led to a delay in recognizing the severity of the issues and taking appropriate actions.

5.Insufficient training and user documentation: The training provided to operators of the Therac-25 was inadequate, and the user documentation did not adequately explain the potential risks and dangers associated with the system. This lack of proper training and information contributed to operator errors and misunderstandings.