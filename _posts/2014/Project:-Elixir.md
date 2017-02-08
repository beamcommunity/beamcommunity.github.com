* Website: http://elixir-lang.org/
* Responsible: José Valim, Eric Meadows Jonsson, Devin Torres
* If you have any questions, send an e-mail to beam-community@googlegroups.com.

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Process monitoring

Brief explanation: Elixir is built on top of the Actor paradigm, which each Actor is called a Process in the Erlang VM parlance. Any Elixir software is made of many of those processes running concurrently exchanging messages between them. The goal of this project is to provide an application thats run in the browser that allows developers to inspect the processes running, their activity and trace the messages exchanged in between them.

Expected results: A web application that interacts with Elixir processes.

Knowledge prerequisites: Good knowledge with web development (HTML/JS), basic Elixir knowledge.

Mentor: José Valim, Eric Meadows Jonsson, Devin Torres

### Idea #2: Windows support

Brief explanation: Many developers use Windows as their main Operating System and Elixir should provide proper support to those developers. The goal of this project is to ensure Elixir natively compiles on Windows and to provide a set of tools to developers who wish to precompile their projects on Windows. We should also provide conveniences to make it easy for Elixir developers to embed C code (via Erlang NIFs) into their mix projects.

Expected results: Elixir reliably running on Windows environment.

Knowledge prerequisites: Intermediate knowledge of build tools on Windows, basic Elixir knowledge.

Mentor: José Valim, Alex Rønne Petersen, Dave Cottlehuber

### Idea #3: Releases

Brief explanation: OTP provides Erlang developers with releases, which allows them to assemble their projects into a package to be deployed in production. The goal of this project is to allow releases to be build directly from Mix (Elixir's build tool) and also support scripts like [Pogo](https://github.com/onkel-dirtus/pogo) for easy management of production nodes.

Expected results: Functionality and tasks to build releases for Elixir projects

Knowledge prerequisites: Intermediate Elixir/OTP knowledge.

Mentor: José Valim, Devin Torres

### Idea #4: XML processor

The majority of tools for processing XML in the ecosystem are outdated. This project should explore the different approaches to provide a XML processor .

Expected results: A decent XML processor.

Knowledge prerequisites: Intermediate Elixir knowledge.

Mentor: José Valim

### Idea #5: Project Jupyter integration

[iPython](http://ipython.org) has gained more and more traction in the Python community with its rich environment for programming. Recently, the iPython project evolved into the [Jupyter Project](jupyter.org), which aims to provide the same rich environment, not only for Python, but for a diverse range of programming languages.

Many languages have already started to integrate with the Jupyter Project, like [Julia](https://github.com/JuliaLang/IJulia.jl), [Haskell](https://github.com/gibiansky/IHaskell) and [Erlang](https://github.com/robbielynch/ierlang). The goal of this project is to provide integration with the Elixir programming language.

Expected results: Basic integration with the Jupyter Project.

Knowledge prerequisites: Previous experience with web development.

Mentor: José Valim

### Idea 6: Elixir interface to SMTP and Sendmail

Send e-mails is a common task in many Elixir applications. This idea aims to provide a good project to be used as a foundation by Elixir applications to deliver e-mail via SMTP or Sendmail, often providing robust APIs and/or abstractions other libraries and frameworks can build on top.

Expected results: A set of APIs for e-mail delivery via SMTP and/or Sendmail.

Knowledge prerequisites: Intermediate Elixir knowledge.

Mentor: José Valim