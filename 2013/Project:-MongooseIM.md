* Website: https://github.com/esl/ejabberd
* Responsible: Michał Ślaski, Stefan Strigler
* If you have any questions, send an e-mail to beam-community@googlegroups.com

# Idea #1: Implementation of XEP-0313 Message Archive Management

Brief explanation: It is a common desire for a user using XMPP for IM to want to store their messages in a central archive on their server. This feature allows them to record conversations that take place on clients that do not support local history storage, and also to synchronise their conversation history seamlessly between multiple clients.

Expected results: A module written in Erlang that interfaces with MongooseIM so that messages get logged to a database backend of choice according to user settings and can be retrieved as defined by XEP-0313.

Knowledge prerequisites: Erlang or any other functional language, a DBMS of your choice, XMPP. 

Mentor: Stefan Strigler

# Idea #2: Implementation of XEP-0280 Message Carbons

Currently many XMPP servers handle message stanzas sent to a user@host (or "bare") JID with no resource by delivering that message only to the resource with the highest priority for the target user. Some server implementations, however, have chosen to send these messages to all of the online resources for the target user. If the target user is online with multiple resources when the original message is sent, a conversation ensues on one of the user's devices; if the user subsequently switches devices, parts of the conversation may end up on the alternate device, causing the user to be confused, misled, or annoyed.

XEP-0280 defines an approach for ensuring that all of my devices get both sides of all conversations in order to avoid user confusion. As a pleasant side-effect, information about the current state of a conversation is shared between all of a user's clients that implement this protocol.

Expected result: A module or patchset for MongooseIM that modifies its behavior according to this XEP.

Knowledge prerequisites: Erlang or any other functional language, XMPP

Mentor: Stefan Strigler

# Idea #3: Webhooks

Through it's event based architecture MongooseIM allows (third-party) modules to interface with various kinds of internal behavior and processing of stanzas. By exposing those events to configurable REST APIs MIM flexibility could be made accessible to web based services as well and thus encourage wide spread adoption of XMPP integrated services within the web community.

Expected result: A module that lets external web based services register at internal hooks and routes and exposes the internal API of those calls respectively to those registered URLs.

Knowledge prerequisites: Erlang or any other functional language, REST/HTTP

Mentor: Stefan Strigler