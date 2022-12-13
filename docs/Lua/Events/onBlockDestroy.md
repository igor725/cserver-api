# onBlockDestroy

Fired when a client destroys a block.

!!! note
    Returning ``false`` here will disallow the client from destroying the block.

## Usage

```lua
function onBlockDestroy(Client: cl, Vector: position, int: blockId)
    print(string.format("Player %s has broken block at %s", cl:getname(), position))
end
```

!!! warning
    ``id`` seems to always be 0.
