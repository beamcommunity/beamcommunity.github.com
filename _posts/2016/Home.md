This is the BEAM Community page for 2016 projects.

## Accepted Projects

This section lists down the projects accepted in GSoC 2016, in the BEAM community. You can check the result of each project below.

* [ejabberd – Privileged Entity Support to Write Powerful External Components for ejabberd](#ejabberd--privileged-entity-support-to-write-powerful-external-components-for-ejabberd)
* [ejabberd – Improve ejabberd configuration and extensibility with Elixir-based configuration DSL](#ejabberd--improve-ejabberd-configuration-and-extensibility-with-elixir-based-configuration-dsl)
* [Elixir/Barrel – Implement an elixir backend for indexing and extending the database](#elixirbarrel--implement-an-elixir-backend-for-indexing-and-extending-the-database)
* [Lasp – Distributed Intermediate Tree Elimination in Lasp](#lasp--distributed-intermediate-tree-elimination-in-lasp)
* [Lasp – Implementing op-based CRDTs in Lasp](#lasp--implementing-op-based-crdts-in-lasp)
* [Zotonic – Implementation of Real-time Statistics in Zotonic](#zotonic--implementation-of-real-time-statistics-in-zotonic)
* [Erlang Dbus: Prepare Erlang DBus for OTP](#erlang-dbus-prepare-erlang-dbus-for-otp)

### ejabberd – Privileged Entity Support to Write Powerful External Components for ejabberd

Writing XMPP components is a good way to enhance the functionality of XMPP servers like ejabberd. Jabber Component Protocol (XEP-0114) is used today for this goal. However, this protocol is quite limited. The goal of this project is to implement XEP-0356 Privileged entity and XEP-0355 Namespace delegation server extensions to XMPP that will allow to run more powerful component on ejabberd. Implementation of these extensions can help to extend ejabberd functionality with existing powerful components like Collecta or SàT and give an impulse to create new services.

* **Student:** Anna Muharram
* **Mentor:** Alexey Shchepin

Source code: [Amuhar/Final.md](https://gist.github.com/Amuhar/e319ba56ba52bf62f1f5ad29b03c7b74)

### ejabberd – Improve ejabberd configuration and extensibility with Elixir-based configuration DSL

This project aims to improve the ejabberd configuration, extensions and plugins writing using the Elixir programming language and its DSL capabilities.

There is plenty of room for improvements in both ejabberd configuration, extensions and plugins writing. The idea would be to built a new configuration DSL (Domain Specific Language) for ejabberd that would both allow to configure it and enhance its feature set through hooks.

The project provides both an easier to understand config file and a more easily extensible server for casual developers.

* **Student**: Gabriel Gatu
* **Mentors**: Holger Weiß, Mickaël Rémond

Source code / Report: [GSoC Work Product Submission](https://gist.github.com/gabrielgatu/7aae9fa01f6640946324e33aad2e609c)

### Elixir/Barrel – Implement an elixir backend for indexing and extending the database

Barrel is a distributed database built on top of Erlang and CouchDB. There are provisions in Barrel to extend the database with user defined modules and hooking them to database events like database creation, deletion, updates etc. Barrel now uses Hooks to let modules subscribe to the events and register a callable that can return and modify results.

Secondary indexes can also be created using functions that accept a Doc and return a Key/Value tuple.

Right now there is provision only for functions written in Erlang or Javascript.

The aim of the proposal is to add Elixir to the list of languages supported by Erlang. This would allow more developers to extend barrel and also brings a whole bunch of libraries and support from the Elixir ecosystem.

* **Student:** sivsushruth
* **Mentors**: Benoit Chesneau, Nicolas Dufour

Source code / Report: [sivsushruth/gsoc](https://github.com/sivsushruth/gsoc/wiki/GSoC-report-for--Barrel-BEAM-Community)

### Lasp – Distributed Intermediate Tree Elimination in Lasp

Lasp computations are formed using a small subset of a functional language. In functional languages, it is very common to see intermediate lists—and, more generally, intermediate trees—serve as glue between functions. If these intermediate structures, however, are not used by any other part of the program, replicating them in the underlying network that supports the Lasp language exacts a non-negligible cost at run-time.

This project aims to enable Lasp to generate efficient reductions of these intermediate trees into a single value that represents the combination of multiple functions.

* **Student:** Borja o'Cook
* **Mentor:** Zeeshan Lakhani

Report: [Lasp and the Google Summer of Code](https://ergl.github.io/gsoc2016.html)

### Lasp – Implementing op-based CRDTs in Lasp

Conflict-free Replicated Data Types (CRDTs) make the design of eventually consistent systems non ad-hoc and anomaly-free by formalizing the reconciliation mechanism of diverging replicas. Pure operation-based (aka op-based) CRDTs are variants of CRDTs that are generic and more efficient as they allow for compact solutions in both the sent messages and the state size. On the other hand, Lasp is a new programming model designed to simplify large scale, fault-tolerant, distributed programming using state-based CRDTs. It would be very interesting to implement the operation-based approach in Lasp and compare it with the currently implemented state-based approach.

* **Student**: g_unis
* **Mentor**: Christopher Meiklejohn

Source Code: [Pure op-based datatypes implementations](https://gist.github.com/gyounes/de1709f254e84812713079d34786afc8)

### Zotonic – Implementation of Real-time Statistics in Zotonic

Implement a module which will help give insight into the traffic of a Zotonic server/site through visualization of the stats in real-time. The system already knows a lot about the visitors (user-agent, referrer, ip-address etc) and it would be nice to leverage this into a real-time display per site or aggregated over the whole server. Including historical views for later analysis.

* **Student:** Tex
* **Mentor:** Arjan Scherpenisse

Source code: [tahteche/zotonic](https://github.com/tahteche/zotonic/commits/mod_admin_statistics?author=tahteche)

### Erlang Dbus: Prepare Erlang DBus for OTP

D-Bus is largely used as RPC mechanism on Linux-based systems but can be also used on any modern OS, thanks to multiple transports, not only dependant on the Linux OS.

Some work needs to be done before proposing it as an OTP application: remove OS-dependant code: UNIX socket handling, use OTP-style Makefiles, integrates unit and functional testing, generates documentation.

*Student gave up before completion.*

## Participating OSS projects

* [Barrel](https://barrel-db.org/)
* [Erlang Dbus](https://github.com/lizenn/erlang-dbus)
* [Ejabberd](https://www.ejabberd.im/)
* [Lasp](https://lasp-lang.org/)
* [Zotonic](http://zotonic.com/)
