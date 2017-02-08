* Website: http://elixir-lang.org/
* Responsible: José Valim, Eric Meadows-Jonsson, Alexei Sholik
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Project Jupyter integration

[iPython](http://ipython.org) has gained more and more traction in the Python community with its rich environment for programming. Recently, the iPython project evolved into the [Jupyter Project](jupyter.org), which aims to provide the same rich environment, not only for Python, but for a diverse range of programming languages.

Many languages have already started to integrate with the Jupyter Project, like [Julia](https://github.com/JuliaLang/IJulia.jl), [Haskell](https://github.com/gibiansky/IHaskell) and [Erlang](https://github.com/robbielynch/ierlang). The goal of this project is to provide integration with the Elixir programming language.

Expected results: Basic integration with the Jupyter Project

Knowledge prerequisites: Previous experience with web development, intermediate knowledge of Elixir or Python

Mentor: José Valim

### Idea 2: Elixir interface to SMTP and Sendmail

Send e-mails is a common task in many Elixir applications. This idea aims to provide a good project to be used as a foundation by Elixir applications to deliver e-mail via SMTP or Sendmail, often providing robust APIs and/or abstractions other libraries and frameworks can build on top.

Expected results: A set of APIs for e-mail delivery via SMTP and/or Sendmail

Knowledge prerequisites: Intermediate Elixir knowledge

Mentor: José Valim

### Idea 3: NoSQL adapters for Ecto

[Ecto](http://github.com/elixir-lang/ecto) is a language integrated query for Elixir. Currently Ecto supports PostgreSQL with on going work to support other SQL databases, like MSSQL and MySQL. The goal of this project is to explore and extend Ecto to support at least one NoSQL database.

As a result, we also expect SQL databases to have improved capabilities. For example, PostgreSQL has great supports for embedding via JSONB columns, which could be leveraged as part of the NoSQL structure.

Expected results: A NoSQL database adapter for Ecto.

Knowledge prerequisites: Intermediate Elixir knowledge.

Mentor: José Valim, Eric Meadows-Jonsson