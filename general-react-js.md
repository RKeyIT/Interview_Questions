# General React/JS Questions

### Subjects

1. General principles
   - Common principles
   - Programming paradigms (imperative and declarative)
   - Functional programming (functors, Key Features)
   - Work with backend (AJAX, HTTP requests, headers, etc)
   - Request parameters and JSON

## General Principles

### Common principles

1.  <details><summary>Naming</summary>

    Necessity of semantic naming is a topic of code understanding and maintainability. That's why any of names should be descriptive to entity what it was assigned to.

    Commonly to name some entities wi'll use camelCase, exclude of constructors naming. In this case name should be written by PascalCase

    Global constants can be written in the UPPERCASE, snake_case or it combinations.

    If it boolean checker it should be beginning from "is".

    Functions should be named by it purpose

    ***

    </details>

1.  <details><summary>DRY/KISS/YAGNI</summary>

    They're fundamental concepts in software development that aimed at reducing code writing problems and improving reusability, maintainability and readability of code writing.

    DRY (Don't Repeat Yourself) - main aspects of DRY are Avoid Duplication, Single Source of Truth, Modularity and Reusability, Maintenance and Readability.

    KISS (Keep It Simple Stupid) - Minimalism, Simplicity and Clarity of code writing principle.

    YAGNI (You Ain't Gonna Need It) - Keeping focus on essential tasks, avoiding adding unnecessary features, reduces complexity.

    ***

    </details>

1.  <details><summary>Code review - for what we need it, how does it work</summary>

    Code review is a crucial process in software development aimed at ensuring code quality, identifying bugs, improving maintainability, and promoting knowledge sharing within the development team.

    In simple case there are two persons. One of them is the code writer and the second one is a reviewer. Commonly the reviewer is a developer with more experience that can find problems of code or approve it if it looks acceptable.

    ***

    </details>

1.  <details><summary>Clean code from Martin - base principles</summary>

    Descriptive names

    KISS or Single Responsibility Principle in functions and methods

    Comments should be written to explain requirement of this way of code writing or provide a context that cannot be understood by the code reading. The code should be written the way that reduce of comments amount.

    Single code style on a project

    Error handling should be explicit and informative. Exceptions should be used rarely.

    ***

    </details>

1.  <details><summary>Clean code - good understanding of necessary of comments, etc</summary>

    Comments should be used as a last possible description. Only if the code can't explain what it's doing. Or if the code-like explanation is complex.

    A code clarity solution is more preferred than leaving comments. If the code is hard to understand then it is a sign that the code can be improved.

    ***

    </details>

1.  <details><summary>Antipatterns</summary>

    Antipatterns are opposite concepts of patterns. While patterns aiming to improve our development-experience, Antipatterns are bad practices, common mistakes and problems that can looks like good decisions but mainly will make worth impact on code quality, performance of application, etc.

    ***

    </details>

### Programming paradigms (imperative and declarative)

1.  <details><summary>Understanding what is paradigm</summary>

    Paradigm is a bundle of programming rules (techniques) that aims to solve problems by more effective way.

    Imperative programming means that the programmer should explain to computer how to solve problem step by step. It's usually uses mutable state manipulations and controlling flow of execution by loops, conditions and function calls. It's explains how exactly some problem should be solved.

    Meanwhile, the declarative programming focuses on expression what should be done. This approach is using of abstraction layers such as methods of global objects, language features or frameworks.

    ***

    </details>

1.  <details><summary>Imperative and Declarative - examples of eac paradigm</summary>

    Imperative is:
    <pre>
    function getOdds(numbers) {
        const odds = [];
    
        for (let i = 0; i < numbers.length; i++) {
            if (numbers[i] % 2 !== 0) odds.push(numbers[i]);
        }
    
        return odds;
    }
    
    const odds = getOdds([1, 2, 3]);
    </pre>

    Declarative is:
    <pre>
    const odds = numbers.filter(el => el % 2 !== 0)
    </pre>

    ***

    </details>

### Functional programming (functors, Key Features)

1.  <details><summary>What is Functional Programming</summary>

    FP is a programming paradigm that based on functions and functions composition. Basically, it means immutability and declarative style of programming.

    ***

    </details>

1.  <details><summary>What is  main feature of FP</summary>

    First-class functions

    Pure functions

    High-Ordered functions

    Function composition

    ***

    </details>

1.  <details><summary>Simple example of program</summary>

    <pre>
    function buildAgeMessage(age) {
        return 'I am ' + age + ' years old.'
    }
    
    function greet(greetingWord) {
        return function(name) {
            return greetingWord + ' everyone, my name is ' + name + '. ' + buildAgeMessage();
        }
    }
    </pre>

    ***

    </details>

### Work with backend (AJAX, HTTP requests, headers, etc)

1.  <details><summary>What is https</summary>

    ***

    </details>

1.  <details><summary>What is AJAX</summary>

    ***

    </details>

1.  <details><summary>What is JSON</summary>

    ***

    </details>

1.  <details><summary>Basic usage of XHR (how to make simple request and handle answer)</summary>

    ***

    </details>

1.  <details><summary>Basic usage of fetch() (how to make simple request and handle answer)</summary>

    ***

    </details>

1.  <details><summary>CRUD HTTP methods</summary>

    ***

    </details>

1.  <details><summary>Difference between PUT, PATCH, POST</summary>

    ***

    </details>

1.  <details><summary>What is REST?</summary>

    ***

    </details>

1.  <details><summary>CORS what is it, why do we need them</summary>

    ***

    </details>

1.  <details><summary>What is CORS and why we need it</summary>

    ***

    </details>

1.  <details><summary>How to get around CORS</summary>

    ***

    </details>

1.  <details><summary>Work with json response</summary>

    ***

    </details>

1.  <details><summary>Set headers in request</summary>

    ***

    </details>

### Request parameters and JSON

1.  <details><summary>Clone objects with JSON methods</summary>

    ***

    </details>

1.  <details><summary>How to add request body</summary>

    ***

    </details>

1.  <details><summary>How to send requests with different content types and what is it for</summary>

    ***

    </details>

1.  <details><summary>Read the response that came from the back-end and process it (how to save the file, how to filter out unnecessary data before using it in the target function)</summary>

    ***

    </details>
