---
title: "Why your tech-startup should do test driven development"
date: 2013-09-29
tags: Tech
---

When it comes to starting a company a lot of attention goes to "what value does it generate?" and "what is the business model?" but for those who work in tech it is equally important to focus on "how are we going to build our product?" as this is one of the key problems that the CTO has to tackle. The answer to this could be "Test Driven Development"

# What is "Test Driven Development"?
The Wikipedia article of [Test driven development](http://en.wikipedia.org/wiki/Test-driven_development) (TDD) describes it as

> "a [software development process](http://en.wikipedia.org/wiki/Software_development_process) that relies on the repetition of a very short development cycle: first the developer writes an (initially failing) automated [test case](http://en.wikipedia.org/wiki/Test_case) that defines a desired improvement or new function, then produces the minimum amount of code to pass that test, and finally [refactors](http://en.wikipedia.org/wiki/Code_refactoring) the new code to acceptable standards."

The basic flow of TDD is this

![TDD Flow](http://upload.wikimedia.org/wikipedia/commons/9/9c/Test-driven_development.PNG)

# Why is TDD good for startups?
Developing a product from the ground up always is a challenge. But doing this in a startup environment is especially hard because of the particular conditions of a startup

1. **The product is a moving target**. In the early stages the product is still in a concept phase so it will undergo a lot of validation which means that existing features change or get dropped and new ones will be added. Hence the code/technology will be in a state of constant flux.
2. **There will be a lot of iterations/releases**. As a consequence of the first point frequent releases will happen. Each and every release needs to be tested properly to make sure it works as expected. Testing is a very time consuming task if not automated as it requires the full attention of the tester to make sure no bug slips quality assurance.
3. **The code is written by a new development team**. In the early stage of a software project, there are no conventions, defined way of structuring code, no standard architecture. So each engineer will write the software in the way that he is used to. Because agreeing on conventions is not only describing how stuff should be done its a process that is carried out by the engineering team and shows how well the team works. As these conventions and best practices form, a lot of code needs to be refactored.

In this particular setup a lot of [benefits of TDD](http://en.wikipedia.org/wiki/Test-driven_development#Benefits) can help with the development.

1. Test-driven development [...] can also drive the design of a program. By focusing on the test cases first, one must imagine how the functionality is used [...] so, the programmer is concerned with the interface before the implementation.
2. TDD can lead to more modularized, flexible, and extensible code. This effect often comes about because the methodology requires that the developers think of the software in terms of small units that can be written and tested independently and integrated together later. This leads to smaller, more focused classes, looser [coupling](http://en.wikipedia.org/wiki/Coupling_(computer_programming)), and cleaner interfaces. The use of the [mock object](http://en.wikipedia.org/wiki/Mock_object) design pattern also contributes to the overall modularization of the code because this pattern requires that the code be written so that modules can be switched easily between mock versions for unit testing and "real" versions for deployment.
3. Test-driven development ensures in this way that all written code is covered by at least one test. This gives the programming team, and subsequent users, a greater level of confidence in the code.
4. While it is true that more code is required with TDD than without TDD because of the unit test code, the total code implementation time could be shorter based on a model by Müller and Padberg. Large numbers of tests help to limit the number of defects in the code. The early and frequent nature of the testing helps to catch defects early in the development cycle, preventing them from becoming endemic and expensive problems. Eliminating defects early in the process usually avoids lengthy and tedious debugging later in the project.

# There is no "Test driven development does not work for us"
A lot of times TDD is not applied to projects because the people involved think it is not suitable for them. For example in the Embedded Software TDD is not very common as a lot of people think the dependency to the target hardware is a showstopper. But its just not true, people like [James Grenning](http://jamesgrenning.heroku.com/My-Book) show that it can be done and it's worth it. So regardless of the area of technology you are in start looking for best practices before dismissing TDD as an option!
