# onWorldLoaded

Fired when a world gets loaded from file.

## Usage

```lua
function onWorldLoaded(World: wrld)
    print(string.format("A new world has been loaded: %s", wrld:getname()))
end
```
