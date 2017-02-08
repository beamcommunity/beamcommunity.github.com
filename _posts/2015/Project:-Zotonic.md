* Website: http://zotonic.com
* Responsible: Marc Worrell, Andreas Stenius, Arjan Scherpenisse, Maas-Maarten Zeeman
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Logon via email

Infrequent visitors of websites tend to forget their passwords. Idea is to let people logon via an email message. This is secure enough for simple web sites.

Scenario:

 * Fill in email, click _logon via email_
 * Receive email, click on link
 * Logged on at the website

There can be additional security measures:

 * Must logon via the browser where the link was clicked
 * Link is only valid once
 * Link is only valid for limited amount of time

Other easy logon options/ideas are welcome

### Idea #2: Create resources via email

Add possibility to create specific pages by sending an email to a special email address.
The pages could include images and attachments included in the email. Special handling could be added to extract the summary or other meta-information.

Problem is to add some basic security, some ideas include:

 * Sender verification (open how to make this more secure)
 * Email back with a verification request (needs a reply)

### Idea #3: Moving the zotonic sh scripts to erlang/escript

Currently we are using shell scripts for the command line functionality. Think of starting Zotonic, installing modules, etc.

These command line scripts are fragile and non-portable. That is why we are thinking of replacing them with either Escript or Erlang modules. This would also create opportunities for exposing the script functionalities in a web interface.

What need to be done is:

 * Check on speed of Erlang scripting, can we have a quick starting local node for the scripts?
 * Design the architecture for the Erlang implementation
 * Ensure hooks/modules that can be used from within Zotonic itself
 * Rewrite the scripts in Erlang

### Idea #4: Cooperative editing

Brief explanation: We want to add cooperative editing of resources. This should use markdown for rich text editing. Currently, when multiple editors are editing the same page in the admin, unexpected results can happen. We'd like to see a collaborative editing feature for pages like mobwrite, etherpad and google docs offer. The direction we are strongly leaning to is using mobwrite’s diff-match-patch in combination with MQTT pubsub.

Knowledge prerequisites: An understanding and interest in various realtime protocols.

### Idea #5: Real-time stats

Brief explanation: add insight to the traffic of a zotonic server. The system already knows a lot about the visitors (user-agent, referrer, ip-address etc) and it would be nice to leverage this into a real-time display per site or aggregated over the whole server. Including historical views for later analysis. An example is how The Guardian uses this kind of real-time information http://www.fastcolabs.com/3026154/how-the-guardian-uses-attention-analytics-to-track-rising-stories

A proof of concept already exists in [mod_admin_stats](https://github.com/zotonic/zotonic/tree/master/modules/mod_admin_stats) for inspiration or as basis for further improvements.

Knowledge prerequisites: understanding of graphing libraries like d3.js, html, stats collection (folsom).

### IDEA #6: OTP-ification of zotonic and the modules.

Brief explanation: Zotonic is a big system consisting of many modules and other functional parts. The idea is to split Zotonic into smaller OTP applications. This would enable easier re-use, improved flexibility, testability and distribution of modules and other parts.

Knowledge prerequisites: understanding of Erlang/OTP, especially application behaviour.