# *Pulsar*<br/>Fibers, Channels and Actors for Clojure
[![Build Status](https://travis-ci.org/puniverse/pulsar.svg?branch=master)](https://travis-ci.org/puniverse/pulsar) [![Dependency Status](https://www.versioneye.com/user/projects/52b019ccec137505ee00002e/badge.png?style=flat)](https://www.versioneye.com/user/projects/52b019ccec137505ee00002e) [![Version](http://img.shields.io/badge/version-0.7.9-blue.svg?style=flat)](https://github.com/puniverse/pulsar/releases) [![License](http://img.shields.io/badge/license-EPL-blue.svg?style=flat)](https://www.eclipse.org/legal/epl-v10.html) [![License](http://img.shields.io/badge/license-LGPL-blue.svg?style=flat)](https://www.gnu.org/licenses/lgpl.html)

Pulsar wraps the [Quasar](https://github.com/puniverse/quasar) library with a Clojure API that's very similar to Erlang.

## Requirements

Java 7 and up and Clojure 1.5 and up are required to run Pulsar.

## Getting started

Add the following dependencies to [Leiningen](http://github.com/technomancy/leiningen/)'s project.clj:

```clojure
[co.paralleluniverse/quasar-core "0.7.9"]
[co.paralleluniverse/pulsar "0.7.9"]
```

Then, the following must be added to the project.clj file:

~~~ clojure
:java-agents [[co.paralleluniverse/quasar-core "0.7.9"]]
~~~

or, add the following to the java command line:

~~~ sh
-javaagent:path-to-quasar-jar.jar
~~~

Alternatively, to build Pulsar from the source, clone the repository and run:

```
lein midje
```

You can run the examples like this:

```
lein -o run -m co.paralleluniverse.pulsar.examples.pingpong
```

For benchmarks, you should use `lein trampoline`, like so:

```
lein trampoline run -m co.paralleluniverse.pulsar.examples.ring-benchmark 1000 1000
```

## Usage

Documentation and examples can be found [here](http://docs.paralleluniverse.co/pulsar/).

You can also read the introductory [blog post](http://blog.paralleluniverse.co/post/49445260575/quasar-pulsar).

When running code that uses Pulsar, the instrumentation agent must be run by adding the following
to the `java` command line
or to the `:jvm-opts` section in project.clj:

```
-javaagent:path-to-quasar-jar.jar
```

## Documentation

* [User Guide](http://docs.paralleluniverse.co/pulsar/)
* [API](http://docs.paralleluniverse.co/pulsar/api/)
* [Marginalia](http://docs.paralleluniverse.co/pulsar/uberdoc.html) (of tests and examples)

## Community

* [Google group](https://groups.google.com/forum/?fromgroups#!forum/quasar-pulsar-user).

## Contributions (including Pull Requests)

Please have a look at some brief [information for contributors](https://github.com/puniverse/quasar/blob/master/CONTRIBUTING.md).

## License

Pulsar is free software published under the following license:


```
Copyright ?? 2013-2017 Parallel Universe

This program and the accompanying materials are dual-licensed under
either the terms of the Eclipse Public License v1.0 as published by
the Eclipse Foundation

  or (per the licensee's choosing)

under the terms of the GNU Lesser General Public License version 3.0
as published by the Free Software Foundation.
```

[![githalytics.com alpha](https://cruel-carlota.gopagoda.com/6f172ebdf11f5b084127c9470cc7c887 "githalytics.com")](http://githalytics.com/puniverse/pulsar)
