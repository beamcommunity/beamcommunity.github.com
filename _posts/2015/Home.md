This is the BEAM Community page for 2015 projects.

## Accepted Projects

This section lists down the projects accepted in GSoC 2015, in the BEAM community. You can check the result of each project below.

* [Ejabberd - Grapherl : stats aggregation & graphing](#ejabberd---grapherl--stats-aggregation--graphing)
* [Ejabberd - XEP-0357 app server](#ejabberd---xep-0357-app-server)
* [Elixir - NoSQL adapters for Ecto](#elixir---nosql-adapters-for-ecto)
* [Elixir - Project Jupyter integration](#elixir---project-jupyter-integration)
* [MongooseIM - Implementation of XEP-0322](#mongooseim---implementation-of-xep-0322)
* [Zotonic - Simplified and Secured Logins](#zotonic---simplified-and-secured-logins)

### Zotonic - Simplified and Secured Logins

The idea behind this project is promote easy login process for
Zotonic.com by using Erlang as it's programming language. With increasing 
web applications, there needs to be way for users to login which is more hassle
free. Moreover this needs to be secure and safe.

This is achieved by multi-factor authentication system in which user is verified
multiple times, firstly by username and password and after that authentication
by user's email(by sending a link having uuid connected to it) or an 
OTP(One time password) sent to his mobile phone.The aim of the project is to
provide more security to user's account but with the main goal to make
authentication more user-friendly and easy-to-use.


* **Student:** Anant
* **Mentor:** Arjan Scherpenisse

Source code: [https://github.com/anant2047/zotonic.git](https://github.com/anant2047/zotonic.git)

### Ejabberd - Grapherl : stats aggregation & graphing

Grapherl is a stats aggregation and on-demand graph generation
system. Leveraging the legendary power of Erlang/OTP, it is designed
(discussed further) to be real-time & highly scalable and customizable
allowing its users to control each and every aspect as they seem
fit. Grapherl is intended but limited to gather and represent metrics
aggregated from ejabberd servers as its designed to be serviceable to
any other application producing metrics like gauge, counter or timing
values.

* **Student:** Vanshdeep
* **Mentor:** Mickaël Rémond


### Ejabberd - XEP-0357 app server

I want to continue implementing XEP-0357 (Push) as an ejabberd
module. The app server part shall be reusable by other XMPP servers.

* **Student:** Christian Ulrich
* **Mentor:** Holger Weiß

Source code: https://github.com/royneary/mod_push and https://github.com/royneary/oshiya

### Elixir - NoSQL adapters for Ecto

The goal of the project is to explore possibility of Ecto supporting
NoSQL databases and creating a NoSQL adapter. I plan to divide time
spent on the project into three main parts: - Creating MongoDB
adapter - Extending support for SQL databases - Native MongoDB driver
or other NoSQL adapters.

* **Student:** Michał Muskała
* **Mentor:** José Valim


### Elixir - Project Jupyter integration

[iPython](http://ipython.org/) has gained more and more traction in the Python community with its rich environment for programming. Recently, the iPython project evolved into the [Jupyter Project](https://github.com/beamcommunity/beamcommunity.github.com/wiki/jupyter.org), which aims to provide the same rich environment, not only for Python, but for a diverse range of programming languages.

Many languages have already started to integrate with the Jupyter Project, like [Julia](https://github.com/JuliaLang/IJulia.jl), [Haskell](https://github.com/gibiansky/IHaskell) and [Erlang](https://github.com/robbielynch/ierlang). The goal of this project is to provide integration with the Elixir programming language.

Expected results: Basic integration with the Jupyter Project

* **Student:** Piotr Przetacznik
* **Mentor:** José Valim

Source code: [https://github.com/pprzetacznik/IElixir](https://github.com/pprzetacznik/IElixir)


### MongooseIM - Implementation of XEP-0322

The main goal of my project is to add support for EXI to
MongooseIM. This will also require extending the Escalus XMPP library
with the ability to communicate with MongooseIM using EXI.

* **Student:** Piotr Ociepka
* **Mentor:** Michał Piotrowski


## Participating OSS projects

* Elixir
* Ejabberd
* MongooseIM
* Zotonic
