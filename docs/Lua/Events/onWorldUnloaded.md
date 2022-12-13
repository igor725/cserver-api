# onWorldUnloaded

Fired when a world gets unloaded from memory.

## Usage

```lua
function onWorldUnloaded(World: wrld)
    print(string.format("A world has been unloaded: %s", wrld:getname()))
end
```
