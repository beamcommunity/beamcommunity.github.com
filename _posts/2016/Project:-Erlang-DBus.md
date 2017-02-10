* Website: https://github.com/lizenn/erlang-dbus
* Possible mentors: Jean Parpaillon
* If you have any questions, send an e-mail to beam-community AT googlegroups DOT com
A native erlang implementation of D-Bus.

D-Bus is now largely used in a lot of applications for language-independant, object-oriented RPC system.

The erlang platform needs an erlang native implementation.Ideally, we would like to propose this application as an OTP application.

Ideas are listed in no particular order. Students providing their own ideas are also welcome!

### Idea #1: Implements a D-Bus service behaviour

[D-Bus](https://dbus.freedesktop.org/doc/dbus-specification.html) is mostly used in a service provider/consumer style. The current implementation only allows consuming services. It should support exposing services.

At first, we could provide a `gen_dbus` behaviour that a module would implement for exposing services.
In a second step, a parse transform module would ease development of D-Bus service by simply annotating functions like, for instance, the [Python D-Bus implementation](https://dbus.freedesktop.org/doc/dbus-python/doc/tutorial.html).

#### Expected results: 

* functional `gen_dbus` behaviour 
* a parse transform allowing exposing erlang functions as D-Bus methods.

#### Knowledge prerequisites: 

* Linux, 
* Erlang, 
* service-oriented architectures

#### Possible Mentors: Jean Parpaillon

### Idea #2: Prepare for OTP integration

[D-Bus](https://dbus.freedesktop.org/doc/dbus-specification.html) is largely used as RPC mechanism on Linux-based systems but can be also used on any modern OS, thanks to multiple transports, not only dependant on the Linux OS.

Some work needs to be done before proposing it as an OTP application:
* remove OS-dependant code: UNIX socket handling,,
* use OTP-style Makefiles,
* integrates unit and functional testing,
* generates documentation.

#### Expected results: 

* UNIX socket handling: see https://github.com/lizenn/erlang-dbus/issues/8
* Makefiles use OTP style
* integrates eunit/common test
* write basic documentation in OTP style

#### Knowledge prerequisites: 

* Linux, 
* Erlang

#### Possible Mentors: Jean Parpaillon

### Idea #3: Implements SASL mechanisms

[D-Bus](https://dbus.freedesktop.org/doc/dbus-specification.html) implementations must support [all SASL mechanisms](https://dbus.freedesktop.org/doc/dbus-specification.html#auth-mechanisms).

As of today, the following mechanisms are supported, through an easily extensible [API](https://github.com/lizenn/erlang-dbus/blob/master/src/dbus_auth.erl):
* [ANONYMOUS](https://github.com/lizenn/erlang-dbus/blob/master/src/dbus_auth_anonymous.erl)
* [COOKIE_SHA1](https://github.com/lizenn/erlang-dbus/blob/master/src/dbus_auth_cookie_sha1.erl)
* [EXTERNAL](https://github.com/lizenn/erlang-dbus/blob/master/src/dbus_auth_external.erl)

#### Expected results: 

* implements other SASL mechanisms: see [RFC4422](http://tools.ietf.org/html/rfc4422)

#### Knowledge prerequisites: 

* Linux, 
* Erlang, 
* Basic authentication mechanisms

#### Possible Mentors: Jean Parpaillon