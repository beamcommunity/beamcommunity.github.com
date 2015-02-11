* Website: https://github.com/esl/MongooseIM
* Responsible: Michał Piotrowski, Stefan Strigler
* If you have any questions, send an e-mail to beam-community@googlegroups.com or mongoose-im AT erlang-solutions DOT com

Students providing their own ideas are also welcome!

### Idea #1: Implementation of XEP-0322 Efficient XML Interchange (EXI) Format

Brief explanation: The Efficient XML Interchange (EXI) format is a compact, high performance XML representation. It improves performance and significantly reduces bandwidth requirements.

Expected results: A module written in Erlang that extends MongooseIM so that it allows clients to connect to the server and start using EXI directly from the beginning.

Knowledge prerequisites: Erlang or any other functional language, XMPP. [GitHub issue](https://github.com/esl/MongooseIM/issues/145)

Mentor: Michał Piotrowski

### Idea #2: Implementation of XEP-0280 Message Carbons

Currently many XMPP servers handle message stanzas sent to a user@host (or "bare") JID with no resource by delivering that message only to the resource with the highest priority for the target user. Some server implementations, however, have chosen to send these messages to all of the online resources for the target user. If the target user is online with multiple resources when the original message is sent, a conversation ensues on one of the user's devices; if the user subsequently switches devices, parts of the conversation may end up on the alternate device, causing the user to be confused, misled, or annoyed.

XEP-0280 defines an approach for ensuring that all of my devices get both sides of all conversations in order to avoid user confusion. As a pleasant side-effect, information about the current state of a conversation is shared between all of a user's clients that implement this protocol.

Expected result: A module or patchset for MongooseIM that modifies its behavior according to this XEP.

Knowledge prerequisites: Erlang or any other functional language, XMPP

Mentor: Stefan Strigler

### Idea #3: Webhooks

Through it's event based architecture MongooseIM allows (third-party) modules to interface with various kinds of internal behavior and processing of stanzas. By exposing those events to configurable REST APIs MIM flexibility could be made accessible to web based services as well and thus encourage wide spread adoption of XMPP integrated services within the web community.

Expected result: A module that lets external web based services register at internal hooks and routes and exposes the internal API of those calls respectively to those registered URLs.

Knowledge prerequisites: Erlang or any other functional language, REST/HTTP

Mentor: Stefan Strigler