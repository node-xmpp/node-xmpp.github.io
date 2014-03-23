---
layout: page
title: "node-stringprep"
category: doc
date: 2014-03-16 13:17:18
order: 5
---


* Name: __node-stringprep__
* NPM package name: __node-stringprep__
* Source: __https://github.com/node-xmpp/node-stringprep__
* Build status: [![Build Status](https://secure.travis-ci.org/node-xmpp/node-stringprep.png)](http://travis-ci.org/node-xmpp/node-stringprep)

Exposes predefined Unicode normalization functions that are required by many protocols. This is just a binding to [ICU](http://icu-project.org/), which is [said to be fast.](http://ayena.de/node/74).

If ICU is not available then we make use of JavaScript fallbacks.


# Usage

```javascript
    var StringPrep = require('node-stringprep').StringPrep;
    var prep = new StringPrep('nameprep');
    prep.prepare('Äffchen')  // => 'äffchen'
```

For a list of supported profiles, see [node-stringprep.cc](http://github.com/node-xmpp/node-stringprep/blob/master/node-stringprep.cc#L160)

Javascript fallbacks can be disabled/enabled using the following methods on the `StringPrep` object:

```javascript
var prep = new StringPrep('resourceprep')
prep.disableJsFallbacks()
prep.enableJsFallbacks()
```

Javascript fallbacks are enabled by default. You can also check to see if native `icu` bindings can/will be used by calling the `isNative()` method:

```javascript
var prep = new StringPrep('resourceprep')
prep.isNative()  // true or false
```