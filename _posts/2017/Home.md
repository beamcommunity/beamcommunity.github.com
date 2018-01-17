This is the BEAM Community page for 2017 projects. You can also check [official Google Summer of Code page for 2017 projects](https://summerofcode.withgoogle.com/organizations/5912941485359104/).

## Accepted Projects

This section lists down the projects accepted in GSoC 2017, in the BEAM community.


### Lasp – A Biparite Proposal for Lasp's Lacking Documentation

Project’s objective is to write documentation for Lasp. However, much like tackling the writing of a novel, an ill-defined goal such as “write documentation” is about as guaranteed to fail as “get to the top of the Best Sellers list.” So, I must first divide the project into two separate branches each of which address specific problems.

#### Broad Documentation

The first will be to address “documentation” as it’s known to the FOSS community at large: a series of individual pages describing the minutiae of function calls and language syntax. The organization of all this disparate information is key, though, to useful documentation. Instead of sporadic, nonsensical linking to and fro, I will instead take inspiration from the documentation of other popular FOSS projects. Python and Crystal are two of many projects whose beneficial documentation methods I hope to replicate for Lasp.

#### The "Book"

Second, I wish to write an introductory “book” for Lasp newcomers. Inspired by Rust’s successful online book, I believe a similar approach to Lasp would not only augment the development of a general documentation, but increase visibility in the larger FOSS community.

* **Student:** Matt Wiese
* **Mentors:** Christopher Meiklejohn, Vitor Enes Duarte


### Elixir – A code formatter for Elixir

By leaving tedious formatting to the machine, code formatters provide a substantial increase in engineering productivity and a consistent style across teams. Hence, this project implements a code formatter that can take a piece of Elixir code and format it automatically according to a standard style guide. It is very similar to tools such as `rustfmt` and `gofmt`.

* **Student**: alexjiao
* **Mentors**: José Valim, whatyouhide


### ejabberd – Ejabberd support for "Let's Encrypt" ACME protocol

The Automatic Certificate Management Environment (ACME) protocol is a communications protocol for automating interactions between certificate authorities and their users' web servers, allowing the automated deployment of public key infrastructure at very low cost. Supporting this protocol will reduce the complexity of acquiring certificates for TLS encryption, via the "Let's encrypt" certificate authority.

The final goal of this project is for ejabberd to fully support the ACME protocol and thus provide an easy and cheap way of acquiring security certificates.

* **Student:** Konstantinos Kallas
* **Mentor**: Evgeny Khramtsov
* **Result**: [blog.process-one.net/lets-encrypt-ejabberd](https://blog.process-one.net/lets-encrypt-ejabberd/)


### Erlang – ETS support for Erlang Lab

Erlang Lab (https://github.com/erlanglab) is an Open Source project aimed at analysing the performance of Erlang and Elixir systems. The project provides web-based visualisations of the analysis. It can help developers to better understand their systems, observe the system behaviour and identify weaknesses.

The Erlang Lab project is still developing and lots of its features are missing. The feature I would like to implement is a plugin for ETS (Erlang Term Storage) tables. The OTP team keeps working on the performance of ETS but Erlang and Elixir programmers, especially the newcomers, are prone to make mistakes which can cause e.g. lock contention on an ETS. Although it is possible to trace this kind of problems using Erlang tracing or dedicated profilers it can be difficult and time-consuming.

The plugin I would like to deliver will rely on tracing techniques and the Erlang system introspection API. Information collected in this way will be presented through the web UI. I believe it will enable developers to quickly identify problems and understand them better.

* **Student:** Kacper Mentel
* **Mentor:** Michal Slaski


### Barrel – Implementation of a RabbitMQ Plugin for BarrelDB

All changes in the Barrel databases and indexes (updates, creations and deletions) can be retrieved in Barrel using the HTTP API. There are many usages for such a log. The replication in barrel is based on it. Having a way to send these changes via RabbitMQ would open it to more applications and usages.

* **Student**: Tah Teche Tende
* **Mentor**: Benoit Chesneau


### Lasp – Implementing a Real World Application in the Lasp Programming Language

The nature of distributed systems and their fault model is chaotic: replicas can fail temporarily or just stop working, and the complexity of adding defensive code against all possible scenarios is unrealistic if complex applications are to be designed. Despite several techniques that try to mitigate this issue (e.g. RPC), a more opaque abstraction layer is needed in order to avoid long implementation times as well as incorrect behaviour driven from faulty or careless code. I believe that providing a programming-language-level abstraction layer is an effective approach to significantly reduce the amount of time focused on how systems can fail, rather than how they should work. Such an approach should mainly consist in supplying systems programmers with basic functionalities in the following areas: node distribution, data replication and partition tolerance. Being in an early adoption stage, Lasp needs applications that can serve as proof of concept in order to increase awareness of its capabilities as well as user adoption. This proposal is about the implementation of a real world application based on previous work published recently at PaPoC'17 - an EuroSys workshop.

* **Student:** goncalotomas
* **Mentors:** Christopher Meiklejohn, Vitor Enes Duarte


### Elixir – Language Server Protocol implementation for Elixir

Language Server Protocol is an attempt to establish a common, cross-language and cross-editor protocol for tools to implement features like auto complete, goto definition, find all references, and alike. It mediates between the editor (the client) and a language smartness provider (the server).

This project aims to develop a server that implements the Language Server Protocol specification for the Elixir language. The end goal is to have a basic functional language server, working with at least one client.

* **Student:** Nishith Kumar Shah
* **Mentors:** Michał Muskała, José Valim


### Zotonic – Port Zotonic Shell Scripts to Erlang EScript

Currently Zotonc uses shell scripts for the command line functionality e.g starting Zotonic, installing modules, etc. These command line scripts are fragile and non-portable hence they should be replaced with either Escript or Erlang modules. This would also create opportunities for exposing the script functionalities in a web interface. The following will be done:

* Check on speed of Erlang scripting.
* Design the architecture for the Erlang implementation.
* Ensure hooks/modules that can be used from within Zotonic itself.
* Rewrite the scripts in Erlang.

* **Student:** Blaise M.
* **Mentor:** Arjan Scherpenisse


### ejabberd – Server-to-Server Stream Management Support for ejabberd

Reliability is essential for communication using XMPP. Although basic XMPP is not reliable in some situations. One of these situations is losing long-lived TCP connection between client and server or server and server because of network or destination failure. If this connection isn’t properly closed, sender will be unaware of the loss and connection will appear as open to server until TCP timeout is reached. All messages which will be sent by server during this time will be lost.

The goal of this project is to implement XEP-0198 for server-to-server communication in ejabberd. This extension allows to request stanza acknowledgement and quickly resume session. Any messages that were not delivered over previous connection will be retransmitted during session resumption without duplication.

* **Student:** Anna Mukharram
* **Mentor:** Holger Weiß
* **Result:** [blog.process-one.net/server-to-server-stream-management-support](https://blog.process-one.net/server-to-server-stream-management-support/)

## Participating OSS projects

* [Barrel](https://barrel-db.org/)
* [Ejabberd](https://www.ejabberd.im/)
* [Lasp](https://lasp-lang.org/)
* [Zotonic](http://zotonic.com/)
