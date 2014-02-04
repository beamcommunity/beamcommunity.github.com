* Website: http://www.process-one.net/en/ejabberd
* Responsible: Mickaël Rémond (mremond at process-one), Alexey Shchepin, Badlop, Evgenyi Khramtsov, Jérôme Sautret, Christophe Romain.
* Notes: Prior knowledge of Erlang (or a functional language) is a good start to begin with the project. We are also open to student proposals.
* If you have any questions, send an e-mail to beam-community@googlegroups.com.
* You can add Mickaël Rémond on XMPP: mremond A T process-one.net


ejabberd is one of the most known Erlang project, developed since 2002 by [ProcessOne](http://www.process-one.net). As a student, you will have the opportunity to work with the ejabberd historical lead developers directly and work on projects that can have a huge impact given the number of worldwide users.

Ideas are listed in no particular orders.

# Idea #1: XMPP and HTTP convergence

Brief explanation: XMPP is a difficult protocol for web developer. It is a connected stateless protocol. However, it is possible to map a lot of the operation, semantic of XMPP on top of HTTP using traditional ReST semantic.. You could for example browse chat rooms, pubsub nodes, etc using a rest interface. If the session can be separated from the routing of the XMPP protocol, it is even possible to send and receive XMPP stanzas through the HTTP protocol.
A lot could be done that way and it would open up a whole new range of use case of ejabberd to traditional web developers or to environnement where using XMPP directly is difficult.

Expected results: ejabberd version that can be controlled either through XMPP or a pure HTTP interface to simplify XMPP usage for web developers.

Knowledge prerequisites: Erlang or a functional language and web development.

Mentor: Mickaël Rémond

# Idea #2: Behaviour analysis and metrics

Brief explanation: An XMPP server like ejabberd provide hundreds of relevant metrics to measure and understand its behaviour. For large scale deployments, statistics gathering need to be as lightweight and unintrusive as possible.
There is already an emerging UDP protocol for lightweight metrics gathering which is called Statsd. We propose to implement a scalable statsd code base in Erlang and add relevants hook in ejabberd for building a Dashboard service.

Expected results: Erlang based stats daemons link to a scalable database back-end and a Dashboard to represent the gathered informations.

Knowledge prerequisites: Good networking kwnowledge.

Mentor: Mickaël Rémond

# Idea #3: Social networking meets chat with Buddycloud protocol

Brief explanation: Buddycloud is an XMPP protocole extension for building federated social networks.
To spread usage of that protocol it would be useful to add it to ejabberd server. ejabberd being one of the most used server would make that protocol available for thousands of deployment.
More details here:
- HTTP API:https://buddycloud.org/wiki/buddycloud_HTTP_API
- XMPP part: https://buddycloud.org/wiki/XMPP_XEP
Both elements could be implemented in ejabberd.

Expected results: ejabberd implementation that natively support Buddycloud protocol through plugins.

Knowledge prerequisites: Erlang or a functional language. Having good knowledge of XMPP protocol is also very important.

Mentor: Alexey Shchepin, Mickaël Rémond

# Idea #4: Improve ejabberd configuration and extensibility

Brief explanation: There is plenty of room for improvements in both ejabberd configuration, extensions and plugins writing. The idea would be to built a new configuration DSL for ejabberd that would both allow to configure it and enhance its feature set through hooks.
It would make both an easier to understand config file and a more easily extensible server for casual developers.
The project will requires to review the existing ejabberd hooks and extend the list to make it suitable for the new DSL.
Elixir language would be a good candidate for the Domain Specific Language.

Expected results: Elixir powered ejabberd version.

Knowledge prerequisites: Knowledge of Erlang and possibly ejabberd.

Mentor: Alexey Shchepin, Mickaël Rémond

# Idea #5: Multi-User chat module scale and robustness

Brief explanation: Multi-user chat module is clustered in ejabberd but each chat room itself are not redundant. Making it possible to have multiple instance of rooms running on different node could make them more scalable and resilient to the loss of a node.

Expected results: More robust chat room service for ejabberd.

Knowledge prerequisites: Knowledge of Erlang and XMPP.

Mentor: Alexey Shchepin, Mickaël Rémond