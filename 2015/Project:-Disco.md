* Website: http://discoproject.org/
* Responsible: Shayan Pooya, Tim Spurway
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com

### Idea #1: Disco Streaming
Add support for streaming data into Disco jobs. Currently, when a Disco job starts, it knows all of the inputs and schedules tasks based on these inputs. An alternative, would be to accept a stream of inputs and create new tasks as the inputs become ready.

The idea has been tackled by Spark before:
http://www.cs.berkeley.edu/~matei/papers/2012/hotcloud_spark_streaming.pdf

There are a lot of projects (Kafka, Flume, Storm) that excel in streaming data from one location to another. The best outcome of this project would be to integrate one such streaming tool. However, a simpler input might be using disco distributed file system as an intermediate storage; input is pushed into DDFS and can be monitored and a new task will be created as soon as there is "enough" input available.

This project will require knowledge of Python and Erlang.

Expected results:  A prototype for Disco Streaming

Knowledge prerequisites: Erlang

Mentors: Shayan Pooya, Tim Spurway

### Idea #2: Add namespace to DDFS.
Currently all of the tags in ddfs are stored in the same namespace.  In order to improve the scalability and usability of ddfs, we can add the namespace meta-data to the tags.  This namespace can be used for determining which directory should be used for storing the blobs of a tag.  For example, the file of the namespace temp/test can be stored in the ddfs/temp/test directory (Although the first iteration does not have to support sub namespaces like this).  With this approach, some of the ddfs operations will get much cheaper.  For example, a ddfs ls will be a per namespace and there is much less work to do.  The most important win, however, will be the garbage collection.  Disco can start and finish the gc on one namespace before starting on the next one and therefore reducing the amount of time (and pressure on the system) that gc takes.

Knowledge prerequisites: Erlang

Mentors: Shayan Pooya, Tim Spurway

### Idea #3:  Network-resource-aware task allocator

Brief explanation:  The current mechanism of allocating tasks to cluster nodes uses a very naive idea of the network topology of the cluster, especially of the rack-locality of cluster nodes.  It would be good to address this taking into account the dynamic network topology present in an environment like AWS (as opposed to assuming a static environment).

There are two components for this project: (a) infer or extract the current cluster network topology while requiring the absolute minimum of user-configuration (ideally none), and (b) exploiting this network topology in a new task allocator algorithm that minimizes network impact of task allocations.

A stretch goal would be to also use this topology in DDFS to minimize network impact of replication and improving replica placement to handle rack-level outages.

Expected results:  A prototype for an improved network-aware task scheduler.

Knowledge prerequisites:  Networking, Erlang.

Mentors:  Shayan Pooya, Tim Spurway

