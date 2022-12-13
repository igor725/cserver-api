# onDespawn

Fired when a client despawns.

## Usage

```lua
function onDespawn(Client: cl)
    print(string.format("Player %s has despawned!", cl:getname()))
end
```
