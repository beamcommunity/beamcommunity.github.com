* Website: https://barrel-db.org/
* Possible mentors: Benoit Chesneau
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com

[Barrel](https://barrel-db.org) is a modern document-oriented database in Erlang focusing on data locality (put/match the data next to you) and P2P.


Ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Implement an elixir backend for indexing and extend the database

Barrel provides a simple way to extend the database with your own modules by hooking them to the database events (database creation/deletion/updates, connections...). Each modules can subscribe to the events and register a callable that may return/modify the results. Additionally, secondary indexes can be created using functions accepting doc and returning a Key/Value tuple.  

For now functions and callable can only be written in Erlang or Javascript. The addition of Elixir to the list of supported language would allow more developers to extend barrel using a concurrent language.

Expected results: a prototype of a barrel node showing the usage of Elixir to index the documents and to hook to the database event.

Knowledge prerequisites: A knowledge of elixir is required to start the project. Example in other supported languages will be provided.

Possible Mentors: Benoit Chesneau

### Idea #2: implement a rabbitmq plugin 

All changes in the databases and indexes (updates, creations and deletions) can be retrieved in Barrel using the HTTP API. There are many usages for such a log. The replication in barrel is based on it. Having a way to send these changes via rabbitmq would open it to more applications and usages.

Expected results: a prototype of a plugin sending the events to  remote application using rabbitmq.

Knowledge prerequisites: A knowledge of Erlang is required. 

Possible Mentors: Benoit Chesneau

### Idea #3: Investigate the btree code

Investigate the btree code  specifically, review the way it is handling lists and where its algorithm can be improved. The investigation can be done directly by using [cbt](https://github.com/benoitc/cbt) which only contains the needed modules.

Expected results: a review of the code and list of possible optimisations that could be done. 

Knowledge prerequisites: Erlang and btree knowledge is required.

Possible Mentors: Benoit Chesneau

### Idea #4: Add quickcheck testing

[QuickCheck](http://www.quviq.com/products/erlang-quickcheck/) is a library for random testing of program properties. Testing automatically barrel using quickcheck would help to improve its code quality. 

Expected results: automates the testing of the barrel code.

Knowledge prerequisites: Quickcheck lite or [Quickcheck-CI](http://quickcheck-ci.com) will be used for the tests. A knowledge or Erlang is required.

Possible Mentors: Benoit Chesneau

### Idea #5: Improve the compaction

The btree backend of Barrel store the data in an append-only manner. It then needs to be compacted from time to time to reduce the size on the disk. When a lot of writes happen on a barrel node, the compaction will take a lot of time to end. A new algorithm is needed to improve it. 

Expected results: a faster compaction of the database.

Knowledge prerequisites: Erlang

Possible Mentors: Benoit Chesneau

### Idea #6: New Javascript backend using a NIF.

The  current Javascript backend in barrel is implemented using spidermonkey 1.8.5 using an Erlang port. Possibly a NIF over spidermonkey or another javascript implementation like V8 could helps to speed its implementation.

Expected results: proof of concept of a new Javascript backend for Barrel

Knowledge prerequisites: Erlang NIFs, C/C++ or any other language used to write the NIF. 

Possible Mentors: Benoit Chesneau

### Idea 7: add windows support.

Provides a way to build a Barrel database node for supported Windows platforms.

Expected results: being able to use Barrel on windows.

Knowledge prerequisites: windows build, erlang build using erlang.mk or rebar 3.

Possible Mentors: Benoit Chesneau