# Socket.io Concepts - 04 Installing Socket.io - 03 First Connection

- When the first connection initialized 

```javascript
io.on('connection', function(socket) {
    console.log('new connection made');
});
```

In html file mentioned the server location

```html
    <script>
    var socket = io('http://localhost:8080');
    </script>
```