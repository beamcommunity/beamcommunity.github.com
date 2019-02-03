This is the BEAM Community page for 2018 projects. You can also check [official Google Summer of Code page for 2018 projects](https://summerofcode.withgoogle.com/archive/2018/organizations/5082029850886144/).

## Accepted Projects

This section lists down projects accepted for GSoC 2018 under the BEAM Community organisation.

### BarrelDB - Create an Elixir client for BarrelDB

Make a BarrelDB client in idiomatic Elixir with its tests and documentation. The project scope depending on the progress done may also involve:

* creating a client-enforced schema and document changeset similar to the one in Ecto
* writing an aggregation framework for the client. Creating a GraphQL API for BarrelDB
* adding a statistics and health service
* supporting rate limiting and throttling.


* **Student**: Jakub Janarek
* **Mentors**: Benoit Chesneau
* **Code**: [Final Report](https://docs.google.com/document/d/1FALaT9tAzQueKY67aUU2J_qFb0WV6fIe9Ca4-EbdMFQ/edit?usp=sharing)


### Elixir - Add dialyzer task to Elixir

Dialyzer is a discrepancy analyzer that ships as part of the Erlang VM. There are two projects that adds Dialyzer support to Elixir applications: dialyxir and dialyzex. The goal of this project is to bring the ideas of both projects with two main new features: better usability (in particular, better error messages and formatting) and the ability to dialyze projects incrementally.

* **Student:** Gabriel Gatu
* **Mentors:** José Valim, Sean Cribbs
* **Code:** [https://github.com/gabrielgatu/mix-dialyzer](https://github.com/gabrielgatu/mix-dialyzer)


### Elixir - Typespecs to StreamData generators

[StreamData](https://github.com/whatyouhide/stream_data) is a library that adds data generation and property-based testing to Elixir. The goal of this project is to read @type declarations from BEAM code and automatically get generators out of them. Once that is done, we should use this information to automatically validate @spec annotations with data generators.

#### Goal 1 - Getting data generators out of @types
First part - Provide a simple way to generate all simple types(int, atom, all, etc.). Maybe a way to compose different generators and getting new ones would be useful for union/all types.

Second part - generators for recursive/recursively dependant/parameterized types which will be a greater challenge.

#### Goal 2 - Automatically validate function @specs
If we have a function spec, we can automatically feed the function it's arguments and check that the result always belongs to the return type of the function.

To check whether a result belong to the correct type generator, we should probably extend the StreamData struct to include a member function as a field. We would check whether different types belong to a data through it.

* **Student**: njichev
* **Mentors**: Andrea Leopardi
* **Code**: [https://github.com/njichev/type-generators](https://github.com/njichev/type-generators)


### Elixir – Monitoring performance of Elixir packages with ElixirBench

ElixirBench platform is a proof of concept that already showed its value, the key deliverable is to bring it up and running for nightly performance monitoring for significant Elixir projects. Given a project in the Github, it will be possible to activate the benchmark service and to automatically monitor the performance of the new released versions by setting up a bench/config.yml file and the benchmark scripts to be run for that project.

* **Student:**: Tallys Martins
* **Mentor**: Tobias Pfeiffer, Michał Muskała
* **Code**: [Final Report](https://gist.github.com/tallysmartins/83bbe000cbc385e8b651e650248e8192)


### Riak – Improving Riak testing suites using Common Test and Intercepts

Riak KV is an open source database with a strong focus on low latency, reliability and fault tolerance. Like any well tested computer system, batteries of tests are run to make sure that the database behaves correctly in typical but also adverse conditions such as network partitions, or even the deployment and upgrade process of nodes running different versions in the same cluster. To this end, one of the resources used by the Riak team is [riak_test](https://github.com/basho/riak_test). Its main function is to provide a test running framework that overlaps significantly with Common Test, but it also contains cluster management and code intercept functionalities. We propose to break up this repository into its discrete components, making important contributions to the Erlang community and adapting the test runner framework into Common Test suites, vastly increasing the reporting ability of current Riak tests.

* **Student:**: Gonçalo Tomás
* **Mentor**: bryan hunt, russelldb
* **Code**: [Final Report](https://gist.github.com/goncalotomas/3a821cca8bf07b8a159abba4df72ca89)


### Tensorflex - Tensorflow bindings for the Elixir programming language

Currently, there is a lack of machine learning tools and frameworks for Elixir. With the number of programmers learning/using machine learning only set to grow, supporting machine learning capabilities is essential for any programming language. Moreover, there are discussions on elixirforum.com regarding this and recent talks given at ElixirConf that reflect the need for Elixir to provide machine learning capabilities. I thus propose to work on Tensorflex, an Elixir framework similar to Keras (for Python). Keras uses Tensorflow as a backend for doing all the ML. Using Native Implemented Functions (NIF) and the Tensorflow C API as a backend, a low-level wrapper will be written in Elixir. This low-level API will then be used to write a Keras-like framework in the form of a high-level API. This will allow Elixir developers to write expedient and efficient machine learning code in Elixir.


* **Student:**: Anshuman Chhabra
* **Mentor**: José Valim
* **Code**: [https://github.com/anshuman23/tensorflex](https://github.com/anshuman23/tensorflex)


## Participating OSS projects

* [Barrel](https://barrel-db.org/)
* [Elixir](https://elixir-lang.org/)
* [Riak](https://github.com/basho/riak)