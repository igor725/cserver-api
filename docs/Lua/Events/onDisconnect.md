# onDisconnect

Fired when a client disconnects.

## Usage

```lua
function onDisconnect(Client: cl, string: reason)
    print(string.format("Client %s has disconnected because \"%s\"", cl:getname(), reason))
end
```
