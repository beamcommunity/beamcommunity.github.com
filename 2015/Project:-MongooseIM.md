* Website: https://github.com/esl/MongooseIM
* Responsible: Michał Piotrowski, Stefan Strigler
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com or mongoose-im AT erlang-solutions DOT com

Students providing their own ideas are also welcome!

### Idea #1: Implementation of XEP-0322 Efficient XML Interchange (EXI) Format

Brief explanation: The Efficient XML Interchange (EXI) format is a compact, high performance XML representation. It improves performance and significantly reduces bandwidth requirements.

Expected results: A module written in Erlang that extends MongooseIM so that it allows clients to connect to the server and start using EXI directly from the beginning.

Knowledge prerequisites: Erlang or any other functional language, XMPP. [GitHub issue](https://github.com/esl/MongooseIM/issues/145)

Mentor: Michał Piotrowski

### Idea #2: Webhooks

Through it's event based architecture MongooseIM allows (third-party) modules to interface with various kinds of internal behavior and processing of stanzas. By exposing those events to configurable REST APIs MIM flexibility could be made accessible to web based services as well and thus encourage wide spread adoption of XMPP integrated services within the web community.

Expected result: A module that lets external web based services register at internal hooks and routes and exposes the internal API of those calls respectively to those registered URLs.

Knowledge prerequisites: Erlang or any other functional language, REST/HTTP

Mentor: Stefan Strigler