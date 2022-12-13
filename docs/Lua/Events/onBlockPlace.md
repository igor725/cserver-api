# onBlockPlace

Fired when a client places a block.

!!! note
    Returning ``false`` here will disallow the client from placing the block.

    Returning a block id here will place it instead of the block the client tried to place.

## Usage

```lua
function onBlockPlace(Client: cl, Vector: pos, int: id)
    print(string.format("Player %s has placed id %s at %s", cl:getname(), id, pos))
end
```
