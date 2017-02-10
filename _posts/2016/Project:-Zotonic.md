* Website: http://zotonic.com
* Responsible: Marc Worrell, Andreas Stenius, Arjan Scherpenisse, Maas-Maarten Zeeman
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Elixir support

Elixir is getting more and more traction these days. Zotonic could benefit from the Elixir community, combining Elixir's modern language features with Zotonic's CMS. This project revolves around the idea of getting Elixir files to compile and load within the Zotonic module system, so that you can write Zotonic modules using Elixir.

Our approach for integration would be that every zotonic module is a standalone Elixir project (with its own `mix.exs` file), and that the Zotonic compiler and module system knows how to interpret these files.

Expected results: An integrated experience for writing Zotonic modules in Elixir

Knowledge prerequisites: Erlang, Elixir

Possible Mentors: Arjan Scherpenisse


### Idea #2: Admin edit page improvements

The Zotonic admin interface serves its purpose nicely as a CMS for basic tasks. However, there are many improvements that could be made to it to improve the usability of its base, the edit page.

For one, the "page connections" could be highlighted more to stress the semantic nature of the Zotonic data model: make it possible to not only show the outgoing connections (like it currently does), but also the incoming connections. Additionally, the page connections interface currently is unusable when there are many (30+) connections.

Expected results: An improved editing experience for the admin users

Knowledge prerequisites: Erlang, HTML5, CSS, Javascript

Possible Mentors: Arjan Scherpenisse, Marc Worrell

### Idea #3: Search query DSL

Zotonic has its own [datamodel](http://zotonic.com/docs/0.13/user-guide/data-model.html) which is loosely based on the principles of the semantic web. Everything is a *resource*, and resources are connected through edges. To traverse this graph, Zotonic has a basic [search mechanism](http://zotonic.com/docs/0.12/manuals/datamodel/search.html) to select resources based on certain properties.

The current query syntax can be used from URLs, from the templates and from stored `query` resources. However, in each of these instances it has subtle differences. We would like to unify this query syntax so that it is the same everywhere, and, ideally, that it can be made extensible so that modules can be able to add their own operators.

For bonus points, this query DSL could be compiled so that it generates an Erlang function that produces the necessary SQL to execute the query.

Expected results: An improved search experience for Zotonic developers, and a more flexible search query model

Knowledge prerequisites: Erlang, SQL

Possible Mentors: Arjan Scherpenisse, Marc Worrell


### Idea #4: Mailinglist / e-mail module extensions

Zotonic's current mailinglist module is battle-tested and works fine. However, it is not up to par with comparable products like Mailchimp. We would like to add the following features to it:

* DKIM signing of e-mail messages
* Integrate e-mail bounce handling so that bounced respondents are automatically unsubscribed
* Using tracking images to check whether a messages has been opened; and rewrite all URLs in mails to track which links have been clicked
* Create a page in the admin to visualize these tracking statistics

Knowledge prerequisites: Erlang; knowledge of e-mail systems

### Idea #5: Real-time stats

Brief explanation: add insight to the traffic of a zotonic server. The system already knows a lot about the visitors (user-agent, referrer, ip-address etc) and it would be nice to leverage this into a real-time display per site or aggregated over the whole server. Including historical views for later analysis. An example is how The Guardian uses this kind of real-time information http://www.fastcolabs.com/3026154/how-the-guardian-uses-attention-analytics-to-track-rising-stories

A proof of concept already exists in [mod_admin_stats](https://github.com/zotonic/zotonic/tree/master/modules/mod_admin_stats) for inspiration or as basis for further improvements.

Knowledge prerequisites: understanding of graphing libraries like d3.js, html, stats collection (folsom).


### Idea #6: Moving the zotonic sh scripts to erlang/escript

Currently we are using shell scripts for the command line functionality. Think of starting Zotonic, installing modules, etc.

These command line scripts are fragile and non-portable. That is why we are thinking of replacing them with either Escript or Erlang modules. This would also create opportunities for exposing the script functionalities in a web interface.

What need to be done is:

 * Check on speed of Erlang scripting, can we have a quick starting local node for the scripts?
 * Design the architecture for the Erlang implementation
 * Ensure hooks/modules that can be used from within Zotonic itself
 * Rewrite the scripts in Erlang


Knowledge prerequisites: Erlang, bash