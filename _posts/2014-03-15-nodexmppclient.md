---
layout: page
title: "node-xmpp-client"
category: doc
date: 2014-03-15 21:07:32
---

## C2S Client to Server 

```
var Client = require('node-xmpp-client')

var client = new Client({
    jid: 'user@example.com',
    password: 'password'
})

client.on('online', function() {
    console.log('online')
})

client.on('stanza', function(stanza) {
    console.log('Incoming stanza: ', stanza.toString())
})
```

## Closing a connection

```
client.end()
```
