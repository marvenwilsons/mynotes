---
tags: [Node.js]
title: tcp / net
created: '2020-06-11T05:01:18.345Z'
modified: '2020-06-11T17:24:34.082Z'
---

## tcp / net

## tcp server
this is a simple tcp server
```js
// index.js
const net = require('net')
const server = net.createServer(function (socket) {
  console.log('A client connected!')
  socket.on('data', function (data) {
    socket.write(data)
  })
})

server.listen(9000)
```

to run the tcp server in terminal
`$ node index`

to connect to the server, using a unix tool `netcat` or `nc`, netcat is unix tool that opens a tcp socket.
`$ nc localhost 9000`
`A client connected!`

## Example 2
```js
const net = require('net')
const socket = net.connect(9000,'localhost')

socket.on('data', function(data) {
  process.stdout.wirte(data)
})

process.stdin.on('data', function (data) {
  socket.write(data)
})
```

## peer to peer connection
we will use the `fully-connected-topology` node module'
https://www.npmjs.com/package/fully-connected-topology
https://www.elastic.co/videos/how-to-write-a-p2p-chat-app-in-nodejs-by-mathias-buus


## useful links
How to connect to a network
https://stackoverflow.com/questions/5489956/how-could-others-on-a-local-network-access-my-nodejs-app-while-its-running-on
