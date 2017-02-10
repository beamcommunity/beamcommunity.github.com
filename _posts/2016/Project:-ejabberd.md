* **Website:** http://www.ejabberd.im/
* **Responsible:** Mickaël Rémond (mremond at process-one)
* **Possible mentors:** Mickaël Rémond ([experienced mentor, since 2006](http://wiki.xmpp.org/web/Real-time_wiki)), Alexey Shchepin, Badlop, Evgenyi Khramtsov, Holger Weiss, Jérôme Sautret, Christophe Romain
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com
* You can add Mickaël Rémond on XMPP: mremond AT process-one DOT net

ejabberd is one of the most known Erlang project, developed since 2002 by [ProcessOne](http://www.process-one.net). As a student, you will have the opportunity to work with the ejabberd historical lead developers directly and work on projects that can have a huge impact given the number of worldwide users.

Ahead of the Summer of code, we have prepared a way to automatically setup for ejabberd development environment [ejabberd-vagrant-dev](https://github.com/processone/ejabberd-vagrant-dev)

As a student, you can select the language you prefer to contribute to ejabberd, between Erlang and Elixir.

Here is a page to help you get started working with ejabberd community as a GSoC student: [A quick introduction to ejabberd for GSoC hopefuls](https://www.ejabberd.im/node/24794)

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

# Idea #1: Privileged Entity Support to Write Powerful External Components for ejabberd

**Brief explanation:** Many open source projects want to extend XMPP server like ejabberd with external component. The de facto approach used today is XEP-0114: Jabber Component that ejabberd implements. It is however too limited in scope to implement powerful component that need to interact more deeply with the server. The goal of this project is to implement newer server extensions to XMPP that allowing more powerful component to run on ejabberd. This is good for open source in general as those components will also work with all other servers that conform to these protocols. The project will implement XEP-0356 Privileged entity and XEP-0355 Namespace delegation.

**Expected results:** The goal is to be able to use external components that leverage the new features of XEP-0356 and XEP-0355. The XMPP microblogging components SàT (Salut à Toi) will be used as a reference to valid the project result. The goal is to make those components fully run onto ejabberd with the newly implemented XEP. To fully support this component, a separate XEP will be implemented by community mentor to add missing Pubsub feature (XEP-0351 Recipient server-side filtering). That component, while not mandatory in the context of the project, will allow full validation of the behaviour on an existing full featured component.

**Knowledge prerequisites:** XMPP servers in general, Erlang

**Difficulty:** Moderate

**Possible Mentor:** Evgeny Khramtsov, Mickaël Rémond

# Idea #2: Server-to-Server Stream Management Support for ejabberd

**Brief explanation:** Stream Management is a feature that adds a reliability layer to communication between entity on an XMPP network. Stream Management is described in XEP-0198. Stream management is already implemented for client to server communication in ejabberd. However, adding the same level of reliability and robustness to server-to-server communication would make the whole XMPP network more robust.

**Expected results:** 

- Implementation of XEP-0198 for server-to-server communication
- ejabberd code may be refactored to allow reuse of client to server feature when possible.
- Ability to cache outgoing messages for a given for a configurable amount of time to allow other end server to reboot or short unavailability will also be added (with correct overflow protection).

**Knowledge prerequisites:** XMPP servers in general, Erlang

**Difficulty:** Moderate

**Possible Mentor:** Holger Weiss

# Idea #3: Support for Things Discovery service in ejabberd

**Brief explanation:** The first step in getting Internet of Things over XMPP to take off is to be able to register things. Implementing XMPP-IOT protocol would allow Things to be installed, configured and claimed by their owner.

**Expected results:** 

- Implementation of ejabberd server component conforming to XEP-0347 Internet of Things - Discovery

**Knowledge prerequisites:** XMPP servers in general, Erlang

**Difficulty:** Moderate

**Possible Mentor:** Jérôme Sautret

# Idea #4: Improve ejabberd configuration and extensibility with configuration DSL

**Brief explanation:** There is plenty of room for improvements in both ejabberd configuration, extensions and plugins writing. The idea would be to built a new configuration DSL (Domain Specific Language) for ejabberd that would both allow to configure it and enhance its feature set through hooks.

It would make both an easier to understand config file and a more easily extensible server for casual developers.
The project will requires to review the existing ejabberd hooks and extend the list to make it suitable for the new DSL.
Elixir language would be a good candidate for the Domain Specific Language.

**Expected results:** Elixir powered ejabberd version.

**Knowledge prerequisites:** Knowledge of Erlang and possibly ejabberd.

**Difficulty:** Difficult

**Possible Mentor:** Alexey Shchepin, Mickaël Rémond

# Idea #5: Web UI administration improvements: Manage ejabberd services, MUC rooms, etc

**Brief explanation:** ejabberd comes with a web console to manage the server. However, many administration features are only available from XMPP clients from users with admin rights or from ejabberdctl command-line tools. For example, managing chat rooms would be more efficiently performed using a web front-end. To spread the use of ejabberd as an easy to use corporate chat services, it is important to make it more manageable through a web browser.

**Expected results:** Revamp ejabberd management web interface with extended features, with a focus on managing users, MUC Room and shared rosters.

**Knowledge prerequisites:** Knowledge of Erlang, XMPP and web developments.

**Difficulty:** Difficult

**Possible Mentor:** Alexey Shchepin, Mickaël Rémond

# Idea #6: XMPP and HTTP convergence

**Brief explanation:** XMPP is a difficult protocol for web developer. It is a connected stateless protocol. However, it is possible to map a lot of the operation, semantic of XMPP on top of HTTP using traditional ReST semantic.. You could for example browse chat rooms, pubsub nodes, etc using a rest interface. If the session can be separated from the routing of the XMPP protocol, it is even possible to send and receive XMPP stanzas through the HTTP protocol.
A lot could be done that way and it would open up a whole new range of use case of ejabberd to traditional web developers or to environnement where using XMPP directly is difficult.

**Expected results:** ejabberd version that can be controlled either through XMPP or a pure HTTP interface to simplify XMPP usage for web developers.

**Knowledge prerequisites:** Erlang or a functional language and web development.

**Difficulty:** Moderate

**Possible Mentor:** Mickaël Rémond