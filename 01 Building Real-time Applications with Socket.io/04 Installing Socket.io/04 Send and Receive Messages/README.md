# Socket.io Concepts - 04 Installing Socket.io - 04 Send and Receive Messages

- How to communicate  server and client
- Primary methiods for handling events in socket.io **EMIT and ON ** methods
```js
io.on('connection', function(socket) {
    console.log('new connection made');

    socket.emit('message-from-server', {
        greeting: 'Hello from Server'
    });

    socket.on('message-from-client', function(message) {
        console.log(message);
    });
});

```
```html
    <script>
    var socket = io('http://localhost:8080');

    socket.on('message-from-server', function(evt) {
        document.body.appendChild(
            document.createTextNode(evt.greeting));
        socket.emit('message-from-client', {
            greeting: 'Hello from Client'
        });
    });
    </script>
```