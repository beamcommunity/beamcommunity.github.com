* Website: https://github.com/processone/tsung
* Responsible: Mickaël Rémond (mremond at process-one), Nicolas Niclausse, Eric Cestari, Jérôme Sautret
* If you have any questions, send an e-mail to beam-community@googlegroups.com.
* You can add Mickaël Rémond on XMPP: mremond A T process-one.net 

# Idea #1: Tsung Integrated Web Server for Control and Graphs

Brief explanation: Tsung is know to be difficult to configure and run in a cluster. Creating a new custom DSL for scenario definition could help improve the power of the platform and make writing scenario easier and more accessible to all kind of users.

Expected results: Tsung version with integrated web server and dynamic HTML and Javascript interface that act as a control interface for Tsung.

Knowledge prerequisites: Knowledge of Erlang or a functional language and web development.

Mentor: Nicolas Niclausse, Mickaël Rémond

# Idea #2: Multimaster support in Tsung

Brief explanation: Tsung can only support one master at the moment to control a full benchmark from only one node. On very large benchmarks, this becomes a bottleneck. Adding the ability to have several master will increase Tsung scability. It requires some changes in Tsung architecture as well as some extra tooling to gather data to generate graphes, for example.

Expected results: Tsung version with ability to support and coordinate multiple master.

Knowledge prerequisites: Knowledge of Erlang or a functional language and web development.

Mentor: Eric Cestari

# Idea #3: Dynamic clients

Brief explanation: Tsung benchmark infrastructure is defined in the scenario, before the benchmark starts. To have better flexibility, especially the ability to add more clients as the benchmark progress. It allows to limit the cost of the infrastructure during the benchmark and help make sure the right resources are used. It would allow to replace instances if it fails during the benchmark as well or allow to swap instances to get more powerful ones.

Expected results: Tsung version with ability to support dynamically added clients.

Knowledge prerequisites: Knowledge of Erlang or a functional language and web development.

Mentor: Eric Cestari