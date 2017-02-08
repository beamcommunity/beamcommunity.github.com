* Website: http://swirl-project.org/
* Responsible: [Dave Cottlehuber](https://twitter.com/dch__) & [Gianluca Stivan](https://twitter.com/yawnt)
* If you have any questions, send an e-mail to beam-community@googlegroups.com.

The Swirl Project is implementing a new peer-to-peer live streaming protocol that is still in draft status, undergoing IETF standardisation. The long-term goal is to develop both clients and server applications compatible with the PPSP protocol, from mobile devices through to high-end content delivery appliances.

The ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Implement the PPSP Tracking Protocol

Brief explanation: The PPSP specification is split into a [PPSP-TP tracker protocol](https://datatracker.ietf.org/doc/draft-ietf-ppsp-base-tracker-protocol/), which resembles HTTP at a first glance, and the underlying [transport protocol, PPSPP](http://datatracker.ietf.org/doc/draft-ietf-ppsp-peer-protocol/). Current development within the Swirl project is focused on only the transport layer, so the tracker is a green field ripe for your adventure!

Expected results: an Erlang or Elixir-based implementation of the [PPSP-TP draft specification](https://datatracker.ietf.org/doc/draft-ietf-ppsp-base-tracker-protocol/) that inter-operates with [tribler](http://svn.tribler.org/) assuming a suitable compatible version is released. This should be a separate OTP application that interacts with the PPSP protocol through an appropriate API.

Knowledge prerequisites: Good knowledge of Erlang/OTP and/or Elixir development. Understanding of HTTP verbs and an interest in learning about peer-to-peer applications, algorithms and data structures such as merkle trees and binmaps.

Mentor: Dave Cottlehuber

### Idea #2: Test & DevOps Support

Brief explanation: the PPSP protocol will need to run on many different platforms. Starting from a bare-bones vagrant file, and using ansible as the primary automation tool, we'll need a comprehensive way of creating installs on many different platforms, primarily FreeBSD and well-known Linux flavours, that deploys the latest code, runs tests, and retrieves the results.

Expected results: A battery of tests are run on cleanly installed / configured servers using a full automated approach.

Knowledge prerequisites: Intermediate knowledge of the unix terminal world, common build tools, some python experience. An interest in Jenkins, Travis CI, and automation in general will help.

Mentor: Dave Cottlehuber

### Idea #3: Live Streaming

Brief explanation: The PPSP protocol includes an optional live streaming mode. This allows consumers to start watching content such as a football match or cultural event as soon as the event has started. 

Expected results: An implementation in Erlang/OTP that complies with the draft [IETF specification, section 6](http://tools.ietf.org/html/draft-ietf-ppsp-peer-protocol-08#section-6).

Knowledge prerequisites: Intermediate Erlang background, with an interest in wire protocols, packets, and peer-to-peer applications, algorithms and data structures such as merkle trees and binmaps

Mentor: Dave Cottlehuber

### Idea #4: Dashboards

Brief explanation: PPSP would be very boring without a useful UI to interact with the application - for metrics and controlling various streams. This idea can either be server side, focused developing the necessary integration and API to expose the dashboard, or client side using HTML5/CSS etc to display and interact with that API.

Expected results: an integrated dashboard that provides performance metrics and ability to interact with the PPSP application such as viewing active content and streams, peers, and modifying relevant properties.

Knowledge prerequisites: some exposure to Erlang applications will be useful, with HTML & CSS experience. Understanding of RESTful applications will be an advantage.

Mentor: Dave Cottlehuber


### Idea #5: Javascript/NodeJS PPSP Implementation

Brief explanation: to assist with integration into web browsers and mobile devices, a nodejs implementation of the core PPSP proocol transport is desirable.

Expected results: a nodejs module or modules that can run as a PPSP peer, downloading & seeding content in compliance with the PPSP specification.

Knowledge prerequisites: intermediate nodejs developer who is a self starter -- this is your baby end to end! An interest in peer-to-peer networks and data structures such as merkle trees, binmaps, and wire protocols such as LEDBAT, as well as getting nodejs into the browser will be required.

Mentor: Gianluca Stivan

### Idea #6 : Anything!

Take a look at some of the plans in the [approach](https://github.com/skunkwerks/swirl/blob/feature/docs/doc/implementation.md#approach) and [future](https://github.com/skunkwerks/swirl/blob/feature/docs/doc/implementation.md#future-plans) plans section, or drop in and discuss some time!

### Reference material

More & more information on both PPSP [overview](https://github.com/skunkwerks/swirl/blob/feature/docs/doc/overview.md) and the actual Swirl [implementation](https://github.com/skunkwerks/swirl/blob/feature/docs/doc/implementation.md) is going up each day, including the application [structure](https://github.com/skunkwerks/swirl/blob/feature/docs/doc/supervision.md).