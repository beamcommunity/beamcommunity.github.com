This is the BEAM Community page for 2014 projects.

## Accepted Projects

This section lists down the projects accepted in GSoC 2014, in the BEAM community. You can check the result of each project below.

* [Elixir on Windows](#elixir-on-windows)
* [Work Stealing Scheduling on Parallella](#work-stealing-scheduling-on-parallella)
* [Disco Worker in Haskell](#disco-worker-in-haskell)
* [MongooseIM: XEP-0280 Message Carbons](#mongooseim-xep-0280-message-carbons)
* [Live Streaming for Swirl Project](#live-streaming-for-swirl-project)
* [Federation of Servers in Zotonic](#federation-of-servers-in-zotonic)

### Elixir on Windows

The student worked on improving the standard library and test coverage for Windows systems as well as providing a web installer for Windows developers.

His work has been merged and has played a substantial role in the adoption of Elixir for Windows developers and gather positive feedback from many Windows users.

* **Student:** Chris Hyndman
* **Mentor:** José Valim

### Work Stealing Scheduling on Parallella

This project aimed to explore different strategies for work stealing in the Parallella board. Unfortunately, this project failed for being behind the schedule.

* **Student:** Aman Mangal
* **Mentor:** Luca Favatella

### Disco worker in Haskell

In this project, Kasia created a Haskell library for submitting map-reduce jobs to Disco. This library is available [here](https://github.com/zuzia/haskell_worker). It has been modeled after Disco python and golang worker libraries. The input of the job can be from the web (http) or Disco Distributed FileSystem (ddfs). A couple of example programs have been added to simplify adoption.

* **Student:** Katarzyna Streich
* **Mentor:** Shayan Pooya

### MongooseIM: XEP-0280 Message Carbons

Shambu added support for XEP-280 (Message Carbons) to Erlang based XMPP chat server MongooseIM. A lot of the work was also put to improve the test suite, including system tests. This project was also useful to check for any irregularities in message handling by the server due to any discrepancy between this new module and existing ones.

* **Student:** Shambhu Prasad
* **Mentor:** Stefan Strigler

### Live Streaming for Swirl Project

The Swirl project aims to bring peer-to-peer streaming to the world and the student worked on many funcionalities required , like secure hasing checking, and other live streaming related functionalities.

* **Student:** Patrik Pettersson
* **Mentor:** Dave Cottlehuber

### Federation of Servers in Zotonic

After a definition phase with Zotonic's core developers to define the overall architecture of the federation setup, Alvaro has been working on the refactoring of Erlang's MQTT server implementation to support additional transportation channels, most importantly SSH connections. Besides this,  Alvaro implemented a new [client library](https://github.com/alvaropag/emqttcli) for MQTT, to be able to send MQTT messages over these trusted SSH connections in the server federation.

* **Student:** Álvaro G. Pagliari
* **Mentor:** Arjan Scherpenisse

## Participating OSS projects

* [Disco proposals](/2014/Project:-Disco.md) - Disco is a distributed computing framework based on the MapReduce paradigm
* [Elixir proposals](/2014/Project:-Elixir.md) - Elixir is a functional meta-programming language that runs on the Erlang VM
* [Erlang Development Environment proposals](/2014/Project:-Erlang-Development-Environment.md) - User friendly installers which set up the whole Erlang development environment
* [MongooseIM proposals](/2014/Project:-MongooseIM.md) - MongooseIM is a robust and efficient XMPP server aimed at large installations
* [Swirl proposals](/2014/Project:-Swirl.md) - swirl is a high-speed modern peer-to-peer content sharing and live streaming application, written in Erlang/OTP, and based on the new [PPSP draft protocol](http://datatracker.ietf.org/doc/draft-ietf-ppsp-peer-protocol/), broadly similar to BitTorrent
* [Work Stealing on the Parallella proposals](/2014/Project:-Parallella.md) - Parallela aims to bring a super computer for everyone and this projects focus on bringing work strealing scheduling to the Parallella
* [Zotonic proposals](/2014/Project:-Zotonic.md) - Zotonic is a high speed, real-time web framework and content management system 
