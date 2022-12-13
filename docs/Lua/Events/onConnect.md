# onConnect

Fired on an incoming connection.

!!! warning
    The client is not fully initialized at this point. For a more complete client, use [onHandshake](/Lua/Events/onHandshake)

!!! note
    Returning ``false`` here will close the connection to the client. 

## Usage

```lua
function onConnect(Client: cl)
    cl:chat(string.format("Incoming connection: %s", cl:getaddr()))
end
```

