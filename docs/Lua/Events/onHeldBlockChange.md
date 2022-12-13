# onHeldBlockChange

Fired when a client changes the block held in his hand.

## Usage

```lua
function onHeldBlockChange(Client: cl, int: new, int: old)
    print(string.format("Client %s has just swapped from %d to %d", cl:getname(), old, new))
end
```
