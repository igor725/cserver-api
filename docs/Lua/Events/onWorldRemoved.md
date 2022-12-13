# onWorldRemoved

Fired when a world gets removed to the world list.

## Usage

```lua
function onWorldRemoved(World: wrld)
    print(string.format("A world has been removed: %s", wrld:getname()))
end
```
