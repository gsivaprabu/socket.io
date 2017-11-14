# Socket.io Concepts - 03 Socket.io Basics - 02 Socket.io Framework

- Socket.io is Javascript based framework
- Built and maintained Node.js module
- In github they mention how to use with express and Koa


## In conjunction with Express

##### Starting with 3.0, express applications have become request handler functions that you pass to http or http Server instances. You need to pass the Server to socket.io, and not the express application function. Also make sure to call .listen on the server, not the app.
```javascript
var app = require('express')();
var server = require('http').createServer(app);
var io = require('socket.io')(server);
io.on('connection', function(){ /* … */ });
server.listen(3000);
```
## In conjunction with Koa

##### Like Express.JS, Koa works by exposing an application as a request handler function, but only by calling the callback method.
```javascript
var app = require('koa')();
var server = require('http').createServer(app.callback());
var io = require('socket.io')(server);
io.on('connection', function(){ /* … */ });
server.listen(3000);
```

- Same method used for Client and Server side also.
- They have slack community.
- Socket.io based on WebSocket technology.