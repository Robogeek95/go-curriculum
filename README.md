# Go Curriculum

## From zero to hero in go
This is my study guide to help me cover topics in go deeply. 
I am switching from software development to software engineering and i have chosen go as my language for the interview.

## Resources
[GoLangDocs](https://golangdocs.com/)

[A tour of Go](https://tour.golang.org/)

[Learn Go with test-driven development](https://github.com/quii/learn-go-with-tests)

## The Curriculum
I borrowed some of the curriculum contents from [Gopher Guides](https://www.gopherguides.com/). They provide instructor led one on one virtual training. They already cover most of the curriculum saving you time of hunting for materials.

I would keep adding new materials to this list, the ones i create along the and great ones i find. If you have some resource you would luke to share, you are welcome to send a PR

## Introduction to Go
Five days deep dive into Go. It's self paced but i suggested you try to stick to the timeline as much as you can.

## **Day One**

### **Syntax And Types**

- [ ] fundamentals of the Go programming language. 
  - [ ] keywords, operators, delimiters that make up the language
  - [ ] proper idioms to declare and structure your code. 
  - [ ] Data structures (structs) H
  - [ ] Zero value and how Go handles it. 
  - [ ] An overview of how strings work in Go
  - [ ] how UTF-8 is handled
  - [ ] different types of string literals will also be covered
  - [ ] declaring variables and constants
  - [ ] how to use iota in Go.

https://pandulaofficial.medium.com/unicode-utf-8-explained-with-examples-using-go-5f8b7f4521d

### **Arrays And Iteration**

Arrays in Go are useful when planning for a detailed layout of memory. Using arrays can sometimes help avoid allocation. However, their primary use is for the building blocks of slices.

- [ ] the basics of creating, initializing, and indexing an array
- [ ] It will also cover basic loop constructs and loop control basics.

### **Slices**

Slices wrap arrays in Go and provide a more general, powerful, and convenient interface to data sequences

- [ ] slice basics such as creating, initializing, and iteration
- [ ] How to grow a slice
- [ ] Working with subsets of slices, 
- [ ] Slice tricks.

### **Maps**

Maps are a powerful built-in data structure that associates keys and values

- [ ] basic map creation
- [ ] Map initialization
- [ ] Map iteration
- [ ] Learn how to determine if values exist in maps and how to update and delete map values.

## **Day Two**

### **Pointers**

A pointer is a type that holds the address to the value of a variable. 
- [ ] learn the difference between `pass by value` and `pass by reference`
- [ ] learn how to declare pointers, and how to reference values as pointers
- [ ] You can also look into performance and security concerns and when to use pointers

### **Functions**

Functions in Go are a primitive type. 
- [ ] How to declare and call functions
- [ ] How to send zero or many arguments, as well as receive zero or many arguments
- [ ] Additionally, look into concepts such as `defer`, `init`, closures, and methods

## **Day Three**

### **Interfaces**

Interfaces in Go provide a way to specify the behaviour of an object: `If something can do this, then it can be used here`

- [ ] Look into how to use interfaces to abstract that behaviour.
- [ ] Empty Interface
- [ ] Satisfying multiple interface
- [ ] Asserting for behaviour
- [ ] The difference between `value` and `pointer` receivers and how they affect the ability to satisfy an interface.

### **Embedding And Composition**

Go does not provide the typical type-driven notion of subclassing. However, it does have the ability to “borrow” pieces of an implementation by embedding types within a `struct` or `interface`. 
- [ ] how promotion from embedding works as well how collision and overriding are handled
- [ ] We will also walk through how to embed types to be able to satisfy a specific interface.

## **Day Four**

### **Errors**

Error handling in Go can feel a bit tedious at first.

- [ ] Benefits of how Go's error model results in more reliable code. 
- [ ] This chapter will also cover how to handle basic errors and return errors as an interface that satisfies the error type. 
- [ ] Custom error types
- [ ] Panics and recovering from panics
- [ ] Sentinel errors

### **Concurrency**

Concurrent programming in many environments is made difficult by the subtleties required to implement correct access to shared variables. Go encourages a different approach in which shared values are passed around on channels and, in fact, never actively shared by separate threads of execution.

- [ ] Concurrency in Go
- [ ] What goroutines are
- [ ] Basic overview of the scheduler and terminology used.

- [ ] Concurrency With The Sync Package
  - [ ] goroutines and how to synchronize communication between them. 
  - [ ] Mechanics for synchronization such as `WaitGroups` and `Mutexes` along with the corresponding patterns for each\
  - [ ] How to spot common concurrency bugs and tools used to debug them.

### **Concurrency With Channels**

Channels are a conduit in Go used to communicate between goroutines.
- [ ] This chapter covers basic channel usage along with the corresponding patterns for each. 
- [ ] Find out the difference between a buffered and unbuffered channel, and when to use them
- [ ] Discover how to use channels for signalling for concepts such as graceful application shutdown. 
- [ ] Finally, learn how to spot common concurrency pitfalls and how to properly structure your concurrent code for to avoid them.

## **Day Five**

### **Context**

Package context defines the Context type, which carries deadlines, cancelation signals, and other request-scoped values across API boundaries and between processes. Context is used for controlling concurrent subsystems in your application. 
- [ ] Cover the different kinds of behaviour with contexts including cancelling, timeouts, and values.

### **Modules And Packages**

Package management is essential in creating repeatable builds in software. 
- [ ] Learn how to add and remove *Modules*, 
- [ ] Learn how to troubleshoot package dependencies
- [ ] Understand the files that control current dependencies
- [ ] Cover what packages are
- [ ] Learn some common approaches for structuring packages in your Go project.

### **Building And Compiling Go Applications**

Go has the ability to build and cross-compile with ease. 
- [ ] Cover the different ways to build your binary 
- [ ] Cover concepts for embedding build information such as version and GitHub SHA-1 hash. 
- [ ] See how build tags are used to conditionally include specific branches of code by targeting specific platforms or simply using the tags provided.

### **Tooling**

Go ships with a strong suite of built-in tools. 
- [ ] Learn the most common tools and how to use them in your daily development workflow. 
- [ ] In addition to the tools that ship with Go, there are a set of very important linters and vetters that can catch runtime bugs as well as significantly improve code quality and performance.

### **Testing Basics**

Testing in Go is easy, and simple to use. There is a strong emphasis on testing in Go. The compiler will catch a lot of bugs for you, but it can not ensure your business logic is sound or bug-free.

While the testing package isn't large, there are some features that are not properly understood. Do ensure you cover the following concepts:

- [ ] `testing.T`
- [ ] Error vs. Fatal
- [ ] Failure Messages
- [ ] Helpers
- [ ] Testing Packages

### **Table Driven Testing**

Table driven tests can be used to cover a lot of ground quickly while re-using common setup and comparison code. Table driven testing is not unique to Go, however, it is very powerful. In this module, 
- [ ] Cover the different ways to create, run, and isolate table-driven tests.

### **Running Tests**

Understanding the different options to run tests can greatly reduce the feedback cycle during development

- [ ] Running Specific Tests
- [ ] Verbose Output
- [ ] Failing Fast
- [ ] Parallel Options
- [ ] Short Testing
- [ ] Timing Out Tests
- [ ] Race Conditions

### **Code Coverage**

Code coverage is a great tool to show what part of your code is being tested. It will help identify areas that need more testing, as well as assist in making sure your tests actually test the part of the code you think it does.
- [ ] code coverage

### **Example Tests**

No project is complete without great documentation. Example tests are a great way to not only document your code, but ensure that the examples you use always work as they are actually a test in addition to the documentation.

### **Stubbing & Mocking Tests**

It's easy to decouple packages in Go using interfaces. Because of this, testing can also be much easier. However, you typically want to stub out your interfaces in tests so that unit testing is much easier.
- [ ] Cover how to write a stub for a service to enable easy and precise testing.

### **Testing Net/HTTP**

In the standard library there are two mechanisms for us to use to test web applications.

- [ ] Unit Style Testing
- [ ] Integration Style Testing

> Note: These are not their "official" names, but they do a good job of describing the styles of testing.
