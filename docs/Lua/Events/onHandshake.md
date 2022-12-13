# onHandshake

Fired on a handshake with a user.

!!! note
    Returning a World here will send the client to it.

## Usage

```lua
function onHandshake(Client: cl)
    cl:chat(string.format("Welcome to the server, %s", cl:getname()))
end
```
