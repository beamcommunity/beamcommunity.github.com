* Website: http://zotonic.com
* If you have any questions, send an e-mail to beam-community@googlegroups.com.

List of preliminary ideas, to be sorted, extended and explained.


### Dropbox integration

Brief explanation: Allow import and export of texts, images, collections, and menu trees using Dropbox.

We have a dedicated Zotonic wiki page about this and related use cases: https://github.com/zotonic/zotonic/wiki/Zotonic-File-Service-API

Expected results: module(s) for integration with dropbox and alike services

Knowledge prerequisites:

Mentor: Andreas Stenius (@kaos)


### Modules repository integration

Brief explanation: Admin interface to search/install/uninstall modules from http://modules.zotonic.com.
The idea is to have an interface with which you can search, explore, install and uninstall modules. Ideally from the browser and the command line. One of the problems is to visualize any startup/runtime problems and module dependencies.

Expected results: Web interface for exploring, installing, updating and uninstalling modules.

Knowledge prerequisites: HTML, web interaction, git

Mentor: Andreas Stenius (@kaos)


### Testability

Brief explanation: Make Zotonic more testable using meck and other techniques. 

Expected results: To have a substantial cover of the core using Travis-CI.

Knowledge prerequisites:

Mentor: Andreas Stenius (@kaos)


### Boot sequence optimization

Brief explanation: Make Zotonic's startup sequence more durable. Zotonic is capable of virtual-hosting for websites. But it's current model of managing sites is not optimal: all enabled sites are started in parallel, causing database overload and timeouts in supervisors.

Expected results:  Having replaced the site startup sequence with an FSM-based model so we can have more reliable site startup without causing timeouts, and thus make Zotonic capable of serving many (the goal is 1000+) sites.

Knowledge prerequisites: Knowledge about Erlang/OTP, supervisors, automated testing

Mentor:Marc Worrell (@mworrell)


### Timezone support

Brief explanation: Add knowledge of timezones to the request context, make it possible to have timezones in calendars, and other date routines.

Expected results:

Knowledge prerequisites:

Mentor: Marc Worrell (@mworrell)


### Calendar synchronization

Brief explanation: Update mod_calendar to enable import/export of iCal events and synchronization with external calendars like Google Calendar.

Expected results:

Knowledge prerequisites:

Mentor:


### Markdown editor

Brief explanation: Add a choice of editor, currently we use TinyMCE for rich text and want to add an option to use markdown for input. This needs to be able to translate stored HTML to markdown if there is no markdown representation of the text.

Expected results: A plugable system which allows multiple input editors for the main content text.

Knowledge prerequisites:

Mentor: Arjan Scherpenisse (@acscherp)


### Cooperative editing

Brief explanation: We want to add cooperative editing of resources. This should use markdown for rich text editing. Currently, when multiple editors are editing the same page in the admin, unexpected results can happen. We'd like to see a collaborative editing feature for pages like `etherpad` and google docs offer.

Knowledge prerequisites: An understanding of various realtime protocols and some experience with the Zotonic admin interface

Mentor: Arjan Scherpenisse (@acscherp)
