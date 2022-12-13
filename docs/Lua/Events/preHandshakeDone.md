# preHandshakeDone

Fires before sending the handshake packet to client.

!!! note
    This event is used to overwrite the sent server name or motd.

## Usage

```lua
function preHandshakeDone(Client: cl, string: name, string: motd)
    return name, motd
end
```
