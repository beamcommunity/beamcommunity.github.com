* Website: http://elixir-lang.org/
* Responsible: José Valim, Yurii Rashkovskii, Devin Torres
* Notes: most ideas here requires only basic Elixir knowledge and a good read on the [Getting Started guide](http://elixir-lang.org/getting_started/1.html) with basic functional programming experience is enough to get started
* If you have any questions, send an e-mail to beam-community@googlegroups.com.

Ideas are listed in no particular order.

### Idea #1: Process monitoring

Brief explanation: Elixir is built on top of the Actor paradigm, which each Actor is called a Process in the Erlang VM parlance. Any Elixir software is made of many of those processes running concurrently exchanging messages between them. The goal of this project is to provide an application thats run in the browser that allows developers to inspect the processes running, their activity and trace the messages exchanged in between them.

Expected results: A web application that interacts with Elixir processes.

Knowledge prerequisites: Good knowledge with web development (HTML/JS), basic Elixir knowledge.

Mentor: José Valim, Yurii Rashkovskii.

### Idea #2: Debugger and inspection

Brief explanation: Debuggers are an essential tool for developers. Although Elixir provides a REPL and term inspecting, there isn't a general purpose debugger available. The goal of this project is to improve the state of art of Elixir's debuggers and inspections tools by providing a debugger with pretty printing, step by step instructions, source navigation and more.

Expected results: A debugger tool.

Knowledge prerequisites: Basic Elixir knowledge.

Mentor: José Valim, Yurii Rashkovskii, Alex Rønne Petersen, Devin Torres

### Idea #3: A Language Integrated Query

Brief explanation: Interaction with databases are a common requirement for many applications. Although Elixir developers have access Erlang libraries that interact to the database, some of them requires writing SQL by hand, others have a complicated to use API. The goal of this project is to provide a language integrated query, similar to [LINQ in C#](http://msdn.microsoft.com/en-us/library/vstudio/bb397926.aspx) and [Query Expressions in F#](http://msdn.microsoft.com/en-us/library/vstudio/hh225374.aspx) allowing a developer to easily interact and manipulate databases.

Expected results: A library integrated with Elixir that allows easy database interaction.

Knowledge prerequisites: Intermediate SQL knowledge, basic Elixir knowledge.

Mentor: José Valim, Yurii Rashkovskii, Alex Rønne Petersen

### Idea #4: Windows support

Brief explanation: Many developers use Windows as their main Operating System and Elixir should provide proper support to those developers. The goal of this project is to ensure Elixir natively compiles on Windows and to provide a set of tools to developers who wish to precompile their projects on Windows.

Expected results: Elixir reliably running on Windows environment.

Knowledge prerequisites: Intermediate knowledge of build tools on Windows, basic Elixir knowledge.

Mentor: José Valim, Devin Torres, Alex Rønne Petersen, Dave Cottlehuber

### Idea #5: Actors abstractions

Brief explanation: [OTP](http://en.wikipedia.org/wiki/Open_Telecom_Platform) provides a supervisors, gen servers and other abstractions useful for Elixir developers. However, there are abstractions that can be built on top of those and would be useful for everyday developers, like [pools](https://github.com/devinus/poolboy), [circuit breakers](http://doc.akka.io/docs/akka/snapshot/common/circuitbreaker.html) and a routers that can delegate messages to a number of routees using different strategies (round robin, broadcast, etc). The goal of this project is to build a set of abstractions so they are available in Elixir's developers toolset.

Expected results: A set of Actor abstractions available in Elixir's developers toolset.

Knowledge prerequisites: Prior knowledge of the actors system, basic Elixir knowledge.

Mentor: José Valim, Devin Torres, Alex Rønne Petersen

### Idea #6: Calendar

Brief explanation: One important but difficult task developers around the world need to work with are related to times, dates and timezones. The goal of this project is to provide a set of functions that works against date and times, considering their timezones. We should be able to calculate dates, check their validity, calculate equivalency between timezones, add dates with time intervals and more. 

Expected results: A set of functions that work on date, time, datetime and timezones.

Knowledge prerequisites: Basic Elixir knowledge.

Mentor: José Valim, Devin Torres