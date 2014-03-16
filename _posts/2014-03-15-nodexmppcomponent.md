---
layout: page
title: "node-xmpp-component"
category: doc
date: 2014-03-15 21:07:55
---

* Name: __node-xmpp-component__
* NPM package name: __node-xmpp-component__
* Source: __https://github.com/node-xmpp/node-xmpp-component__
* Build status: [![Build Status](https://secure.travis-ci.org/node-xmpp/node-xmpp-component.png)](http://travis-ci.org/node-xmpp/node-xmpp-component)

An XMPP component library built in nodejs.

```
var Component = require('node-xmpp-component')
var component = new Component(...parameters...)
```

### Parameters

* __jid__ [String]: The jid of the user you wish to log in as. If no _host_ parameter provided an SRV lookup will be performed on the domain (where possible).
* __password__ [String]: Password to be used for login
* __host__ [String] _optional_: The host where the the XMPP server is located
* __port__ [Int] _optional_: Port number to connect on
