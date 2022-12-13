# server
This library contains some server's functions.

## int: server.uptime

```lua
server.uptime()
```

Returns the current server uptime in milliseconds.

## server.stop

```lua
server.stop()
```

Stops the server.

## table: server.info

```lua
server.info()
```

Returns the table with the server info.

### Server info table
| Field     | Type      | Description                                  |
|-----------|-----------|----------------------------------------------|
| flags     | int       | The flags the server compiled with.          |
| software  | string    | Server software name.                        |
| tag       | string    | The git commit tag the server compiled with. |
