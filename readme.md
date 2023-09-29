# Todo
## Scenario
Welcome to the TODO application, where users are able to create lists, rename them, add items to those lists, and mark each item as completed. 

Recently users have reported that they have been unable to mark items as completed. A new test has been introduced that demonstrates the issue (see [ListsControllerTests.cs - Line 153](./todo.api.test/ListsControllerTests.cs)).

A significant amount of feedback has been received requesting the ability to delete todo lists, and to be able to remove items from those lists. A couple of tests have also been introduced in [ListControllerTests.cs](./todo.web.test/ListControllerTests.cs) to help implement the new features. Unlike the case for deleting lists, the UI has not been updated to accomodate deleting individual todo items.

**Running `dotnet test` will reveal three failing tests. Each needs to be resolved without altering the contents of the existing unit test. The [list razor page](./todo.web/Views/List/List.cshtml) should also be updated to allow deleting individual todo items.**

The exam is independent, but intended to be completed in a short amount of time. Try to make minimal changes to the existing code to pass the failing tests. Be sure to consider the following while making your changes:

* You are not expected to extensively refactor any element of the code, however opportunities for improvement should be noted.
* The unit tests should remain as-written. If you feel a test could be improved upon, make note of it as something to be discussed.
* Try to spot design patterns being used in the project, and whether they are they being used effectively.
    * **You are also asked to provide a short text (up to 500 characters) identifying at least two design patterns used in the project and providing an explaination of how each design pattern is used and some of the benefits or drawbacks it brings.** This response will be used by the board to assess your ability to communicate effectively in writing and be part of the assessment for your ability to develop IM/IT system.
* When todo.api is started, a SQLite database is created at ./AppData/todo.db. When running tests, the database is created in memory.
* Test data is being generated in the `todo.data.TodoContext.Seed()` for both the automated testing and when the application is running. Each test is isolated and generates a fresh set of data.

## Getting Started
1. (Optionally) [Download visual studio code (VSCode)](https://code.visualstudio.com/download)
1. [Download .NET 6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
1. Clone this project, or [download the source](https://github.com/tc-ca/todo/archive/refs/heads/main.zip) and extract its contents
1. (Optionally) Open VSCode and open the top-level folder (file -> open folder)
1. In a terminal at the root of the project, run the following commands (note that the `dotnet run` commands must be executed in separate terminal instances)

``` PowerShell
dotnet dev-certs https --trust
dotnet run --project todo.api/todo.api.csproj
dotnet run --project todo.web/todo.web.csproj
```

1. View todo.api swagger documentation at https://localhost:7180/swagger
1. Browse the web application at https://localhost:7172/

## Running xUnit tests
* Follow the steps in [Getting Started](#getting-started)
* In the integrated terminal, run `dotnet test`

## Submitting Your Exam
You may fork the repository on github, or submit the modified source files as an email attachment to &lt;contact info here&gt;.

Your answer to the question identifying the design patterns must be included in your email submission or added to your github repository. If added to your github repository, you are required to indicate in your email where the file is located.

**Important:** You must send an email to the identified contact prior to the deadline indicated in your invitation, the email must contain your submission or a link to your github repository. The date/time on the email or github file timestamps will be used to ensure the files were submitted before the deadline.
