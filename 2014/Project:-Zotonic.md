Zotonic is the open source, high speed, real-time web framework  and content management system, built with Erlang. 

Zotonic is fast and stable - suited for anything from basic websites to complex distributed applications. Zotonic is a growing community of developers interested in seeing Zotonic grow into a successful worldwide project. We have T-shirts :-) See more at: http://zotonic.com

The Zotonic - Google Summer of Code is coordinated by: Marc Worrell (The Netherlands) and Andreas Stenius (Sweden)

Questions about Zotonic:  marc@worrell.nl @mworrell

General questions about the Beam community: beam-community@googlegroups.com.

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

***


### IDEA 1. Low level efficiency (aka Elli/webmachine)
https://github.com/mmzeeman/elli_machine Uses cutting edge russian space age technology. See: http://drakon-editor.sourceforge.net/. It has a different goal as webmachine and cowboy-rest interface. These are aimed at serving requests for REST-services. We want to build a general purpose CMS on top of it with support for websockets, comet, virtual hosts and more.
Unit-tests for decision steps in low-level http handling. Etags, If-Range, and friends.
Integrate elli handover requests needed for handling websockets and large-file uploads.


### IDEA 2. Support low power systems (aka running on ARM or low-level VPS)
Brief explanation: make Zotonic ideal for cheap low-power systems. Currently there are some inefficiencies in Zotonic, which hinder deployment on these machines. One is a sensitivity to certain timeout situations, which happen more often on slower machines, and another is the time to compile templates to BEAM code.
This project would involve one or more of the following items:

 * Better supervision tree, use circuit breakers for modules/sites
 * Timeouts (stability of supervision tree)
 * ErlyDTL - more efficient template compilation, not compile to code but to byte-machine or data structure
 * Dispatcher - compile dispatch rules to erlang or an efficient data structure

Expected result(s): adaptations to Zotonic so that it runs more smoothly on slow and small machines

Knowledge prerequisites: a bit of Erlang/OTP for understanding of supervisor trees.


### IDEA 3. Dropbox/GDrive/SkyDrive integration
Brief explanation: Allow import and export of texts, images, collections, and menu trees using Dropbox.

We have a dedicated Zotonic wiki page about this and related use cases: https://github.com/zotonic/zotonic/wiki/Zotonic-File-Service-API

Expected results: module(s) for integration with dropbox and alike services

Knowledge prerequisites: client/server implementations, interest in data synchronization


### IDEA 4. Federation of servers
Brief explanation: We want to be able to federate Zotonic servers. Goals are: federation of users, vertical sharding of data, distribution of backups, manual failover, and offloading compute intensive tasks.
See also: https://github.com/zotonic/zotonic/wiki/Federation-versus-Zynamo

Expected result(s): Basis of (some parts of) the federation infrastructure. For example a way to move a site between servers and distribute backups.

Knowledge prerequisites: Understanding of distributed systems, interested in federation and data-distribution protocols.

Mentor: Marc Worrell (@mworrell)


### IDEA 5. Cooperative editing
Brief explanation: We want to add cooperative editing of resources. This should use markdown for rich text editing. Currently, when multiple editors are editing the same page in the admin, unexpected results can happen. We'd like to see a collaborative editing feature for pages like mobwrite, etherpad and google docs offer. The direction we are strongly leaning to is using mobwrite’s diff-match-patch in combination with MQTT pubsub.

Knowledge prerequisites: An understanding and interest in various realtime protocols.


### IDEA 6. Real-time stats
Brief explanation: add insight to the traffic of a zotonic server. The system already knows a lot about the visitors (user-agent, referrer, ip-address etc) and it would be nice to leverage this into a real-time display per site or aggregated over the whole server. Including historical views for later analysis. An example is how The Guardian uses this kind of real-time information http://www.fastcolabs.com/3026154/how-the-guardian-uses-attention-analytics-to-track-rising-stories

A proof of concept already exists in [mod_admin_stats](https://github.com/zotonic/zotonic/tree/master/modules/mod_admin_stats) for inspiration or as basis for further improvements.

Knowledge prerequisites: understanding of graphing libraries like d3.js, html, stats collection (folsom).


### IDEA 7. OTP-ification of zotonic and the modules.
Brief explanation: Zotonic is a big system consisting of many modules and other functional parts. The idea is to split Zotonic into smaller OTP applications. This would enable easier re-use, improved flexibility, testability and distribution of modules and other parts.

Knowledge prerequisites: understanding of Erlang/OTP, especially application behaviour.
